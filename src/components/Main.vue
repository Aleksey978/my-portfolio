<script>
export default {
    created() {
    this.startInterval();
  },
  methods: {
    startInterval() {
      setTimeout(() => {
        this.classObject['my-class'] = false;
      }, 5000);   
    }
  },

  data() {
    return {
      classObject: {
        'my-class': true,
      },
    };
  }
}
</script>

<template>
<div>
    <p class="main__desc my-class">Выпускник HTML-Academy</p>
    <h1 data-text="Помогаю в создании крутых пользовательских интерфейсов." :class="classObject" class="main__title">Помогаю в создании крутых пользовательских интерфейсов.</h1>
    <div class="skills">
        <div class="skill__item">
            <h4 class="skills__title">ВЕБСАЙТЫ</h4>
            <p :class="classObject" class="skill__desc" data-text='Саздаю сайты по макетам Figma, Sketch, Adobe XD,  гарантирую адаптивную, кроссбраузерную, семантически верную вёрстку вашего сайта. Работаю как с крупными команиями так и с малым бизнесом.'></p>
        </div>
        <div class="skill__item">
            <h4 class="skills__title">react & Vue Приложения</h4>
            <p :class="classObject" class="skill__desc" data-text="Создаю веб-приложений с использованием Vue.js и React.js. Моя цель - создавать мощные и интуитивно понятные пользовательские интерфейсы, которые улучшают взаимодействие пользователей и бизнеса."></p>
        </div>
        <div class="skill__item">
            <h4 class="skills__title">навыки</h4>
            <p :class="classObject" class="skill__desc skill__desc__exp" data-text="Эксперт:  React JS, Vue JS, HTML, CSS, JS.
                Работаю с макетами: Figma, Sketch, Adobe XD. "></p>
        </div>
    </div>
    <div class="portfolio">
        <h4 class="portfolio__title">ПОРТФОЛИО</h4>
        <ul class="portfolio__list">
            <li class="portfolio__item">
                <a href="https://aleksey978.github.io/1561087-technomart-29/">

                    <h5 class="portfolio_item_title">Техномарт</h5>
                    <div class="three-dee tehnomart">
                        <!-- <img src="/tehnomart.png" alt="Your Image"> -->
                    </div>
                    <!-- <img class="portfolio__item--img" src='../tehnomart.png' alt="Техномарт"> -->
                    <!-- <p class="portfolio__item__desc">В проекте Техномарт предоставлена вёрстка из двух страниц, в проекте использовались HTML5, CSS немного JS, мой первый проект в программировании, успешно защищен в HTML Academy</p> -->
                </a>
            </li>
            <li class="portfolio__item">
                <a href="https://aleksey978.github.io/Pink-21/index.html">
                    <h5 class="portfolio_item_title">Pink</h5>
                    <div class="three-dee pink">
                        <!-- <img src="/tehnomart.png" alt="Your Image"> -->
                    </div>
                    <!-- <img class="portfolio__item--img" src="../pink.png" alt="Pink"> -->
                    <!-- <p class="portfolio__item__desc">В проекте Pink предоставлена адаптивная вёрстка из трёх страниц, в проекте использовались HTML5, CSS, LESS, немного JS, мой первый второй в программировании, успешно защищен в HTML Academy</p> -->
                </a>
            </li>
            <li class="portfolio__item">
                <a href="https://aleksey978.github.io/">
                    <h5 class="portfolio_item_title">Hugge</h5>
                    <div class="three-dee hugge">
                        <!-- <img src="/tehnomart.png" alt="Your Image"> -->
                    </div>
                    <!-- <img class="portfolio__item--img" src="../hugge.png" alt="hugge"> -->
                    <!-- <p class="portfolio__item__desc">Лендинг на тему "биоразлагаемые упаковки для продуктов", созданный с помощью библиотеки ReactJS</p> -->
                </a>
            </li>
            <li class="portfolio__item">
                <a href="https://aleksey978.github.io/calculator/">
                    <h5 class="portfolio_item_title">Calculator</h5>
                    <div class="three-dee calculator">
                        <!-- <img src="/tehnomart.png" alt="Your Image"> -->
                    </div>
                    <!-- <img class="portfolio__item--img" src="/calculator.png" alt="Calculator"> -->
                    <!-- <p class="portfolio__item__desc">Простой калькулятор написанный на языке Java Script с использованием фреймворка VueJS</p> -->
                </a>
            </li>
            <li class="portfolio__item">
                <a href="https://aleksey978.github.io/weather/">
                    <h5 class="portfolio_item_title">Weather</h5>
                    <div class="three-dee weather">
                        <!-- <img src="/tehnomart.png" alt="Your Image"> -->
                    </div>
                    <!-- <img class="portfolio__item--img" src="../weather.png" alt="Pink"> -->
                    <!-- <p class="portfolio__item__desc">Приложение для Просмотра погоды в любом городе по поиску написанный на языке Java Script с использованием фреймворка VueJS, использованна библиотека Axios для подключения к стороннему API для отправки запроса о погоде по запросу пользователя</p> -->
                </a>
            </li>
            <li class="portfolio__item">
                <a href="https://aleksey978.github.io/blog/">
                    <h5 class="portfolio_item_title">Blog</h5>
                    <div class="three-dee blog">
                        <!-- <img src="/tehnomart.png" alt="Your Image"> -->
                    </div>
                    <!-- <img class="portfolio__item--img" src="../blog.png" alt="Blog"> -->
                    <!-- <p class="portfolio__item__desc">Приложение типа блог, написанный на языке Java Script с использованием фреймворка VueJS, реализовано добавление нового поста, удаление, сортировка, поиск по постам, навигация по страницам (страници сделаны просто для примера), так же использованна анимация от VueJS</p> -->
                </a>
            </li>
        </ul>
    </div>
