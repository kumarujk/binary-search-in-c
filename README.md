# binary-search-in-c
the binary search is for the searching the element in the sorted array.


#include<stdio.h>
int bs(int *,int ,int);
void main(){
    int a[]={2,4,5,9,12};
    int data;
    int n =sizeof(a)/sizeof(*a);
    scanf("%d",&data);
    
    printf("%d is found @ %d",data,bs(a,n,data));
}
    int bs(int *a,int n,int data){
        int low=0,high=n-1,mid;
        while(low<=high){
            mid=(low+high)/2;
            if(a[mid]==data)
            return mid;
            else if(data>a[mid])
            low=mid+1;
            else
            high=mid-1;
        }
        return -1;
    }

