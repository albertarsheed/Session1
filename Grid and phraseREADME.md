# Session1
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Scanner;

public class Sethod 
{
     public static void main(String[] args) throws NumberFormatException, IOException
    {
	    BufferedReader sc=new BufferedReader(new InputStreamReader(System.in));
	    String s[]=sc.readLine().split(" ");
	      int n=Integer.parseInt(s[0]);
	      int m=Integer.parseInt(s[1]);
	      char[][] c=new char[n][m];
	      for(int i=0;i<n;i++)
	      {
	    	  String s1=sc.readLine().trim();
	    	  for(int j=0;j<m;j++)
	    	  {
	    		  c[i][j]=s1.charAt(j);
	    		
	    	  }
	    	   
	      }
	      int h=0,v=0,d1=0,d2=0;
	      for (int i=0;i<n;i++) // horizontal search (left --> right)
	      {
	      for (int j=0;j<m-3;j++)
	      {
	      if (c[i][j]=='s' && c[i][j+1]=='a' && c[i][j+2]=='b' && c[i][j+3]=='a')
	      {
	      h++;
	      }
	      }
	      }
	      for (int i=0;i<m;i++) // vertical search (top --> bottom)
	      {
	      for (int j=0;j<n-3;j++)
	      {
	      if (c[j][i]=='s' && c[j+1][i]=='a' && c[j+2][i]=='b' && c[j+3][i]=='a')
	      {
	      v++;
	      }
	      }
	      }
	      for (int i=0;i<n-3;i++) // 1st diagonal search (top --> bottom & left --> right)
	      {
	      for (int j=0;j<m-3;j++)
	      {
	      if (c[i][j]=='s' && c[i+1][j+1]=='a' && c[i+2][j+2]=='b' && c[i+3][j+3]=='a')
	      {
	      d1++;
	      }
	      }
	      }
	      for (int i=n-1;i>2;i--) // 2nd diagonal search (bottom --> top & left --> right)
	      {
	      for (int j=0;j<m-3;j++)
	      {
	      if (c[i][j]=='s' && c[i-1][j+1]=='a' && c[i-2][j+2]=='b' && c[i-3][j+3]=='a')
	      {
	      d2++;
	      }
	      }
	      }
	      System.out.println(h+v+d1+d2);
	}
}
