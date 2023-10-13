#### 第二章课后习题答案

##### 2.6复习题

1.函数

2.包含iostream头文件，将头文件内容添加到源代码中

3.using是预编译指令，使用std命名空间

4.cout<<"Hello World!"<<endl;

5.int cheeses;

6.cheeses=32;

7.cin>>cheeses;

8.cout<<"We have "<<cheese<<" verities of cheese"<<endl;

9.

1）函数名叫froop，带有一个参数t，参数类型是double类型，函数返回一个整型值

2）函数名叫rattle，带有一个参数n，参数类型是int类型，函数无返回值

3）函数名叫prune，函数无参数，函数返回一个整型

10.当函数没有返回值时，void rattle(int n)

11.

1）using namespace std;

2）using std::cout;

3）std::cout

##### 2.7编程练习

1.

```c++
#include <iostream>

using namespace std;

int main(void)

{

	cout<<“My name is ublack921”<<endl;

	cout<<"I live in ShanDong"<<endl;

	return 0;

}
```



2.

```c++
#include <iostream>

using namespace std;

int main(void)
{
    double distance
    count <<"Enter the distance(in long):";
    cin >>distance;
    cout <<"The distance "<<distance<<"long"<<"equal"<<220*diatance<<"yard."<<endl;
    return 0;
}
```

3.

```c++
#include <iostream>

void print_mice();
void print_run();    
using namespace std;

int main(void)
{
    print_mice();
    print_mice();
    print_run();
    print_run();
    
    return 0;
}

void print_mice(void)
{
    cout<<"Three blind mice"<<endl;
}

void print_run(void)
{
     cout<<"See how they run"<<endl;
}
```

4.

```c++
#include <iostream>

using namespace std;

int main(void)
{
    int age;
    cout<<"Enter your age："
    cin>>age;
    cout<<"Your are "<<age<<"years old,equals= "<<12*age<<"month old"<<endl;
    
    return 0;
}
```

5.

```c++
#include <iostream>

void convert(double);

using namespace std;
int main(void)
{
    double c_degree,f_degree;

    cout<<"Please enter a Celsius value:";
    cin>>c_degree;
    
    f_degree=convert(c_degree);
    
    cout<<c_degree<<"degrees Celsius is "<<f_degree<<"degrees Fahrenheit"<<endl;
    return 0;
}

double convert(double c)
{
    return 1.8*c+32.0;
}
```

6.

```c++
#include <iostream>

double convert(double L);
using namespace std;
int main(void)
{
    double l_year,a_unit;
    cout<<"Enter the number of light years:";
    cin>>l_year;
    a_unit=convert(l_year);
    cout<<l_year<<"light years="<<a_unit<<"astronomical units"<<endl;
    return 0;
}

double convert(double L)
{
    return L*63240;
}
```

7.

```c++
#include <iostream>

void link(int a,b);
using namespace std;
int main(void)
{
    int M,H;
    cout<<"Enter the number of hours: ";
    cin>>H;
    cout<<"Enter the number of minutes: ";
    cin>>M;
    
    link(H,M);
    
    return 0;
}

void link(int a,b)
{
     cout<<"Time: "<<a<<":"<<b<<endl;
}
```



#### 第三章课后习题答案

##### 3.6复习题

1.int, short, long, long long, unsigned, signed, char

根据数据运算的需要，选择合适的数据类型和应用进行匹配

2.

```c++
a)short a=80;
b)unsigned int b=42110;
c)unsigned int c=3000000000; long c=3000000000; long long c=3000000000;
```

3.C++语言没有提供自动防止超出整数类型范围的功能，需要程序员自己预估数据大小并选择合适的数据类型，每种数据类型的宽度，C++没有做规定，具体的值由开发平台和编译器决定。

4.默认C++整数在不超出int类型范围的应用情况下，默认优先使用int类型

33： int类型

33L: 以long类型来存储整数常量

5.在基于ASCII码的平台下，两者等价。但是char grade=65，先将65存储为int类型，然后再类型转换，将int转换为char存储在grade。

6.

```c++
1）char ch=88;
  cout<<ch<<endl;

2)//强制转换
    cout<<(char)88<<endl; 
    //cout<<char(88)<<endl;
```

7.不同的平台和编译器对应的long和long long类型的大小是不同的，如果long长度为4字节，则存放在double类型中不会出现舍入误差，如果long long类型为8字节，则存放在double类型中会出现舍入误差。

8.a)8*9+2=74

   b)6*3/4=4;

   c)3/4*6=0;

   d)6.0*3/4=4.5;

   e)15%4=3.

9.

```c++
//两种强制类型的转换
int sum=(int)x1+(int)x2;  //int sum=int(x1)+int(x2)
int sum=(int)(x1+x2); //int sum=int(x1+x2)
```

10.

```c++
a)cars---->int
b)iou---->float
c)level---->char
d)crat---->char32_t
e)fract---->double;//精度提升 double精度要比float高
```

##### 3.7编程练习

1.

```c++
//1英尺=12英寸
#include <iostream>
const int FOOT_TO_INCH=12;

using namespace std;
int main(void)
{
    int height;
    
    cout<<"Please enter your height int inches_";
    cin>>height;
    
    cout<<"Your height convert to "<<height/FOOT_TO_INCH;
    cout<<" food and "<<height%FOOT_TO_INCH<<endl;
    
    return 0;
}
```

2.

```c++
#include <iostream>

const int FOOT_TO_INCH=12;
const double INCH_TO_METER=0.0254;
const double KILLOGRAM_TO_POUND=2.2;

using namespace std;
int main(void)
{
    int height_foot,height_inch;
    double weight_pound,height,weight,bmi;
	
    cout<<"Please enter your height foot:";
    cin>>height_foot;
    cout<<"Please enter your height inch:";
    cin>>height_inch;
    cout<<"Please enter your weight in pounds:";
    cin>>weight_pound;
    
    height=(height_foot*FOOT_TO_INCH+height_inch)*INCH_TO_METER;
    weight=weight_pound/KILLOGRAM_TO_POUND;
    
    bmi=weight/(height*height);
    cout<<"Your BMI is "<<bmi<<endl;
    return 0;
}
```

3.

