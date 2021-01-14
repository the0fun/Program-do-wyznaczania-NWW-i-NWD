# Program-do-wyznaczania-NWW-i-NWD
NWD schematem Euklidesa
#include <iostream>

using namespace std;

long int NWD(int a,int b);
long int NWW(int a,int b);

int main()
{
    int wybor,a,b;
    cout <<"Wyznacz\n1)NWD\n2)NWW\n";
    cin>>wybor;
    cout<<"Podaj liczby\n1) ";cin>>a; cout<<"2) ";cin>>b;

    if (wybor==1)
    {
        cout<<NWD(a,b);
    }
    else
    {
        cout<<NWW(a,b);
    }
}

long int NWD(int a,int b)
{
    int bufor = a%b;
    if (bufor == 0)
        return b;
    else
        a = b;
        b = bufor;
        return NWD(a,b);
}

long int NWW(int a,int b)
{
    return (a*b)/NWD(a,b);
}
