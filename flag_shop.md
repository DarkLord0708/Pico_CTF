* first I looked at what the program was doing
* taking a look at the account balance I found a few thing
    * account balance only changes when we do some transaction of the knockoff flags
    * also account balance is and int<br><br>
```accountbalance = accountbalance - total;```<br>
where, ```total = 900*numberofflags;```<br>
where, ```numberofflags``` is also an int<br>
from the hint we get the idea of using large numbers.<br>
In C when an int number is decreased beyond the scope of int it gives a garbage value<br>
but that values does actually mean something, for example:<bt>
say int has -5 to 6, not if I do,<br>
```int i = -5;```<br>
```i = i-1;```<br>
then i becomes 6<br>
so as we can see, these values go in a cycle (kind of)<br>
so, when I enter a large number in the number of flags prompt (say, 100000000000)<br>
this increases my account balance to a large positive number<br>
and now I can do a transaction to get the real flag.