```c++
#include <iostream>

const int DEGREE_TO_MINUTE=60;
const int DEGREE_TO_SECOND=3600;
using namespace std;
int main(void)
{
    int degree,minute,second;
    double degree_style;
    
    cout<<"Enter a latitude in degrees,minutes,and seconds:"<<endl;
    cout<<"First,enter the degrees: ";
    cin>>degree;
    cout<<"Next,enter the minutes: ";
    cin>>minute;
    cout<<"Finally,enter the seconds: ";
    cin>>second;
    
    degree_style=degree+(double)minute/DEGREE_TO_MINUTE+(double)second/DEGREE_TO_SECOND;
    cout<<degree<<" degrees,"<<minute<<" minutes,"<<second<<" second="<<degree_style<<"degrees"<<endl;
    return 0;
}
```

4.

```c++
#include <iostream>

const int DAY_HOUR=24;
const int HOUR_TO_MINUTE=60;
const int MINUTE_TO_SECOND=60;

using namespace std;
int main(void)
{
    long long seconds;
    int days,hours,minutes;
    
    cout<<"Please enter the number of seconds: ";
    cin>>seconds;
    
    days=seconds/(DAY_HOUR*HOUR_TO_MINUTE*MINUTE_TO_SECOND);
    seconds=seconds%(DAY_HOUR*HOUR_TO_MINUTE*MINUTE_TO_SECOND);
    
    hours=seconds/(HOUR_TO_MINUTE*MINUTE_TO_SECOND);
    seconds=seconds%(HOUR_TO_MINUTE*MINUTE_TO_SECOND);
    
    minutes=seconds/MINUTE_TO_SECOND;
    seconds=seconds%MINUTE_TO_SECOND;
    
    cout<<days<<" days,"<<hours<<" hours,"<<minutes<<" minutes,"<<seconds<<" seconds."<<endl;
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    long long global_amount,american_amount;
    double population_percent;
    cout<<"Enter the world's population: ";
    cin>>global_amount;
    cout<<"Enter the population of US: ";
    cin>>american_amount;
    
    population_percent=100*(double)american_amount/(double)global_amount;
    cout<<"The population of the US is "<<population_percent<<"% of the world population."<<endl;
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    double distance_in_miles,fuel_in_gallon;
    double fuel_consume;
    double distance_in_kilometer,fuel_in_litre;
	cout<<"Enter the distance in miles: ";
    cin>>distance_in_miles;
    cout<<"Enter the fuel consume in gallon: ";
    cin>>fuel_in_gallon;
    
    fuel_consume=distance_in_miles/fuel_in_gallon;
    cout<<"The fuel consume is "<<fuel_consume<<" miles/gallon."<<endl;
    
    cout<<"Enter the distance in kilometer: ";
    cin>>distance_in_kilometer;
    cout<<"Enter the fuel in litre: ";
    cin>>fuel_in_litre;
    fuel_consume=(fuel_in_litre/distance_in_kilometer)*100;
    cout<<"The fuel consume is "<<fuel_consume<<" L/100KM."<<endl;
    
    return 0;
}
```

7.

```c++
#include <iostream>

const double GALLON_TO_LITRE=3.875;
const double HKM_TO_MILE=62.14;

using namespace std;
int main(void)
{
    double fuel_consume_eur, fuel_consume_us;
    cout<<"Enter the fuel consume in europe(L/100KM): ";
    cin>>fuel_consume_eur;
    
    fuel_consume_us=(GALLON_TO_LITRE*HKM_TO_MILE)/fuel_consume_eur;
    cout<<"The fuel consume is "<<fuel_consume_us<<" mile/gallon."<<endl;
    return 0;
}
```

#### 第四章课后习题答案

##### 4.12复习题

1.

```c++
a:char actor[30];

b:short betsie[200];

c:float chuck[13];

d:long double dipsea[64];
```

2.

```c++
#include <array>
array<char, 30> actor;
array<short, 100> betsie;
array<float, 13> chuck;
array<long double, 64> dipsea;
```

3.

```c++
int arr[5]={1,2,3,4,5};
```

4.

```c++
int arr[5]={1,3,5,7,9};
evev=arr[0]+arr[4];
```

5.

```c++
float ideas[10];
cout<<ideas[1]<<endl;
```

6.

```c++
char str[]="cheeseburger";
```

7.

```c++
string str="Waldorf Salad";
```

8.

```c++
struct fish

{
	char kind[30];
	int weight;
	float length;
};
```

9.

```c++
struct fish

{
	char kind[30];
	int weight;
	float length;
};
fish ff={"Bigfish",12,4.2};
```

10.

```c++
enum Response {No,Yes,Maybe};
```

11.

```c++
double ted;
double *pt=&ted;
cout<<"ted="<<*pt<<endl;
```

12.

```c++
float treacle[10];
float *pt=&treacle[0];//float *pt=treacle
cout<<pt[0]<<" "<<pt[9]<<endl;
```

13.

```c++
int size;
cout<<"Enter a number: "<<endl;
cin>>size;
int *pt=new int[size];
vector<int> arr(size);
```

14.打印字符串的地址，不会打印字符串。

15.

```c++
struct fish

{
	char kind[30];
	int weight;
	float length;
};

fish *pt=new fish;
cout<<pt->kind<<","<<pt->weight<<","<<pt->length<<endl;
```

16.

```c++
cin >>address;//从输入读取 直到遇到空格
```

17.

```c++
#include<iostream>
#include<array>
#include<vector>
#include<string>

const int size=10;
std::vector<std::string> arr(size);
std::array<std::string, size>array;
```

##### 4.13编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    const int size=20;
    char first_name[size],last_name[size];
    char grade;
    int age;
    
    cout<<"What is your first name?";
    cin.getline(first_name,size);
    cout<<"What is your last name?";
    cin.getline(last_name,size);
    cout<<"What letter grade do you deserver?";
    cin>>grade;
    cout<<"What is your age?";
    cin>>age;
    
    cout<<"Name: "<<last_name<<", "<<first_name<<endl;
    cout<<"Grade: "<<grade+1<<endl;
    cout<<"Age: "<<age<<endl;
    return 0;
}
```

2.

```c++
#include <iostream>
#include <string>
using namespace std;
int main(void)
{
    string name;
    string dessert;
	cout << "Enter your name: "<<endl;
    getline(cin,name);
    cout <<"Enter your favorite dessert: "<<endl;
    getline(cin,dessert);
    cout <<"I have some delicious "<<dessert;
    cout <<"for you，"<< name <<endl;;
                 
    return 0;
}
```

3.

```c++
#include <iostream>
#include <cstring>

