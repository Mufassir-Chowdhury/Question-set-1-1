# 2019331068

### Question Setter

Name: **Abdullah All Ferdouse**  
Registration \# **2019331068**  
Session: _2019-2020_  
GitHub Username: _shihab-2019331068_  
Cell: _01575087097_  
Email: _siababdullah3946@gmail.com_

## Question Set with Answers

Shahjalal University of Science and TechnologyDepartment of Computer Science and Engineering 1st Year 1st Semester Final Examination — June 2020 \(Session 2019-20\)  
 Course No. — **CSE 133** Course Title — **Structured Programming Language**  
 Time — **3 Hours**           Credit: **3.00**           Total Marks \# **100**  
\(Answer all the questions\)

### Group A

1. Answer the following Questions in short. \(Any **Five**\).5 × 2 = 10

\(a\) _which following character does not belong to the c character set?_  


```text
 (i) '~',   (ii) '#',   (iii) '$',   (iv) '^'
```

**Answer :** _\(iii\)._   
 \(b\) _Write the printf function to print the following string:_  
   _"It is very hard to get 80% marks in C course."_  
 **Answer :**

```c
printf("It is very hard to get 80%% marks in C course.");
```

\(c\) _Write a function "int alt\_ceil\(int a,int b\);" so that we can use_  
   _it instead of ceil\(\(float\)a/b\)_  
 **Answer :**   


```c
int alt_ceil(int a,int b)
{
     return (a+b-1)/b;
}
```

\(d\) _What is the value of an element in enum if it is not assigned with anything?_  
 **Answer :** _If unassigned, the first element will be 0. Other unassigned_  
  _elements will get the value of their previous element incremented by one._  
 \(e\) _Create a function that swaps the value of a and b,_  
 _but in this function, you can not use other variable._  


**Example Answer :**

```c
void alt_swap(int &a,int &b)
{
     a = a+b;
     b = a-b;
     a = a-b;
}
```

\(f\) _What is the size of "int a\[36\]\[52\]\[78\];" in bytes?_  
 **Answer :** _584064_   


\(g\) _Write the value of x in the following code._  


```c
#define a 3+9
int x = 9/a/3;
```

**Answer :** _6_   


\(h\) _What header file is needed to use log\(\) function?_  
 **Answer :** _math.h_   


2. Answer the following Questions. \(Any **Four**\).4 × 5 = 20

\(a\) _Write the variable types of a,b,c and the output of the_   
   following code   


```c
#include<stdio.h>

int b = 0;

void foo(int a)
{
        static int c = 0;
        printf("%d,%d,%d\n",a++,b++,c++);
}

int main()
{
        int a = 0;
        foo(a);
        foo(b);
        foo(a);
}
```

**Answer :**  
 _a is a local variable_   
 _b is a global variable_   
 _c is a static variable_   
 _OUTPUT:_   
 _0,0,0_   
 _1,1,1_   
 _0,2,2_   


\(b\) _Write three different types of right and wrong variable names._   
 **Answer :**   


```text
Right variable names: (i) a, (ii) a1, (iii) a_
Wrong variable names: (i) _a, (ii) 1a,(iii) &a
```

\(c\) _What is the value of g in the following code?_  
 **Answer :**   


```c
char g = 'e'-'n'+'a'-'m'+'s'-'i'+'r';
```

**Answer :** _g_   


\(d\) _How many binary search operations will be needed to find_  
   _68 in a normal number sequence 1,2,3,...,10^4?_  


**Answer :** _10_   


\(e\) _Create a function that creates and returns the address of_  
   _an array that contains all digits in the octal number system._   
 **Answer :**   


```c
int *foo()
{
        static int a[8] = {0,1,2,3,4,5,6,7};
        return a;
}
```

\(f\) _Create a function that scans an array of size 5 without using '\[' or '\]'._  
 **Answer :**   


```c
void foo()
{
        int *a = (int*) malloc(5*sizeof(int));
        for(int i = 0; i < 5; i++) scanf("%d",a+i);
}
```

3. Answer the following Questions. \(Any **Two**\).2 × 10 = 20

\(a\) _Write a recursive function that prints all the permutations_  
   _of a given string 's'._   
 **Answer :**   


