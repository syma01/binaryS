import java.util.*;
import java.util.Scanner;
import java.util.Arrays;

 public class binaryS{  //here returns the index of
       public static void main(String[] args){
  Scanner input = new Scanner(System.in);
  System.out.println("enter the size of array : ");
  int n = input.nextInt();
  System.out.println("enter numbers : ");
  int[] list = new int[n];
  
  for(int i = 0; i < n; i++){
	  list[i] = input.nextInt();
  }  
    System.out.println("For what number you are looking for?");
  
     int target = input.nextInt();
     int result = binarySearch(list,target);	
   System.out.print(result);	 
  }
         public static int binarySearch(int[] list, int target){
	  int low = 0;
	  int high = list.length - 1; 
	 while( high >= low){
	  int mid = (low + high) / 2;
	 	 
	  if(target< list[mid])
		high = mid - 1;  
	  
	  else if(target > list[mid])
	    high = mid + 1;	
	  
	  else 
        	return mid;		
	 
	 }
	 return -1;
  } 
	 }
	  
  
  
 