using namespace std;
int main(void)
{
    const int size=20;
    char first_name[SIZE],last_name[SIZE];
    char full_name[2*SIZE];
    
    cout<<"Please enter your first name: "<<endl;
    cin.getline(first_name,SIZE);
    cout<<"Please enter your last name:"<<endl;
    cin.getline(last_name,SIZE);
    
    strcpy(full_name,last_name);
    strcat(full_name,", ");
    strcat(full_name,first_name);
    
    cout<<"Here is the information in a single string: ";
    cout<<full_name<<endl;
    
    return 0;
}
```

4.

```c++
#include <iostream>
#include <string>

using namespace std;
int main(void)
{
	string last_name,first_name,full_name;
    
    cout<<"Please enter your first name: "<<endl;
    getline(cin,first_name);
    cout<<"Please enter your last name:"<<endl;
    getline(cin,last_name);
    
	full_name=last_name+", "+first_name;
    
    cout<<"Here is the information in a single string: ";
    cout<<full_name<<endl;
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;

struct CandyBar
{
    char brand[20];
    float weight;
    int calorie;
};

int main(void)
{
    CandyBar snack={"Mocha Munch",2.3,350};
    cout<<"Band= "<<snack.brand<<endl;
    cout<<"Weight= "<<snack.weight<<endl;
    cout<<"calorie= "<<snack.calorie<<endl;
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;

struct CandyBar
{
    char brand[20];
    float weight;
    int calorie;
};

int main(void)
{
    CandyBar snack[3]={{"Mocha Munch",2.3,350},{"sfbae",3.2,500},{"sdcdw",4.3,620}};
    cout<<"1stBand= "<<snack[0].brand<<endl;
    cout<<"1stWeight= "<<snack[0].weight<<endl;
    cout<<"1stcalorie= "<<snack[0].calorie<<endl;
    cout<<"******************************************"<<endl;
    cout<<"2ndBand= "<<snack[1].brand<<endl;
    cout<<"2ndWeight= "<<snack[1].weight<<endl;
    cout<<"2ndcalorie= "<<snack[1].calorie<<endl;   
    cout<<"******************************************"<<endl;   
    cout<<"3thBand= "<<snack[2].brand<<endl;
    cout<<"3thWeight= "<<snack[2].weight<<endl;
    cout<<"3thcalorie= "<<snack[2].calorie<<endl;
    return 0;
}
```

7.

```c++
#include <iostream>

struct Pizza
{
	char company[20]; 
  	float diameter;
    float weight;
};
using namespace std;
int main(void)
{
    Pizza dinner;
    cout<<"Please enter the Pizza's company:";
    cin.getline(dinner.company,20);
    cout<<"Please enter the size of pizza in inches:";
    cin>>dinner.diameter;
    cout<<"Please enter the weight of pizza in pounds:"
    cin>>dinner.weight;
    
    cout<<"Pizza company: "<<dinner.company<<"diameter in inches: "<<dinner.diameter<<"weight in pounds: "<<dinner.weight<<endl;
    
    return 0;
}
```

8.

```c++
#include <iostream>

struct Pizza
{
	char company[20]; 
  	float diameter;
    float weight;
};
using namespace std;
int main(void)
{
    Pizza *pizza=new Pizza;
    cout<<"Please enter the Pizza's company:";
    cin.getline(pizza->company,20);
    cout<<"Please enter the size of pizza in inches:";
    cin>>pizza->diameter;
    cout<<"Please enter the weight of pizza in pounds:";
    cin>>pizza->weight;
    
    cout<<"Pizza company: "<<pizza->company<<"diameter in inches: "<<pizza->diameter<<"weight in pounds: "<<pizza->weight<<endl;
    
    delete Pizza;
    return 0;
}
```

9.

```c++
#include <iostream>
#include <cstring>
using namespace std;

struct CandyBar
{
    char brand[20];
    float weight;
    int calorie;
};

int main(void)
{
    //CandyBar snack[3]={{"Mocha Munch",2.3,350},{"sfbae",3.2,500},{"sdcdw",4.3,620}};
    CandyBar *pt=new CandyBar[3];
    strcpy(pt[0].brand, "Mocha Munch");
    pt[0].weigt=2.3;
    pt[0].calorie=350;
    
    strcpy(pt[1].brand, "sfbae");
    pt[1].weight=3.2;
    pt[1].calorie=500;
    
    strcpy(pt[2].brand, "sdcdw");
    pt[2].weight=4.3;
    pt[2].calorie=620;
    
    cout<<"1stBand= "<<pt->brand<<endl;
    cout<<"1stWeight= "<<pt->weight<<endl;
    cout<<"1stcalorie= "<<pt->calorie<<endl;
    cout<<"******************************************"<<endl;
    cout<<"2ndBand= "<<(pt+1)->brand<<endl;
    cout<<"2ndWeight= "<<(pt+1)->weight<<endl;
    cout<<"2ndcalorie= "<<(pt+1)->calorie<<endl;   
    cout<<"******************************************"<<endl;   
    cout<<"3thBand= "<<(pt+2)->brand<<endl;
    cout<<"3thWeight= "<<(pt+2)->weight<<endl;
    cout<<"3thcalorie= "<<(pt+2)->calorie<<endl;
    
    delete []pt;
    return 0;
}
```

10.

```c++
#include <iostream>
#include <array>

using namespace std;
int main(void)
{
    array<float,3>record_list;
    
    cout<<"Please enter three records of 40 meters: "<<endl;
    cout<<"First record:";
    cin>>record_list[0];
    cout<<"Second record:";
    cin>>record_list[1];
    cout<<"Third record:";
    cin>>"record_list[2]:";
    
    cout<<"1st: "<<record_list[0]<<";"<<"2nd: "<<record_list[1]<<";"<<"3rd: "<<record_list[2]<<endl;
    average=(record_list[0]+record_list[1]+record_list[2])/3;
    cout<<"Average: "<<average<<endl;
    
    return 0;
}
```



#### 第五章课后习题答案

##### 5.8复习题

1.入口循环：程序进入循环体之前，**先执行表达式的判断**。若为真则开始执行循环体内的语句；若为假，则不执行循环体内的语句，越过循环体，执行循环体外的语句。for循环      while循环

出口循环：**首先执行循环体内的语句**，然后再判断表达式。若表达式为真，则再次执行循环体，若为假，则退出循环，执行循环之后的语句。do....while循环 

2.01234

3.0369

​	12

4.6

   8

5.k = 8

6.

```c++
int i;
for(i=1;i<64;i*=2)
{
    cout<<i<<",";
}
cout<<i<<endl;
```

7.使用花括号{}。

8.int x=(1,024) 有效 ，最后x=20; ","运算符优先级比“=”赋值运算符低，有括号，先运算括号里面的，024是八进制数，代表十进制数字是20。

第二条语句有效先计算赋值运算符，y=1；(y=1), 024; 最终表达式的值是024。

9.cin>>ch 忽略空白、换行、制表符。

cin.get(ch)、ch=cin.get()   读取所有字符，存储在变量ch里。

##### 5.9编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    int min, max, sum=0;
    
    cout<<"Enter the min number: ";
    cin>>min;
    cout<<"Enter the max number: ";
    cin>>max;
    
    for(int i=min;i<=max;i++)
    {
        sum+=i;
    }
    cout<<"sum="<<sum<<endl;
    
    return 0;
}
```

2.

```c++
#include <iostream>
#include <array>
const int ArSize = 16;// example of external declaration

using namespace std;
int main(void)
{
	//long long factorials[ArSizel;
    array<long double,ArSize>factorials;
    factorials[0] = factorials[1] = 1;
    for (int i = 2;i < ArSize; i++)
    	factorials[i] = i * factorials[i-1];
    for (int i = 0;i < ArSize; i++)
        cout << i << "! = " << factorials[i] <<endl;
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    double num,sum=0;
    do
    {
        cout<<"Please enter a number to add: ";
        cin>>num;
        sum+=num;
    }
    while(num!=0);
    cout<<"Input end,sum="<<sum<<endl;
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
const int DEPOSIT_BASE=100;
int main(void)
{
    double daphne_deposit=DEPOSIT_BASE;
    double cleo_deposit=DEPOSIT_BASE;
    int year=0;
    
    while(daphne_deposit>=cleo_deposit)
    {
        daphne_deposit+=0.1*DEPOSIT_BASE;
        cleo_deposit+=0.05*cleo_deposit;
        year++;
    }
    cout<<"After "<<year<<"years,"<<"cleo more daphne"<<endl;
    cout<<"Daphne has "<<daphne_deposit<<"dollars"<<endl;
    cout<<"cleo has "<<cleo_deposit<<"dollars"<<endl;
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    const string Month[]={"Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Aep","Oct","Nov","Dec"};
    int sale_num[12];
    int sum=0;
    
    for(int i=0;i<12;i++)
    {
        cout<<"Enter the sale number of "<<Month[i]<<endl;
        cin>>sale_num[i];
    }
    cout<<"Input Done!"<<endl;
    
    for(int i=0;i<12;i++)
    {
        sum+=sale_num[i];
    }
    cout<<"Total sale:"<<sum<<endl;
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    const string Month[]={"Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Aep","Oct","Nov","Dec"};
    int sale_num[3][12];
    int sum=0;
    
    for(i=0;i<3;i++)//行
    {
        cout<<"Starting "<<i+1<<"year's data."<<endl;
    	for(int j=0;j<12;j++)//列
    	{
        	cout<<"Enter the sale number of "<<Month[j]<<endl;
        	cin>>sale_num[i][j];
    	}   
    }

    cout<<"Input Done!"<<endl;
    
    for(int i=0;i<3;i++)
    {
        for(int j=0;j<12;j++)
   		{
        	sum+=sale_num[i][j];
    	}
    }
    cout<<"Total sale:"<<sum<<endl;
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
struct car
{
    string manufacturer;
    int date;
};

int main(void)
{
    int car_number;
    car *pcar;
    
    cout<<"How many cars do you wish to catalog?";
    cin>>car_number;
    cin.get();
    pcar=new car[car_number];
    
    for(int i=0;i<car_number;i++)
    {
        cout<<"Car #"<<i+1<<":"<<endl;
        cout<<"Please enter the maker: ";
        getline(cin,pcar[i].manufacturer);
        cout<<"Please enter the year made: ";
        cin>>pcar[i].date;
        cin.get();
    }
    cout<<"Here is your collection:"<<endl;
    for(int i=0;i<car_number;i++)
    {
        cout<<pcar[i].date<<" "<<pcar[i].manufacturer<<endl;
    }
    
    return 0;
}
```

8.

```c++
#include <iostream>
#include <cstring>

using namespace std;
const char DONE[]="done";
int main(void)
{
    char words[20];
    int counter=0;
    cout<<"Enter words(to stop,type the word done):"<<endl;
    do
    {
        cin>>words;
        cin.get();
        counter++;
    }
    while(strcmp(word,DONE)!=0);
    cout<<"You entered a total of "<<counter-1<<" words"<<endl;
    
    return 0;
}
```

9.

```c++
#include <iostream>
#include <string>

using namespace std;
const char DONE[]="done";
int main(void)
{
    string words;
    int counter=0;
    cout<<"Enter words(to stop,type the word done):"<<endl;
    do
    {
        cin>>words;
        cin.get();
        counter++;
    }
    while(words!=DONE);
    cout<<"You entered a total of "<<counter-1<<" words"<<endl;
    
    return 0;
}
```

10.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    int row;
    cout<<"Please enter the number of rows: ";
    cin>>row;
    
    for(int i=0;i<row;i++)
    {
        for(int j=0;j<row-i-1;j++)
        {
            cout<<".";
        }
        for(int j=0;j<=i;j++)
        {
            cout<<"*";
        }
        cout<<endl;
    }
    
    
    return 0;
}
```



#### 第六章课后习题答案

##### 6.10复习题

1.version1执行两次   version只需判断一次，效率高

2.ch+1输出的是整型数是多少；++ch 是ASCII码向后或向前挪一位。

3.输出：

```c++
H$i$!$
$S$e$n$d$ $ct1 = 9, ct2=9
```

4.a.weight>=115 && weight<125;

​	b.ch=='q' || ch=='Q';

​    c.(x%2==0) && (x!=26);

​	d.(x%2==0) && (x%26!=0);

​	e.(donation>=1000 && donation<=2000) || (1==guest);

​	f.(ch>='a' && ch<='z') || (ch>='A' && ch<='Z');

5.x是bool类型 ，此时相同

6.(x>=0) ? x : -x;

7.

```c++
switch(ch)
{
    case 'A':a_grade++;break;
    case 'B':b_grade++;break;
    case 'C':c_grade++;break;
    case 'D':d_grade++;break;
    default: f_grade++;
}
```

8.定义choice为int型，输入字符型如q终止程序时，会出现运行错误；定义choice为char型，此时输入q或数字5都可以正常终止程序。

9.

```c++
int line=0;
char ch;
while(cin.get(ch) && ch!='Q')
{
    if(ch=='\n')
        line++;
}
```

##### 6.11编程练习

1.

```c++
#include <iostream>
#include <cctype>

using namespace std;
int main(void)
{
    char input;
    
    cout<<"Please enter a character:";
    cin>>input;
    
    while(input!='@')
    {
        if(isdigit(input))
        {
            cin>>input;
            continue;
        }
        else if(islower(input))
        {
            input=toupper(input);
        }
        else
            input=tolower(input);
        cout<<input;
        cin>>input;
    }
    
    
    return 0;
}
```

2.

```c++
#include <iostream>
#include <array>

using namespace std;
int main(void)
{
    array<double,10> donation;
    
    double input;
    int count=0;
    double sum=0.0;
    double average;
    int bigger=0;
    
    cout<<"Please enter the double numerial: ";
    while((cin>>input))
    {
        donation[count++]=input;
        if(count==10)
            break;
        cout<<"Please enter the double numerial: ";
    }
    
    for(int i=0;i<count;i++)
    {
        sum+=donation[i];
    }
    
    average=sum/count;
    
    for(int i=0;i<count;i++)
    {
        if(donation[i]>average)
            bigger++;
    }   
    cout<<"Average="<<average<<endl;
    cout<<bigger<<"number are bigger than average."<<endl;
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;

void showmenu(void);
int main(void)
{
    char ch;
    showmenu();
    cin.get(ch);
    
    while(ch!='c' && ch!='t' && ch!='g')
    {
        cin.get();//把回车消耗掉
        cout<<"Please enter a character:c,p,t,g:";
        cin.get(ch);
    }
    switch(ch)
    {
        case 'c':break;
        case 'p':break;
        case 't':cout<<"A maple is a tree."<<endl;break;
        case 'g':break;
    }
    return 0;
}

void showmenu(void)
{
    cout<<"Please enter one of the following choices:"<<endl;
	cout<<"c) carnivore\t\t p)pianist"<<endl;
	cout<<"t) tree\t\t\t g) game"<<endl;
}
```

4.

```c++
#include <iostream>

using namespace std;

const int strsize=40;
const int usersize=4;
struct bop
{
    char fullname[strsize];
    char title[strsize];
    char bopname[strsize];
    int preference;
};

bop user[usersize]=
{
    {"Pick","Level_A","RR",0},
    {"Jack","Level_B","JJ",1},
    {"Micheal","Level_C","MM",2},
    {"Pose","Level_D","RR",0}
};

void showmenu(void);
void print_by_fullname(void);
void print_by_title(void);
void print_by_bopname(void);  
void print_by_pref(void);
    
int main(void)
{
    char input;
    showmenu();
    cin.get(input);
    
    while(input!='q')
    {
        switch(input)
        {
            case 'a':print_by_fullname();break;
            case 'b':print_by_title();break;
            case 'c':print_by_bopname();
            case 'd':print_by_pref();
            default:cout<<"Please enter character a,b,c,d,q:"<<endl;
        }
        cin.get();
        cout<<"Next input:";
        cin.get(input);
    }
    
    return 0;
}

void showmenu(void)
{
    cout<<"Benevolrnt order of programmer report"<<endl;
    cout<<"a. display by name\t\t b. display by title"<<endl;
    cout<<"c. display by bopname\t\t d. diaplay by preference"<<endl;
    cout<<"q. quit"<<endl;
}

void print_by_fullname(void)
{
    for(int i=0;i<usersize;i++)
        cout<<user[i].fullname<<endl;
}

void print_by_title(void)
{
    for(int i=0;i<usersize;i++)
        cout<<user[i].title<<endl;
}

void print_by_bopname(void)
{
    for(int i=0;i<usersize;i++)
        cout<<user[i].bopname<<endl;
}

void print_by_pref(void)
{
    for(int i=0;i<usersize;i++)
    {
        switch(user[i].preference)
        {
            case 0:cout<<user[i].fullname<<endl;break;
            case 1:cout<<user[i].title<<endl;break;
            case 2:cout<<user[i].bopname<<endl;break;
        }
    }
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    double income,tax;
    cout<<"Please enter your income:";
    cin>>income;
    
    while((cin>>income) && (income >=0))
    {
        if(income<=5000)
            tax=0.0;
        else if(income<=15000)
            tax=(income-5000)*0.1;
        else if(income<=35000)
            tax=10000*0.1+(income-15000)*0.15;
        else
            tax=10000*0.1+20000*0.15+(income-35000)*0.2;
    	cout<<"Your tax="<<tax<<endl;
        cout<<"Next income:"<<endl;
    }
    return 0;
}
```

6.

```c++
#include <iostream>
#include <string>
using namespace std;

struct patrons
{
    string name;
    double donation;
};

int main(void)
{
    int number;
    patrons *ppatrons;
    bool empty=true;
    cout<<"Enter the number of donors:";
    cin>>number;
    
    ppatrons=new patrons[number];
    
    for(int i=0;i<number;i++)
    {
        cout<<"donor #"<<i+1<<":"<<endl;
        cout<<"Enter the name of donor:";
        cin>>ppatrons[i].name;
        cout<<"Enter the donation amount:";
        cin>>ppatrons[i].donation;
    }
    
    cout<<"***************Grand Patrons***********"<<endl;
    for(int i=0;i<number;i++)
    {
        if(ppatrons[i].donation>=10000)
            cout<<ppatrons[i].name<<":"<<ppatrons[i].donation<<endl;
        empty=false;
    }
    if(empty==true)
        cout<<"None"<<endl;
    empty=true;
    
    cout<<"*****************Patrons************"<<endl;
    for(int i=0;i<number;i++)
    {
        if(ppatrons[i].donation<10000)
        {
            cout<<ppatrons[i].name<<":"<<ppatrons[i].donation<<endl;
        	empty=false;
        }
    }
    if(empty==true)
        cout<<"None"<<endl;    
    
    return 0;
}
```

7.

```c++
#include <iostream>
#include <cctype>
#include <string>

using namespace std;
int main(void)
{
    string words;
    int vowels=0,consonants=0,others=0;
	
    cout<<"Please enter a sentence:";    
    while((cin>>words) && words!="q")
    {
		if(isalpha(words[0]))
        {
            switch(words[0])
            {
                case 'a':
                case 'e':
                case 'i':
                case 'o':
                case 'u':
                case 'A':
                case 'E':
                case 'I':
                case 'O':
                case 'U':
                    vowels++;
                    break;
                default:
                    consonants++;
            }
        }
        else
        {
            others++;
        }
    }
    cout<<"vowels:"<<vowels<<endl;
    cout<<"consonants:"<<consonants<<endl;
    cout<<"others:"<<others<<endl;
    return 0;
}
```

8.

```c++
#include <iostream>
#include <fstream>
#include <string>
#include <cstdlib>

using namespace std;
int main(void)
{
    ifstream inFile;
    string file_name;
    char ch;
    int count=0;
    
    cout<<"Enter the file name:";
    getline(cin,file_name);
    inFile.open(file_name);
    if(!inFile.is_open())
    {
        cout<<"Failed to open the file."<<endl;
        exit(EXIT_FAILURE);
    }
    while(!inFile.eof())
    {
        inFile>>ch;
        count++;
    }
    cout<<file_name<<" has "<<count<<" characters."<<endl;
    inFile.close();
    return 0;
}
```

9.

```c++
#include <iostream>
#include <string>
#include <fstream>
#include <cstdlib>

using namespace std;

struct patrons
{
    string name;
    double donation;
};

int main(void)
{
    ifstream inFile;
    string file_name;
    
    int number;
    patrons *ppatrons;
    bool empty=true;
    int i=0;
    
    cout<<"Enter the file name:";
    getline(cin,file_name);
    inFile.open(file_name);
    if(!inFile.is_open())
    {
        cout<<"Failed to open the file!"<<endl;
        exit(EXIT_FAILURE);
    }
    
    inFile>>number;
    if(number<=0)
        exit(EXIT_FAILURE);
    
    ppatrons=new patrons[number];
    
    inFile.get();//消耗掉换行
    
    while((!inFile.eof()) &&　(i<number))
    {
        getline(inFile,ppatrons[i].name);
		cout<<"Read name: "<<ppatrons[i].name<<endl;
        inFile>>ppatrons[i].donation;
        cout<<"Donation: "<<ppatrons[i].donation<<endl;
        i++;
        inFile.get();
    }
    
    cout<<"***************Grand Patrons***********"<<endl;
    for(int i=0;i<number;i++)
    {
        if(ppatrons[i].donation>=10000)
            cout<<ppatrons[i].name<<":"<<ppatrons[i].donation<<endl;
        empty=false;
    }
    if(empty==true)
        cout<<"None"<<endl;
    empty=true;
    
    cout<<"*****************Patrons************"<<endl;
    for(int i=0;i<number;i++)
    {
        if(ppatrons[i].donation<10000)
        {
            cout<<ppatrons[i].name<<":"<<ppatrons[i].donation<<endl;
        	empty=false;
        }
    }
    if(empty==true)
        cout<<"None"<<endl;    
    
    return 0;
}
```



#### 第七章课后习题答案

##### 7.12复习题

1.①定义函数 ②调用函数  ③函数原型声明

2.

```c++
a) void igor(void);
b) float tofu(int);
c) double mpg(double,double);
d) long summation(long [],int);
e) double doctor(const char *str);
f) void ofcourse (boss bs);
g) char *plot(map *pt);
```

3.

```c++
void set_array(int arr[],int size, int value)
{
    for(int i=0;i<size;i++)
        arr[i]=value;
}
```

4.

```c++
void set_array(int *begin,int*end,int value)
{
    for(int *pt=begin;pt!=end;pt++)
        *pt=value;
}
```

5.

```c++
double max_number(const double arr[],int size)
{
    int max_value=arr[0];
    for(int i=1;i<size;i++)
    {
        if(max_value<arr[i])
        {
            max_value=arr[i];
        }
    }
    return max_value;
}
```

6.const一般应用于指针,由于指针按地址传递,可以更改原始数据,加上const可以防止原始数据被修改而基本类型的数据是按值传递的,函数调用时使用的是其副本,不会更改原本的值

7.

```c++
//字符数组:char str[ ]="Hello world";
//双引号: “hello world”；
//指向字符串中首字符的指针：char *pt="hello world";
```

8.

```c++
int replace(char *str,char c1,char c2)
{
    int count=0;
    while(*str)
    {
        if(*str==c1)
        {
            *str=c2;
            count++;   
        } 
        str++;
    }
    return count;
}
```

9.*"pizza" : 取出字符串中第一个字符的值，即p;   "pizza"表示的是整个字符串的地址，也就是首字符的地址。

“taco”[2]: "taco"[2]--->int *pt=taco--->taco[2]=c

10.要按值传递它，只要传递结构名glitz即可。要传递它的地址，请使用地址运算符&glitz，按值传递将自动保护原始数据，但这是以时间和内存为代价的。按地址传递可节省时间和内存，但不能保护原始数据，除非对函数参数使用了const限定符。另外，按值传递意味着可以使用常规的结构成员表达法，但传递指针则必须使用间接成员运算符。

11.

```c++
int judge(int (*pf)(const char *));
```

12.

```c++
void show(applicant ap)
{
    cout<<ap.name<<endl;
    for(int i=0;i<3;i++)
        cout<<ap.credit_ratings[i]<<endl;
}