```c
void permutation(char s[],int i = 0)
{
        int n = strlen(s)-1;
        if(i == n)
        {
                printf("%s\n",s);
        }
        for(int j = i; j <= n; j++)
        {
                if(!(j-i) or s[i] != s[j])
                {
                        swap(s[i],s[j]);
                        permutation(s,i+1);
                        swap(s[i],s[j]);
                }
        }
}
```

\(b\) _Create a function that prints all the odd numbers from 1 to 100._  
   _You must use these 8 keyword atleast once._  
   _if,else,for,while,do-while,switch,continue,break._   
 **Answer :**   


```c
void print_all_odd()
{
        int i;
        for(i = 1; i < 31; i++)
        {
                if(!(i%2)) continue;
                else printf("%d ",i);
        }
        i -= 2;
        while(i += 2)
        {
                printf("%d ",i);
                if(i >= 61) break;
        }
        i -= 2;
        do
        {
                i++;
                switch(i%2)
                {
                        case 1: printf("%d ",i);
                        case 0: continue;
                }
        }
        while(i < 100);
}
```

\(c\) _Describe malloc, calloc, realloc and free functions with examples._  
 **Answer :**   


```text
malloc function takes a size as a parameter and allocates that memory
to a pointer.
Example: int *p = (int*)malloc(10*sizeof(int));

calloc function takes number of total elements and size of
one element and alocates the needed memory to a pointer. Initialy
all the elements are assigned with the value zero.
Example: int *p = (int*)calloc(10,sizeof(int));

realloc function takes a pointer and a size and re allocates memory
to that pointer and returns that memory to a pointer.
The extra memory is assigned with garbage value.
Example: int *v = (int*)realloc(u,10*sizeof(int));

free function frees the memory allocated to a pointer;
Example: free(p);
```

### Group B

1. Answer the following Questions in short. \(Any **Five**\).5 × 2 = 10

\(a\) _What following keyword is not a standard keyword in c programming?_  


```text
(i) default, (ii) pascal, (iii) calc, (iv) volatile
```

**Answer :** _\(iii\)_   


\(b\)_Write the printf function to print the following string._  
   _"int m = 6, n = 2; cout &lt;&lt; m\n &lt;&lt; endl;"_  
 **Answer :**   


```c
printf("int m = 6, n = 2; cout << m\\n << endl;");
```

\(c\) _What is the value of x in the following code._  


```c
long long x = LLONG_MAX + 100;
```

**Answer :** _-9223372036854775709_  


\(d\) _Write the values of w,x,y,z in the following code_   


```c
float w,x,y,z;
w = 3/2; x = 5/2.0; y = 7.0/2; z = (float)9/2;
```

**Answer :** _w = 1.0, x = 2.5, y = 3.5, z = 4.5_  


\(e\)_Write the values of a,b,c,d,e,f,g,h in the following code._  


```c
typedef enum{
        a,b,c = 9,d,e,f = -5,g,h
} elem;
```

**Answer :** _a = 0, b = 1, c = 9, d = 10, e = 11, f = -5, g = -4, h = -3_  


\(f\) _Write the returned value from foo\(5263.3214,123.321\)._  
   _The foo function is given below._   


```c
double foo(double x,double y)
{
        return sqrt(x*x-3*x*y+y*y+x*y);
}
```

**Answer :** _5140.0004_  


\(g\)_What is the difference between empty string and null string?_  


**Answer :** _Empty string has a null character \('\0'\) at index 0._  
   _But null string does not have any character._

\(h\)_What happens if you run this code?_  


```c
#include "stdio.h"

#define 1 0
#define messi 1
#define ronaldo 0

int main()
{
        if(messi > ronaldo)
             printf("Messi is greater than Ronaldo.");
        else printf("Messi is better than Ronaldo.");
}
```

**Answer :** _It gives an error because macro names must be identifiers._  


2. Answer the following Questions. \(Any **Four**\).4 × 5 = 20

\(a\) _Swap two variables with xor operator._   


**Answer :**

```c
int x = 9, y = 4; x = x^y; y = x^y; x = x^y;
```

\(b\) _Create a function to convert a number from an integer to a binary._  


**Answer :**

