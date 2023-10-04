# Classes

In Java, a class is a blueprint or template for creating objects. It defines the structure and behavior of objects of that
class. Classes are one of the fundamental concepts in object-oriented programming (OOP) and serve as the foundation for 
creating objects and organizing code.

````java
// Creating class Cookie
public class Cookie{
    private String color; // you should make all your class variables private
    // Creating a constructor
    public Cookie(String color){
        this.color = color;
    }
    // Creating a getter for color
    public String getColor(){
        return color; // this will return the color of the cookie
    }
    // Creating a setter for color
    public void setColor(String color){
        this.color = color; // this will change the cookie color with the given color
    }
}
````

# Pointers

````java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> map1 = new HashMap<>();
        HashMap<String, Integer> map2 = new HashMap<>();
        map1.put("value",11);
        map2 = map1;
        System.out.println(map1);
        System.out.println(map2);
        // both map1 and map2 are pointing to the same hashmap
    }
}
````