void show(const applicant *pt)
{
    cout<<pt->name<<endl;
    for(int i=0;i<3;i++)
        cout<<ap->credit_ratings[i]<<endl;
}
```

13.

```c++
typedef void (*p_f1)(applicant *a);
p_f1 p1=f1;

typedef char *(*p_f2)(const applicant *a1,const applicant *a2);
p_f2 p2=f2;

p_f1 ap[5];

p_f2 (*pa)[10];
```

##### 7.13编程练习

1.

```c++
#include <iostream>

using namespace std;

double harmean(double x,double y);
int main(void)
{
    double n1,n2;
    double result;
    
    cout<<"Please enter two number, until one of them is zero: ";
    cin>>n1>>n2;
    
    while(n1!=0 && n2!=0)
    {
        result=harmean(n1,n2);
        cout<<"The harmean is : "<<result<<endl;
        cout<<"Please enter two number, until one of them is zero: ";
        cin>>n1>>n2;
    }   
    return 0;
}

double harmean(double x,double y)
{
    return 2.0*x*y/(x+y);
}
```

2.

```c++
#include <iostream>

using namespace std;

const int MAX=10;
int fill_golf(double ar[],int n);
void show_golf(double ar[],int n);
double average_golf(double ar[], int n);
int main(void)
{
    double golf[MAX];
    
    int size=fill_golf(golf,MAX);
    if(size>0)
    {
        show_golf(golf,size);
        cout<<"Average: "<<average_golf(golf,size)<<endl;
    }
    else
    {
        cout<<"There is no scores!"<<endl;
    }
    
    return 0;
}

