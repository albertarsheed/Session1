# Session1
#Mrinal is a coder from BVCOE. He always takes his laptop with him wherever he goes. One day (while on a trek trip ) a monster challenged him to solve one easy task else he was going to kill him.the task is as follows- Given a series of n numbers a1, a2, ..., an and a number of magic-queries. A magic-query is a pair (i, j) (1 ≤ i ≤ j ≤ n). For each magic-query (i, j), you have to return the number of distinct elements in the subsequence ai, ai+1, ..., aj.
import java.io.*;
import java.util.*;

public class SegmentTree 
{
   public static void main(String[] args) throws Exception
   {
	   Scanner sc=new Scanner(System.in);
	      
	         int n=sc.nextInt();
	          int a[]=new int[n];
	         
	          for(int i=0;i<n;i++)
	          {
	        	  a[i]=sc.nextInt();
	          }
	          int k=sc.nextInt();
	      while(k-->0) 
	      {
	    	  TreeSet<Integer>tr=new TreeSet();
	    	  int l=sc.nextInt();
	    	  int r=sc.nextInt();
	    	  
	    	   for(int i=l-1;i<r;i++)
	    	   {
	    		   tr.add(a[i]);
	    	   }
	    	   System.out.println(tr.size());
	    	       
	      }
	      
	      
   }
}
