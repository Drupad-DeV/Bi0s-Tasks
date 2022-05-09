<div align="center"> <h1> Nice Netcat</h1></div>
<img align = "right" src = "https://img.shields.io/badge/Points-15%20-blueviolet" width = 80>
<img align = "left" src = "https://img.shields.io/badge/Catagory-Genral%20Skills-yellow" width = 150>
<br><br> <h4>
PicoCTF <b><a href= "https://play.picoctf.org/practice/challenge/156?page=1"> Nice netcat... </a></b></h4>

## Description:
- There is a nice program that you can talk to by using this command in a shell: ```$ nc mercury.picoctf.net 22902``` but it doesn't speak English...

### Solution: 

- The command ``` $ mercury.picoctf.net 22902``` gave back these numbers which when converted to ACII the flag was captured:
```sh
$ mercury.picoctf.net 22902 | nano flag.txt
$ cat flag.txt
112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 100 51 100 102 100 54 100 102 125 10
```
- After converting these to Ascii got the output as 
```sh
$ picoCTF{g00d_k1tty!_n1c3_k1tty!_f2d7cafa}