int fill_golf(double ar[],int n)
{
    double temp;
    int i;
    for(i=0;i<MAX;i++)
    {
        cout<<"Enter golf scores, No."<<i+1<<": ";
        cin>>temp;
        if(!cin)
        {
            cin.clear();
            while(cin.get() != '\n');
            cout<<"Invalid input, terminate."<<endl;
            break;
        }
        else if(temp<0)
        {
            break;
        }
        else
        {
            arr[i]=temp;
        }
    }
    return i;
}

void show_golf(double ar[],int n)
{
    cout<<"golf result: ";
    for(int i=0;i<n;i++)
    {
        cout<<ar[i]<<" ";
    }
    cout<<endl;
}

double average_golf(double ar[], int n)
{
    double average,sum=0;
    
    for(int i=0;i<n;i++)
    {
        sum+=ar[i];
    }
    average=sum/n;
    
    return average;
}
```

3.

```c++
#include <iostream>

using namespace std;
struct box
{
    char maker[40];
    float height;
    float width;
    float length;
    float volume;
};
void set_box(box *p_b);
void show(box b);
int main(void)
{
    box b={"cube",3,4,5};
    
    set_box(&b);
    show(b);
    
    return 0;
}

void set_box(box *p_b)
{
    p_b->volume=p_b->height*p_b->width*p_b->length;
}

