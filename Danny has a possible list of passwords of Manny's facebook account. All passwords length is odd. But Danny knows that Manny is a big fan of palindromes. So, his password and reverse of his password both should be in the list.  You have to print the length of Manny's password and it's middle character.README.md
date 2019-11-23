# Session1

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.HashSet;

public class TestTrial {
    public static void main(String args[] ) throws Exception {
        
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int t=Integer.parseInt(br.readLine().trim());
        HashSet<String> hs=new HashSet<>();
        while(t-->0) {
        String s= br.readLine();
        hs.add(s);
        }
        for(String s:hs) {
        	StringBuffer bf=new StringBuffer(s);
        	bf.reverse();
        	if(hs.contains(bf.toString())) {
        		System.out.println(s.length()+" "+s.charAt(s.length()/2));break;
        	}
        }
    }
}
