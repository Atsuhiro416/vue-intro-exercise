<template>
  <div id="app">
    <Header></Header>
    <main>
      <div id="eyecatch">
        <p>機械ではできない仕事を</p>
        <div class="news">
          <div class="news-content">
            <p class="news-date">2019/01/01</p>
            <p class="news-title">ニュースタイトルがここに入ります。3月の決算報告書</p>
          </div>
          <div class="news-logo">
            <p>news</p>
          </div>
        </div>
      </div>

      <div id="mission-wrapper" class="wrap">
        <div class="mission-message">
          <h2 class="mission-title">お客様のために進化する成長企業であり続ける</h2>
          <p class="mission-description">顧客主導型サービスを提供する企業として、お客様の会社経営に必要なサービスと情報を提供し続ける企業支援会社を目指します。企業が現在直面している「勝ち残るため」の戦略を提供できる会社として、ホームページをはじめ、各種マーケティングをご提供いたします。</p>
          <button class="mission-link">ミッション詳細</button>
        </div>
        <img src="./assets/mission-img.jpg" alt="">
      </div>

      <div id="service-wrapper" class="wrap">
        <h2 class="section-title">service</h2>
        <div v-for="(service, index) in services" :key="index" :class="`service${index + 1}`">
          <img :src="service.img" alt="">
          <div class="service-card">
            <h3>{{service.title}}</h3>
            <p class="service-subtitle">{{service.subtitle}}</p>
            <p class="service-description">{{service.description}}</p>
            <a href="#">{{service.link}}</a>
          </div><!-- /.service-card -->
        </div><!-- /.service1 -->
      </div>

      <div class="company-recruit flex between">
        <div v-for="(item, index) in companyRecruit" :key="index" :class="item.isClass">
          <div class="logo">
            <h2>{{item.en}}</h2>
            <p>{{item.ja}}</p>
          </div>
        </div>
      </div>

      <div id="faq-wrapper" class="wrap">
        <h2>FAQ</h2>
        <p>良くある質問</p>
      </div>


      <div id="contact-wrapper">
        <h2>contact</h2>
        <p class="contact-subtitle">お問い合わせ</p>
        <p class="contact-message">お気軽にお問い合わせください。</p>
        <p class="contact-description">資料請求・お問い合わせなどなんでも気軽にお問い合わせください。お仕事のご連絡もお問い合わせページに飛んでいただいて、入力フォームご記入お願いいたします。</p>
        <a href="#">お問い合わせへ</a>
      </div>
    </main>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  data() {
    return {
      services: [
        {
          title: "Web制作事業",
          subtitle: "コーチングのミッション",
          description: "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供、建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります",
          img: require("./assets/service2.jpg"),
          link: "サービス詳細"
        },
        {
          title: "Web制作事業",
          subtitle: "コーチングのミッション",
          description: "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供、建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります",
          img: require("./assets/service1.jpg"),
          link: "サービス詳細"
        }
      ],
      companyRecruit: [
        {
          isClass: "company",
          en: "company",
          ja: "会社概要"
        },
        {
          isClass: "recruit",
          en: "recruit",
          ja: "採用情報"
        }
      ]
    };
  },

  components: {
    Header,
    Footer
  }
};
</script>

<style>
@charset "UTF-8";
/* リセットcss */
html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent;
}

body {
  line-height: 1;
}

article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section {
  display: block;
}

nav ul {
  list-style: none;
}

blockquote, q {
  quotes: none;
}

blockquote:before, blockquote:after,
q:before, q:after {
  content: '';
  content: none;
}

a {
  margin: 0;
  padding: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent;
  text-decoration: none;
}

/* change colours to suit your needs */
ins {
  background-color: #ff9;
  color: #000;
  text-decoration: none;
}

/* change colours to suit your needs */
mark {
  background-color: #ff9;
  color: #000;
  font-style: italic;
  font-weight: bold;
}

del {
  text-decoration: line-through;
}

abbr[title], dfn[title] {
  border-bottom: 1px dotted;
  cursor: help;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

/* change border colour to suit your needs */
hr {
  display: block;
  height: 1px;
  border: 0;
  border-top: 1px solid #cccccc;
  margin: 1em 0;
  padding: 0;
}

input, select {
  vertical-align: middle;
}

/* 共通のスタイル */
.section-title {
  font-size: 30px;
  font-weight: bold;
  margin: 30px 0;
  text-align: center;
}

img {
  display: block;
  width: 100%;
}

.wrap {
  width: 80%;
  margin: 0 auto 50px;
}

.flex {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  -ms-flex-wrap: wrap;
      flex-wrap: wrap;
}

.between {
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
}

.around {
  -ms-flex-pack: distribute;
      justify-content: space-around;
}

#eyecatch {
  height: 600px;
  background: url(./assets/eyecatch.jpg) no-repeat;
  background-size: cover;
  background-position: center;
  position: relative;
}

#eyecatch > p {
  position: absolute;
  top: 60%;
  left: 25%;
  -webkit-transform: translate(-50%, -50%);
          transform: translate(-50%, -50%);
  font-size: 50px;
  font-style: italic;
  font-weight: bold;
  color: #f2f2ff;
  line-height: 1;
}

.news {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 50%;
  height: 60px;
}

.news-content {
  background-color: #f2f2f2;
  display: inline-block;
  width: 80%;
  height: 100%;
}

