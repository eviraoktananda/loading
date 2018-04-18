<html>
<head>

<style>
#myProgress {
  width: 100%;
  background-color: #ddd;
}
#myBar {
  width: 0%;
  height: 30px;
  background-color: #6f6ac7;
  text-align: center;
  line-height: 30px;
  color: white;
}
</style>
</head>
<body>
<h1>Click the button</h1>

<div id="myProgress">
  <div id="myBar">0%</div>
</div>

<br>
<button onclick="move()">Click Me</button>

<script>
function move() {
  var elem = document.getElementById("myBar");
  var width = 0;
  var id = setInterval(frame, 800);
  function frame() {
    if (width >= 100) {
      setTimeout('window.location = "http://www.itk.ac.id"', 1000);
    } else {
      width++;
      elem.style.width = width + '%';
      elem.innerHTML = width * 1  + '%';
    }
  }
}
</script>
</body>
</html>