</div>
</template>

<style>
.main__title{
    position: relative;
    font-size: 54px;
    font-weight: normal;
    max-width: 820px;
    animation: glitch 1s linear infinite;
}

@media (max-width: 1800px) {
    .main__title {
        font-size: 32px;
        max-width: 520px;
    }
}

@media (max-width: 704px) {
    .main__title {
        font-size: 20px;
        max-width: 304px;
    }
}

.main__title::after {
    cursor: pointer;
    position: absolute;
    content: attr(data-text);
    top: 2px;
    left: 0px;
    width: 820px;
    background-color: rgb(7,30,61);
    color: #ffffff;
    overflow: hidden
}
@media (max-width: 1800px) {
  .main__title::after {
    width: 520px;
  }
}
@media (max-width: 704px) {
  .main__title::after {
    width: 304px;
  }
}
.main__desc {
    font-size: 16px;
    margin-top: 36px;
    position: relative;
    padding-left: 55px;
    margin-bottom: 21px;
    /* max-width: 160px; */
}
.main__desc::before {
    content: '';
    width: 32px;
    height: 32px;
    position: absolute;
    left: 0px;
    top: -4px;
    background-image: url(/htmlAcademy.svg);
}
.skills {
    margin-top: 106px;
    display: flex;
}

@media (max-width: 1060px) {
  .skills {
    flex-wrap: wrap;
}
}

@media (max-width: 701px) {
  .skills {
    margin-top: 43px;
    margin-left: 2px;
}
}

.skills .skill__item:not(:last-child) {
    margin-right: 42px;
    width: 602px;
}

@media (max-width: 1980px) {
    .skills .skill__item:not(:last-child) {
    margin-right: 121px;
    width: 765px;
    }
}

@media (max-width: 1800px) {
  .skills .skill__item:not(:last-child) {
    margin-right: 37px;
    width: 423px;
    }
}

@media (max-width: 1060px) {
  .skills .skill__item:not(:last-child) {
    margin-bottom: 130px;
    }
}

@media (max-width: 704px) {
  .skills .skill__item:not(:last-child) {
    margin-bottom: 43px;
    }
}

.skills .skill__item:last-child {
    width: 402px;
}

.skill__desc span{
    color: #21E6C1;
}
.skill__item{
    position: relative;
}

.skills__title {
    color: #21E6C1;
    width: max-content;
    margin-bottom: 30px;
    font-size: 14px;
    text-transform: uppercase;
    padding-bottom: 16px;
    border-bottom: 1px solid #21E6C1;
}
@media (max-width: 704px) {
  .skills__title {
    font-size: 10px;
}
}
.portfolio {
    margin-top: 144px;
}
@media (max-width: 1800px) {
  .portfolio {
    margin-top: 202px;
}
}

