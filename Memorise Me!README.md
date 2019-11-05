# Session1
#Arijit is a brilliant boy. He likes memory games. He likes to participate alone but this time he has to have a partner. So he chooses you.

In this Game , your team will be shown N numbers for few minutes . You will have to memorize these numbers.

Now, the questioner will ask you Q queries, in each query He will give you a number , and you have to tell him the total number of occurrences of that number in the array of numbers shown to your team . If the number is not present , then you will have to say “NOT PRESENT” (without quotes).
/***
*Solution in Java
*
*
****/

import java.io.*;
import java.util.*;
public class TestClass {
    public static void main(String args[] ) throws Exception {
         BufferedReader sc=new BufferedReader(new InputStreamReader(System.in));
    int n=Integer.parseInt(sc.readLine().trim());
    int a[]=new int[n];
    String s1[]=sc.readLine().split(" ");
   Map<Integer,Integer>hs=new HashMap();
    for(int i=0;i<n;i++){
        int e=Integer.parseInt(s1[i]);
        if(hs.get(e)==null) {
        	hs.put(e,1);
        }
        else {
        	hs.put(e,hs.get(e)+1);
        }
       
    }
    int m=Integer.parseInt(sc.readLine().trim());
    
    for(int i=0;i<m;i++){
       int g=Integer.parseInt(sc.readLine().trim());
       if(hs.get(g)==null) {
           System.out.println("NOT PRESENT");
    	   
       }
       else {
    	   System.out.println(hs.get(g));
       }
      
    }
    }
}

