Q1.
#include <iostream>
using namespace std;
int main()
{
    int n;cin>>n;
    int c=1,k;
    for(int i=1;i<=n;i++)
    {
        for(int j=i;j<=n;j++)
        {
            cout<<j<<" ";
        }
        cout<<"\n";
        if(i!=n)
        {
        while(c<=i)
        {
            cout<<" ";
            c++;
        }
        }
        c=1;
    }
    k=n-1;c=1;
    while(k>=1)
    {
        while(c<k)
        {
            cout<<" ";
            c++;
        }
        for(int j=k;j<=n;j++)
        {
            cout<<j<<" ";
        }
        cout<<"\n";
        k--;c=1;
    }
}
  
  
  
Q2.

#include <iostream>
#include <string>
#include <algorithm>
using namespace std;
void allsubstring(string a, string b)
{
	int m, n;
	if ((m = b.length()) > (n = a.length()))
		return;
	for (int i = 0;i <= n - m;i++)
	{
		if (is_permutation(a.begin()+i, a.begin()+i+m,b.begin()))
		{
			cout<<"substring "<<a.substr(i,m) <<" present at index "<<i<< '\n';
		}
	}
}
int main()
{
	string a,b;
	cin>>a>>b;
	allsubstring(a,b);
}
