# Linked list
Linked lists are dynamic just like array lists. In linked lists, instead of all the elements being in a contiguous memory,
they are spread out. Linked list also have a variable head that points to the first node and tail that points to the last node.
Both of these variables are pointers that just point to node. Each node is going to have a pointer that points to the next node.
The last node has a pointer as well, it just points to null.
***
## The main differences between Linked List and Array List
1. Arraylist stores elements in a contiguous block of memory whereas in Linked list elements are not stored in contiguous
memory locations.
2. Array list provides fast random access to elements using their index. Linked list does not provide fast random access.
3. Insertion and deletion in array list is slower when compared to linked list.
4. Array list use less memory than linked list for the same number of elements.
5. Array list is generally fast for read-heavy operations and when you need fast random access. Linked list is more suitable
for scenarios where frequent insertion and deletion is required  

![image](https://github.com/Vishwas2/DSA-in-Java/assets/67436082/6048a6de-31c8-4f78-9313-59bd3b2fc89d)
***
## Big O
### Adding something to the end
Adding something to the end of a linked list is O(1)
### Removing an item at the end
We cannot move backward in the list we can only move in the direction of the arrows are going. So we need to start at the head
and iterate through the list until we get to the pointer pointing to the last element and set tail equal to that pointer.
Because we had to touch every node and iterate though the list,
this will be O(n).
### Adding an item to the beginning of the linked list
This will be very simple since we need to set the pointer of the new element equal to head, this will be O(1).
### Removing the first element
This will also be O(1).
### Inserting a node at a given position
In this case we will have to iterate through the list, so it will be O(n)
### Removing the node that we just inserted
Since we need to iterate through the list to remove the node, it will be O(n)
### Looking for something by value/index
We will have to iterate through the entire list in this case, so it will be O(n). An array list would be better in this case.  

![mpv-shot0001](https://github.com/Vishwas2/Web-development-course/assets/67436082/efeab4e1-b3cd-4cfd-9668-cfbc1e86ad19)
***
## A node consists of both the value and the pointer
![image](https://github.com/Vishwas2/Web-development-course/assets/67436082/4f99ce5b-6754-4bb9-acc7-91c9b3d328dd)
***

## Constructor
````java
public class LinkedList {
    public LinkedList(int value){}
    // Create new node
    public void append(int value){}
    // Create new node 
    // Add node to end
    public void prepend(int value){}
    // Create new node 
    // add node to beginning
    public boolean insert (int index, int value){}
    // Create new node
    // insert node at a particular index
}
````
All the above 4 methods create a new node. So we don't want to write this code 4 different times so we create a new class
that does nothing but create nodes
````java
class Node {
    int value;
    Node index;
    Node(int value){
        this.value = value;
    }
}
````

````java
import org.w3c.dom.Node;

public class LinkedList {
    private Node head;
    private Node tail;
    private int length;
    class Node {
        int value;
        Node index;
        Node(int value){
            this.value = value;
        }
    }
    public LinkedList(int value) {
        Node newNode = new Node(value);
        head = newNode;
        tail = newNode;
        length = 1;
    }
}
````

