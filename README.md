# integration
#include<iostream>
#include<stdlib.h>
using namespace std;
int choice;
class inputs
{
public:
    inputs()
    {
        int Qstring;
        cout<<"\n1.simple integration\n";
        cout<<"2.integration by parts\n";
        cout<<"3.exit\n";
        cin>>choice;
    }
    simple_integration(int constant,int power)
    {
        int i,cpower;
        cout<<"your Question is"<<endl<<constant<<"x"<<"^"<<power<<endl;
        power=power+1;
        cpower=power;
        for(i=0;i<100;i++)
        {
        if(constant%2==0 && power%2==0)
        {
            power=power/2;
            constant=constant/2;
        }
        if(constant%3==0 && power%3==0)
        {
            power=power/3;
            constant=constant/3;
        }
        if(constant%5==0 && power%5==0)
        {
            power=power/5;
            constant=constant/5;
        }
        if(constant%7==0 && power%7==0)
        {
            power=power/7;
            constant=constant/7;
        }
        if(constant%11==0 && power%11==0)
        {
            power=power/11;
            constant=constant/11;
        }
        }
        cout<<"ans:"<<"("<<constant<<"/"<<power<<")"<<"x"<<"^"<<cpower;
    }
    integration_by_parts()
    {
        int a,b,m,n,i,k,j,p=0;
        cout<<"\nA.[e^(mx)].B.[x^(n)]\n";
        cout<<"Enter the values of A,B,m,n\n";
        cout<<"A=";
        cin>>a;
        cout<<"B=";
        cin>>b;
        cout<<"m=";
        cin>>m;
        cout<<"n=";
        cin>>n;
        k=n;
cout<<a*b<<"[";
for(i=k;i>=1;i--)
{


    cout<<"X^"<<"("<<(n-p)<<")"<<"/"<<"("<<m<<")"<<"\te^"<<"("<<m<<"x"<<")"<<"\t+\t1";
    cout<<"/"<<m<<"^"<<i<<"[";
    for(j=k;j>=k-p;j--)
    {
           cout<<j<<".";

    }
    cout<<"X^"<<"("<<(n-p-1)<<")"<<"\t"<<m<<"^"<<i<<"e^"<<"("<<m<<"x"<<")"<<"/"<<"("<<m<<")";
    p++;

}
for(i=k;i>1;i--)
    {cout<<"]";}
cout<<"]";
}
};
int main()
{
  int jump=0;
       for(jump=0;jump>=0;jump++)
       {
        inputs ob;
        char qw;
        if(choice==1)
        {
            int constant,power;
            cout<<endl<<"Enter a constant of variable";
            cin>>constant;
            cout<<"Enter a power";
            cin>>power;
            ob.simple_integration(constant,power);
        }
        if(choice==2)
        {
            ob.integration_by_parts();
        }

        if(choice==3)
        {
        system("exit");
        }
}
}

