# Project4
package recursion;

import java.util.Scanner;

public class Recursion {

	// Class example
	public static int sum_up(int n) {
		if (n <=0 ) {
			return 0;
		}
		else {
			return n + sum_up(n-1);
		}
	}
	
	// Class example
	public static int sum_up_tail(int n) {
		return sum_up_tail(n, 0);
	}
	public static int sum_up_tail(int n, int tmp) {
		if (n <1 ) {
			return tmp;
		}
		else {
			return sum_up_tail(n-1, tmp+n);
		}
	}
	
	public static int fact(int n) {
		if(n==1) {
			return 1;
		} else {
			int result = n * fact(n-1);
			return result;
		}
	}
	
	public static int fib(int n) {
		if(n<=1) {
			return 1;
		} else {
			int result = fib(n-2)+fib(n-1);
			return result;
		}
	}
	
	public static int gcd(int num1, int num2) {
		if (num2<=num1 && num1%num2 == 0) {
			return num2;
		}else if(num1<num2) {
			return gcd(num2,num1);
		} else {
			return gcd(num2, num1%num2);
		}
	}


	public static int power (int x, int y) {
		if(y==0) {
			return 1;
		} else if (x==0) {
			return 0;
		} else if (y<0) {
	        throw new IllegalArgumentException("Invalid Power");
		}   else {
			return x * power(x,y-1);
		}
	}


	public static int balance(int x, int y) {
		if(x-y==1) {
			return y; 
		} else if (y-x==1) {
			return x;
		} else if (x>y) {
			return balance(x-1,y+1);
		} else if (y>x) {
			return balance(x+1,y-1);
		}
		return x;
	}
		
	public static int Ackermann(int m, int n) {
		if(m==0) {
			return n+1;
		} else if(n==0) {
			return Ackermann(m-1,1);
		} else {
			return Ackermann(m-1,Ackermann(m,n-1));
		}
	}
	
	public static playGuessingGame(int m) {
		
	}

}