void show(box b)
{
    cout<<"maker: "<<b.maker<<endl;
    cout<<"height: "<<b.height<<endl;
    cout<<"width: "<<b.width<<endl;
    cout<<"length: "<<b.length<<endl;
    cout<<"volume: "<<b.volume<<endl;
}
```

4.

```c++
#include <iostream>

using namespace std;

long double probability(unsigned int numbers, unsigned int picks);
int main(void)
{
	unsigned int total, choices;
	long double field=probability(47,5);
    long double special=probability(27,1)
    long double result=field*special;
    cout<<result<<endl;
	cout<<"Bye."<<endl;
	
	return 0;
}

long double probability(unsigned int numbers, unsigned int picks)
{
	double n, p;
	long double result=1.0;
	for(n=numbers, p=picks; p>0; n--, p--)
	{	
		result=result*(n/p);
	}
	return result;
}
```

5.

```c++
#include <iostream>

using namespace std;

long long factorial(unsigned int n);
int main(void)
{
    int number;
    long long result;
    
    cout<<"Enter a number for factorial: ";
   
    while( cin>>number)
    {
        result=factorial(number);
        cout<<number<<"!="<<result<<endl;
        cout<<"Enter a number for factorial: ";
    }    
    return 0;
}

long long factorial(unsigned int n)
{
    if(n==0)
        return 1;
    else
        return n*factorial(n-1);   
}
```

6.

```c++
#include <iostream>

