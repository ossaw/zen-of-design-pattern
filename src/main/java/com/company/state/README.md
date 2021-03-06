# 状态模式(State Pattern) 
定义：Allow an object to alter its behavior when its internal state changes. The object will appear to change its classes.（当一个对象内在状态改变时允许其改变行为，这个对象看起来像改变了其类。）  


 状态模式的核心是封装，状态的变更引起了行为的变更，从外部看起来就好像这个对象对应的类发生了改变一样。状态模式的通用类图如图所示。  
![Alt text](state.jpg "状态模式类图")

 我们先来看看状态模式中的3个角色。

- State抽象状态角色：接口或抽象类，负责对象状态定义，并且封装环境角色以实现状态切换。
- ConcreteState具体状态角色：每一个具体状态必须完成两个职责：本状态的行为管理以及趋向状态处理，通俗地说，就是本状态下要做的事情，以及本状态如何过渡到其他状态。
- Context环境角色：定义客户端需要的接口，并且负责具体状态的切换。


# 状态模式的应用
### 1.状态模式的优点
 * 结构清晰：避免了过多的switch...case或者if...else语句的使用，避免了程序的复杂性，提供系统的可维护性。
 * 遵循设计原则：很好地体现了开闭原则和单一职责原则，每个状态都是一个子类，你要增加状态就要增加子类，你要修改状态，你只修改一个子类就可以了。
 * 封装性非常好：这也是状态模式的基本要求，状态变换放置到类的内部来实现，外部的调用不用知道类内部如何实现状态和行为的变换。


### 2.状态模式的缺点 
状态模式既然有优点，那当然有缺点了。但只有一个缺点，子类会太多，也就是类膨胀。如果一个事物有很多个状态也不稀奇，如果完全使用状态模式就会有太多的子类，不好管理。  


### 3.状态模式的使用场景
 * 行为随状态改变而改变的场景。
 * 条件、分支判断语句的替代者：在程序中大量使用switch语句或者if判断语句会导致程序结构不清晰，逻辑混乱，使用状态模式可以很好地避免这一问题，它通过扩展子类实现了条件的判断处理。
 
### 4.状态模式的注意事项
状态模式适用于当某个对象在它的状态发生改变时，它的行为也随着发生比较大的变化，也就是说在行为受状态约束的情况下可以使用状态模式，而且使用时对象的状态最好不要超过5个。

 