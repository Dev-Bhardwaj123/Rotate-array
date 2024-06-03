# Rotate-array
Rotate array by d places in left manner
//Rotate array by d places
#include<iostream>
using namespace std;

void leftRotate(int arr[],int n,int d){
	int temp[d];
	for(int i=0;i<d;i++){
		temp[i]=arr[i];
	}
	for(int i=d;i<n;i++){
		arr[i-d]=arr[i];
	}
	for(int i=0;i<n;i++){
		arr[n-d+i]=temp[i];
	}
}

int main(){
	int n;
	cout<<"Enter size of arrays: ";
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++){
		cin>>arr[i];
	}
	int d;
	cout<<"Enter places to be rotated by: ";
	cin>>d;
	leftRotate(arr,n,d);
	for(int i=0;i<n;i++){
		cout<<arr[i]<<" ";
	}
	
}
