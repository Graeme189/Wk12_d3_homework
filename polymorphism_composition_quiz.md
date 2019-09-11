# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

The ability of an object to take on more than one form.

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

An example could be, with classes called 'Printer' and 'Monitor', implementing an interface called 'IConnect' that would allow both 'Printer' and 'Monitor' to be added to an ArrayList in a 'Network' class using the same method: 

ICONNECT:
public interface IConnect {
    public String connect(String data);
}

NETWORK:
public void connect(IConnect device){
    devices.add(device);  
}

PRINTER:
public class Printer implements IConnect{
    public String connect(String data) {
    return "connecting to " + data + " network";
    }   
}

3. What can we use to implement polymorphism in Java?

We use interfaces.

4. How many 'forms' can an object take when using polymorphism?

As many as required.

5. Give an example of when you could use polymorphism.

As above, you could use this when you wanted different classes to use the same method within a separate class.


# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

When an object is 'composed' of other, separate objects

7. When would you use composition? Provide a simple example in Java.

When you have an object that uses several different components, e.g. in the below the 'Guitar' class is partly composed of the 'Strings' and 'Plectra' class

class Strings {
    private int number;
}

class Plectra {
    private int thickness
}

class Guitar {
    private String make;
    private String model;
    private Strings strings;
    private Plectra plectrum;
}

8. What is/are the advantage(s) of using composition?

- Composition allows for several components to be used in one object
- It also means that objects can implement only the components/behaviours/objects that object needs

9. When an object is destroyed, what happens to all the objects it is composed of?

All these objects are destroyed too.
