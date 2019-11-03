# Session1
import java.io.*;
import java.util.*;


public class StackQueue 
{
	
    public static void main(String[] args) throws IOException
    {
    	
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
     
         int n = Integer.parseInt(br.readLine().trim());
         while(n-->0) 
         {
             String s=br.readLine().trim();
             if(HowIsIt(s)) {
            	 System.out.println("YES");
             }else {
            	 System.out.println("NO");
             }
               
         }
        	 
         }

         static boolean HowIsIt(String s) {
        	   Stack<Character> st=new Stack<>();
        	 for(int i=0;i<s.length();i++)
             {
          	   if(s.charAt(i)==']') 
          	   {
          		   if(!st.isEmpty()&&st.peek()=='[') {
          		   st.pop();   }
          		   else {
          			   return false;
          		   }
          	   }
          	   else if(s.charAt(i)==')') 
          	   {
          		   if(!st.isEmpty()&&st.peek()=='(') {
          			 st.pop();   }
          		   else {
          			   return false;
          		   }
          	   }
          	   else if(s.charAt(i)=='}') 
        	   {
        		   if(!st.isEmpty()&&st.peek()=='{') {
        			   st.pop();   }
        		   else {
        			   return false;
        		   }
        	   }
          	   else {
          		   st.push(s.charAt(i));
          	   }
             }
        	 if(st.isEmpty()) {
        		 return true;
        	 }else {
        		 return false;
        	 }
         }
       
}
