# Session1

import java.util.*;

public class RegexChecUp 
{
    public static void main(String args[] ) throws Exception 
    {
        
        Scanner sc= new Scanner(System.in);
          int n=sc.nextInt();
          int k=sc.nextInt();
          int a[]=new int[n];
          long s1=0;
          for(int i=0;i<n;i++)
          {
              a[i]=sc.nextInt();
              if(i<k) {
            	  s1+=a[i];
              }
          }
          long MaxSum=0;
          int x=0;
          for(int i=0;i<k;i++) 
          {
        	  if(MaxSum<s1) {
        		  MaxSum=s1;
        	  }
        	  s1=s1-a[k-1-x];
        	  s1=s1+a[n-1-x];x++;
          }
       System.out.println(MaxSum);
    }
}
