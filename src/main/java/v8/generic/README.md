### Generic Class
```java
public class Pair<T> {
    private T first;
    private T second;
}
```
### Generic Method
```java
class ArrayAlg {
    public static <T> T getMiddle(T... a) {
        return a[a.length / 2];
    }
}

String middle = ArrayAlg.<String>getMiddle("John", "Q.", "Public");
```
### Bounds for Type Variables
```java
class ArrayAlg {
    static <T extends Comparable> T min(T[] a) {
    }
    static <T extends Comparable & Serializable> T min(T[] a) {
    }
}

```
### Type Erasure
* There are no generics in the virtual machine, only ordinary classes and methods.
* All type parameters are replaced by their bounds.
* Bridge methods are synthesized to preserve polymorphism.
* Casts are inserted as necessary to preserve type safety.

