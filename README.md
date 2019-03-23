# Registering-entrance-of-people-in-auditorium
#include<iostream.h>
#include<conio.h>
class audi
	{
		int age,token_no;
		static int count;
		char name[12];
	public:
		void in();
		int get()
		{
		 return count;
		}
		void details();
	};
int audi::count=0;
void audi::in()
	{
	count++;
	cout<<"NAME=";
	cin>>name;
	cout<<"AGE=";
	cin>>age;
	token_no=count+1213;
	cout<<"YOUR TOKEN NUMBER IS "<<token_no<<endl;
	}
void audi::details()
	{
	cout<<"NAME="<<name<<"\t\tTOKEN NO="<<token_no<<"\nAGE="<<age;
	}
int main()
	{
	clrscr();
	audi k[100];
	cout<<"::ENTER DETAILS OF PERSON ENTERING IN AUDITORIUM::\n";
	for(int i=0;i<100;i++)
		{
		 k[i].in();
		 int m;
		 cout<<"\nMORE ENTRIES\n1.YES\n2.NO\n=";
		 cin>>m;
		 if(m!=1)
			{
			i=100;
			}
		}
	int l=k[i].get();
	cout<<"\n::DETAILS OF PEOPLE ARE IN AUDITORIUM::\n";
	cout<<"THERE ARE "<<l<<" PEOPLE IN AUDITORIUM";
	for(int j=0;j<l;j++)
		{
		cout<<"\n PERSON NO."<<j+1<<endl;
		k[j].details();
		}
	cout<<"\nDeveloper:-KULDEEP RAWAT\n\t   IT3\n\t   20276803117";
	getch();
	return 0;
	}
