#include <bits/stdc++.h>
using namespace std;

int main() {
    
	vector <int> arr[100];
	int n,l;
	cin>>n>>l;
	for(int i=0;i<n;i++)
	   {
	       for(int j=0;j<l;j++)
	       {
	           int value;
	           cin>>value;
	           arr[i].push_back(value);
	       }
	       
	   } 
    
    vector <float> v;
    
    for(int j=0;j<l;j++)
    {
        int sum=0;
        for(int i=0;i<n;i++)
         {
             sum+=arr[i][j];
         }
         float value = sum;
         value=value/l;
         v.push_back(value);
    }
	    float sum = 0;
	    for(int j=0;j<l;j++)
        {
            
            for(int i=0;i<n;i++)
             {
                sum=sum+pow((arr[i][j]-v[j]),2);
             }
          
    }
    cout<<sum<<endl;
	
	return 0;
