# Named implementations of the instances

In languages like Java, it is a common practice to implement an interface with the named class:

```java
public class SomeImpl implements SomeInterface {}
```

Interface implementation does **not** need the named class. This is wrong and has no purpose.

Interface implementations should be anonymous instances with named references:

```kt
val something = SomeInterface {...}
```

(Verb interfaces.)

#oop