.news-date {
  margin: 5px 0 0 5px;
}

.news-title {
  margin: 10px;
}

.news-logo {
  position: absolute;
  right: 0;
  bottom: 0;
  -webkit-box-sizing: border-box;
          box-sizing: border-box;
  color: #f2f2f2;
  background-color: #000;
  display: inline-block;
  width: 20%;
  height: 100%;
  padding-top: 25px;
}

.news-logo p {
  text-align: center;
}

#mission-wrapper {
  background-color: #000;
  width: 100%;
  height: 400px;
  position: relative;
}

#mission-wrapper > img {
  width: 40%;
  position: absolute;
  bottom: -5%;
  right: 5%;
}

.mission-message {
  color: #f2f2f2;
  width: 70%;
  position: absolute;
  top: 20%;
  left: 5%;
  z-index: 10;
}

.mission-title {
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 30px;
}

.mission-description {
  margin-bottom: 30px;
}

.mission-link {
  display: block;
  padding: 5px 10px;
}

#service-wrapper {
  background-color: #f2f2f2;
  width: 100%;
  height: 1100px;
}

#service-wrapper h2 {
  padding-top: 10px;
}

.service1,
.service2 {
  width: 100%;
  height: 40%;
  position: relative;
}

.service1 > img,
.service2 > img {
  width: 50%;
}

.service1 {
  margin-bottom: 100px;
}

.service1 > img {
  position: absolute;
  top: 0;
  right: 0;
}

.service1 .service-card {
  position: absolute;
  top: 15%;
  left: 10%;
  z-index: 10;
}

.service2 .service-card {
  position: absolute;
  top: 15%;
  left: 40%;
}

.service-card {
  background-color: #fff;
  border: 1px solid #000;
  width: 45%;
  height: 200px;
  padding: 50px;
}

.service-card h3 {
  margin-bottom: 20px;
}

.service-card a {
  color: #000;
  border: 1px solid;
  padding: 5px 10px;
  display: inline-block;
  margin-left: 80%;
}

.service-subtitle {
  margin-bottom: 20px;
}

.service-description {
  margin-bottom: 20px;
}

.company-recruit {
  height: 400px;
}

.company-recruit .logo {
  text-align: center;
  margin-top: 110px;
}

.company {
  width: 45%;
  height: 70%;
  background: url(./assets/company.jpeg) no-repeat;
  background-size: cover;
  color: #f2f2f2;
}

.company h2 {
  font-size: 30px;
}

.recruit {
  width: 45%;
  height: 70%;
  background: url(./assets/recruit.jpg) no-repeat;
  background-size: cover;
  color: #f2f2f2;
  margin-left: 132px;
}

.recruit h2 {
  font-size: 30px;
}

#faq-wrapper {
  height: 100px;
  background-color: #000;
  color: #f2f2f2;
}

#faq-wrapper h2 {
  font-size: 35px;
  display: inline-block;
  margin-top: 35px;
  margin-left: 20px;
}

#faq-wrapper p {
  display: inline-block;
  width: 82%;
  text-align: center;
}

#contact-wrapper {
  background: url(./assets/contact-bg.jpg) no-repeat center center;
  background-size: cover;
  color: #f2f2f2;
  text-align: center;
  height: 500px;
}

#contact-wrapper h2 {
  font-size: 30px;
  padding-top: 100px;
  margin-bottom: 20px;
}

#contact-wrapper a {
  color: #f2f2f2;
  border: 1px solid #f2f2f2;
  padding: 10px 20px;
}

.contact-subtitle {
  font-weight: bold;
  margin-bottom: 50px;
}

.contact-message {
  font-size: 40px;
  margin-bottom: 30px;
}

.contact-description {
  margin-bottom: 40px;
}

@media screen and (max-width: 768px) {
  .wrap {
    margin-bottom: 5%;
  }
   #eyecatch > p {
    top: 50%;
    left: 50%;
    width: 80%;
    font-size: 60px;
    text-align: center;
  }
  .news {
    width: 100%;
  }
  #mission-wrapper > img {
    bottom: -10%;
  }
  .mission-message {
    top: 20%;
    left: 15%;
  }
  .mission-description {
    margin-bottom: 20px;
  }
  .mission-link {
    width: 50%;
  }
  #service-wrapper h2 {
    padding-top: 30px;
    font-size: 300%;
  }
  .service1, .service2 {
    width: 80%;
    margin: 0 auto;
  }
  .service1 > img, .service2 > img {
    position: static;
    display: block;
    width: 100%;
  }
  .service2 {
    margin-top: 50px;
  }
  .service-card {
    width: 86%;
    padding: 20px;
    position: static !important;
    border: none;
  }
  .service-card a {
    margin-left: 50%;
  }
  .company-recruit {
    width: 100%;
    margin-bottom: 30px;
  }
  .company-recruit .logo {
    margin-top: 15%;
  }
  .company {
    width: 100%;
    height: 50%;
  }
  .recruit {
    width: 100%;
    margin-left: 0;
    height: 50%;
  }
  #faq-wrapper p {
    width: 40%;
  }
  #contact-wrapper {
    padding-bottom: 10px;
  }
  #contact-wrapper h2 {
    font-size: 40px;
    padding-top: 40px;
  }
  .contact-message, .contact-description {
    width: 80%;
    margin: 0 auto 30px;
  }
  .contact-description {
    line-height: 1.5rem;
  }
}
</style>
