# ArrayProgram
Q1: Find the minimum and maximum elements in array?
Ans:

class  ArrayDemo
{
	public static void main(String[] args) 
	{
		int intArray[]=new int []{45,27,58,33,99};
		int small=intArray[0];
		int big=intArray[0];
		for(int i=0;i<intArray.length;i++)
		{
			if(intArray[i]>big)
				big=intArray[i];
			else if(intArray[i]<small)
				small=intArray[i];
		}
		System.out.println("Minnimum element is :" +small);
		System.out.println("Maximum element is :" +big);

	}
}


Q2:Write a program to reverse the array?
Ans:

class ArrayReverse 
{
	public static void main(String[] args) 
	{
		int intArray[]=new int []{9,8,7,6,5,12,4};
		int i;
		System.out.print("Original array elements is \n");

		for(i=0;i<intArray.length;i++)
		{
			System.out.print(intArray[i]+"\t");

		}
		System.out.print("\n\nArray elements after Reversing Order\n");
		for(i=intArray.length-1;i>=0;i--)
		{
			System.out.print(intArray[i]+"\t");

		}
	}
}


Q3:Write a program to sort a given array?
Ans:

class ArraySort 
{
	public static void main(String[] args) 
	{
		int x[]=new int []{9,8,7,6,5};
		System.out.print("Original array elements is \n");

		for(int i=0;i<x.length;i++)
		{
			System.out.print(x[i]+"\t");

		}
		System.out.print("\n\nArray elements after sorting\n");
		for(int i=0;i<x.length;i++)
		{
			for(int j=i+1;j<x.length;j++)
			{
				int temp=0;
				if(x[i]>x[j])
				{
					temp=x[i];
					x[i]=x[j];
					x[j]=temp;
				}
			}
			System.out.print(x[i]+"\t");
				
		}

	}
}


Q5:Move all negative elements to one side of the array?
Ans:

class ArrayOneSide
{
	public static void main(String[] args) 
	{
		int intArray[]=new int []{-1,6,8,7,-4,-3};
		
		int j=0;
		for(int i=intArray.length-1;i>0;i--)
		{
			if(intArray[i]>0)
			{
				if(i!=j)
				{
					int temp;
					temp=intArray[i];
					intArray[i]=intArray[j];
					intArray[j]=temp;
				}
				j++;
			}
		}
		for(int i=0;i<intArray.length;i++)
		{
		System.out.print(intArray[i]+" ");
		}
	}
}


Q6:Find duplicates in an array?
Ans:

class ArrayDuplicate
{
	public static void main(String[] args) 
	{
		int intArray[]=new int []{2,4,5,2,7,5};
		System.out.print("Duplicate elements in the given array is :\n");
		for(int i=0;i<intArray.length;i++)
		{
			for(int j=i+1;j<intArray.length;j++)
			{
				if(intArray[i]==intArray[j])
				{
					System.out.println(intArray[j]);
				}
			}


		}
		
	}
}


Q7:Find a factorial of a large number?
Ans:

class ArrayFact 
{
	public static void main(String[] args) 
	{
		int intArray[]=new int []{1,2,3,4,5};
		int big=intArray[0];
		int fact=1;
		for(int i=0;i<intArray.length;i++)
		{
			if(intArray[i]>big)
				big=intArray[i];
		}
		for(int i=0;i<big;i++)
		{
			fact =fact*intArray[i];

		}
		System.out.println("Factorial of the large number is :"+fact);
	}
}


Q8:How to find common elements  in three sorted array?
Ans:

class ArraySortThreeEle 
{
	public static void main(String[] args) 
	{
		int intArray1[]=new int []{1,3,4,5,6};
		int intArray2[]=new int []{2,3,6,11,12};
		int intArray3[]=new int []{2,3,4,6,8};
		int i=0,j=0,k=0;
		System.out.print("Commen elements in three sorted array is :\n");
		while(i<intArray1.length && j<intArray2.length && k<intArray3.length)
		{
			if(intArray1[i]==intArray2[j] && intArray2[j]==intArray3[k])
			{
				System.out.print(intArray1[i]+" ");
				i++;
				j++;
				k++;
			}
			else if(intArray1[i] < intArray2[j])
			{
				i++;
			}
			else if(intArray2[j] < intArray3[k])
			{
				j++;
			}
			else
			{
				k++;
			}
		}
	}
}


Q10:Write a program to find the sum and product of all elements of an array?
Ans:

class ArraySum 
{
	public static void main(String[] args) 
	{
		int intArray[]=new int []{1,2,3,4,5};
		int sum=0,product=1;
		for(int i=0;i<intArray.length;i++)
		{
			sum=sum+intArray[i];
			product=product*intArray[i];
		}
		
		System.out.println("Sum of all the elements in the array is :"+sum);
		System.out.println("Product of all the elements in the array is :"+product);

	}
}

