* enetring a random string in the username and password fields said, icorrect username. Then I tired "admin" as username then prompt said incorrect password. So, I luckily found the username.
* Also nothing was happening in inspect elements when I was pressing submit. So, there was no serverside involvement in this.
* To look at the source code, used "Ctrl+U", then looked at index.js
* this file had a "btoa" function which was decoding a base64 encoded string.
* from this I found that username was indeed admin and I found the encoded password.
* I copied these strings and saved them in username.txt and password.txt ans used piping.<br>
```cat username.txt | base64 -d```<br>
```cat password.txt | base64 -d```<br>
these gave username and password and enetering these into the fields gave the flag.<br>
