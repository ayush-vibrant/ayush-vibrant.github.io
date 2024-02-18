# Understanding Pass-by-Value and Pass-by-Reference in Java

In Java, when calling a function and the parameter is of type int , it is passed by value.
Java uses a pass-by-value mechanism for all primitive data types, including int . This means that a copy of the value is passed to the function, and any modifications made to the parameter inside the function will not affect the original value outside the function.

```javascript
public void updateValue(int value) {
    value = 10; // Modifying the parameter inside the function
}

int num = 5;
updateValue(num);
System.out.println(num); // Output: 5
```

> In the above code, even though the value parameter is assigned a new value inside the updateValue function, the original num variable remains unchanged because int is passed by value.

> [!TIP]
> Now if you ever feel the need to pass int as pass by reference. The hack is to pass `int[] nums` as a param. Here num would be an int array of size 1. Where nums[0] would be that int that you wanted to be passed by reference.


Now, if the parameter is of type `Integer` , which is an object wrapper for `int`, the situation is slightly different. Java objects are passed by value as well, but the value being passed is actually a reference to the object.

```javascript
public void updateValue(Integer value) {
    value = 10; // Modifying the reference inside the function
}

Integer num = 5;
updateValue(num);
System.out.println(num); // Output: 5
```

> In this case, the num variable is of type Integer, and its value is a reference to an object containing the value 5. When updateValue is called, a copy of the reference is passed to the function. However, when the value parameter is assigned a new value of 10, it only modifies the local reference inside the function and does not affect the original num variable outside the function.


In summary, Java uses pass-by-value for both `int` and `Integer` types. With `int`, a copy of the value is passed, and with `Integer` , a copy of the reference to the object is passed.

If a user-created `Pair` class object is passed as a parameter to a function in Java, it follows the same pass-by-value mechanism as for other objects.

Here's an example of a `Pair` class:

```javascript
public class Pair<T1, T2> {
    private T1 first;
    private T2 second;
    public Pair(T1 first, T2 second) {
        this.first = first;
        this.second = second;
}
    // Getters and setters omitted for brevity
}
```


When you pass a `Pair` object as a parameter, the value being passed is a copy of the reference to the `Pair` object. Inside the function, you can modify the state of the `Pair` object, but you cannot modify the reference itself (i.e., make it refer to a different object).


```javascript
public void updatePair(Pair<Integer, String> pair) {
    pair.setFirst(10); // Modifying the state of the Pair object
    pair.setSecond("Updated");
}

Pair<Integer, String> myPair = new Pair<>(5, "Original");
updatePair(myPair);
System.out.println(myPair.getFirst()); // Output: 10
System.out.println(myPair.getSecond()); // Output: "Updated"
```

> In the above code, the updatePair function takes a Pair<Integer, String> object as a parameter. Inside the function, the state of the pair object is modified using the provided setters. When you access the myPair object after calling updatePair, you can observe that the changes made inside the function are reflected in the original Pair object.

So, in summary, when you pass a user-created `Pair` class object as a parameter, Java uses pass-by-value, where the value being passed is a copy of the reference to the object.


**NOTE:**

Passing a `Pair` object and passing an `Integer` object are not the same in Java.
When you pass a `Pair` object as a parameter, as explained earlier, you are passing a copy of the reference to the object. This means that any modifications made to the state of the Pair object inside the function will affect the original object outside the function.
On the other hand, when you pass an `Integer` object as a parameter, Java treats it as pass-by-value. This means that a copy of the reference to the `Integer` object is passed, but modifications made to the parameter inside the function will not affect the original object outside the function.


```javascript
public void updatePair(Pair<Integer, String> pair) {
    pair.setFirst(10); // Modifying the state of the Pair object
    pair.setSecond("Updated");
}

public void updateInteger(Integer value) {
    value = 10; // Modifying the parameter value
}

Pair<Integer, String> myPair = new Pair<>(5, "Original");
updatePair(myPair);
System.out.println(myPair.getFirst()); // Output: 10
System.out.println(myPair.getSecond()); // Output: "Updated"
Integer myInteger = 5;
updateInteger(myInteger);
System.out.println(myInteger); // Output: 5
```

> When the myPair object is passed to the updatePair function, the modifications made to the pair parameter inside the function affect the original myPair object. However, when the myInteger object is passed to the updateInteger function, the modification of the value parameter inside the function does not affect the original myInteger object.
