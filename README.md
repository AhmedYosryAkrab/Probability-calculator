# Probability-calculator
A calculator program to calculate Mean,Standard deviation,Coefficeint of variance.


package Probability1;                            /*Java program using methods to calculate mean,sd & cv*/

import java.util.Scanner;

public class Compute {

	public static double mean(double mean){
		double sum = 0;
		double mean1 =0;
		int n=0;
		Scanner a=new Scanner(System.in);
		n=a.nextInt();
		double [] arr=new double [n];
				for(int i=0;i<n;i++){
					arr[i]=a.nextDouble();

				}	
		for(double i : arr){
			sum=sum+i;
		}
		mean1 = sum/n;
		
		return mean1;
	}
	   
	
	public static double sd(double sd){
		double sum = 0;
		double sum2 = 0;
		double sd1=0;
		int n=0;
		Scanner b=new Scanner(System.in);
		n=b.nextInt();
		double [] arr=new double [n];
				for(int i=0;i<n;i++){
					arr[i]=b.nextDouble();

				}	
		for(double i : arr){
			sum=sum+i;
		}
		for(double i : arr){
			sum2=sum2+(double)Math.pow(i, 2);
		}
		                                                              /*sum =(double)Math.pow(sum, 2);*/
		
		double i = 0;
		sd1= Math.sqrt(((sum2)-((sum*sum)/n)/n-1));
		return sd1;
	}
	
	public static double cv(double cv){
		double sum = 0;
		double sum2 = 0;
		double mean2;
		double sd2;
		double cv1=0;
		int n=0;
		Scanner c=new Scanner(System.in);
		n=c.nextInt();
		double [] arr=new double [n];
				for(int i=0;i<n;i++){
					arr[i]=c.nextDouble();

				}	
		for(double i : arr){
			sum=sum+i;
		}
		for(double i : arr){
			sum2=sum2+(double)Math.pow(i, 2);
		}
		mean2 = sum/n;
		sd2= Math.sqrt(((sum2)-((sum*sum)/n)/n-1));
		cv1=(sd2/mean2)*100;

		return cv1;
	}
	
	public static void main(String[] args) {
		double sum = 0;
		double mean=0;
		double sd=0;
		double cv=0;
		int z=0;
		System.out.println("press 1 to get mean"+"\n"+"press 2 to get Standard deviation"+"\n"+"press 3 to get Coefficient of variance"+"\n");
		Scanner d=new Scanner(System.in);
		z=d.nextInt();
		if(z==1){
			System.out.println("1)Determine size of array of the needed numbers to be calculated");
			
			System.out.println("2)Ensert numbers to know the Mean");
			
			System.out.println("Mean:\n"+mean(mean));
		}
		else if(z==2){
			System.out.println("1)Determine size of array of the needed numbers to be calculated\n");
			
			System.out.println("2)Ensert numbers to know the Standard deviation\n");
			
			System.out.println("Standard deviation:\n"+sd(sd));
		}
		else if(z==3){
			System.out.println("1)Determine size of array of the needed numbers to be calculated\n");
			
			System.out.println("2)Ensert numbers to know the Coefficient of variance\n");
			
			System.out.println("Coefficient of variance:\n"+cv(cv)+"%");
		}
		else {
			System.out.println("not in range");
		}	
	}
}
