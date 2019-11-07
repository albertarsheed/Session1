# Session1
import java.io.*;
import java.util.*;
import java.util.stream.Collectors;

public class SegmentTree 
{
   public static void main(String[] args) throws Exception
   {
      String bf=new BufferedReader(new InputStreamReader(System.in)).lines().collect(Collectors.joining());
      if(bf.contains("public static void main(String[] args)")||bf.contains("import java")) {
          System.out.println("Java");
      }else if(bf.contains("#include")) {
          System.out.println("C");
      }else {
          System.out.println("Python");
      }
   }
   
}
