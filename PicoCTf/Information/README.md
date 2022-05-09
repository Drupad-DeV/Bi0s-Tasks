<div align="center"> <h1> Information </h1></div>
<img align = "right" src = "https://img.shields.io/badge/Points-10%20-blueviolet" width = 80>
<img align = "left" src = "https://img.shields.io/badge/Catagory-Forensics%20Skills-yellow" width = 150>
<br><br> <h4>
PicoCTF <b><a href= "https://play.picoctf.org/practice/challenge/186?page=1"> Information </a></b></h4>

## Discription:
- Files can always be changed in a secret way. Can you find the flag? cat.jpg
### Solution: 

- To get any information on Metadata of an image exiftool is commonly used here and by doing so we get a base 64 encoded code at the Licence catagory. By decoding it we get the Flag. 
```sh
$ exiftool cat.jpg
$ License: cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
$ echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 --decode
$ picoCTF{s4n1ty_v3r1f13d_28e8376d}
```
<img src="https://i.ibb.co/pX8z1Cr/Screenshot-from-2022-05-09-18-26-15.png" alt="Screenshot-from-2022-05-09-18-26-15" border="0"></a><br /><br />
