What is a typeclass?
====================

If you've used Java a reasonable amount there's a prime candidate of how we do things with inheritance:

```java
public interface Comparable<T> {
    public int compareTo(T o);
}
```

Later on in Java we got this as an alternative:

```java
public interface Comparator<T> {
    int compare(T o1, T o2);
}
```

The above is probably the closest Java has to typeclasses.
