# Experiment-19
## AIM
To do sorting in c++.

## Problem Statement
1.) Write a c++ to do selection sorting.

2.) Write a c++ to do insertion sorting.

3.) Write a c++ to do bubble sorting.
## THEORY
A sorting algorithm is used to arrange elements of an array or list in a specific order, based on a defined comparison rule. The comparison operator helps in determining whether one element should come before or after another. Various algorithms apply different strategies to achieve the sorted result.

Selection Sort:
Selection Sort is a basic comparison-based sorting method. The algorithm works by repeatedly finding the minimum (or maximum) element from the unsorted portion of the array and swapping it with the first element of that portion. This process divides the list into two parts: the sorted and unsorted segments. The sorted part grows one element at a time, as the smallest elements are placed in order.

Insertion Sort:
Insertion Sort operates by building a sorted list one element at a time. It picks each element from the unsorted portion of the array and inserts it into its correct position within the already sorted portion. This process mimics how you sort playing cards in your hand, where each new card is inserted into the correct spot among the already sorted cards.

Bubble Sort:
Bubble Sort is a straightforward sorting technique where adjacent elements are repeatedly compared, and if they are in the wrong order, they are swapped. The algorithm "bubbles" the largest unsorted element to its correct position at the end of the list after each pass. Though simple, Bubble Sort is not ideal for large datasets due to its poor performance in terms of time complexity.

## Code
1-
```javascript
//Sharvari Murade
//23070123088
#include <iostream>
using namespace std;

void swap(int *a, int *b){
    int temp;
    temp = *a;
    *a=*b;
    *b=temp;

}
void s_sort(int *a, int elements){
    int n=0;
    int *b;

    while (n!= elements){
        b = a+1; 
        for(int i = 0; i<(elements-1)-n; i++){
            if(*a > *b) {
                swap(a,b);
            }
            b++;
        }
        n++;
        a++;
    }
}
int main(){
    int no_el;
    cout << "How many elements in your array ? "<<endl;
    cin>>no_el;
    int arr[no_el];
    cout<<"Enter "<<no_el<<" Elements: "<<endl;
    for(int i=0; i<no_el;i++){
        cin>>arr[i];
    }
    cout<<"Sorted Array: ";
    s_sort(&arr[0],no_el);

    for(int i=0; i<no_el;i++){
        cout<<arr[i]<< " ";

    }
    return 0;


}
```
2-
```javascript
//Sharvari Murade
//23070123088
#include <iostream>
using namespace std;

void insertionsort(int arr[], int n){
    for (int i = 1; i<n ; i++){
        int key = arr [i];
        int j =i-1;

        while (j>= 0 &&  arr[j]>key){
            arr[j+1] = arr[j];
            j--;
        }
        arr[j+1]= key;
    }
}
int main(){
    int arr[]= {64, 25, 12,22,11};
    int n = sizeof(arr) / sizeof(arr[0]);
    cout<< "Original array: ";
    for (int i =0; i<n;i++){
        cout<<arr[i]<<" ";
    }
    insertionsort(arr,n);
    cout<< "\n Sorted array: ";
    for (int i = 0; i< n ; i++){
        cout << arr[i]<<" ";
    }
    return 0;
    }
```
3- 
```javascript
//Sharvari Murade
//23070123088
#include<iostream>
using namespace std;

void swap(int* a,int* b){
int temp;
 temp=*a;
*a=*b;
 *b=temp;
}
int main(){
 int elements;
  cout<<"How many elements in the array? :";
  cin>>elements;
   int array[elements];
 cout<<"Enter elements:";
for(int i=0;i<elements;i++){
 cin>>array[i];
 }
for(int i=0;i<elements;i++){
 cout<<array[i]<<" ";
  }
 int n=0;
while(n!=elements){
 for(int i=0;i<elements-n;i++){
if(array[i]>array[i+1]){
swap(&array[i],&array[i+1]);
 }
}
 n++;
 }
 cout<<"\nSorted array is:"<<endl;
for(int i=0;i<elements;i++){
 cout<<array[i]<<" ";
 }

 return 0;
}
```
## OUTPUTS
1- <img width="346" alt="image" src="https://github.com/user-attachments/assets/e08b4ba5-1284-4d90-9f29-ca617b619674">


2- <img width="322" alt="image" src="https://github.com/user-attachments/assets/a96ff43e-731c-4a2a-ba49-3fd144414e2c">


3- <img width="341" alt="image" src="https://github.com/user-attachments/assets/a2627e60-4078-4d1a-9726-460a98c23c6b">


