<div align="center"> <h1> Wave a Flag</h1></div>
<img align = "right" src = "https://img.shields.io/badge/Points-10-blueviolet" width = 100>
<img align = "left" src = "https://img.shields.io/badge/Catagory-Genaral%20Skills-yellow" width = 150>
<br><br> <h4>
PicoCTF <b><a href= "https://play.picoctf.org/practice/challenge/170?page=1"> Wave a flag </a></b></h4>

## Discription: 

- Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

### Solution: 

- Change the file to executable using the command *chmod +x* and then execute the file by using the -h arfument the flag will be visible.
```sh
xavior@Drupad-Lenovo:~/Desktop/PICO CTF$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
xavior@Drupad-Lenovo:~/Desktop/PICO CTF$ 
'''

