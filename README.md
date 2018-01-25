//# Josephus-Problem-New
//# Josephus-Problem
Josephus, a Jewish historian living in the 1st century, and his 40 soldiers were trapped in a cave, the exit of which was blocked by Romans. They chose suicide over capture and decided that they would form a circle and start killing themselves using a step of three. Josephus states that by luck or maybe by the hand of God, he and another man remained the last and gave up to the Romans. Josephus was a smart person, and he would have been saved because he could compute where he should stand to be the survivor. As a software engineer, if you were to compute this place where Josephus should stand, given the group size of N and step on M, how would you do it?

//c++ Code :

#include <iostream>


int josephus(int n, int k)
{
    if (n == 1) 
    return 1;
    return ((josephus(n – 1, k) + k – 1) % n) + 1;
}

int main()
{
   unsigned int k, n;
   int c, q;

   cin >> q;
   c = 0;
   while (++c <= q)
   { 
      cin >> n >> k;
      cout << "Case " << c << ": " << josephus(n, k) << endl;
   }

return 0;
}

//INPUT 1 :
41  //Josehus + 40 soldiers i.e. "n"
3   //Step of 3 i.e "k"

//OUTPUT 1 :

Case 1:31


//INPUT 2 :
41  //Josehus + 40 soldiers i.e. "n"
2   //Step of 2 i.e "k"

//OUTPUT 2 :

Case 1:19
