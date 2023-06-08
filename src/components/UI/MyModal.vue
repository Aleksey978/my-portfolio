<script>
import MyButton from './MyButton.vue'
export default {
  components: { MyButton },
  name: 'my-dialog',
  props: {
    show: {
      type: Boolean,
      default: true
    }
  },
  methods: {
    hideDialog() {
    this.$emit('update:show', false);
    }
  }
}
</script>


<template>
    <transition name="slide-fade">
        <div class="modal" v-show="show" @click.stop="hideDialog">
            <form class="form" @click.stop>
                <h3 class="form__title">Напиши прямо сюда</h3>
                <label for="email">ТВОЙ ИМЕЙЛ</label>
                <input id="email" placeholder="email.com" type="text">
                <label for="message">СООБЩЕНИЕ</label>
                <textarea id="message" placeholder="сообщение..." type="text"/>
                <my-button type="submit" class="form__btn">Отправить</my-button>
            </form>
            <div>
                <h3  class="form__title">Или свяжись по</h3>
                <ul>
                    <li class="feetback__item"><p>WatsApp</p><a href="https://wa.me/79145168123?text=%D0%9F%D1%80%D0%B8%D0%B2%D0%B5%D1%82!%20%F0%9F%91%8B%20%D0%9C%D0%B5%D0%BD%D1%8F%20%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D0%B5%D1%81%D1%83%D0%B5%D1%82...">Aleksey Chetvercin</a></li>
                    <li class="feetback__item"><p>Telegramm</p><a href="https://t.me/AlekseyChetv">AlekseyChetv</a></li>
                </ul>
            </div>
        </div>
    </transition>
</template>

<style>
.modal {
    display: flex;
    position: absolute;
    left: 0;
    right: 0;
    top: 100px;
    padding: 170px  136px;
    bottom: 0;
    width: 100%;
    height: 100%;
    background-color: #071E3D;
    z-index: 10;
    flex-wrap: wrap;
}
@media (max-width: 1200px) {
    .modal {
        padding: 60px  136px;
        justify-content: center;
    }
}
.form {
    display: flex;
    flex-wrap: wrap-reverse;
    max-width: 417px;
    flex-direction: column;
    margin-right: 113px;
}
@media (max-width: 1200px) {
    .form {
        margin-left: auto;
        margin-right: auto;
    }
}
.form label{
    color: #21E6C1;
    font-size: 14px;
    font-weight: 400;
    margin-bottom: 13px;
}
.form input{
    height: 37px;
    background: transparent;
    border: 1px solid white;
    outline: none;
    margin-bottom: 37px;
    color: white;
    font-size: 16px;
    padding-left: 12px;
}
.form__title {
    font-size: 40px;
    margin-bottom: 72px;
}
@media (max-width: 768px) {
    .form__title {
        font-size: 24px;
        margin-bottom: 32px;
    }
}
.form__btn {
    width: 100px;;
}
#message {
    height: 123px;
    background: transparent;
    border: 1px solid white;
    outline: none;
    margin-bottom: 47px;
    color: white;
    font-size: 18px;
    padding-left: 12px;
}
@media (max-width: 768px) {
    #message {
        margin-bottom: 8px;
    }
}
.feetback__item {
    list-style: none;
    display: flex;
    margin-bottom: 24px;
}
@media (max-width: 768px) {
    .feetback__item {
        flex-direction: column;
    }
}
.feetback__item p{
    color: #21E6C1;
    width: 203px;
}
.feetback__item a{
    text-decoration: none;
    color: white;
}
.slide-fade-enter-active {
  transition: all .7s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active до версии 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
</style>