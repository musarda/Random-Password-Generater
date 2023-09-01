<div align="center">
  <h1>Random Password Generater</h1>
</div>
<!------------BADGE------------>
<div style="text-align: center;" align="center">
  <a href="https://musarda.github.io">
    <img src="https://img.shields.io/badge/Visit%20My-Website-E6E6E6" alt="Web Site Rozeti">
  </a>
  <a href="https://www.github.com/musarda"> <!--GitHub Link-->
    <img src="https://img.shields.io/badge/-GitHub-000?style=quare&labelColor=000&logo=GitHub&logoColor=white&link=link" alt="Github Badge">
  </a>
  <a href="https://www.youtube.com/@CodeChain"> <!--YouTube Link-->
    <img src="https://img.shields.io/badge/-YouTube-c4302b?style=quare&labelColor=c4302b&logo=YouTube&logoColor=white&link=link" alt="YouTube Badge">
  </a>
  <a href="https://discord.gg/kf29ZKZyw6"> <!--Discord Link-->
    <img src="https://img.shields.io/badge/-Discord-738adb?style=quare&labelColor=blurple&logo=Discord&logoColor=white&link=link" alt="Discord Badge">
  </a>
  <a href="https://www.glitch.com/@musarda44"> <!--Glitch Link-->
    <img src="https://img.shields.io/badge/-Glitch-2800ff?style=quare&labelColor=2800ff&logo=Glitch&logoColor=white&link=link" alt="Glitch Badge">
  </a>
  <a href="https://discord.gg/Kaye7tpHcQ"> <!--Discord2 Link-->
    <img src="https://img.shields.io/badge/-Discord-738adb?style=quare&labelColor=blurple&logo=Discord&logoColor=white&link=link" alt="Discord Badge">
  </a>
</div>
<br>
<div align="center">
  This is a simple web based sample <b>Random Password Generator</b> application.
</div>


## Images
<img src="https://github.com/musarda/Random-Password-Generater/blob/main/img/img-1.png?raw=true" title="Random Password Generater" alt="HC-SR04" width="250"> <img src="https://github.com/musarda/Random-Password-Generater/blob/main/img/img-g.png?raw=true" title="Generate" alt="Generate" width="250"> <img src="https://github.com/musarda/Random-Password-Generater/blob/main/img/img-c.png?raw=true" title="Copy" alt="Copy" width="250">

## How to use

First of all, we need a code editor with which we can run the code, so we will use **Visual Studio Code** in this project.

1. **[Download](https://code.visualstudio.com/)** **Visual Studio Code**,
2. **Copy [Code](https://github.com/musarda/Random-Password-Generater/tree/main/Code)** Folder After Installing Visual Studio Code,
3. After Uploading the Code to **Visual Studio Code**, **Right Click** on the **index.html** file > **Click Reveal in File Explorer** and **Open the Chrome** File Named **Index in the Folder**,
4. **Random Password Generator Ready! Remember This Is Just An Example.**

## Features

- **Random password generation**
- **Copying the password to the clipboard**

## Setup

```bash
gh repo clone musarda/Random-Password-Generater
```

## Code
**You can reach [here](https://github.com/musarda/Random-Password-Generater/tree/main/Code)**

### HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>musarda | Random Password Generater</title>
</head>
<body>
    <div class="body">
        <div class="box">
            <h2>Random Password Generater</h2>
            <input type="text" name="" placeholder="Create password" id="password" readonly>
            <table>
                <th><div id="button" class="btn1"onclick="genPassword()">Generate</div></th>
                <th><a  id="button" class="btn2" onclick="copyPassword()">Copy</a></th>
            </table>
        </div>
    </div>
    <script src="./script.js"></script>
</body>
</html>
```
### CSS
```css
* {
    margin: 0;
    padding: 0;
    user-select: none;
    box-sizing: border-box;
}

body {
    background-color: #212121;
    justify-content: center;
    align-items: center;
    display: flex;
    min-height: 100vh;
}

.box {
    background-color: rgb(197, 197, 197);
    padding-top: 30px;
    padding: 30px;
    border-radius: 12px;
}

.box h2 {
    margin-bottom: 40px;
    text-align: center;
    font-size: 26px;
    color: #131313;
    font-family: sans-serif;
}

input {
    padding: 20px;
    user-select: none;
    height: 50px;
    width: 400px;
    border-radius: 6px;
    border: none;
    border: 2px solid #212121;
    outline: none;
    font-size: 22px;
}

input::placeholder {
    font-size: 23px;
} 

#button {
    font-family: sans-serif;
    font-size: 15px;

    margin-top: 40px;
    border: 2px solid #212121;
    width: 155px;
    height: 50px;
    text-align: center;
    background-color: #6b6b6b;
    display: flex;
    color: #fff;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    border-radius: 7px;
} 

.btn2 {
    margin-left: 85px
}

#button:hover {
    color: white;
    background-color: #212121;
}
```
### JavaScript
```js
var password = document.getElementById("password");
function genPassword() {
    var chars = "0123456789abcdefghijklmnopqrstuvwxyz!@#$%^&*()ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    var passwordLength = 12;
    var password = "";
    for (var i = 0; i <= passwordLength; i++) {
        var randomNumber = Math.floor(Math.random() * chars.length);
        password += chars.substring(randomNumber, randomNumber + 1);
    }

    document.getElementById("password").value = password;
}

function copyPassword() {
    var copyText = document.getElementById("password");
    copyText.select();
    copyText.setSelectionRange(0, 999);
    document.execCommand("copy");
}

```

# Licence
This project is licensed under the MIT license. See the **[LICENSE](https://github.com/musarda/Random-Password-Generater/blob/main/LICENSE)** file for more information.
