# Session1
import java.util.*;

public class TalentHiring {
   public static void main(String[] args) {
	Scanner sc=new Scanner(System.in);
	int n=sc.nextInt();
	ArrayList<Integer> tr1=new ArrayList();
	ArrayList<Integer> tr2=new ArrayList();
	while(n-->0) {
		int a=sc.nextInt();
		int b=sc.nextInt();
		if(a==0) {
			tr1.add(b);
		}else {
			tr2.add(b);
		}
	}
	Collections.sort(tr1);
	Collections.sort(tr2);
		while(tr1.size()>0) {
			System.out.print(tr1.get(tr1.size()-1)+" ");
			tr1.remove(tr1.size()-1);
		}
		while(tr2.size()>0) {
			System.out.print(tr2.get(tr2.size()-1)+" ");
			tr2.remove(tr2.size()-1);
		
		
	}
}
}
