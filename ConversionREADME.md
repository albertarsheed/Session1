# Session1
#Given a string, convert it into its number form .

*    A or a -> 1
*    B or b -> 2
*    C or c -> 3
*      . . .
*    Z or z -> 26
*    space -> $

import java.util.*;

public class StringStck {
   public static void main(String[] args) {
	Scanner sc=new Scanner(System.in);
	 int q=sc.nextInt();sc.nextLine();
	 while(q-->0) {
		 String s=sc.nextLine();
		  s=s.toLowerCase();
		  
		 String r="";
		 for(int i=0;i<s.length();i++) {
			 if(Character.isWhitespace(s.charAt(i))) {
				 r=r+'$';
			 }
			 else {
				int a=((int)s.charAt(i))-96;
				r=r+a;
			 }
		 }
		 System.out.println(r);
		
	 }
}
}
