<h1 align="center"> МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>
<br>
<br>
<br>
<br>
<br>
<br>
<p align="center">Лабораторная работа №6</p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p align="right">Выполнил: Шандро Никита Богданович</p>
<p align="right">Проверил: Соболев Е. И.</p>
<br>
<br>
<br>
<br>
<br>
<br>

<p align="center">г. Южно-Сахалинск <br> 2023 год</p>

<h2 align="center">Введение</h2>
<p align="justify">Написание кода на js и загрузка его на сервер.</p>

<h2>Цели и задачи</h2>
1.	Сделайте alert по нажатию на кнопку.
<br>
2.	Сделайте изменение текста в input по нажатию кнопки.
<br>
3.	Сделайте вывод содержимого input по нажатию кнопки.
<br>
4.	 Сделайте кнопку по нажатию на нее, она выводит alert содержимое input, возведенное в квадрат.
<br>
5.	 Сделайте кнопку по нажатию, она осуществляет обмен содержимым между двумя input.
<br>
6.	Сделайте кнопку по нажатию на нее поменяется ее текст.
<br>
7.	Сделайте кнопку по нажатию на нее, она меняет цвет текста в input, используя свойства CSS.
<br>
8.	Сделайте кнопки по нажатию на них, одна из них блокирует input с помощью атрибута disabled, а другая разблокирует.
<br>
9.	Сделайте кнопку при наведении на нее появляется alert.
<br>
10.	 Сделайте кнопку при двойном на нее появляется alert.
<br>
11.	 Сделайте область с помощью div при наведении на нее появляется alert.
<br>
12.	Сделайте кнопку и картинку, при нажатии кнопки картинка меняется.
<br>
13.	Сделайте alert по нажатию на кнопку. Используя this.
<br>
14.	Сделайте изменение текста в input по нажатию кнопки. Используя this.
<br>
15.	Сделайте кнопку, при нажатии кнопки кнопка блокируется.
<br>
16.	Сделайте кнопку, при нажатии кнопка считает количество нажатий на нее.
<br>
17.	Сделайте кнопку, при нажатии курсор мышки должен измениться.
<br>
18.	Используя JavaScript, сделайте так, чтобы при клике на кнопку исчезал элемент с id=&quot;hide&quot

```html

<!DOCTYPE HTML>
<html>
<head>
    <meta charset="utf-8">
</head>
<body>
    <input type="button" id="hider" value="Нажмите, чтобы спрятать текст"/>
    <div id="hide">Текст</div>
<script>
    /* ваш код */
</script>
</body>
</html>
```
19.	Создайте кнопку, при клике на которую, она будет скрывать сама себя.
20.	Напишите простой калькулятор.
<br>
Задачи CodeWars:

1.	https://www.codewars.com/kata/the-coupon-code
2.	https://www.codewars.com/kata/unlucky-days
3.	https://www.codewars.com/kata/angle-between-clock-hands
4.	https://www.codewars.com/kata/my-language-skills
5.	https://www.codewars.com/kata/run-length-encoding
6.	https://www.codewars.com/kata/walk-the-object-path
   
<br>
Задача. Написать простой сайт о себе c блоками, header, nav, footer, используете три движка pug, handlebars, EJS


<h2>Решение задач</h2>

### Код JS

```js
// Задача 1
function task1() {
  alert("Кнопка была нажата!");
}

// Задача 2
function task2() {
  var input = document.getElementById('myInput');
  input.value = "Новый текст!";
}

// Задача 3
function task3() {
  var input = document.getElementById('myyInput').value;
  alert(input);
}

// Задача 4
function task4() {
  alert(Math.pow(document.getElementById('myyInputt').value, 2))
}

// Задача 5
function task5() {
  var temp = document.getElementById('input51').value; 
  document.getElementById('input51').value = document.getElementById('input52').value; 
  document.getElementById('input52').value = temp;
}

// Задача 6
function task6() {
  this.innerHTML = 'Текст кнопки поменялся';
}

// Задача 7
function task7() {
  document.getElementById('Inputs').style.color = 'red'
}

// Задача 8
function task8() {
  document.getElementById('Innput').disabled = true;
}
function task81() {
  document.getElementById('Innput').disabled = false;
}

// Задача 12
function task12() {
  document.getElementById('myImage').src = 'more.jpg'
}

// Задача 16
var clickCount = 0;
function task16() {
  clickCount++;
  document.getElementById("clickCount").innerHTML = "Количество нажатий: " + clickCount;
}

// Задача 18
function task18() {
    document.getElementById('hide').style.display = 'none';
}

// Задача 19
function task19() {
  let arr = [1, 6, 8, 4, 5, 0, 4, 7, 3, 1];
  let min = 0;
  let max = 0;
  for(let i = 0; i < arr.length; i++)
  {
      if (arr[max] < arr[i]) max = i;
      if (arr[min] > arr[i]) min = i;
  }
  alert(arr);
  alert(max + min);
}

// Задача 20
function task20() {
  function calculate(num1, operator, num2) {
    switch (operator) {
      case '+':
        return num1 + num2;
      case '-':
        return num1 - num2;
      case '*':
        return num1 * num2;
      case '/':
        if (num2 !== 0) {
          return num1 / num2;
        } else {
          return 'Ошибка: Деление на ноль невозможно!';
        }
      default:
        return 'Ошибка: Неверный оператор!';
    }
  }
  const number1 = parseFloat(prompt('Введите первое число:'));
  const operator = prompt('Введите оператор (+, -, *, /):');
  const number2 = parseFloat(prompt('Введите второе число:'));
  const result = calculate(number1, operator, number2);
  
  alert(`Результат: ${result}`);
}

```