using namespace std;
const int MAX=40;
int Fill_array(double arr[],int size);
void Show_array(double arr[],int size);
void Reverse_array(double arr[],int size);
int main(void)
{
    double array[MAX];
    
    int size=Fill_array(array,MAX);
    Show_array(array,size);
    Reverse_array(array,size);
    Show_array(array,size);
    
    Reverse_array(array+1, size-2);
    Show_array(array,size);
    cout<<endl;
    return 0;
}

int Fill_array(double arr[],int size)
{
    int i;
    double temp;
    
    for(i=0;i<size;i++)
    {
        cout<<"Please enter a number:";
        cin>>temp;
        if(!cin)
        {
            cin.clear();
            while(cin.get()!='\n');
            break;
        }
        else
            arr[i]=temp;
    }
    return i;
}

void Show_array(double arr[],int size)
{
    cout<<"The array content: "<<endl;
    for(int i=0;i<size;i++)
        cout<<arr[i]<<" ";
    cout<<endl;
}

void Reverse_array(double arr[],int size)
{
    double temp;
    for(int i=0;i<(size/2);i++)
    {
        temp=arr[i];
        arr[i]=arr[size-i-1];
        arr[size-i-1]=temp;
    }
}
```

7.

```c++
#include <iostream>

using namespace std;
const int Max=5;

double *fill_array(double *begin, double *end);
void show_array(double *begin, double *end);
void revalue(double r, double *begin, double *end);

int main(void)
{
	double properties[Max];
	
	double *pa=fill_array(properties, properties+Max);
	show_array(properties, pa);
	
	if((pa-properties)>0)
	{
		cout<<"Enter revalution factor: ";
		double factor;
		while(!(cin>>factor))
		{
			cin.clear();
			while(cin.get()!='\n')
				continue;
			cout<<"Bad input:input process terminated."<<endl;
		}
		revalue(factor, properties, pa);
		show_array(properties, pa);
	}
	return 0;
}

double *fill_array(double *begin, double *end)
{
	double temp;
	double *pt;
	for(pt=begin;pt!=end;pt++)
	{
        cout<<"pt: "<<pt<<endl;
        cout<<"begin: "<<begin<<endl;
        cout<<"pt-begin: "<<pt-begin<<endl;
		cout<<"Enter value #"<<(pt-begin)+1<<": ";
		cin>>temp;
		if(!cin)
		{
			cin.clear();//清除缓冲区
			while(cin.get()!='\n') //读取缓冲区内容，直到遇到回车
				continue;
			cout<<"Bad input:input process terminated."<<endl;
			break;
		}
		else if(temp<0)
			break;
		else
			*pt=temp;	
	}
	return pt;
}

