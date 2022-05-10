<div align="center"> <h1> GETaHEAD</h1></div>
<img align = "right" src = "https://img.shields.io/badge/Points-20%20-blueviolet" width = 80>
<img align = "left" src = "https://img.shields.io/badge/Catagory-Web%20Exploitation-yellow" width = 150>
<br><br> <h4>
PicoCTF <b><a href= "https://play.picoctf.org/practice/challenge/132?page=1"> GETaHEAD </a></b></h4>

## Discription: 
- Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:47967/

### Hints:
1. Maybe you have more than 2 choices
2. Check out tools like Burpsuite to modify your requests and look at the responses

### Solution 
- By the Hints it was clear that this challege had something to do with HTTPS requests, so a quick research about http requests gave me the details about diffrent typs of requests such as POST GET HEAD etc.
- So by interupting the Connection using burpsuit I founded out that there is a POST and a GET request going to the server accordin to the options on the website
- When the GET request was changed to HEAD (Hint from challenge title) we got the flag has response 
<img src="https://i.ibb.co/DYDTsyj/Screenshot-from-2022-05-09-20-31-06.png" /> <img src="https://i.ibb.co/30fTw9c/Screenshot-from-2022-05-09-20-31-25.png" />
```sh
$ picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}
```
