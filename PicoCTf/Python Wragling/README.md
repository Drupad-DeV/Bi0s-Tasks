<div align="center"> <h1> Python  Wragling</h1></div>
<img align = "right" src = "https://img.shields.io/badge/Points-10-blueviolet" width = 80>
<img align = "left" src = "https://img.shields.io/badge/Catagory-Genral%20Skills-yellow" width = 150>
<br><br> <h4>
PicoCTF <b><a href= "https://play.picoctf.org/practice/challenge/147?page=1"> Python Wragling. </a></b></h4>

## Dicription:
- Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?

### Solution: 

- To get the flag open the python file *ende.py* with the argument *-d* with the file *flag.txt.en* with the password from the file *pw.txt*. 
- You will get the flag as the output
```sh
$ cat pw.txt
$ dbd1bea4dbd1bea4dbd1bea4dbd1bea4
$ python3 ende.py -d flag.en.txt
Please enter the password:dbd1bea4dbd1bea4dbd1bea4dbd1bea4
$ picoCTF{4p0110_1n_7h3_h0us3_dbd1bea4}
```
