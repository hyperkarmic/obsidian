In JavaScript you have shallow copying and deep copying. A shallow copy of an object is a copy of the object that includes a reference to the original object’s properties, rather than creating new copies of the properties. A deep copy, on the other hand, creates new copies of the original object’s properties, rather than including a reference to the original properties.
***

In this example, the Object.assign() method is used to create a shallow copy of the original object. The copy object includes a reference to the same b property as the original object, rather than creating a new copy of the b property. You can also see that it’s only a shallow copy because once you change b in the original object, that changes is also reflected in the copy object.
***
In JavaScript, a shallow copy is a copy of an object that creates a new object with the same properties as the original object, but does not copy the objects that are referenced by the original object.
***
Most object copying methods are shallow - the deep cloning technique is
const copy = structuredClone(original);
***

#js #javascript #deep-copy #shallow-copy