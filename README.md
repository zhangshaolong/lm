lm
==

讨论

Module
    自动添加观察者事件
    管理事件冒泡及终止传递事件
    自动维护父Module及子Modules
    自动扫描注册的组件，尽量简单
    维护自己的生命周期，销毁的时候，优先销毁子Modules
    Module只有一个数据源，里面的各种组件可以共享其中的数据，数据与组件可以实现MVVM
    
观察者
    支持target对事件源对象的引用
    支持on事件的时候，返回Deferred来获取事件handlerId，从而支持对事件的取消
    当注册了多个on的时候，fire时会使用handlerId进行区分，可以返回执行结果
    event对象包含target、data
    实现一个shareEvent，处理多模块事件共享，主要处理业务耦合性比较高的情况。
    
组件
    需要提供统一的组件销毁方法，以便Module进行统一维护
    需要提供统一的渲染方法，以便Module来控制展示
    需要提供一个流程控制的方法，以便处理Module之间的运行依赖关系

DataSet
    
Router
