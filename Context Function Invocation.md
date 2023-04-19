# Context Function Invocation

Simple function body:

```kt
fun makeReport(name: String, from: LocalDate) {
	val data1 = foo(name)
	val data2 = fetch(data1)
	if (!inRange(from)) return
	listOf(data1, data2)
}
```

## Rules
+ Function's body defines the context of the execution.
+ All values created are part of the context.
+ Functions take implicit arguments from the context by matching the type of the values. We do not pass explicit arguments to functions.

### Example

```kt
fun makeReport(name: ReportName, from: ReportFromDate) {
	val data1 = foo			// function call
	val data2 = fetch		// function call
	if (inRange) return
	makeList				// no common methods
}
```

## Consequences
+ Use of common types (`String`, `Int`) becomes discouraged. Instead, we should use domain types (type classes...).
+ Overloading of the functions is disabled.
+ Function body becomes small once when all possible arguments exist simultaneously in the same context.
+ Possible issues with inheritance. The highest type in the hierarchy wins. On the good side, inheritance becomes less desirable.

#idea