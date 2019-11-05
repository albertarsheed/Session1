# Session1
import java.util.LinkedList;
import java.util.*;
import java.util.Scanner;
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class DangerGame 
{
    public static void main(String[] args)
    {
	    Scanner sc=new Scanner(System.in);
	    String s=sc.next();
	    Pattern p=Pattern.compile("\\d{4}");
	    Matcher m=p.matcher(s);
	    TreeSet<Integer>tr=new TreeSet();
	    while(m.find()) {
	    	tr.add(Integer.parseInt(m.group()));
	    }
	   for(Integer i:tr) {
		   System.out.println(i);
	   }
	}
}
