# Relationship-countdown-<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Our Relationship ❤️</title>
<style>
body{
  margin:0;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
  font-family:Arial,sans-serif;
  background:linear-gradient(135deg,#160b12,#3b1025);
  color:white;
}
.box{
  padding:30px 20px;
}
.heart{
  font-size:60px;
}
h1{
  font-size:30px;
}
#timer{
  font-size:26px;
  font-weight:bold;
  line-height:1.6;
}
p{
  opacity:.75;
}
</style>
</head>

<body>
<div class="box">
  <div class="heart">❤️</div>
  <h1>Our Time Together</h1>
  <p>Since 30 May 2026 • 12:40 PM</p>
  <div id="timer">Loading...</div>
</div>

<script>
const start = new Date("2026-05-30T12:40:00+05:30");

function updateTimer(){
  let diff = Date.now() - start.getTime();

  let days = Math.floor(diff / 86400000);
  diff %= 86400000;

  let hours = Math.floor(diff / 3600000);
  diff %= 3600000;

  let minutes = Math.floor(diff / 60000);
  diff %= 60000;

  let seconds = Math.floor(diff / 1000);

  document.getElementById("timer").innerHTML =
    days + " days " +
    String(hours).padStart(2,"0") + ":" +
    String(minutes).padStart(2,"0") + ":" +
    String(seconds).padStart(2,"0");
}

updateTimer();
setInterval(updateTimer,1000);
</script>

</body>
</html>
