# Big O
It is a way of comparing two or more codes mathematically about how efficient they run.
***

## Time Complexity
Time complexity of a code is measured in the number of operations it takes to complete.

## Space Complexity
Space complexity is the amount of space the code will take.
***

## Big O Worst Case
Technically Big O is always worst case

## O(n)
 Code Example :  
````java
public class Main{
    public static void printItems(int n){
        for (int i = 0; i<n;i++){
         System.out.println(i);
        }
    }
}
````
 * The above given code is O(n) because we have to n operation for input n.

## Drop Constants
 Consider the following code :
````java
public class Main{
    public static void printItems(int n){
        for (int i = 0;i<n; i++){
         System.out.println(i);
        }
        for (int j = 0;j<n; j++){
         System.out.println(j);
        }
    }
}
````
* The above code performs 2n operations for input n. You might think that the time complexity will now be O(2n), but that
would be incorrect. The time complexity in this case is O(n) because we dropped the constant 2. It doesn't matter what the
constant is, we have to drop it for simplification.

## O(n<sup>2</sup>)
Consider the following example :
````java
public class Main{
    public static void printItems(int n){
        for (int i = 0; i<n;i++){
            for (int j = 0;j<n;j++){
             System.out.println(i+" "+j);
            }
        }
    }
}
````
* In the above code if you give 10 as input, it will perform 100 operations. So, for an input of n this code will perform
 n<sup>2</sup> operations. The time complexity of the above code is O(n<sup>2</sup>).

## Drop Non-Dominants 
Consider the following example :
````java
public class Main{
    public static void printItems(int n){
        for (int i = 0; i<n; i++){
            for (int j = 0; j<n; j++){
             System.out.println(i+" "+j);
            }
        }
        for (int k = 0;k<n;k++){
         System.out.println(k);
        }
    }
}
````
* The above code performs n<sup>2</sup> + n operations for n as input. As the value of n becomes very large, n becomes very 
small as compared to n<sup>2</sup> so we write the time complexity for this code as O(n<sup>2</sup>).

## O(1)
Consider the following code :
```java
public class Main{
public static int addItems(int n) {
    return n+n;
}}
```
* In the above code it doesn't matter what is the value of n, there is only going to be one operation. This is O(1). In 
this situation as n grows the number of operations remain the same.

## O(log n)
Consider a sorted array(ascending) of 8 numbers 1 to 8. If I want to find 1, the quickest way to narrow it down is to 
cut the array in half see if 1 is first half or second half. Since the array is not in the second half so we remove it. Now,
we repeat this process until we get the desired number(1 in this case). It took us 3 steps to reach the number 1 in an array 
of 8 numbers and 2^3 = 8 . Now we take this and convert it into logarithm which becomes log<sub> 2 </sub>8 = 3. O(log n) is 
very efficient (next best thing after O(1)).
