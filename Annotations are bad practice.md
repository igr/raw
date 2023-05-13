# Annotations are bad practice

Annotations, at least how they are used in languages like Java, are lazy shortcuts or shortcuts for lazy.

The annotations' benefits are significantly small compared to the negative impact on the code architecture.

## Example

The JPA repository function:

```java
@Query("select * from all where...")
public List<Foo> findThem()
```

should be:

```scala
def findThem = query("select * from ...")
```

## Example

The Spring wiring annotations:

```java
@Service
public class SomeService {
	public SomeService(Dependecy dep) {}
}
```

should be manually wired:

```scala
def someService = SomeService(dependency)
```

#oop