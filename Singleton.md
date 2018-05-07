## Singletons

### How are they implemented?

Java: In Java, Singleton classes are implemented to only have one object/ one instance of a class. A prime example is a window handler of filesystem

public class ClassicSingleton {

	private static ClassicSingleton instance = null;
    protected ClassicSingleton() {
      // Exists only to defeat instantiation.
    }
    public static ClassicSingleton getInstance() {
      if(instance == null) {
         instance = new ClassicSingleton();
      }
      return instance;
    }

}

Swift: The design priciple behind singletons in Swift are exactly the same as what's stated above about Singletons in Java, with some minor syntax differences. Singletons in Swift are actually a 1-1 port of Objective-C's singleton implementation, which isn't as fleexible as most things in Swift, but gets the job done.

class ClassicSingleton {

    class var sharedInstance: ClassicSingleton {
        struct Static {
            static var onceToken: dispatch_once_t = 0
            static var instance: ClassicSingleton? = nil
        }
        dispatch_once(&Static.onceToken) {
            Static.instance = ClassicSingleton()
        }
        return Static.instance!
    }

}

### Can they be made thread safe

Java: Assuming that a Singleton is implemented in a normal way (something that of the example above), there are 3 ways to make your Singleton thread safe.

1) Create the instance variable at the time of class loading
2) Synchronize the getInstance() method
3) Use synchronzied block inside the if loop and volatile variable


Swift: In order to make your thread safe in swift, there are two ways to make your singleton class thread safe, both of which are done within the class

1) let object:ClassicSingleton = ClassicSingleton.shareInstance
2) make your init() private to prevent others from using default() initializer 

### Can a singleton instance be lazily instantiated?

Java: In Java, thread safe lazy instantiation is accomplished through a patter called 'Initialization-on-demand holder idiom': this idion ensures a safe, highly concurrent lazy initialization with good performance

public class Something {

    private Something() {}

    private static class LazyHolder {
        static final Something INSTANCE = new Something();
    }

    public static Something getInstance() {
        return LazyHolder.INSTANCE;
    }
}


Swift: In swift, lazy instantiating is the alternate for the init() instantiation pattern. 

class TestClass {

    // both of below will init once
    
    // init at first
    let a: Int = {
        print("aaa")
        return 1+2
    }()
    
    // lazy init
    lazy var b: Int = {
        print("bbb")
        return 2+3
    }()
}



