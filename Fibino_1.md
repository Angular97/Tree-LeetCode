#include<bits/stdc++.h>
using namespace std;
int fibno(int n)
{
    if(n<=1) return n;
      cout<<"hello"<<" "<<n<<endl;
    int f1=fibno(n-1);
    int f2=fibno(n-2);
    int f=f1+f1;
    return f;
}
int fibno_dp(int n,vector<int>&mem)
{
    if(n<=1) return n;
    if(mem[n]!=0) return mem[n];
    cout<<"hello"<<" "<<n<<endl;
    int f1=fibno_dp(n-1,mem);
    int f2=fibno_dp(n-2,mem);
    int f=f1+f1;
    mem[n]=f;
    return f;
}
int main()
{
    int n;
    cin>>n;
    vector<int>mem(n+1);
   // cout<<fibno(n);
    cout<<fibno_dp(n,mem);
}
