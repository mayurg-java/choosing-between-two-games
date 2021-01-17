# choosing-between-two-games
this code is made for my Coursera assessment which calls one of two methods as per user input. program works fine but when i submit it into Codio it is showing me two errors which I don't know how to solve.

package simpleGame;

import java.util.Scanner;

public class SimpleGame {
    
	/**
	 * Write a method to convert the given seconds to hours:minutes:seconds.
	 * @param seconds to convert
	 * @return string for the converted seconds in the format: 23:59:59
	 * 
	 * Example(s): 
	 * - If input seconds is 1432, print and return output in the format: 0:23:52
	 * - If input seconds is 0, print and return output in the format: 0:0:0
	 * - If input seconds is not valid (e.g. -1), print and return output in the format: -1:-1:-1
	 */
	public static String convertTime(int sec){
		// TODO: Your code goes here
		@SuppressWarnings("resource")
		Scanner in = new Scanner(System.in);
        System.out.print("Input seconds: ");
		int seconds = in.nextInt(); 
        int p1 = seconds % 60;
        int p2 = seconds / 60;
        int p3 = p2 % 60;
        p2 = p2 / 60;
     
        System.out.print( p2 + ":" + p3 + ":" + p1);
		System.out.print("\n");
		return null;
	}

	/**
	 * Write a method that adds all the digits in the given positive integer.
	 * @param integer to add digits
	 * @return integer in which all the digits in the given positive integer are added.
	 * 
	 * Example(s): 
	 * - If input is 565, print and return 16.
	 * - If input is 7, print and return 7.
	 * - If input is 0, print and return 0.
	 */
	public static int digitsSum(int input){
		// TODO: Your code goes here
		   @SuppressWarnings("resource")
		Scanner in = new Scanner(System.in);
		      System.out.print("Input an integer: ");
		      int digits = in.nextInt();
			  System.out.println("The sum is " + sumDigits(digits));
			return digits;
		    }

		 public static int sumDigits(long n) {
				int result = 0;
				
				while(n > 0) {
					result += n % 10;
					n /= 10;
				}
				
				return result;	}
	
	public static void main(String[] args) {
		// Create an instance of the SimpleGame class.
		// TODO: Your code goes here
		
		Scanner sc = new Scanner(System.in);
		 System.out.println("pick a Game");
		 int myInt = sc.nextInt();
		
		// Ask the user which game to play.
		// Then ask the user for input and pass the value to the corresponding method.
		
		// If the user enters 1, ask for an integer to convert and call the convertTime method.
		// If the user enters 2, ask for an integer and call the digitsSum method.
		
		// TODO: Your code goes here
		
		 if(myInt == 1) {
			 convertTime(myInt);
		 }
		if(myInt == 2) {
			 digitsSum(myInt);
		 }
		
		sc.close();
	}	
	 
	 

}