@media (max-width: 1060px) {
  .portfolio {
    margin-top: 110px;
}
}

@media (max-width: 704px) {
  .portfolio {
    margin-top: 32px;
}
}
/* .portfolio__list .portfolio__item:not(:first-child){
    margin-left: 40px;
} */
.portfolio__title {
    color: #21E6C1;
    font-size: 14px;
    margin-bottom: 25px;
}
@media (max-width: 704px) {
  .portfolio__title {

    font-size: 10px;

}
}
.skills__list {
    list-style: none;
    display: flex;
    justify-content: space-between;
    margin-top: 16px;
    flex-wrap: wrap;
}
.skills__list li {
    margin-right: 10px;
}
.portfolio__list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    /* grid-auto-rows: 21rem; */
    grid-gap: 40px;
    list-style: none;
}
@media (max-width: 704px) {
  .portfolio__list {
    grid-gap: 16px;
}
}
.portfolio__item {
    margin-bottom: 40px;
    position: relative;
    cursor: pointer;
    border: 1px solid #21E6C1;
    width: 281px;
    height: 280px;
    background-color: rgb(33,	230,	193, 0.1);
    text-align: center;
    transition: 0.4s ease;
    /* overflow: hidden; */
}
@media (max-width: 704px) {
  .portfolio__item {
    height: 50px;
    width: 100%;
    margin-bottom: 0;
}
}
.portfolio__item::before {
    content: '';
    width: 1px;
    height: 800%;
    top: -500%;
    left: 0;
    background: rgb(33,	230,	193, 0.1);
    position: absolute;
    animation: line 5s ease-in-out;
}


@keyframes line {
  0% {
    transform: translateY(-80%);
  }
  90% {
    transform: scale(1);
  }
  92% {
    transform: scale(6);
    background: rgb(33,	230,	193, 1);
  }
  94% {
    transform: scale(0);
  }
  100% {
    transform: translateY(0%);
  }
}

.portfolio__item a {
    text-decoration: none;
    color: white;
}
.portfolio_item_title {
    font-size: 24px;
    font-weight: 700;
    position: absolute;
    bottom: 24px;
    left: 24px;
}
@media (max-width: 704px) {
  .portfolio_item_title {
    font-size: 14px;
    bottom: 14px;
    left: 24px;
}
}
.portfolio__item__desc {
    text-align: center;
    height: 100%;
    width: 280px;
    padding-left: 10px;
    padding-right: 10px;
    margin: 0 auto;
    background: rgb(7,30,61);
background: linear-gradient(0deg, rgba(7,30,61,0.4990371148459384) 0%, rgba(7,30,61,1) 94%);
    transition: .5s ease;
}
.portfolio__item:hover  .portfolio__item__desc{
    transform: translateY(-250px);
}

.portfolio__item--img {
    width: 280px;
    height: 320px;
}
.skills__item--website {
    padding-bottom: 2px;
    transition: 0.4s ease;
    position: relative;
}
.skills__item--website_item {
    cursor: default;
}
.skills__item--website_item:hover {
    border-bottom: 1px solid #21E6C1;
}


.skill__desc:before,
.skill__desc:after {
    cursor: pointer;
    position: absolute;
    content: attr(data-text);
    top: 68px;
    left: 0;
    background-color: rgb(7,30,61);
    color: #ffffff;
    overflow: hidden;
    /* white-space: nowrap; */
}

@media (max-width: 704px) {
  .skill__desc:before,
  .skill__desc:after {
    font-size: 10px;
    top: 32px;
}
}




.skill__desc:after,
.main__title:after {
        left: -1px;   
}


.my-class:after {
    /* animation: glitch-2 3s ease-in-out reverse infinite; */
    animation: glitch-1 3s ease-in-out reverse infinite;
}
.three-dee {
    margin: 0 auto 0;
    display: block;
    opacity: 0.1;
    z-index: 42;
    outline: 3px solid cyan;
    width: 280px;
    height: 281px;
    transition: 0.8s;
}
@media (max-width: 704px) {
  .three-dee {
    display: none;
}
}

