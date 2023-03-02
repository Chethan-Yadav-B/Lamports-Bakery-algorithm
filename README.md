# Lamports-Bakery-algorithm

 In Lamport's bakery algorithm, processes are treated as customers. In this, each
 process waiting to enter its critical section gets a token number, and the process with the
 lowest number enters the critical section. If two processes have the same token number,
 the process with a lower process ID enters its critical section.
      
      Algorithm :
      do{
          entering[i] :=  true; // show interest in critical section
         // get a token number
          number[i] := 1 + max(number[0],  number[1], ..., number[n - 1]);
          entering [i] :=  false;
          for ( j :=  0 ;  j {<} n; j++)
          {
       // busy wait until process Pj receives its token number
              while (entering [j])
              { ; } // do nothing
             while (number[j] !=  0 &&  (number[j], j) < (number[i], i)) // token comparison
               { ; } // do nothing
             }
              // critical section
               number[i] :=  0;  // Exit section
              // remainder section
          } while(1);
              Structure of process Pi for Lamport's bakery algorithm to critical section problem.  