//显示数组内容
void show_array(double *begin, double *end)
{
	for(double *pt=begin; pt!=end; pt++)
	{
		cout<<"Property #"<<(pt-begin)/sizeof(double)<<": $";
		cout<<*pt<<endl;
	}
}

//重新修改比例系数
void revalue(double r, double *begin, double *end)
{
	for(double *pt=begin; pt!=end; pt++)
	{
		*pt*=r;
	}
}
```

8.

```c++
/*8.a
#include <iostream>
#include <string>
#include <array>

using namespace std;

const int Seasons=4;
const array<string, Seasons> Snames={"spring","summer","fall","winter"};

void fill(double arr[],int size);
void show(const double arr[],int size);
int main(void)
{
	double expenses[Seasons];
	fill(expenses,Seasons);
	show(expenses,Seasons);
	return 0;
}

void fill(double arr[],int size)
{
	for(int i=0;i<size;i++)
	{
		cout<<"Enter "<<Snames[i]<<" expenses: ";
		cin>>arr[i];
	}
}

void show(const double arr[],int size)
{
	double total=0.0;
	cout<<"EXPENSES:"<<endl;
	for(int i=0;i<size;i++)
	{
		cout<<Snames[i]<<": $"<<arr[i]<<endl;
		total+=arr[i];
	}
	cout<<"Total expenses: $"<<total<<endl;
}
*/

/*8.b
#include <iostream>
#include <string>
#include <array>

using namespace std;

const int Seasons=4;
const array<string, Seasons> Snames={"spring","summer","fall","winter"};

struct Spend
{
	double money[Seasons];
};

void fill(double arr[],int size);
void show(const double arr[],int size);
int main(void)
{
	Spend expenses;
	fill(expenses.money,Seasons);
	show(expenses.money,Seasons);
	return 0;
}

void fill(double arr[],int size)
{
	for(int i=0;i<size;i++)
	{
		cout<<"Enter "<<Snames[i]<<" expenses: ";
		cin>>arr[i];
	}
}

void show(const double arr[],int size)
{
	double total=0.0;
	cout<<"EXPENSES:"<<endl;
	for(int i=0;i<size;i++)
	{
		cout<<Snames[i]<<": $"<<arr[i]<<endl;
		total+=arr[i];
	}
	cout<<"Total expenses: $"<<total<<endl;
}
*/
```

9.

```c++
#include <iostream>

using namespace std;
const int SLEN=30;

struct student
{
    char fullname[SLEN];
    char hobby[SLEN];
    int ooplevel;
};

int getinfo(student pa[],int n);
void display1(student st);
void display2(const student *ps);
void display3(const student pa[], int n);

int main(void)
{
    cout<<"Rner class size: ";
    int class_size;
    cin>>class_size;
    while(cin.get()!='\n')
        continue;
    
    student *ptr_stu=new student[class_size];
    int entered=getinfo(ptr_stu,class_size);
    for(int i=0;i<entered;i++)
    {
        display1(ptr_stu[i]);
        display2(&ptr_stu[i]);
    }
    display1(ptr_stu,entered);
    delete [] ptr_stu;
    cout<<"Done"<<endl;
    
    return 0;
}

int getinfo(student pa[],int n)
{
    int i;
    for(i=0;i<n;i++)
    {
        cout<<"Enter the name of a student: ";
        cin>>pa[i].fullname;
        cout<<"Enter the hobby of a student: ";
        cin>>pa[i].hobby;
        cout<<"Enter the level of a student: ";
        cin>>pa[i].ooplevel;
        
        if(!cin)
        {
            cin.clear();
            while(cin.get()!='\n');
            break;
        }
    }
    return i;
}

void display1(student st)
{
    cout<<"Name: "<<st.fullname<<endl;
    cout<<"Hobby: "<<st.hobby<<endl;
    cout<<"Level: "<<st.ooplevel<<endl;
}

void display2(const student *ps)
{
    cout<<"Name: "<<ps->fullname<<endl;
    cout<<"Hobby: "<<ps->hobby<<endl;
    cout<<"Level: "<<ps->ooplevel<<endl;
}

void display3(const student pa[], int n)
{
    for(int i=0;i<n;i++)
    {
        cout<<"Name: "<<pa[i].fullname<<endl;
    	cout<<"Hobby: "<<pa[i].hobby<<endl;
   		cout<<"Level: "<<pa[i].ooplevel<<endl;
    }
}
```

10.

```c++
#include <iostream>

using namespace std;

double add(double x,double y);
double subtract(double x,double y);
double calculate(double x,double y, double (*pt)(double x,double y));
int main(void)
{
    double result=calculate(2.2,10.4,add);
    cout<<"The result of add is: "<<result<<endl;
    
    result=calculate(10.4,2.5,subtract);
    cout<<"The result of subtract is: "<<result<<endl;
    
    return 0;
}

double add(double x,double y)
{
    return x,y;
}

double subtract(double x,double y)
{
    return x-y;
}

double calculate(double x,double y, double (*pt)(double x,double y))
{
    return pt(x,y);
}
```

#### 第八章课后习题答案

##### 8.7复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 8.8编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```





#### 第九章课后习题答案

##### 9.5复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.

##### 9.6编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

8.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```





#### 第十章课后习题答案

##### 10.9复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 10.10编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```





#### 第十一章课后习题答案

##### 11.8复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.

##### 11.9编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```



#### 第十二章课后习题答案

##### 12.9复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 12.10编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```





#### 第十三章课后习题答案

##### 13.10复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 13.11编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```







#### 第十四章课后习题答案

##### 14.6复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 14.7编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```





#### 第十五章课后习题答案

##### 15.7复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 15.8编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```





#### 第十六章课后习题答案

##### 16.9复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 16.10编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```





#### 第十七章课后习题答案

##### 17.7复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 17.8编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```





#### 第十八章课后习题答案

##### 18.11复习题

1.

2.

3.

4.

5.

6.

7.

8.

9.

10.



##### 18.12编程练习

1.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

2.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

3.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

4.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

5.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

6.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

7.

```c++
#include <iostream>

using namespace std;
int main(void)
{
    
    
    
    return 0;
}
```

















































































































































