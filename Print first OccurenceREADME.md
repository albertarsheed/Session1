# Session1

import java.util.*;
import java.io.*;

class TestClass {
    public static void main(String args[] ) throws Exception {
       
        BufferedReader sc=new BufferedReader(new InputStreamReader(System.in));
        int t=Integer.parseInt(sc.readLine().trim());
        while(t-->0){
        String s=sc.readLine().trim();
        LinkedHashSet<Character>ls=new LinkedHashSet();
        
        for(int i=0;i<s.length();i++){
            ls.add(s.charAt(i));
        }
        for(Character cc:ls){
            System.out.print(cc);
        }
 System.out.println();
    }
       
    }
}
