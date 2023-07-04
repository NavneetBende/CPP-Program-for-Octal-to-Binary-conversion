# CPP-Program-for-Octal-to-Binary-conversion

Octal to Binary Conversion
There are 2 approaches of converting an octal number into a binary number like:

Write 3 digit binary number for all the digits of a number from left to right. 
first convert octal to decimal and then decimal to binary .
We are using the second approach, it is a long but very simple approach which can also be implemented easily with minimum chances of error.

Octal to binary conversion
While loop in C
Method 1:-
Accept octal number
Convert it into decimal Equivalent
Convert this decimal value into Binary
Make sure you have visited these two pages before moving ahead with the code –

Octal to Decimal conversion
Decimal to Binary Conversion
Method 1 Code in C++
Run
// this program converts octal to binary
// by converting octal->decimal->binary
#include<iostream>
#include<math.h>
using namespace std;

 
void
convert (int octal) 
{
  
int i = 0, decimal = 0;
  
 
    //converting octal to decimal
    while (octal != 0)
    
    {
      
int digit = octal % 10;
      
decimal += digit * pow (8, i);
      
 
octal /= 10;
      
i++;
    
} 
 
printf ("Decimal Value: %d\n", decimal);
  
 
long long binary = 0;
  
int rem;
  
i = 1;
  
 
    // converting decimal to binary here
    while (decimal != 0)
    
    {
      
rem = decimal % 2;
      
decimal /= 2;
      
binary += rem * i;
      
 
	// moving to next position ex: units -> tens
	i *= 10;
    
}
  
 
cout << binary;

}


 
int
main () 
{
  
int octal;
  
 
cout << "Octal Value: "; cin >> octal;
  convert (octal);
  return 0;
}
Output
Octal Value: 12
Decimal Value: 10
Binary Value: 1010
Related Pages
Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Permutations in which n people can occupy r seats in a classroom 

Octal to Binary conversion

Quadrants in which a given coordinate lies

Method 2
Each digit of an octal number can be converted into its binary Equivalent (see image)

Binary Representation for Octal digit:
0 => 000
1 => 001
2 => 010
3 => 011
4 => 100
5 => 101
6 => 110
7 => 111
Octal to Binary conversion in C++
Method 2 Code in C++
Run
#include<iostream>
#define MAX 1000
using namespace std;

 
void
convert (char octalnum[])
{
  
int i = 0;
  
 
cout << "Equivalent Binary Number: ";
  
while (octalnum[i])
    
    {
      
	//use switch case for multiple condition
	switch (octalnum[i])
	
	{
	
case '0':
	  
printf ("000");
	  break;
	
case '1':
	  
printf ("001");
	  break;
	
case '2':
	  
printf ("010");
	  break;
	
case '3':
	  
printf ("011");
	  break;
	
case '4':
	  
printf ("100");
	  break;
	
case '5':
	  
printf ("101");
	  break;
	
case '6':
	  
printf ("110");
	  break;
	
case '7':
	  
printf ("111");
	  break;
	  
	    //for invalid case 
	default:
	  
cout << "\n Invalid octal digit %c " << octalnum[i];
	  
return;
	
}
      
i++;
    
}
  
return;

 
}


int
main () 
{
  
char octalnum[MAX];
  
 
cout << "Insert an octal number: ";
  
cin >> octalnum;
  convert (octalnum);
}
Output
Insert an octal number: 347
Equivalent Binary Number: 011100111
