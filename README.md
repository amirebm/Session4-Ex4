 // برنامه ایی بنوسید که اعدادی رو در آرایه ذخیره و به 2 صورت آنرا مرتب کند


# Session4-Ex4
package com.personal.Ex4;

import java.util.Scanner;

public class Ex4 {
	
	
	public static void main(String[] args) {

		 Ex4 sort = new Ex4();
		int arrayLength;
		Scanner sc= new Scanner(System.in);
		System.out.println("Enter a the size of array");
		arrayLength=sc.nextInt();
		int[] ar= new int[arrayLength];
		
		System.out.println("Please enter "+ arrayLength+ " numbers for array:");
		
		for (int i = 0; i < ar.length; i++) 
		ar[i]=sc.nextInt();	
		
		System.out.println("Araye be soorate moratab nashode");
        printArray(ar);
		
		System.out.println("Mortab saazi be raveshe HOBABI");
		int c= sort.BubbleSort(ar);
        printArray(ar);
		System.out.println("Tedad dafate baresi dar ravaeshe Hobabi:  "+c);

		System.out.println("Mortab saazi be raveshe Insert va Nozoli");

        c=sort.InsertSort(ar);
        printArray(ar);
		System.out.println("Tedad dafate baresi dar ravaeshe Insert:  "+c);
	
	}

	static void printArray(int arr[])
    {
        int n = arr.length;
        for (int i=0; i<n; ++i)
            System.out.print(arr[i] + " ");
        System.out.println();
    }
    public int BubbleSort(int[] ar) {
	
	int Bubblecounter=1;
	int temp;
	for (int i = 0; i < ar.length; i++) {
		
		for (int j = 0; j < ar.length; j++) {
			
			if(ar[j]>ar[i]) {
				temp=ar[j];
				ar[j]=ar[i];
				ar[i]=temp;
				Bubblecounter++;
			}
		}
		
	}
	return Bubblecounter;
	}	

public int InsertSort(int[] ar) {
	
	int i,j,t;
	int InsertCounter=1;
	 
	for (i = 1; i < ar.length; i++) {
		t=ar[i];
		for ( j = i; j > 0; j--) {
			
			InsertCounter++;
			if(t<=ar[j-1])
				break;
			ar[j]=ar[j-1];
				
			
		}
		
		ar[j]=t;
	}
	
	return InsertCounter;
}

   	}

