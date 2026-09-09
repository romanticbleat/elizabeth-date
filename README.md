<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Для Елизаветы ❤️</title>

<style>
*{
    box-sizing:border-box;
    -webkit-tap-highlight-color:transparent;
}

body{
    margin:0;
    min-height:100vh;
    font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;
    background:linear-gradient(135deg,#ffd6e7,#fff0f5,#ffdce9);
    display:flex;
    justify-content:center;
    align-items:center;
    overflow-x:hidden;
    color:#3b2630;
}

.container{
    width:100%;
    max-width:520px;
    min-height:100vh;
    padding:20px;
    display:flex;
    align-items:center;
    justify-content:center;
}

.screen{
    display:none;
    width:100%;
    text-align:center;
    animation:fade .5s ease;
}

.screen.active{
    display:block;
}

@keyframes fade{
    from{
        opacity:0;
        transform:translateY(15px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.card{
    background:rgba(255,255,255,.9);
    border-radius:30px;
    padding:30px 22px;
    box-shadow:0 15px 50px rgba(150,60,90,.18);
}

h1{
    font-size:30px;
    margin:10px 0 15px;
}

h2{
    font-size:25px;
    margin:10px 0 20px;
}

p{
    font-size:17px;
    line-height:1.55;
}

.heart{
    font-size:55px;
    animation:pulse 1.3s infinite;
}

@keyframes pulse{
    50%{
        transform:scale(1.15);
    }
}

button{
    border:none;
    border-radius:18px;
    padding:15px 22px;
    font-size:17px;
    font-weight:600;
    cursor:pointer;
    transition:.2s;
    margin:7px;
}

.main-btn{
    background:#ff5c91;
    color:white;
    box-shadow:0 8px 20px rgba(255,92,145,.3);
}

.main-btn:active{
    transform:scale(.95);
}

.option{
    display:block;
    width:100%;
    margin:10px 0;
    background:#fff;
    border:2px solid #ffd0df;
    color:#442a34;
}

.option:hover{
    background:#fff0f5;
    transform:scale(1.02);
}

.option.selected{
    background:#ff76a5;
    color:white;
    border-color:#ff76a5;
}

.buttons{
    margin-top:20px;
}

.yes{
    background:#ff4f87;
    color:#fff;
}

.no{
    background:#eee;
    color:#555;
    position:relative;
}

textarea{
    width:100%;
    min-height:120px;
    border:2px solid #ffd0df;
    border-radius:18px;
    padding:15px;
    font-size:16px;
    resize:none;
    outline:none;
    font-family:inherit;
}

.date{
    font-size:27px;
    font-weight:800;
    color:#ff4f87;
    margin:15px 0;
}

.small{
    font-size:14px;
    opacity:.7;
}

.summary{
    text-align:left;
    background:#fff4f8;
    padding:15px;
    border-radius:20px;
    margin:15px 0;
}

.telegram{
    background:#229ed9;
    color:white;
    width:100%;
}

.final-heart{
    font-size:80px;
    animation:pulse 1.4s infinite;
}

.floating-heart{
    position:fixed;
    bottom:-30px;
    pointer-events:none;
    animation:float 6s linear forwards;
    opacity:.7;
}

@keyframes float{
    from{
        transform:translateY(0) rotate(0);
        opacity:0;
    }
    20%{
        opacity:.8;
    }
    to{
        transform:translateY(-110vh) rotate(360deg);
        opacity:0;
    }
}
</style>
</head>

<body>

<div class="container">

<!-- 1 -->
<div class="screen active" id="screen1">
<div class="card">
<div class="heart">❤️</div>
<h1>Для Елизаветы</h1>
<p>
Есть кое-что, что я давно хотел тебе предложить...
</p>
<button class="main-btn" onclick="go(2)">
Открыть 💌
</button>
</div>
</div>

<!-- 2 -->
<div class="screen" id="screen2">
<div class="card">
<h2>Елизавета, маленький вопрос 👀</h2>
<p>Веришь, что человек может неожиданно стать для тебя очень важным?</p>

<button class="option" onclick="answer(2,'Да ❤️')">Да ❤️</button>
<button class="option" onclick="answer(2,'Возможно 👀')">Возможно 👀</button>
<button class="option" onclick="answer(2,'Не знаю 😅')">Не знаю 😅</button>
</div>
</div>

<!-- 3 -->
<div class="screen" id="screen3">
<div class="card">
<h2>А если человек...</h2>
<p>
Иногда пишет первым, заботится, хочет проводить с тобой время
и постоянно пытается тебя рассмешить?
</p>

<button class="option" onclick="answer(3,'Это мило 🥹')">Это мило 🥹</button>
<button class="option" onclick="answer(3,'Подозрительно 😂')">Подозрительно 😂</button>
<button class="option" onclick="answer(3,'Мне нравится ❤️')">Мне нравится ❤️</button>
</div>
</div>

<!-- 4 -->
<div class="screen" id="screen4">
<div class="card">
<h2>Следующий вопрос 😌</h2>
<p>
Что важнее на свидании?
</p>

<button class="option" onclick="answer(4,'Хорошая компания ❤️')">Хорошая компания ❤️</button>
<button class="option" onclick="answer(4,'Место ✨')">Красивое место ✨</button>
<button class="option" onclick="answer(4,'Еда 😋')">Вкусная еда 😋</button>
<button class="option" onclick="answer(4,'Чтобы было весело 😂')">Чтобы было весело 😂</button>
</div>
</div>

<!-- 5 -->
<div class="screen" id="screen5">
<div class="card">
<h2>Представь ситуацию 👀</h2>
<p>
Тебе пишут:<br><br>
<b>«Собирайся. Я заеду за тобой»</b> 🚗
</p>

<button class="option" onclick="answer(5,'Я бы пошла ❤️')">Я бы пошла ❤️</button>
<button class="option" onclick="answer(5,'А куда? 👀')">А куда? 👀</button>
<button class="option" onclick="answer(5,'Надо подумать 😂')">Надо подумать 😂</button>
</div>
</div>

<!-- 6 -->
<div class="screen" id="screen6">
<div class="card">
<h2>Последний вопрос...</h2>
<p>
А если этот человек — я? 😏
</p>

<div class="buttons">
<button class="yes" onclick="go(7)">
Тогда я согласна ❤️
</button>

<button class="no" id="noBtn">
Нет 😈
</button>
</div>
</div>
</div>

<!-- 7 -->
<div class="screen" id="screen7">
<div class="card">
<div class="heart">🥰</div>
<h1>Тогда решено!</h1>

<p>
Елизавета, официально приглашаю тебя
на свидание.
</p>

<div class="date">
18.09.2026<br>
18:18
</div>

<p>
🚗 <b>Я приеду за тобой.</b>
</p>

<button class="main-btn" onclick="go(8)">
Что дальше? 💌
</button>
</div>
</div>

<!-- 8 -->
<div class="screen" id="screen8">
<div class="card">
<h2>Небольшие условия 😌</h2>

<p>
После школы спокойно идёшь домой,
отдыхаешь, приводишь себя в порядок
и собираешься.
</p>

<p>
👗 Одежда — по погоде и по твоему вкусу.
Главное — чтобы тебе самой было комфортно.
</p>

<p>
❌ Вульгарно одеваться не надо 😂
</p>

<p>
А в <b>18:18</b> просто выходишь ко мне.
Никаких дополнительных планов.
Я всё остальное беру на себя ❤️
</p>

<button class="main-btn" onclick="go(9)">
Хорошо 😌
</button>
</div>
</div>

<!-- 9 -->
<div class="screen" id="screen9">
<div class="card">
<h1>Но есть одна проблема... 😏</h1>

<p>
Я не знаю, что именно тебе хочется.
Поэтому теперь выбор за тобой.
</p>

<div class="heart">👇</div>

<button class="main-btn" onclick="go(10)">
Выбрать ❤️
</button>
</div>
</div>

<!-- 10 -->
<div class="screen" id="screen10">
<div class="card">
<h2>Начнём с самого важного 😋</h2>
<p>Что будем кушать?</p>

<button class="option" onclick="selectOption('food','🍕 Пицца',11)">🍕 Пицца</button>
<button class="option" onclick="selectOption('food','🍣 Суши',11)">🍣 Суши</button>
<button class="option" onclick="selectOption('food','🍔 Бургеры',11)">🍔 Бургеры</button>
<button class="option" onclick="selectOption('food','🍝 Паста',11)">🍝 Паста</button>
<button class="option" onclick="selectOption('food','🤷 Что-нибудь другое',11)">🤷 Что-нибудь другое</button>
</div>
</div>

<!-- 11 -->
<div class="screen" id="screen11">
<div class="card">
<h2>А запивать чем? 🥤</h2>

<button class="option" onclick="selectOption('drink','☕ Кофе',12)">☕ Кофе</button>
<button class="option" onclick="selectOption('drink','🫖 Чай',12)">🫖 Чай</button>
<button class="option" onclick="selectOption('drink','🥤 Лимонад',12)">🥤 Лимонад</button>
<button class="option" onclick="selectOption('drink','💧 Воду',12)">💧 Воду</button>
<button class="option" onclick="selectOption('drink','🤷 Мне всё равно',12)">🤷 Мне всё равно</button>
</div>
</div>

<!-- 12 -->
<div class="screen" id="screen12">
<div class="card">
<h2>Куда отправляемся? 🚗</h2>

<button class="option" onclick="selectOption('place','🎬 В кино',13)">🎬 В кино</button>
<button class="option" onclick="selectOption('place','🎳 В боулинг',13)">🎳 В боулинг</button>
<button class="option" onclick="selectOption('place','☕ В уютное кафе',13)">☕ В уютное кафе</button>
<button class="option" onclick="selectOption('place','🛍️ Погулять по ТЦ',13)">🛍️ Погулять по ТЦ</button>
<button class="option" onclick="selectOption('place','🚗 Просто покататься',13)">🚗 Просто покататься</button>
<button class="option" onclick="selectOption('place','🤷 Решай сам',13)">🤷 Решай сам</button>
</div>
</div>

<!-- 13 -->
<div class="screen" id="screen13">
<div class="card">
<h2>А где погуляем? 🌙</h2>

<button class="option" onclick="selectOption('walk','🌳 В парке',14)">🌳 В парке</button>
<button class="option" onclick="selectOption('walk','🌃 По центру',14)">🌃 По центру</button>
<button class="option" onclick="selectOption('walk','🌊 У воды',14)">🌊 У воды</button>
<button class="option" onclick="selectOption('walk','🚗 Где-нибудь красиво',14)">🚗 Где-нибудь красиво</button>
<button class="option" onclick="selectOption('walk','🤷 Куда Данияр повезёт',14)">🤷 Куда Данияр повезёт</button>
</div>
</div>

<!-- 14 -->
<div class="screen" id="screen14">
<div class="card">
<h2>Чем займёмся? 😏</h2>

<button class="option" onclick="selectOption('activity','🎬 Посмотрим фильм',15)">🎬 Посмотрим фильм</button>
<button class="option" onclick="selectOption('activity','🎳 Поиграем',15)">🎳 Поиграем</button>
<button class="option" onclick="selectOption('activity','🚶 Просто погуляем',15)">🚶 Просто погуляем</button>
<button class="option" onclick="selectOption('activity','💬 Поговорим обо всём',15)">💬 Поговорим обо всём</button>
<button class="option" onclick="selectOption('activity','❤️ Главное — вместе',15)">❤️ Главное — вместе</button>
</div>
</div>

<!-- 15 -->
<div class="screen" id="screen15">
<div class="card">
<h2>Какое настроение? ✨</h2>

<button class="option" onclick="selectOption('mood','🌹 Романтика',16)">🌹 Романтика</button>
<button class="option" onclick="selectOption('mood','😂 Повеселиться',16)">😂 Повеселиться</button>
<button class="option" onclick="selectOption('mood','😌 Спокойный вечер',16)">😌 Спокойный вечер</button>
<button class="option" onclick="selectOption('mood','🎲 Полная спонтанность',16)">🎲 Полная спонтанность</button>
</div>
</div>

<!-- 16 -->
<div class="screen" id="screen16">
<div class="card">
<h2>И последнее 💭</h2>

<p>
Есть какое-нибудь твоё пожелание
для нашего вечера?
</p>

<textarea id="wish" placeholder="Например: хочу что-нибудь необычное ❤️"></textarea>

<button class="main-btn" onclick="finishQuestionnaire()">
Готово 💌
</button>
</div>
</div>

<!-- 17 -->
<div class="screen" id="screen17">
<div class="card">
<h2>Вот что у нас получилось ❤️</h2>

<div class="summary">
<p>🍽️ <b>Еда:</b> <span id="sFood"></span></p>
<p>🥤 <b>Напиток:</b> <span id="sDrink"></span></p>
<p>📍 <b>Место:</b> <span id="sPlace"></span></p>
<p>🚶 <b>Прогулка:</b> <span id="sWalk"></span></p>
<p>🎉 <b>Занятие:</b> <span id="sActivity"></span></p>
<p>✨ <b>Настроение:</b> <span id="sMood"></span></p>
<p>💭 <b>Пожелание:</b> <span id="sWish"></span></p>
</div>

<p>
Теперь осталось отправить это Данияру 😏
</p>

<button class="telegram" onclick="sendTelegram()">
📩 Отправить Данияру в Telegram
</button>

<p class="small">
Telegram откроется с готовым сообщением.
Останется только нажать «Отправить».
</p>
</div>
</div>

<!-- 18 -->
<div class="screen" id="screen18">
<div class="card">
<div class="final-heart">❤️</div>

<h1>До встречи, Елизавета!</h1>

<p>
18 сентября.<br>
18:18.
</p>

<p>
Я приеду за тобой. 🚗
</p>

<p>
И обещаю — скучно не будет 😏
</p>

<p>
<b>До встречи ❤️</b>
</p>
</div>
</div>

</div>

<script>

const answers = {
    food:"",
    drink:"",
    place:"",
    walk:"",
    activity:"",
    mood:"",
    wish:""
};

function go(number){

    document.querySelectorAll(".screen").forEach(screen=>{
        screen.classList.remove("active");
    });

    const target=document.getElementById("screen"+number);

    if(target){
        target.classList.add("active");
        window.scrollTo({
            top:0,
            behavior:"smooth"
        });
    }
}

function answer(question,value){

    setTimeout(()=>{
        if(question===2) go(3);
        if(question===3) go(4);
        if(question===4) go(5);
        if(question===5) go(6);
    },200);
}

function selectOption(type,value,nextScreen){

    answers[type]=value;

    setTimeout(()=>{
        go(nextScreen);
    },180);
}

function finishQuestionnaire(){

    answers.wish=document.getElementById("wish").value.trim();

    if(!answers.wish){
        answers.wish="Нет, всё на усмотрение Данияра ❤️";
    }

    document.getElementById("sFood").textContent=answers.food || "Не выбрано";
    document.getElementById("sDrink").textContent=answers.drink || "Не выбрано";
    document.getElementById("sPlace").textContent=answers.place || "Не выбрано";
    document.getElementById("sWalk").textContent=answers.walk || "Не выбрано";
    document.getElementById("sActivity").textContent=answers.activity || "Не выбрано";
    document.getElementById("sMood").textContent=answers.mood || "Не выбрано";
    document.getElementById("sWish").textContent=answers.wish;

    go(17);
}

function sendTelegram(){

    const message =
`❤️ Елизавета согласилась на свидание!

📅 Дата: 18.09.2026
⏰ Время: 18:18

🍽️ Еда: ${answers.food}
🥤 Напиток: ${answers.drink}
📍 Место: ${answers.place}
🚶 Прогулка: ${answers.walk}
🎉 Чем заняться: ${answers.activity}
✨ Настроение: ${answers.mood}
💭 Пожелание: ${answers.wish}

❤️ Я согласна на свидание!`;

    const url =
        "https://t.me/teunaev7?text=" +
        encodeURIComponent(message);

    window.location.href=url;

    setTimeout(()=>{
        go(18);
    },1000);
}


/* Убегающая кнопка "Нет" */

const noBtn=document.getElementById("noBtn");

function moveNoButton(){

    const maxX=Math.max(20,window.innerWidth-140);
    const maxY=Math.max(20,window.innerHeight-80);

    const x=Math.random()*maxX;
    const y=Math.random()*maxY;

    noBtn.style.position="fixed";
    noBtn.style.left=x+"px";
    noBtn.style.top=y+"px";
    noBtn.style.zIndex="9999";
}

if(noBtn){

    noBtn.addEventListener("pointerenter",moveNoButton);

    noBtn.addEventListener("pointerdown",(e)=>{
        e.preventDefault();
        moveNoButton();
    });
}


/* Плавающие сердечки */

function createHeart(){

    const heart=document.createElement("div");

    heart.className="floating-heart";
    heart.textContent=["❤️","💗","💕","💖","💘"][Math.floor(Math.random()*5)];

    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(15+Math.random()*25)+"px";
    heart.style.animationDuration=(4+Math.random()*4)+"s";

    document.body.appendChild(heart);

    setTimeout(()=>{
        heart.remove();
    },8000);
}

setInterval(createHeart,900);

</script>

</body>
</html>
