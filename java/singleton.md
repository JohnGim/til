# What is a Singleton?

--

It is a class that can only have one object, or an instance of the class, at a time.

This means that if you try to instantiate the Singleton class after it has already been instantiated, the new variable STILL points to the first instance it was created. 

In order to create a Singleton class, make sure to have:

1. Private constructor

2. Static method that has a return type object of this Singleton class. Lazy Initialization is used here often.

The example below is a Singleton.

```Java
class Singleton {
    private static Singleton first_instance = null;
    public String s;
 
    private Singleton()
    {
        s = "Hello I am a string part of Singleton class";
    }
 
    public static Singleton getInstance()
    {
        if (first_instance == null)
            first_instance = new Singleton();
 
        return first_instance;
    }
}
```

Any time the Singleton object is initialized, the `getInstance()` method shoud be used as such: `Singleton x = Singleton.getInstance();`

Compare to a class that is not a Singleton, and will create a new instance of the object every time it's called.

```Java
class NonSingleton {
    private static Singleton NonSingleton;
    public static Singleton NonSingleton()
    {
        return NonSingleton;
    }
}
```