### Код HTML

```html
<!DOCTYPE html>
<html>
 <head>
  <script src="6.js"></script>
  <title>Лаба 6</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
 </head>
 <body>
  
<h1>Лаба 6</h1>
<p>
    <button onclick="task1()">1 Задание</button>
</p>

<p>
    <button onclick="task2()">2 Задание</button>
    <input type="text" id="myInput" value="hello world">
</p>

<p>
  <button onclick="task3()">3 Задание</button>
  <input type="text" id="myyInput" value="hello world">
</p>

<p>
  <button onclick="task4()">4 Задание</button>
  <input type="number" id="myyInputt" value="3">
</p>

<p>
  <button onclick="task5()">5 Задание</button>
  <input type="text" id="input51" value="hello">
  <input type="text" id="input52" value="world">
</p>

<p>
  <button onclick="this.innerHTML = 'Текст поменялся'">6 Задание</button>
</p>

<p>
  <button onclick="task7()">7 Задание</button>
  <input type="text" id="Inputs" value="hello world">
</p>

<p>
  <button onclick="task8()">8 Задание(блокировать)</button>
  <button onclick="task81()">8 Задание(разблокировать)</button>
  <input type="text" id="Innput" value="hello world">
</p>

<p>
  <button onmouseover="alert('Вы навелись на кнопку')">9 Задание</button>
</p>

<p>
  <button ondblclick="alert('двойное нажатие')">10 Задание</button>
</p>

<style>
	.a {
	 border: 2px double rgba(121, 121, 121, 0); 
	 background-color: rgb(216, 216, 216);
	 width:100px;
	}
</style>

<p>
  <div class="a" onmouseover="alert('Наведение на область')">11 Задание</div>
</p>

<p>
  <button onclick="task12()">12 Задание</button><br>
  <img id="myImage" src="les.jpg" width="200" height="200">
</p>

<p>
  <button onclick="alert(this.innerHTML)">13 Задание</button>
</p>

<p>
  <input type="text" id="Inputqq" value="sdadadsa">
  <button onclick="this.previousElementSibling.value = 'Изменён'">14 Задание</button>
</p>

<p>
  <button onclick="this.disabled = true;">15 Задание</button>
</p>

<p>
  <button onclick="task16()">16 Задание</button>
<p id="clickCount">Количество нажатий: 0</p>
</p>

<p>
  <button onclick="this.style.cursor = 'pointer'">17 Задание</button>
</p>

<p>
  <button onclick="task18()">18 Задание</button>
  <p id="hide">id=hide</p>
</p>

<p>
  <button onclick="this.style.display = 'none'">19 Задание</button>
</p>

<p>
  <button onclick="task20()">20 Задание</button>
</p>

</body>
</html>
```
### Три движка
```js
const express = require('express');
const hbs = require('hbs');
const pug = require('pug');
const ejs = require('ejs');
const app = express();

hbs.registerPartials(__dirname + "/views/partials");

app.use(express.static(__dirname));

app.get("/", function(request, response) {
    response.sendFile("index.html");
});

app.get("/about_me", function(req, resp){
    resp.render('about.hbs');
});

app.get("/about_me/pug", function(req, resp){
    resp.render('pug/about_me.pug');
});

app.get("/about_me/EJS", function(req, resp){
    resp.render('about_me.ejs');
});

app.listen(3000, function(req, resp){
    console.log("Server online.")
});
```

<h2>Вывод</h2>
В этой лабораторной работе я научился работать с javascript.
