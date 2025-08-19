# constructor-deault-paramaterised-destructor.cpp
#include<iostream.h>
#include<conio.h>
#include<string.h>
class emp
{
	char name[10];
	int age,salary;
	public:
		emp()
		{

		}
		emp(int a)
		{
			strcpy(name,"Something");
			age=a;
			salary=a*1000;
		}
		emp(char name[],int age,int salary)
		{
			strcpy(this->name,name);
			this->age=age;
			this->salary=salary;
		}
		void show()
		{
			cout<<name<<" "<<age<<" "<<salary<<endl;
		}
		~emp()
		{
			cout<<"The End of "<<name<<endl;
		}
};
void main()
{
	clrscr();
	emp a,b(18),c("Ram",21,15000);
	{
		emp d("Sham",22,12000);
		d.show();
	}
	a.show();
	b.show();
	c.show();
	getch();
}
