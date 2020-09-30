/*HTML*/

<!DOCTYPE html>
<html>
<head>
    <title>Gradient Background</title>
<body id="gradient">
    <h1>Background Generator</h1>
    <input class="color1" type="color" name="color1" value="#00ff00">
    <input class="color2" type="color" name="color2" value="#ff0000">
    <h2>Current CSS Background</h2>
    <h3></h3>
</body>
</html>


/*CSS5*/

body {
    font: 'Raleway', sans-serif;
    color:red;
    color: rgba(0,0,0,.5);
    text-align: center;
    text-transform: uppercase;
    letter-spacing: .5em;
    top: 15%;
    background: linear-gradient(to right, red, yellow);
}

h1 {
    font: 600 3.5em 'Raleway', sans-serif;
    color:blue;
    color: rgba(0,0,0,.5);
    text-align: center;
    text-transform: uppercase;
    letter-spacing: .5em;
    width: 100%;
}

h2 {
    font: 900 1em 'Raleway', sans-serif;
    color:yellow;
    color: rgba(0,0,0,.5);
    text-align: center;
    text-transform: none;
    letter-spacing: 0.01em;
}

/*JS*/

window.onload = function(){
    var css = document.querySelector("h3");
    var color1 = document.querySelector(".color1");
    var color2 = document.querySelector(".color2");
    var body = document.getElementById("gradient")

    //my code starts here
    alert("This is 90% from a course on udemy")
    function randColor() {
    return "#" + Math.random().toString(16).slice(2, 8)
    }

    color1.value = randColor()
    color2.value = randColor()
    setGradient()
    //ends here

function setGradient() {
    body.style.background = 
    "linear-gradient(to right, " 
    + color1.value 
    + ", " 
    + color2.value 
    + ")";

    css.textContent = body.style.background +";";
    }

    //setGradient gets called automatically every time an input is selected 
    color1.addEventListener("input", setGradient)
    color2.addEventListener("input", setGradient)

}


