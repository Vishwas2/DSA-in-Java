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

## Different terms for inputs
Consider the following code :
````java
public class Main{
    public static void printItems(int a, int b){
        for (int i = 0;i<a;i++){
         System.out.println(i);
        }
        for (int j = 0;j<b;j++){
         System.out.println(j);
        }
    }
}
````
You might think that the time complexity of the above code is O(2n) and we drop the constant, so it becomes O(n) but, that
would be wrong. Because a is not equal to n and b is also not equal to n. The time complexity of the above code is O(a+b)
and that is as far as you can simplify this. Likewise instead of one loop after another if we had one inside another then
the time complexity would be O(a*b)

## Big O of Array Lists
We will use an array list instead of an array because we need a data structure that will be dynamic and allow us to add new 
items but a lot of the concepts will apply to arrays also.  
If we want to add or delete an element at the back of an array list, there is nothing that needs to be re-indexed in the
array list. It is one operation to add or remove something (time complexity = O(1)). But if we need to add or delete any 
element to the index 0 then we will have to change the position of every other element in the list. The time complexity in
this case would be O(n). If we want to look for an item by value then we will have to traverse through the entire list(worst case)
and the time complexity will be O(n). On the other hand, if we were looking by index then it will only take 1 operation and
the time complexity will be O(1)

![1_5ZLci3SuR0zM_QlZOADv8Q](https://github.com/Vishwas2/DSA-in-Java/assets/67436082/78804dfd-bd6d-4ed7-b095-dcf4aa949dcd)
***
![image](https://github.com/Vishwas2/DSA-in-Java/assets/67436082/99085325-7bf5-4bce-a79a-921ff6b981ca)
***
![image](https://github.com/Vishwas2/DSA-in-Java/assets/67436082/8fc1507e-37d1-48d7-a0ed-d54c9e455860)
