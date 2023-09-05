# Mini Calender

This is a simple mini calendar that displays the current month, day, and year. It is built using HTML, CSS, and JavaScript.

# Screenshot

![image](https://github.com/MuktaSunat11/Js-Day13-Homework/assets/112772976/377b1132-ec30-4bad-9be0-0b9129ea07bd)

# Html File
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini Calender</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="calender-container">
        <p class="month-name" id="month-name">Sept</p>
        <p class="day-name" id="day-name">Tuesday</p>
        <p class="day-number" id="day-number">5</p>
        <p class="year" id="year">2023</p>
    </div>
    <script src="script.js"></script>
</body>
</html>
```
# Css File
```
body {
    margin: 0;
    display: flex;
    justify-content: center;
    height: 100vh;
    align-items: center;
    font-family: cursive;
    background-color: slateblue;
  }
.calender-container {
    background-color: white;
    width: 300px;
    text-align: center;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    overflow: hidden;
}
.month-name{
    margin: 0;
    background-color: orangered;
    color: white;
    padding: 10px;
    font-size: 30px;
    font-weight: bold;
  }
.day-name {
    font-size: 20px;
    color: darkgray;
}
.day-number {
    font-size: 80px;
    margin: 0;
    font-weight: bold;
}
  
.year {
    margin: 20px 0;
    font-size: 20px;
    color: darkgray;
    font-weight: 500;
}
```
# Javascript File
```
const monthNameEl = document.getElementById("month-name");
const dayNameEl = document.getElementById("day-name");
const dayNumEl = document.getElementById("day-number");
const yearEl = document.getElementById("year");

const date = new Date();
const month = date.getMonth();
monthNameEl.innerText = date.toLocaleString("en", {
  month: "long",
});

dayNameEl.innerText = date.toLocaleString("en", {
  weekday: "long",
});

dayNumEl.innerText = date.getDate();

yearEl.innerText = date.getFullYear();
```
