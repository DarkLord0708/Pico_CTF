* took a look at the C file
* encrypt() funcitono is essentially doing XOR enccryption of two strinngs<br>
Doing XOR even times is equivalent to not doing it and doing XOR odd times is equivalent to doing it once<br>
So, all the loops are basically randomly doing XOR of the ctxt binary string with a random string from a given list<br>
So, we have a total of 2<sup>5</sup> = 32 possibilities<br>
* so I changed the code a bit
* first removed all the extra "never" strings
* made a list of all possible combinations using itertools.combinations
* then encrypted it aganinst the output.txt contents as hexcode
* then encrypting it back with the flag prefix "picoCTF{"
* and finally used .decode() also .isprintable() to narrow down the search
* found that the key was "Africa!"
* once I got the key, replaced the flag prefix with the key and ran the code, this gave the flag
