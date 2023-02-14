# Collections in java

The Java collection framework offers a framework for managing and manipulating the group of objects. The Collections Framework is a 
hierarchy of interfaces and classes that provides an easy management of a group of objects. In Java collections framework is used to 
perform all the operations on data such as searching, sorting, insertion, manipulation, and deletion.

### Hierarchy of collection framework

![Image](https://static.javatpoint.com/images/java-collection-hierarchy.png)

### Methods in collection interface

-`add(object)` method used to add an object to collection.

-`addAll(Collection )` method used to add all the elements from one collection to the other.

-`clear()` method delete all the elements in the collection.

-`contains(Object )` method returns boolean value to show whether element is present or not.

-`containsAll(Collection )` method is used to campare two collections.

-`equals(Object )` method compares the specified object with this collection for equality.

-`hashCode()` method returns hash code value of collection.

-`isEmpty()` method used to check collection whether it is empty or not.

-`iterator()` returns an iterator over a element.

-`max()` method used to return maximum in collection

-`parallelStream()` method returns a parallel Stream with this collection as its source.

-`remove(Object )` method used to remove the object in collection.

-`removeAll(Collection )` method remove all the objects in collection.

-`size()` method used to return the size .

-`spliterator()` method  is used to create a Spliterator over the elements in this collection.

-`stream()` method is used to return a sequential Stream with this collection as its source.

-`toArray()` method used to return array containing all elements in collection.




## Interfaces 

Collections framework have different interfaces. Each interface used to deal with different type of data. 

### Iterable Interface

This is the root interface for the complete  framework. All subclasses implements the iterable interface.

### Collection Interface

This interface implemented by all the classes in the collection framework. This interface includes all the primary techniques which each
collection has like adding the information into the collection, removing the information, clearing the records, etc.

### List Interface

List interface is a child interface of the collection interface. It inhibits a list kind of structure wherein we will save the ordered series 
of data.  This also allows duplicate data to be present in it. This interface is implemented by various clases like arraylist, vector and stack.

##### Implementing  the List interface using arraylist.

```java
import java.io.*;
import java.util.*;

class GFG {
	
	public static void main(String[] args)
	{
		ArrayList<Integer> al = new ArrayList<Integer>();

		for (int i = 1; i <= 5; i++)
			al.add(i);
		System.out.println(al);
		al.remove(3);
		System.out.println(al);
		for (int i = 0; i < al.size(); i++)
			System.out.print(al.get(i) + " ");
	}
}

```


### Queue Interface

The Queue interface is used to hold the elements in FIFO order. It is an ordered list of objects with its use limited to inserting elements at the 
end of the list and deleting elements from the start. Priority Queue class is used to implement queue interface.

##### Implementing the queue interface using priority queue.

 ```java

import java.util.*;

class GfG {
	public static void main(String args[])
	{
		PriorityQueue<Integer> pQueue = new PriorityQueue<Integer>();
		pQueue.add(10);
		pQueue.add(20);
		pQueue.add(15);
		System.out.println(pQueue.peek());
		System.out.println(pQueue.poll());
		System.out.println(pQueue.peek());
	}
}

 ```

### Deque Interface

The deque interface is used to add and delete elements from both the end. This interface extends queue interface.

##### Implementing deque interface.

```java
import java.util.*;
public class ArrayDequeDemo {
	public static void main(String[] args)
	{
		ArrayDeque<Integer> de_que = new ArrayDeque<Integer>(10);
		de_que.add(10);
		de_que.add(20);
		de_que.add(30);
		de_que.add(40);
		de_que.add(50);
		System.out.println(de_que);
		de_que.clear();
		de_que.addFirst(564);
		de_que.addFirst(291);
		de_que.addLast(24);
		de_que.addLast(14);

		System.out.println(de_que);
	}
}

```

### Set Interface

This is a unordered collection of data. we can't store duplicate values in set. This set interface is implemented by various classes like HashSet, 
TreeSet, LinkedHashSet, etc.

##### Implementing set interface using hashset.

```java
import java.util.*;

public class HashSetDemo {
	public static void main(String args[])
	{
		HashSet<String> hs = new HashSet<String>();

		hs.add("Geeks");
		hs.add("For");
		hs.add("Geeks");
		hs.add("Is");
		hs.add("Very helpful");
		Iterator<String> itr = hs.iterator();
		while (itr.hasNext()) {
			System.out.println(itr.next());
		}
	}
}

```


## References

-[geeks for geeks](https://www.geeksforgeeks.org/collections-in-java-2/)

-[java point](https://www.javatpoint.com/collections-in-java)

-[scaler](https://www.scaler.com/topics/java/collections-in-java/)
