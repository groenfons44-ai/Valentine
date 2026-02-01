#   
```
<!DOCTYPE html>
<html 
```
```
lang="nl">

```
```
<head>
```
```


```
```
    
```
```
<meta charset="UTF-8">

```
```
    
```
```
<title>💖 Mini Game voor Jou 💖</title>

```
```
    
```
```
<style>

```
```
        
```
```
body {

```
```
            font-family: Arial, sans-serif;
            
```
```
background: linear-gradient(135deg, #ff758c, #ff7eb3);

```
```
            
```
```
height: 100vh;

```
```
            
```
```
margin: 0;

```
```
            
```
```
overflow: hidden;

```
```
            color: white;
            
```
```
text-align: center;

```
```
        }
        
```
```
h1 {

```
```
            
```
```
margin-top: 30px;

```
```
        }
        .heart {
            
```
```
position: absolute;

```
```
            
```
```
font-size: 30px;

```
```
            cursor: pointer;
            user-select: none;
        }
        #counter {
            
```
```
font-size: 20px;

```
```
            
```
```
margin-top: 10px;

```
```
        }
        
```
```
#final {

```
```
            display: none;
            font-size: 28px;
            margin-top: 40px;
        }
    </style>
</head>
<body>
```
```


```
```

<h1>💘 Verzamel 5 hartjes 💘</h1>
<div id="counter">Hartjes: 0 / 5</div>

<div 
```
```
id="final">

```
```
    🌹 Tadaaaa 🌹  
    
```
```
<br><br>

```
```
    Wil jij mijn Valentijn zijn? 💕  
    
```
```
<br><br>

```
```
    ❤️ 14 februari – jij & ik ❤️
</div>
```
```


```
```

<script>
```
```


```
```
    
```
```
let score = 0;

```
```

    
```
```
function spawnHeart() {

```
```
        
```
```
const heart = document.createElement("div");

```
```
        heart.classList.add("heart");
        heart.innerHTML = 
```
```
"❤️";

```
```
        heart.style.left = Math.random() * (window.innerWidth - 
```
```
50) + "px";

```
```
        heart.style.top = Math.random() * (window.innerHeight - 
```
```
50) + "px";

```
```

        heart.onclick = () => {
            score++;
            document.getElementById(
```
```
"counter").innerText = `Hartjes: ${score} / 5`;

```
```
            heart.remove();

            if (score >= 5) {
                document.getElementById(
```
```
"final").style.display = "block";

```
```
            }
        };

        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 
```
```
3000);

```
```
    }

    setInterval(() => {
        
```
```
if (score < 5) spawnHeart();

```
```
    }, 
```
```
800);

```
```
</script>

</body>
</html>

```
