# My-exercise-in-Class
#include <iostream>
using namespace std;
void main()
{
	int n;
	int a[100];
	cout<<"Enter n: ";
	cin>>n;
	cout<<"Enter elements: ";
	for(int i=0;i<n;i++)
	{
		cin>>a[i];
	}
	int k=0,max=0;
	for(int i=0;i<n;i++)
	{
		while(a[i+k]<=a[i+k+1]&&i+k<n)
		{
			k++;
		}

		if(k>max)
		{
			max=k;
		}
		k=0;
	}
	for(int i=0;i<n;i++)
	{
		while(a[i+k]<=a[i+k+1]&&i+k<n)
		{
			k++;
		}

		if(max==k)
		{
			for(int j=i;j<i+k+1;j++)
			{
				cout<<a[j]<<" ";
			}
			cout<<endl;
		}
		k=0;
	}
	}
