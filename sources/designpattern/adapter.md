### 适配器模式



- 对象适配器模式与类适配器模式比较
    
    
    类适配器采用了继承的方式来实现;而对象适配器是通过传递对象来实现，这是一种组合的方式。
    类适配器由于采用了继承，可以重写父类的方法;对象适配器则不能修改对象本身的方法等。
    适配器通过继承都获得了父类的方法，客户端使用时都会把这些方法暴露出去，增加了一定的使用成本;对象适配器则不会。
    类适配器只能适配他的父类，这个父类的其他子类都不能适配到;而对象适配器可以适配不同的对象，只要这个对象的类型是同样的。
    类适配器不需要额外的引用;对象适配器需要额外的引用来保存对象。
    
    总的来说，使用对象适配器比较好。当然具体问题具体分析。
    
    
- 应用场景

    
    当想使用一个已经存在的类，但它的接口不符合需求时。
    当想创建一个可以复用的类，该类可以与其他不相关的类或不可预见的类协同工作。

- 优点

    
    提高了类的复用性，适配器能让一个类有更广泛的用途。
    提高了灵活性，更换适配器就能达到不同的效果。不用时也可以随时删掉适配器，对原系统没影响。
    符合开放封闭原则，不用修改原有代码。没有任何关系的类通过增加适配器就能联系在一起。

- 缺点


    过多的使用适配器，会让系统非常零乱，不易整体进行把握。明明调用A接口，却被适配成B接口


- Android中的源码分析


    说到适配器，ListView和RecyclerView就再熟悉不过了，ListView现在应该很少用了吧，这里就以RecyclerView来分析