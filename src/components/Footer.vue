<template>
  <footer>
    <div class="footer-main">
      <div class="footer-main-content content">
        <div class="footer-main-column footer-main-left">
          <img :src="require(`../assets/img/${colLeft.img}`)" alt="Cose da barbiere">
          <button class="footer-main-btn">{{colLeft.textBtn}}</button>
        </div>
        <div class="footer-main-column footer-main-center">
          <img :src="require(`../assets/img/${smLogo}`)" alt="Logo Avada Baebers">
          <ul>
            <li>{{barber.name}}</li>
            <li>{{barber.street}}</li>
            <li>{{barber.street}}</li>
            <li>{{barber.city}}</li>
            <li>{{barber.phone}}</li>
          </ul>
          <span class="follow">follow us</span>
          <div class="footer-icons">
            <i v-for="(icons, index) in iconsFooter" :key="index" :class="`${iconsFooter[index]}`"></i>
          </div>
        </div>
        <div class="footer-main-column footer-main-right">
          <img :src="require(`../assets/img/${colRight.img}`)" alt="Cose da barbiere">
          <button class="footer-main-btn">{{colRight.textBtn}}</button>
        </div>
      </div>
    </div>
    <div class="footer-copyright">
      @ Copyright 2012 - {{getYear()}} | Lorem ipsum dolor sit amet consectetur, adipisicing elit. Error, vero?
    </div>
  </footer>
</template>

<script>
    export default {
        name: 'Footer',
        props: {
          smLogo: String,
          iconsFooter: Array,
          barber: Object,
          colLeft: Object,
          colRight: Object,
        },
        methods: {
          getYear() {
            return new Date().getFullYear()
          }
        }
    }
</script>

<style scoped lang="scss">
  .footer-main {
    background-color: #111110;
    padding: 45px 0 60px;
    .footer-main-content {
      display: flex;
      font-family: 'Lato', sans-serif;
      .footer-main-column {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 40%;
      }
      .footer-main-left, .footer-main-right {
        img {
          width: 80%;
          margin-bottom: 15px;
        }
        .footer-main-btn {
          font-size: 12px;
          width: fit-content;
          padding: 10px 35px;
          text-transform: uppercase;
          color: #ffcf6a;
          background-color: rgba(0, 0, 0, 0);
          border: none;
          border: 2px solid #ffcf6a;
          cursor: pointer;
        }
        .footer-main-btn:hover {
            opacity: 0.7;
        }
      }
      .footer-main-center {
        color: #505050;
        width: 20%;
        img {
          width: 80%;
        }
        ul {
          list-style: none;
          margin: 40px 0;
          text-align: center;
          li {
            line-height: 1.4;
          }
        }
        span.follow {
          color: #ffcf6a;
          text-transform: uppercase;
          margin-bottom: 35px;
        }
        .footer-icons {
          display: flex;
          justify-content: space-evenly;
          width: 60%;
          color: #fff;
        }
      }
    }
  }
  .footer-copyright {
    font-family: 'Lato', sans-serif;
    height: 70px;
    background-color: #353333;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #4f659a;
  }
</style>