.tehnomart {
    background: url(./tehnomart.png), rgb(7,30,61);
    background-blend-mode: lighten;
    background-size: cover;
}
.pink {
    background: url(./pink.png), rgb(7,30,61);
    background-blend-mode: lighten;
    background-size: cover;
}
.hugge {
    background: url(./hugge.png), rgb(7,30,61);
    background-blend-mode: lighten;
    background-size: cover;
}
.calculator {
    background: url(./calculator.png), rgb(7,30,61);
    background-blend-mode: lighten;
    background-size: cover;
}
.weather {
    background: url(./weather.png), rgb(7,30,61);
    background-blend-mode: lighten;
    background-size: cover;
}
.blog {
    background: url(./blog.png), rgb(7,30,61);
    background-blend-mode: lighten;
    background-size: cover;
}


  .three-dee:hover {
    animation: show-overlap 0.4s linear alternate;
    opacity: 1;
  }


@keyframes show-overlap {
  0% { opacity: 0;  }
  10% { opacity: 0.3;  }
  20% { opacity: 0.1;  }
  30% { opacity: 0.6;  }
  40% { opacity: 0.8;  }
  50% { opacity: 1;  }
  60% { opacity: 0.5;  }
  70% { opacity: 0.3;  }
  100% { opacity: 1;}
}












  



















@keyframes glitch-1 {
  0% {
    clip: rect(232px, auto, 101px, 30px);
  }
  5% {
    clip: rect(67px, auto, 94px, 30px);
  }
  10% {
    clip: rect(40px, auto, 66px, 30px);
  }
  15% {
    clip: rect(87px, auto, 82px, 30px);
  }
  20% {
    clip: rect(137px, auto, 61px, 30px);
  }
  25% {
    clip: rect(34px, auto, 14px, 30px);
  }
  30% {
    clip: rect(133px, auto, 74px, 30px);
  }
  35% {
    clip: rect(76px, auto, 107px, 30px);
  }
  40% {
    clip: rect(59px, auto, 130px, 30px);
  }
  45% {
    clip: rect(29px, auto, 84px, 30px);
  }
  50% {
    clip: rect(22px, auto, 67px, 30px);
  }
  55% {
    clip: rect(67px, auto, 62px, 30px);
  }
  60% {
    clip: rect(10px, auto, 105px, 30px);
  }
  65% {
    clip: rect(78px, auto, 115px, 30px);
  }
  70% {
    clip: rect(105px, auto, 13px, 30px);
  }
  75% {
    clip: rect(15px, auto, 75px, 30px);
  }
  80% {
    clip: rect(66px, auto, 39px, 30px);
  }
  85% {
    clip: rect(133px, auto, 73px, 30px);
  }
  90% {
    clip: rect(36px, auto, 128px, 30px);
  }
  95% {
    clip: rect(68px, auto, 103px, 30px);
  }
  100% {
    clip: rect(14px, auto, 100px, 30px);
  }
}

@keyframes glitch-2 {
  0% {
    clip: rect(129px, auto, 36px, 30px);
  }
  5% {
    clip: rect(36px, auto, 4px, 30px);
  }
  10% {
    clip: rect(85px, auto, 66px, 30px);
  }
  15% {
    clip: rect(91px, auto, 91px, 30px);
  }
  20% {
    clip: rect(148px, auto, 138px, 30px);
  }
  25% {
    clip: rect(38px, auto, 122px, 30px);
  }
  30% {
    clip: rect(69px, auto, 54px, 30px);
  }
  35% {
    clip: rect(98px, auto, 71px, 30px);
  }
  40% {
    clip: rect(146px, auto, 34px, 30px);
  }
  45% {
    clip: rect(134px, auto, 43px, 30px);
  }
  50% {
    clip: rect(102px, auto, 80px, 30px);
  }
  55% {
    clip: rect(119px, auto, 44px, 30px);
  }
  60% {
    clip: rect(106px, auto, 99px, 30px);
  }
  65% {
    clip: rect(141px, auto, 74px, 30px);
  }
  70% {
    clip: rect(20px, auto, 78px, 30px);
  }
  75% {
    clip: rect(133px, auto, 79px, 30px);
  }
  80% {
    clip: rect(78px, auto, 52px, 30px);
  }
  85% {
    clip: rect(35px, auto, 39px, 30px);
  }
  90% {
    clip: rect(67px, auto, 70px, 30px);
  }
  95% {
    clip: rect(71px, auto, 103px, 30px);
  }
  100% {
    clip: rect(83px, auto, 40px, 30px);
  }
}
</style>
