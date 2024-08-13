# Oopl
#include<iostream>
using namespace std;

class bank
{
public:
char name[10];
char acc_no[10];
int with_amt,dep_amt;
int balance;

void assign();
void deposit();
void withdraw();
void display();
};

void bank::assign()
{
cout<<"Enter name of account holder:";
cin>>name;
cout<<"Enter account number:";
cin>>acc_no;
cout<<"Enter balance amount:";
cin>>balance;
}

void bank::deposit()
{
cout<<"\n Enter amount to be deposited";
cin>>dep_amt;
balance=balance+dep_amt;
}

void bank::withdraw()
{
if(balance<500)
{
cout<<"Insufficient amount";
}
else
{
cout<<"\n Enter amount to be withdraw";
cin>>with_amt;
balance=balance-with_amt;
}
}

void bank::display()
{
cout<<"bank details";
cout<<"\n name of account holder:"<<name;
cout<<"\n account number:"<<acc_no;
cout<<"\n balance amount:"<<balance;
}

int main()
{
bank b;
int choice,ch;
do{
cout<<"1.assign 2.deposit 3.withdraw 4.display ";
cout<<"\nEnter operation to be performed";
cin>>choice;

switch(choice)
{
case 1:b.assign();
       break;
case 2:b.deposit();
       break;
case 3:b.withdraw();
       break;
case 4:b.display();
       break;
}
cout<<"\n Do you want to continue(0/1)";
cin>>ch;
}
while(ch==1);
}



#include<iostream>
using namespace std;
int n,i;
class bank
{
string name,acc_no;
int balance,with_amt,depo_amt;
public:
void accept();
void withdraw();
void deposit();
void display();
}b[100];

void bank::accept()
{
    cout<<"enter number of records";
    cin>>n;
    for(i=0;i<n;i++)
    {
        cout<<"enter your name,account no and balance:\n";
        cin>>b[i].name>>b[i].acc_no>>b[i].balance;

    }
    
}

void bank::withdraw()
{   
    string accno;
    cout<<"enter account no:";
    cin>>accno;
    for(i=0;i<n;i++)
    {
        if(b[i].acc_no==accno)
        {
        cout<<"enter amount to withdraw";
        cin>>with_amt;
        if(with_amt<b[i].balance)
        {
            b[i].balance=b[i].balance-with_amt;
        }
        }
    }
}

void bank::deposit()
{   
    string accno;
    cout<<"enter account no:";
    cin>>accno;
    for(i=0;i<n;i++)
    {
        if(b[i].acc_no==accno)
        {
        cout<<"enter amount to deposit";
        cin>>depo_amt;
        if(depo_amt<b[i].balance)
        {
            b[i].balance=b[i].balance+depo_amt;
        }
        }
    }
}

void bank::display()
{   
    
    cout<<"\n"<<"name"<<"\t"<<"acc no"<<"\t"<<"balance";
    for(i=0;i<n;i++)
    {
        cout<<"\n"<<b[i].name<<"\t"<<b[i].acc_no<<"\t"<<b[i].balance;
        
    }
}


