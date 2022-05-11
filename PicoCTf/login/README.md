<div align="center"> <h1> Login</h1></div>
<img align = "right" src = "https://img.shields.io/badge/Points-100%20-blueviolet" width = 100>
<img align = "left" src = "https://img.shields.io/badge/Catagory-Web%20Exploitation-yellow" width = 150>
<br><br> <h4>
PicoCTF <b><a href= "https://play.picoctf.org/practice/challenge/200?page=1&search=login"> Login</a></b></h4>

## Description:
- My dog-sitter's brother made this website but I can't get in; can you help? [login.mars.picoctf.net](https://login.mars.picoctf.net/)

### Solution: 

- The URL on the challenge Description will direct to a login page.
- On viewing the page source we will find an Interesting Java Script being loaded.

```
<!doctype html>
<html>
    <head>
        <link rel="stylesheet" href="styles.css">
        <script src="index.js"></script>
    </head>
    <body>
        <div>
          <h1>Login</h1>
          <form method="POST">
            <label for="username">Username</label>
            <input name="username" type="text"/>
            <label for="username">Password</label>
            <input name="password" type="password"/>
            <input type="submit" value="Submit"/>
          </form>
        </div>
    </body>
</html>
```
- On browsing through the Script an interesting base 64 string was found which on decrypting would give the flag

```(async()=>{await new Promise((e=>window.addEventListener("load",e))),document.querySelector("form").addEventListener("submit",(e=>{e.preventDefault();const r={u:"input[name=username]",p:"input[name=password]"},t={};for(const e in r)t[e]=btoa(document.querySelector(r[e]).value).replace(/=/g,"");return"YWRtaW4"!==t.u?alert("Incorrect Username"):"cGljb0NURns1M3J2M3JfNTNydjNyXzUzcnYzcl81M3J2M3JfNTNydjNyfQ"!==t.p?alert("Incorrect Password"):void alert(`Correct Password! Your flag is ${atob(t.p)}.`)}))})();```

- The base 64 ```cGljb0NURns1M3J2M3JfNTNydjNyXzUzcnYzcl81M3J2M3JfNTNydjNyfQ```

- Flag : ```picoCTF{53rv3r_53rv3r_53rv3r_53rv3r_53rv3r}```
