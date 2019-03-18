# c-topic-wise-question-
#include <iostream>
#include<bits/stdc++.h>

using namespace std;

int main() {
    int n,m;
    cin>>n>>m;
    int a[n]={0};
    int b[m]={0};
    for(int i=0;i<n;i++)
    {
        cin>>a[i];
    }
    for(int j=0;j<m;j++)
    {
        cin>>b[j];
    }
    sort(a,a+n);
    sort(b,b+m);
    int c[m+n]={0};
    int p=0,count=0;
    for(int i=0;i<n;i++)
    {
        for(int j=0;j<m;j++)
        {
            if(a[i]==b[j])
            {
                c[p++]=a[i];
                b[j]=-1;
                count++;
            }
        }
    }
    if(count==0)
    {
        for(int i=0;i<n;i++)
        {
            cout<<a[i]<<" ";
        }
        for(int j=0;j<m;j++)
        {
            cout<<b[j]<<" ";
        }
    }
    else
    {
        sort(c,c+p);
        for(int j=0;j<p;j++)
        {
            cout<<c[j]<<" ";
        }
        cout<<"c "<<endl;
        int k=0;
        for(int i=0;i<p;i++)
        {
            k=0;
            for(int j=0;j<n;j++)
            {
                if(c[i]==a[j])
                {
                    k++;
                    if(k>1)
                    {
                        //cout<<"-1"<<a[j]<<" ";
                        a[j]=-1;
                    }
                    
                }
            }
        }
        for(int i=0;i<n;i++)
        {
            if(a[i]>0)
            {
            cout<<a[i]<<" ";
            }
        }
        for(int j=0;j<m;j++)
        {
            if(b[j]>0)
            {
            cout<<b[j]<<" ";
            }
        }
    }
        
    
    
	return 0;
}



https://ide.geeksforgeeks.org/Lia2Dw8AVk
