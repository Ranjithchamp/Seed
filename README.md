# Seed
import java.util.Scanner;

public class Seed {

	
	public static void main(String[] args) {
		Scanner input=new Scanner(System.in);
		System.out.println("Enter Seed :");
		int number=input.nextInt();
		int dumy=number;
		int count=0;
		while(dumy!=0)
		{
			++count;
			dumy=dumy/10;
		}
    int dumy1=number;
    int []arr=new int[count];
    int i=0;
    int summ=0;
    while(dumy1!=0)
    {
    	summ=summ*10;
    	summ=summ+dumy1%10;
    	dumy1=dumy1/10;
    }
    while(summ!=0)
    {
    	arr[i++]=summ%10;
    	summ=summ/10;
    }
    int mul=1;
    for(int j=0;j<arr.length;j++)
    {
    	mul=mul*arr[j];
    }
    mul=mul*number;
    System.out.println("Output is ");
System.out.println(mul);
	}

}
