# Receiver Parameter
Receiver parameters are called "this". And you can call the method from your instance without passing anything.
```java
public class Thing {
	// Receiver parameter
	public void doNothing(Thing this) {
		
	}
	
	public static void main(String[] args) {
        	Thing thing = new Thing();
        	thing.doNothing();
        }
}
```

# Unicode
Unicode gets replaced before compilation.
```java
public class Test {
	public static void main(String[] args) {
		if (true == false) { // \u000a\u007d\u007b
			System.out.println("Java can be weird. This line DOES get printed!");
		}
	}
}
```

## Variable names
Variable names can be almost any Unicode string
```java
class Test {
	private int __; // Works
	private int äöüß; // Works
	
	private int _; // Works only in Java 8 and older
}
```

## Parenthesis
You can use as many as you want
```java
class Test {
	public static void main(String[] args) {
		System.out.println("First line");
		{{{{{{{{{{{{{{{{{{{{{
			System.out.println("Second line");
		}}}}}}}}}}}}}}}}}}}}}
	}
}
```

## "--> operator"
This isn't actually a new operator, it's just "--" and ">" combined
```java
class Test {
	public static void main(String[] args) {
		int countdown = 10;

		// Counting down to 0
		while(countdown --> 0) {
			System.out.println(countdown);
		}

		// ... and back up
		while(countdown ++< 10) {
			System.out.println(countdown);
		}
	}
}
```

## Random Links
Randomly inserting links into your code is no problem. This still compiles fine:
```java
class Test {
	public static void main(String[] args) {
		https://blog.jeff-media.com
		System.out.println("Visit my website");
	}
}
```
