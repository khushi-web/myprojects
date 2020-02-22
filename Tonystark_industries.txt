//this project is basically for the users who want to develop a c++ menu driven programs
//and building applications through their real life it contains an assumed
//example of a company STARK INDUSTRIES the first part of the program contains the
//basic description of an organization including officers,engineers and labours
//the second part of the program describes an interview and all the necessary details of the employee
//using various classes and functions integrated together
//madeby khushi agarwal and divija gupta 
#include<iostream.h>
#include<conio.h>
#include<stdio.h>
#include<string.h>
#include<fstream.h>
#include<ctype.h>
#include<stdlib.h>
class building
{
	int enrollno;
	int age;
	char name[25];
	char address[50];
	char qual[20];
	void bonus() //function is private it calculates the bonus for each employee at the end of the month depending upon their skills,time devoted and hardwork
	{     int x,y;
		  cout<<"enter the salary of the month:";
	cin>>x;
	cout<<"enter the bonus points:";
	cin>>y;
		x=x-y;
		y=x*10;
		cout<<x<<','<<y<<'\n';
	}



 public:
	void input()//takes the required input
	{
		cout<<"name:";
		gets(name);
		cout<<"enrollno:";
		cin>>enrollno;
		cout<<"address";
		gets(address);
		cout<<"qualification";
		gets(qual);
		cout<<"age";
		cin>>age;
	}
	void output()  //displays the output
	{      clrscr();
		cout<<name<<'\n';
		cout<<enrollno<<'\n';
		cout<<address<<'\n';
		cout<<qual<<'\n';
		cout<<age<<'\n';
	}
	int getenroll()
	{
		return enrollno;
		}
	void entry()
	{
	    int i4,j4,k=0;
	    for(i4=1;i4<=9;i4++)
	{
	    i4<=5 ? k++: k--;
	    for(j4=1;j4<=9;j4++)
	    {
		if(j4<=6-k||j4>=4+k)
		    cout<<"*";
		    else
		    cout<<" ";
	    }
	}

	char n;
		cout<<"good morning!,please enter the enrollno."; //this function accepts the enrollno. and assigns respective floors to the employees
		cin>>n;
		switch(n)
		{
			case'R':
			cout<<"you can enter the first and ground floor";//for the labours
			break;
			case'G':
			cout<<"you can enter the 2nd and 3rd floor ";//for the engineers and officers
			break;
			case 'B':
			cout<<"you can enter any floor";//for the head manager
			break;
		default:
		cout<<"entry restricted";
		}
	}
	void labour()
	{
		int A[200],i,e,ctr=0;
				for(i=1;i<=100;i++) //loop to create an array to record the enroll ids of the labour
		{
			A[i]=i+100)
		}
		cout<<"list of employee numbers:"<<'/n'<<"A["<<i<<"]";
		cout<<"welcome"<<'/n';
		cout<<"please enter your enrollno.";
		cin>>e;
		if(A[e]==A[i]) //matches with the existing record saved
		ctr=1;
		cout<<"thankyou"<<'/t'<<"please enter";
		if(ctr==0)
		cout<<"your ID doesn't match our records!!!";
	}
 void department()//this function assign the deparments to the labour
 {
	int b,i5;
	for(i5=0;i5<=30;i5++)
	cout<<"#";
    cout<<'\n';
	cout<<"please enter the required security code";
	cin>>b;
	switch(b)
	{
		case'1':
		cout<<"you can enter the tyre manufaturing department";
		break;
		case'2':
		cout<<"you can enter the electronics department";
		break;
		case'3':
		cout<<"you can enter the IP manufaturing department";
		break;
		default:
		cout<<"#####sorry not entered properly";
	}
    }
	//the two functions above gives the description of manufaturing unit under labours

	void engineers()
	{
		int B[200],j,e1,ctr=0;
		for(i=1;1<=100;i++) //loop to record enroll ids of the engineers
		{
			B[j]=j+200;
		}
		cout<<"list of enroll nos. of engineers is:"<<'/n'<<"B["<<j<<"]";
		cout<<"please place your ID to scan your enroll number";
		cin>>e1;
		if(B[e1]==B[j])
		ctr1=1;
		cout<<"thank you!!! please enter";
		if (ctr1==0)
		cout<<"!!!!!!your enroll number doesn't exist in our records!!!!";
	}
	void officers()
	{
		int C[200],ctr3=0,e2;
		for (k=1;k<=100;k++)//loop to record the enroll ids of the officers
		{
			C[k]=k+300;
		}
		cout<<"the list of enroll no.s of officers :"<<'\n'<<"C["<<k<<"]";
		cout<<"please place your id to scan";
		cin>>e2;
		if(C[e2]==C[k])
		ctr2=1;
		cout<<"thankyou!!please enter";
		if(ctr==0)
		cout<<"!!!!your enrollno. doesnot match!!!";
	}

	int sorting(int A[],int size) //to sort the enroll nos of mechanical engineers
	{	int i,j,min_A,pos,temp;
		for(i=0;i<size;i++)
		{	min_A=A[i];
			pos=i;
			for(j=i+1;j<size;j++)
			{
				if(A[j]<min_A)
				min_A=A[j];
				pos=j;
			}
		}
		temp=A[i];
		A[i]=A[pos];
		A[pos]=temp;

	for(i=0;i<=size;i++)
	{
		cout<<"A["<<i<<"]";
		}
		return 0;
 }
 int searching(int B[],int size1,int x2) //to search the age of a particular employee
 {
	int BEG=0, END=size1-1,found=0,mid;
	while(BEG<END && found==0)
       {	if(B[mid]==x2)
		{found=0;
		break;
		cout<<"age found";
		}
		else if(B[mid]>x2)
		END=mid-1;
		else if(B[mid]<x2)
		END=mid+1;
		else if(found==0)
		cout<<"age not found";
       }
       return 0;
 }
 void salary()// this function calculates the salary of the employees and displays it on the screen
 {
	int n1;
	cout<<"hello! please enter the number of your working days:";
	cin>>n1;
	if
	(n1=='R')
	cout<<"your salary is"<<1000*n1;
	if(n1=='B')
	cout<<"your salary is"<<3000*n1;
	else
	cout<<"you do not belong to this unit hence will not recieve any salary:";
	cout<<"your bonus for the month is:";
	bonus();
	cout<<"congratulations!!!!!";
}
 };
	void delete_rec()//to delete any selected record
	{
		ifstream fin("file.dat",ios::in|ios::binary);
		ofstream fout("temp1.dat",ios::out|ios::binary);
		int rno; char found='f',confirm='n';
		cout<<"enter the record to be deleted";
		cin>>rno;
		building b;
		while(!fin.eof())
		{
			fin.read((char*)&b,sizeof(b));
			{
				if(rno==b.getenroll())
				{
				    b.output();
				    found='t';
				    cout<<"are you sure you want to delete this record sir!!!";
				    cin>>confirm;
				    if(confirm=='n')
			fout.write((char*)&b,sizeof(b));

				}
				else
		    fout.write((char*)&b,sizeof(b));
		    if(found=='f')
		    cout<<"record not found!!"<<'\n';
		fin.close();
		fout.close();
		remove("file.dat");
		rename("temp1.dat","file.dat");
		fout.open("file.dat",ios::in|ios::binary);
		cout<<"now the file contains:";
		building c;
		while(!fin.eof())
		{
		    fin.read((char*)&c,sizeof(c));
		    if(fin.eof())
			break;
		    c.output();
		}
		fin.close();
	}
		}
	}
	void modify()//for modification of the record
{       int h,x3,ctr=0;
	cout<<"enter the enrollment number:";
	cin>>h;
	building  b;
	{
		ifstream fin("file.dat",ios::in|ios::binary);
		ofstream fout("temp.dat",ios::out|ios::binary);
		cout<<"enter the enrollno.to modify:";
		cin>>x3;
		building b;
		while(!fin.eof())
		{
		fin.read((char*)&b,sizeof(b));
		if(!fin.eof())
		if(x3==b.getenroll())
		fout.write((char*)&b,sizeof(b));
		if(ctr==0)
		fout.close();
		fin.close();
		remove("file.dat");
		rename("temp.dat","file.dat");
		}

	}
}

	void copy() //copying the records into another temporary file
	{
		ifstream fin("file2.dat",ios::in|ios::binary);
		ofstream fout("temp2.dat",ios::out|ios::binary);
		building b;
		while(!fin.eof())
		{
			fin.read((char*)&b,sizeof(b));
			if(!fin.eof())
			fout.write((char*)&b,sizeof(b));
		}
		fin.close();
		fout.close();
	}
 void check()//func checks the details of the employee for verification
  {
	ofstream fout("file3.txt",ios::out);
	char ch2,ch;
	int num;
	do
	{
		cout<<"enter the employee name:";
		cin>>ch;
		cout<<"enter the enrollno.:";
		cin>>num;
		cout<<"enter the enrollno.:";
		cin>>ch2;
	}while(ch2=='y'||ch2=='Y');
		fout.close();
	}//part 2 of this application describes the information of an employee  who arrives for an interview

    class interview
 {
	char name1[20];
	char desig[30];
	char address[50];
	char city[20];
	char state[20];
	int age1;
	public:
	void matrix() //This matrix is under private section the class interview this matrix is used to store employee salaries for the month
	{
		int a[10][10],b[10][10],m,n,j,k,i;
		cout<<"enter the number of rows and columns of matrix days":
		cin>>m>>n;
		cout<<"\nenter the rows and columns of matrix salary";
		cin>>p>>q;
		if(n==p)
		{
			cout<<"\n enter the elements of matrix days";
			for(i=0; i<m; ++i)
			for(j=0; j<n; ++j)
			cin>>A[i][j];
			cout<<"\n enter the lements of matxix salary:\n";
			for(i=0; i<p; ++i)
			for(j=0; j<q ++j)
			cin>>B[i][j];
			cout<<"\n matrix days is:";
			for(i=0; i<m; ++i)
			{
				cout<<"\n";
				for(j=0; j<n: j++)
				cout<<A[i][j]<<"";
			}
			cout<<"\n matrix salary is ";
			for(i=0; i<p; ++i)
			{
				cout<<"\n";
				for(j=0; j<q; ++j)
				cout<<B[i][j]<<"";
			}
			cout<<"\n product of matrices"; //multiplies the no of days worked with thw salary per day
			for(i=0; i<m; ++i)
			{
				cout<<"\n";
				for(j=0;j<q;++j)
				{
					 C[i][j]=0;
					for(k=0;k<n;++k)
						C[i][j]= C[i][j]+A[i][k]*B[k][j];
					cout<<C[i][j]<<"";
				}
				}
			}
			else
			cout<<"\n the matrices are not compatible for multiplication";
		}
	void input1()
	{
		cout<<"enter the name ";
		gets(name1);
		cout<<"enter qualification";
		gets(desig);
		cout<<"enter address";
		gets(address);
		cout<<"enter city";
		gets(city);
		cout<<"enter age";
		cin>>age1;
		cout<<"state";
		gets(state);
	}
	void output1()
	{     clrscr();
		cout<<"name"<<'/t'<<name1;
		cout<<"designation"<<'/t'<<desig;
		cout<<"address"<<'/t'<<address;
		cout<<"city"<<'/t'<<city;
		cout<<"state"<<'/t'<<state;
		cout<<"age"<<'/t'<<age1;
	}
	int getid()
	{
		return age1;
	}
		void string1()
			{
		    char str[90],cstr[90];
		    int t;
		    cout<<"enter the string sir:";
		    gets(str);
		    for(t=0;str[t]!='\0';t++)
			cstr[t]=str[t];
			cstr[t]='\0';
			cout<<cstr[t];

			}
		void copy1() //copying the records into another temporary file
		{
		ifstream fin("file4.dat",ios::in|ios::binary);
		ofstream fout("temp3.dat",ios::out|ios::binary);
		building b;
		while(!fin.eof())
		{
			fin.read((char*)&b,sizeof(b));
			if(!fin.eof())
			fout.write((char*)&b,sizeof(b));
		}
		fin.close();
		fout.close();
		}
       void search1()//this function search for name of the employee
	{
		int age, found1=0;
		ifstream fin("info.dat",ios::in|ios::binary);
		if(!fin.eof())
		{
			cout<<"sorry !! could not open the file";
			exit(-1);
		}
		else
		{
		interview i;
		while(!fin.eof())
		{            cout<<"enter the element to be searched";
				cin>>age;
			if(age==i.getid())
			{
				i.output1();
				found1=1;
				break;
			}
		}
		}
		if(found1==0)
		cout<<"the mentioned name not found";
	}
		};
 void main()
{
	int choice,y1,y2,t[30],t1[30];
	building b;
	interview i;
	b.entry();
	b.input();
	b.output();
	int i6,space,k1=0;
	{
	    for(i6=1;i6<=20;i6++)
	{
	    for(space=1;space<=(20-i6);space++)
	    {
		cout<<" ";
	    }
	    while(k1!=(2*i6-1))
	    {
		cout<<"@";
		k1++;
	    }
	    k1=0;
	    cout<<'\n';
	}
	}
	cout<<"hello!! good morning how can i help you";
	cout<<"1.press 1 for modification:"<<'\n'
	<<"2.press 2 for deleting the record:"<<'\n'
	<<"3.press 3 for copying the record  :"<<'\n'<<"4.press 4 for sorting:"<<'\n'
	<<"5.press 5 for searching" ;
	cin>>choice;
	switch(choice)
	{
		case 1:
		    modify();
		    break;
		case 2:
		delete_rec();
		break;
		case 3:
		copy();
		break;
		case 4:
		y1=b.sorting(t,2);
		break;
		case 5:
	       y2= b.searching(t1,2,51);
		break;
		case 6:
		check();
		break;
		default:
		cout<<"incorrect input";
	}
	i.input1();
	i.output1();
		int n3;
		cout<<"menu:"<<'\n';
		cout<<"1.copying into a text file";
		cout<<'\n';
		cout<<"2.copying into a string";
		cout<<'\n';
		cout<<"enter your choice:";
		cin>>n3;
		switch(n3)
		{
		case'1':i.copy1();
			break;
		case'2': i.string1();
			break;
			default:
			cout<<"incorrect input";
			break;
	}

	i.search1();
	b.salary();
	getch();
 }











