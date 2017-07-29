---
layout: post
title:  "Junior Developer - lotum - Toronto, ON"
date:   2017-07-29 12:35:58 +0100
categories: Job Interview lotum Simple Questions
topics: pre-interview, questions
summary: My Answers to the pre-interview questions for the Junior Developer Position.
image: /assets/blogPage/Bulbasaur.png
---

<p>

<strong>Question 1:</strong> 
Write a function that prints the numbers from 1 to 100. But for multiples of three print “Foo” instead of the number and for the multiples of five print “Bar”. For numbers which are multiples of both three and five print “FooBar”.

 
Example output: 1 2 Foo 4 Bar Foo 7 8 Foo Bar 11 Foo 13 14 FooBar …


public class Main {

	public static void main(String[] args) {
		//call the function from main
		function();
	}
	
	public static void function()
	{
		//loop from 1 to 100
		for (int i = 1; i <= 100; i++)
		{
			//if both conditions are true
			if((i % 3 == 0) && (i % 5 == 0))
			{
				System.out.print("FooBar");
			}
			
			//if i is only divisible by 3
			else if(i % 3 == 0)
			{
				System.out.print(" Foo ");
			}
			
			//if i is only divisible by 5
			else if(i % 5 == 0)
			{
				System.out.print(" Bar ");
			}
			
			// print i when no conditions are true
			else
			{
				System.out.print(" " + i + " ");
			}
		}
	}
}





<strong>Question 2:</strong>
Write a function that determines the number of even numbers that appear in a range of integers 0..n, where n is supplied as the sole argument to your function.
Example:
even_integers(3)
2


public class Main {

	public static void main(String[] args) {
		
		//call the function from main and pass the n argument
		System.out.print(even_integers(3));
	}
	
	public static int even_integers(int range)
	{
		// counter to keep track of instance of even numbers
		int counter = 0;
		
		//loop from 0 to the passed n range 
		for(int i = 0; i <= range; i ++)
		{
			//check if number is even
			if(i % 2 == 0)
			{
				//increment instance
				counter++;
			}
		}
		
		//return the number of times even number is with a range
		return counter;
	}
}






<strong>Question 3:</strong>
Given the following pseudo code, determine the range of possible values for “a”.
x = random_int(1,6)
y = random_int(1,6)
z = random_int(1,6)
a = x + y + z

Range has a start point and end point.

variable x can be any number between 1 and 5

variable  y also, can be any number between 1 and 5

variable  z also, can be any number between 1 and 5

to find and determine the start of range, we must find the lowest number all of these 3 variables can have at any instance.
In this case it is 1.

variable a, can have an instance of adding 1 three times.
1+1+1 = 3.

RangeStart will be 3.


Range End will be the largest number the that is returned by the random_int function.
In this case that is 5.


variable a, can have also have an instance of adding 5 three times.
5+5+5 = 15.

RangeEnd = 15;

Range: 3-15


Test Case 1:

x = 6;
y = 5;
z = 4;

a = 6+5+4;
sum of a = 15

15 is within range




import java.util.Random;

public class Main {

	public static void main(String[] args) {
		
		int x, y, z;
		int a = 0;
		
		x = random_int(1,6);
		y = random_int(1,6);
		z = random_int(1,6);
		
		a = x + y + z;
		
		System.out.println(a);
	}
	
	public static int random_int(int firstNum, int secondNum)
	{
		Random r = new Random();
		int low = firstNum;
		int max = secondNum;
		return (r.nextInt(max-low) + low);
	}
}





<strong>Question 4:</strong>
Given: words = ['one', 'one', 'two', 'three', 'three', 'two']


import java.util.HashSet;
import java.util.Set;

public class Main {

	public static void main(String[] args) {
		
	//set of empty string
	Set<String> set = new HashSet<String>();
	
	//array of words
	String[] words = {"one", "one", "two", "three", "three", "two"};
	
	//for each loop
	for(String newWords : words)
	{
		//add values from words to the set only if not added previously
		set.add(newWords);
	}
	//print the set
	System.out.print(set);
	}
}

</p>