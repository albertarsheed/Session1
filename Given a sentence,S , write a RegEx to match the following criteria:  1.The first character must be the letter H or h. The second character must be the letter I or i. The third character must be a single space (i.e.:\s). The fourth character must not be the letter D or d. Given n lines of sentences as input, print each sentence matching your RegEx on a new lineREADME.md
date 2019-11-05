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
        int n=sc.nextInt();
        sc.nextLine();
        while(n-->0) {
        String s=sc.nextLine();
        String ss="^[H|h][I|i]\\s[^D|d][a-zA-Z\\s]*";
      
        Pattern p=Pattern.compile(ss);
        Matcher m=p.matcher(s);
        while(m.find()) {
            System.out.println(m.group());
        }
        }
    }
}
