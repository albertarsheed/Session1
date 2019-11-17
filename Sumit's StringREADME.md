# Session1
import java.util.*;

public class SumataString 
{
   public static void main(String[] args) {
	Scanner sc=new Scanner(System.in);
	     int t=sc.nextInt();
	     sc.nextLine();
	     while(t-->0) {
	    	 String s=sc.next();
	    	 int sum=0;
	    	 for(int i=1;i<s.length();i++) {
	    		 if(s.charAt(i)-s.charAt(i-1)==1||s.charAt(i)-s.charAt(i-1)==-1) {
	    			 sum+=0;
	    		 }else if(s.charAt(i)=='a'&&s.charAt(i-1)=='z') {
	    			 sum+=0;
	    		 }else if(s.charAt(i)=='z'&&s.charAt(i-1)=='a') {
	    			 sum+=0;
	    		 }else {
	    			 sum+=1;
	    		 }
	    	 }
	    	 if(sum==0) {
	    		 System.out.println("YES");
	    	 }else {
	    		 System.out.println("NO");
	    	 }
	     }
	
}
   
}
