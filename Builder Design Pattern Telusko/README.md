# Builder Design Pattern

Builder pattern is to avoid having complex constructors. In general, you should avoid having a constructor that takes a large number of parameters.
Because the below problems are faced
  1. Suppose we dont want to pass all the parameters to the constructor.
  2. If we want to pass all the elements we should know the sequence of the constructor also.

Coding example below 
  Suppose we want to create the object of the phone class using the builder design pattern approach
   
  
  ``` 
   1.Phone 
  // Builder Pattern 
  public class Phone {
  private String os;
	private int ram;
	private String processor;
	private double screenSize;
	private int battery;
  public Phone(String os, int ram, String processor, double screenSize, int battery) {
		super();
		this.os = os;
		this.ram = ram;
		this.processor = processor;
		this.screenSize = screenSize;
		this.battery = battery;
	}
  @Override
	public String toString() {
		return "Phone [os=" + os + ", ram=" + ram + ", processor=" + processor + ", screenSize=" + screenSize
				+ ", battery=" + battery + "]";
	}
} 
```

```
 2. PhoneBuilder
 
 
public class PhoneBuilder {

	private String os;
	private int ram;
	private String processor;
	private double screenSize;
	private int battery;
	
	public PhoneBuilder setOs(String os) {
		this.os = os;
		return this;
	}
	public PhoneBuilder setRam(int ram) {
		this.ram = ram;
		return this;
	}
	public PhoneBuilder setProcessor(String processor) {
		this.processor = processor;
		return this;
	}
	public PhoneBuilder setScreenSize(double screenSize) {
		this.screenSize = screenSize;
		return this;
	}
	public PhoneBuilder setBattery(int battery) {
		this.battery = battery;
		return this;
	}
	
	public Phone getPhone(){
		return new Phone(os, ram, processor, screenSize, battery);
	}
	
}
```

```
3. Client
public class Client {
	
	public static void main(String[] args) {
		Phone p  = new PhoneBuilder().setOs("Andriod").setRam(2).setBattery(3000).getPhone();
		System.out.println(p);
	}
}

```
