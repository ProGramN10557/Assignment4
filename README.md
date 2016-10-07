/**
 * Finish all the assignments before next class. There is no standard answer for this assignment.
 * 
 
 */
 
1. Write JUnitTest for all the problems in assignemnt3.

import static org.junit.Assert.*;

import org.junit.Test;

public class findPowerTest {

	@Test
	public void test() {
		findPowerofthree test = new findPowerofthree();
		int[] res = {1,3,9,27};
		Assert.assertArrayEquals(test.findPowerOfThree(4),res);
		int[] res1 = {1};
		Assert.assertArrayEquals(test.findPowerOfThree(1),res1);
	}

}

public class countDigitsTest {

	@Test
	public void test() {
		countDigits test = new countDigits();
		Assert.assertTrue(test.countDigits(152) == 2);
		Assert.assertTrue(test.countDigits(300) == 0);
		Assert.assertTrue(test.countDigits(31) == 1);
	}

}


public class pascalTriangleTest {

	@Test
	public void test() {
		pascalTriangle test = new pascalTriangle();
		int[][] res = {{1,0,0,0},{1,1,0,0},{1,2,1,0},{1,3,3,1}},{1,4,6,4,1}};
		Assert.assertArrayEquals(test.generate(5),res);
		
	}

}

public class reverseVowelsTest {

	@Test
	public void test() {
		reverseVowels test = new reverseVowels();
		Assert.assertEquals(test.reverseV("Vishaal"), "Vashail");
		Assert.assertEquals(test.reverseV("Java"), "Java");
		Assert.assertEquals(test.reverseV("classes"), "clessas");
		
	}

}

public class lengthOfLastWordTest {

	@Test
	public void test() {
		lengthOfLastWord test = new lengthOfLastWord();
		Assert.assertTrue(test.lengthOfLastWord("     vish") == 4);
		Assert.assertTrue(test.lengthOfLastWord("     aal    ") ==3);
		Assert.assertTrue(test.lengthOfLastWord("Zz    ") == 2);
		
	}

}

public class reverseString2Test {

	@Test
	public void test() {
		reverseWords test = new reverseWords();
		String str = "I learn java";
		String strrev = "java learn I";
		Assert.assertEquals(test.reverseWord(str),strrev);
	}

}


public class checkMessegeTest {

	@Test
	public void test() {
		checkMessege mes = new checkMessege();
		Assert.assertTrue(mes.checkMessage("SOSSOSSOX") == 1);
		Assert.assertTrue(mes.checkMessage("SDESOS") == 2);
		
	}

}

2. Implement Class MusicAlbum which encapsulated a music Album, each album has a string variable albumTitle and a String variable singer representing the name of singer, double variable price representing the price of album, objects of this class are Initialized using all of its instance variables.
The class has accessor methods for all its Variables and a mutator method for price.

Public class MusicAlbum{
	private String albumTitle;
	private String singer;
	private double price;
	
	public MusicAlbum(String albumTitle,String singer,double price) {
	     this.albumTitle = albumTitle;
             this.price = price;
             this.singer = singer;
	     
	}
	public String getAlbumTitle(){
		return AlbumTitle;
	}
	
	public void SetAlbumTitle(String albumTitle){
	       this.AlbumTitle = AlbumTitle;
	}
	
       public String getSinger() {
       return singer;
        }

    public void setSinger(String singer) {
       this.singer = singer;
    	}
	
	public double getPrice() {
	      return price;
	}
	
	public void setPrice(double price) {
	        this.price = price;
	}
	
}

3. Write a class named GasTank containing:
An instance variable named amount of type double, initialized to 0.
A method named addGas that accepts a parameter of type double . The value of the amount instance variable is increased by the value of the parameter.
A method named useGas that accepts a parameter of type double . The value of the amount instance variable is decreased by the value of the parameter.
A method named getGasLevel that accepts no parameters. getGasLevel returns the value of the amount instance variable.


public class GasTank {
double amount = 0;
void addGas(double voladd){
this.amount = this.amount +  voladd;
}
void useGas(double volminus){
this.amount = this.amount- volminus;
}
double getGasLevel(){
return this.amount;
}
	

}


4. Design and implement a class called Car. You need to create necessary attributes for this class, and method if needed
Define the Car constructor to initialize these values (in that order). Include getter and setter methods for all instance data.

public class Car {
    private String brand;
    private String color;
    private String model;
    private int mileage;
     
     public Car(String brand,String color,String model,int mileage){
    	 
    	this.brand = brand;
        this.color = color;
	this.model=model;
    	 this.mileage =mileage;
     }
     
public void setBrand(String brand){
    	 this.brand = brand;
     }
     public String getBrand(){
    	 return brand;
     }

     public void setColor(String color){
    	 this.color = color;
     }
     public String getColor(){
    	 return color;
     }
     
     
     
     public void setModel(String model){
    	 this.model = model;
     }
     public String getModel(){
    	 return model;
     }
     
        
        
     public void setMileage(int Mileage){
    	 this.Mileage = Mileage;
     }
     
     public int getMileage(){
    	 return Mileage;
     }
     
}
5. Combine with problem 3 and 4, define a class named Driver that contains methods like drive and addGas so that the driver can drive the car.

public class Driver {
       private String name;
       private Double gasamount;
       
       
       public Driver(String name){
    	   this.name = name;
    	    	   
       }
       
       public void drive(){
    	   System.out.println("Remove Car from garage");
System.out.println("Drive safely on the road");

       }
       
public class GasTank {
	double amount = 0;
	void addGas(double voladd){
		this.amount = this.amount +  voladd;
	}
	void useGas(double volminus){
		this.amount = this.amount- volminus;
	}
	double getGasLevel(){
		return this.amount;
	}
	

}
     


Bonus: 
Design a java class that encapsulate the data structure Stack (Last in First out). The class has 2 methods:
(push): method for adding items to stack, the push operation adds items to the top of the list
(pop): method for retrieving items from the stack. The pop operation removes an item from the top of the list, and returns its value to the caller.
In the case of overflow the user should be informed with a message
In the case of underflow, the user should be informed with a message & a value of zero is returned.

Assumptions: The stack will hold up to 10 integer values.

public class Stack {
	public final int StackSize = 10;
	private int top;
	private int[] array;
	
	public Stack(int StackSize){
		   array = new int[StackSize];
		   top = -1;
	   }
       public int pop(){
    	   if(top == -1){
    		   System.out.println("Stack empty");
           return 0;
    	   }
    	   return arr[top--]; 
       }
    	   
       public void push(int num){
    	 if(top > StackSize - 1){
    		 System.out.println("out of range");
    	 }
    	   array[++top] = num;
       }
}

