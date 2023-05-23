<script>
export default {
  
}
</script>

<template>
<div>
    <h1 class="main__title">Привет! Меня зовут Алексей, я занимаюсь фронТэнд разработкой</h1>
    <p class="main__desc">Выпускник HTML-Academy</p>
    <div class="skills">
        <div class="craete">
            <h4 class="skills__title">СОЗДАЮ</h4>
            <ul class="skills__list">
                <li class="skills__item--website">
                    <span class="skills__item--website">Вебсайты</span>
                    <span class="skills__item--website_desc">Верставю сайты по вашим макетам, гарантирую адаптивную, кроссбраузерную, семантически верную вёрстку вашего сайта в кратчайшие сроки </span>
                </li>
                <li class="skills__item--website">
                    <span class="skills__item--website">pixel-perfect верстку</span>
                    <span class="skills__item--website_desc">Верстаю в полном соответствии с предоставленным макетом, используя расширение Pixel-perfect</span>
                </li>
                <li class="skills__item--website">
                    <span class="skills__item--website">Простые веб приложения</span>
                    <span class="skills__item--website_desc">Разрабатываю не сложные веб приложения с использованием таких фреймворков как ReactJS и VueJS</span>
                </li>
            </ul>
        </div>
        <div class="skill__item">
            <h4 class="skills__title">НАВЫКИ</h4>
            <ul class="skills__list">
                <li>HTML5</li>
                <li>CSS, SCSS, SASS</li>
                <li>Figma</li>
                <li>JS</li>
                <li>ReactJS</li>
                <li>VueJS</li>
            </ul>
        </div>
    </div>
    <div class="portfolio">
        <h4 class="portfolio__title">ПОРТФОЛИО</h4>
        <ul class="portfolio__list">
            <li class="portfolio__item">
                <h5>Техномарт</h5>
                <img class="portfolio__item--img" src='/tehnomart.png' alt="Техномарт">
                <p class="portfolio__item__desc">В проекте Техномарт предоставлена вёрстка из двух страниц, в проекте использовались HTML5, CSS немного JS, мой первый проект в программировании, успешно защищен в HTML Academy</p>
            </li>
            <li class="portfolio__item">
                <h5>Pink</h5>
                <img class="portfolio__item--img" src="/pink.png" alt="Pink">
            </li>
            <li class="portfolio__item">
                <h5>Pink</h5>
                <img class="portfolio__item--img" src="/pink.png" alt="Pink">
            </li>
            <li class="portfolio__item">
                <h5>Pink</h5>
                <img class="portfolio__item--img" src="/pink.png" alt="Pink">
            </li>
            <li class="portfolio__item">
                <h5>Pink</h5>
                <img class="portfolio__item--img" src="/pink.png" alt="Pink">
            </li>
            <li class="portfolio__item">
                <h5>Pink</h5>
                <img class="portfolio__item--img" src="/pink.png" alt="Pink">
            </li>

        </ul>
    </div>
</div>
</template>

<style>
.main__title{
    font-size: 40px;
    max-width: 718px;
}
.main__desc {
    font-size: 16px;
    margin-top: 36px;
    position: relative;
    padding-left: 35px;
    max-width: 160px;
}
.main__desc::before {
    content: '';
    width: 32px;
    height: 32px;
    position: absolute;
    left: 0;
    top: 10px;
    background-image: url(/htmlAcademy.svg);
}
.skills {
    margin-top: 106px;
    display: flex;
    justify-content: space-between;
}

.skill__item{
    width: 54%;
}
.craete {
    width: 40%;
}
.skills__title {
    color: #21E6C1;
    font-size: 14px;
}
.portfolio {
    margin-top: 144px;
}
.portfolio__title {
    color: #21E6C1;
    font-size: 14px;
}
.skills__list {
    list-style: none;
    display: flex;
    justify-content: space-between;
    margin-top: 16px;
    flex-wrap: wrap;
}
.portfolio__list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-auto-rows: 21rem;
    grid-gap: 2rem;
    list-style: none;
}
.portfolio__item {
    cursor: pointer;
    text-align: center;
    transition: 0.4s ease;
    overflow: hidden;
}

.portfolio__item__desc {
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
.skills__item--website_desc {
    opacity: 0;
    transition: 1s;
    display: block;
    position: absolute;
    width: 330px;
    top: 26px;
}
.skills__item--website:hover+ .skills__item--website_desc {
    opacity: 1;
    transition: 1s;
}
</style>