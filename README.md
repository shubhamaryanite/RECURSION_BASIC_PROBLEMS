# RECURSION_BASIC_PROBLEMS
Through this file, solutions of some basic problems using recursion are being provided.



                                 *********Recursion*********
                            
                      a. What	is	Recursion?

In	previous	lectures,	we	used	iteration	to	solve	problems.	Now,	we’ll	learn	about	
recursion	 for	 solving	 problems	which	 contain	 smaller	 sub-problems	 of	 the	 same	
kind.	
Recursion	 in	 computer	 science	 is	 a	 method	 where	 the	 solution	 to	 a	 problem	
depends	on	solutions	to	smaller	instances	of	the	same	problem.	By	same	nature	it	
actually	means	that	the	approach	that	we	use	to	solve	the	original	problem	can	be	
used	to	solve	smaller	problems	as	well.	
So	 in	 other	 words	 in	 recursion	 a	 function	 calls	 itself	 to	 solve	 smaller	 problems.
Recursion	is	a	popular	approach	for	solving	problems	because	recursive	solutions	
are	generally	easier	to	think	than	their	iterative	counterparts	and	the	code	is	also	
shorter	and	easier	to	understand.
                            ******************************************
                            ******************************************


                      b. How	Does	Recursion	Work?

We	can	define	the	steps	of	a	recursive	solution	as	follows:
1. Base	Case:	
A	recursive	function	must	have	a	terminating	condition	at	which the	function	
will	stop	calling	itself.	Such	a	condition	is	known	as	a	base	case.
2. Recursive	Call:
The	recursive	function	will	recursively	invoke	itself on	the	smaller	version	of	
problem.	We	need	to	be	careful	while	writing	this	step	as	it	is	important	to	
correctly	 figure	 out	 what	 your	 smaller	 problem	 is	 on	 whose	 solution	 the	
original	problem’s	solution	depends.
3. Small	Calculation:
Generally	we	perform	a	some	calculation	step	in	each	recursive	call.	We	can	
perform	 this	 calculation	 step	 before	 or	 after	 the	 recursive	 call	 depending	
upon	the	nature	of	the	problem.
It	is	important	to	note	here	that	recursion	uses	stack	to	store	the	recursive	calls.	
So,	to	avoid	memory	overflow	problem,	we	should	define	a	recursive	solution	with	
minimum	 possible	 number	 of	 recursive	 calls	 such	 that	 the	 base	 condition	 is	
achieved	before	the	recursion	stack	starts	overflowing	on getting	completely	filled.
Now,	let	us	look	at	an	example	to	calculate	factorial	of	a	number	using	recursion.
                              
                              **********************************
                              **********************************

                                   Example	Code	1:

#include<iostream>
using namespace std;
int fact(int n)
{
				if(n==0)											//Base	Case
				{
								return 1;
				}
				return n	*	fact(n-1);				//Recursive	call	with small	calculation
}
int main()
{
				int num;
				cin>>num;
				cout<<fact(num);
				return 0;
}
  
Output:
120																    //For num=5
  
  
  
