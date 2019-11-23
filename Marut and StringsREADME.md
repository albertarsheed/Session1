# Session1

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.*;

public class AbCdEfG {
    public static void main(String args[] ) throws Exception {
        
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int t=0;
        String ss=br.readLine().trim();
        if(!Character.isDigit(ss.charAt(0))){
        	 System.out.println("Invalid Test");
        }else {
        t=Integer.parseInt(ss);
        if(t>10||t<=0){
            System.out.println("Invalid Test");
        }else{
        while(t-->0) {int cap=0;int smal=0;
        String s= br.readLine();
                for(int i=0;i<s.length();i++) {
                	if(Character.isUpperCase(s.charAt(i))) {
                		cap++;
                	} 
                	else if(Character.isLowerCase(s.charAt(i))) {
                		smal++;
                	}
                }
                if(cap+smal==0||s.length()>100) {
                	System.out.println("Invalid Input");
                }else {
                	System.out.println(Math.min(smal,cap));
                }
               
        }
        
    }}}
}