```c
int to_binary(int x)
{
        int bx = 0, ab[50], i = 0;
        for(; x; x /= 2, i++) ab[i] = x%2;
        reverse(ab,ab+i);
        for(int j = 0; j < i; j++) bx = bx * 10 + ab[j];
        return bx;
}
```

\(c\) _Create a function that reads two integers from a file and_  
   _prints the summation of them in another file._  


**Answer :**   


```c
void foo()
{
        freopen("input.txt","r",stdin);
        freopen("output.txt","w",stdout);
        int a,b;
        scanf("%d%d",&a,&b);
        printf("%d",a+b);
        fclose(stdin);
        fclose(stdout);
}
```

\(d\) _Find 5 errors in the following code._   


```c
#include <studio.h>

01.int main()
02.{
03.        const int N = 1e3+7;
04.        bool is_prime[N];
05.        memset(is_prime,0,sizeof(is_prime));
06.        int t = 0
07.        for(int i = 2; i < N; i++)
08.        {
09.                if(is_prime[i] = 0)
10.               {
11.                       printf("%dth prime is %d/n",++t,&i);
12.                       for(int j = i; j <= N; j += i)
13.                             is_prime[j] = 01;
14.                }
15.        }
16.}
```

**Answer :**   
 _Errors are given bellow._  
 _\(i\) Expected a semicolon \(';'\) after "int t = 0" in line 6._   
 _\(ii\) In line 9, single equal sign is assigning the value instead of checking equality._   
 _\(iii\) In line 11, '/n' character is used instead of '\n'._  
 _\(iv\) In line 11, the address of i is being printed instead of the value._  
 _\(v\) In line 13, the nuber 01 is not a decimal number._  


\(e\) _Write a function to scan a whole sentence in a single character array._  


**Answer :**   


```c
void scan_sentence()
{
        char s[N];
        scanf("%[^\n]",s);
}
```

\(f\) _What is the value of x in the following code?_

```c
#include <stdio.h>

int main()
{
        int a[5][5];
        for(int i = 0; i < 5; i++)
        {
                for(int j = 0; j < 5; j++) a[i][j] = j;
        }
        int x = &a[3][2] - &a[1][4];
}
```

**Answer :** _8_   


3. Answer the following Questions. \(Any **Two**\).2 × 10 = 20

\(a\) _Write a recursive function that returns n^k modulo m in_   
   _logarithmic time complexity._   


**Answer :**   


```c
int power_mod(int n,int k,int m)
{
        if(k == 0) return 1;
        if(k%2) return (power_mod(n,k-1,m)*n) % m;
        int x = power_mod(n,k/2,m)%m;
        return (x*x)%m;
}
```

\(b\) _Write a function that takes an array 'a', and sorts it_   
   _in ascending order using merge sort._   


**Answer :**   


```c
void merge_sort(int a[],int l,int r)
{
        if(l >= r) return;
        if(l+1 == r)
        {
                if(a[l] > a[r]) swap(a[l],a[r]);
                return;
        }
        int m = l+r >> 1;
        merge_sort(a,l,m); merge_sort(a,m+1,r);
        int le = l, ri = m+1,i = l;
        int t[r-l+1];
        for( ; i <= r; i++)
        {
                if(le > m) t[i-l] = a[ri++];
                else if(ri > r) t[i-l] = a[le++];
                else if(a[le] < a[ri]) t[i-l] = a[le++];
                else t[i-l] = a[ri++];
        }
        for(int j = l; j <= r; j++) a[j] = t[j-l];
}

void foo(int a[])
{
        int n = sizeof(a);
        merge_sort(a,0,n-1);
}
```

\(c\) _Write a function to multiply two n by n 2D matrices 'a' and 'b'._

**Answer :**   


```c
void multiply_matrices()
{
        int ans[n][n];
        memset(ans,0,sizeof(ans));
        for(int i = 0; i < n; i++)
        {
                for(int j = 0; j < n; j++)
                {
                        for(int k = 0; k < n; k++)
                        {
                                ans[i][j] += a[i][k]*b[k][j];
                        }
                }
        }
}
```

### END

* [x] I am declaring that, the above work is my own work. Whatever added above

  except the template is the result of my brainstorming. I also understand that

  submitting work that isn’t my own may result in permanent failure of this course

  as well as the whole current semester.

