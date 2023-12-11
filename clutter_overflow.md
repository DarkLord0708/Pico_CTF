* had an executable C program and its code
* looking at the code found out that it was using ```gets```, when the size of gets is defined and it is overflowed then it affects the previous variable (code in this case is the previous long variable)
* we had to make ```code``` = to ```0xdeadbeef```this could be achieved by overflowing clutter which was getting inputted by ```gets``` and had a size of 256 (0x100)
* representing this in hexadecimal we get ```\xef\xbe\xad\xde``` because hexadecimal takes 2bits at a time and reads it backwards
* so started by feeding a lot of "A"'s in the program using,<br>
```(python -c "print('A'*256)") | ./chall```<br>
* but this didn't work, so by some trial and error I found that clutter starts overflowing after 264 A's, then used<br>
```python -c "print('A'*264)"```<br>
* this gave a lot of A's
* copied all these and then used,<br>
```echo "AAAAAA....AAA\xef\xbe\xad\xde" | ./chall```<br>
* this worked, then used this with the netcat command
* this gave me the flag.
