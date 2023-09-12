import java.util.*;
import java.io.*;

public class Main {

	public static void main(String[] args) {
		Scanner obj=new Scanner(System.in);
		PrintWriter out=new PrintWriter(System.out);
		
		int t=obj.nextInt();
		while(t--!=0)
		{
			int n=obj.nextInt();
			HashMap<Integer,Integer> map=new HashMap<>(); // for array
			for(int i=0;i<n;i++)
			{
				int temp=obj.nextInt();
				map.put(temp, map.getOrDefault(temp, 0)+1);
			}
			//for d array
			for(int i=0;i<n;i++)
			{
				int temp=obj.nextInt();
				map.put(temp, map.getOrDefault(temp, 0)+1);
			}
			int max=0;
			for(Map.Entry<Integer,Integer> m:map.entrySet())
			{
				max=Math.max(max, m.getValue());
			}
			out.println(max);
		}
		out.flush();
	}
}
