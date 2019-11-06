# Session1
import java.io.*;
import java.util.*;

public class SegmentTree 
{
   public static void main(String[] args) throws Exception
   {
	  BufferedReader sc=new BufferedReader(new InputStreamReader(System.in));
	     int t=Integer.parseInt(sc.readLine().trim());
	     while(t-->0) {
	    	 String s=sc.readLine();
	    	 if(pali(s)) {
	    		 if(s.length()%2==0) {
	    			 System.out.println("YES EVEN");
	    		 }else {
	    			 System.out.println("YES ODD");
	    		 }
	    	 }else {
	    		 System.out.println("NO");
	    	 }
	     }
	      
	      
   }
   static boolean pali(String s) {
	   StringBuffer ss=new StringBuffer(s);
	   ss.reverse();
	   if(s.equals(ss.toString())) {
		   return true;
	   }else {
		   return false;
	   }
   }
}
