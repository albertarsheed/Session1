# Session1
/* IMPORTANT: Multiple classes and nested static classes are supported */

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.*;
class TestClass {
    public static void main(String args[] ) throws Exception {
       
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String name = br.readLine();
         LinkedHashSet<Character>lk=new LinkedHashSet();
         for(int i=0;i<name.length();i++){
             lk.add(name.charAt(i));
         }
         for(Character c:lk){
             System.out.print(c);
         }
    }
}
