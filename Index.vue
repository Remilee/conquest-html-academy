<template>
  <div class="Index">
    <header>
      <nav>
        <div class="container">
          <div class="nav-wrapper">
            <a class="logo">
              <img class="logo-img" src="src/assets/logo.svg" alt="" width="19px">
              <span class="logo-text">CONQUEST</span></a>
            <ul class="menu">
              <li class="menu-item"><a href="#">Каталог</a></li>
              <li class="menu-item"><a href="#">Акции</a></li>
              <li class="menu-item"><a href="#">Доставка</a></li>
              <li class="menu-item"><a href="#">Контакты</a></li>
            </ul>
            <ul class="section">
              <li class="section-item"><a href="#"><img src="src/assets/search.svg" alt="" width="19px"></a></li>
              <li class="section-item"><a href="#"><img src="src/assets/favorite.svg" alt="" width="25px"></a></li>
              <li class="section-item"><a href="#"><img src="src/assets/basket.svg" alt="" width="19px"></a></li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
    <main>
      <div class="promotion">
        <div class="container">
          <div class="promotion-wrapper">
            <p class="promotion-season">
              Весна/Лето 2019
            </p>
            <p class="promotion-collection">Коллекция
            </p>
            <p class="promotion-description">Швейцарские часы в наличии в Москве
              и с доставкой по всему миру</p>
          </div>
          <button class="promotion-button">СМОТРЕТЬ КАТАЛОГ</button>
        </div>
      </div>
      <div class="bestsellers">
        <div class="container">
          <div class="bestsellers-header">
            <h2 class="section-title">Популярные модели</h2>
            <button class="show-more">Смотреть все</button>
          </div>
          <ul class="catalog-list">
            <li class="catalog-item">
              <span class="catalog-item-title">RADO</span>
              <span class="catalog-item-price">65 300 ₽</span>
              <img class="catalog-item-img" src="src/assets/watch_1.png" width="313px"/>
              <a class="link-details" href="#"><span>Подробнее</span></a>
            </li>
            <li class="catalog-item">
              <span class="catalog-item-title">BVLGARI</span>
              <span class="catalog-item-price">81 700 ₽</span>
              <img class="catalog-item-img" src="src/assets/watch_1.png" width="313px"/>
              <a class="link-details" href="#"><span>Подробнее</span></a>
            </li>
            <li class="catalog-item">
              <span class="catalog-item-title">BVLGARI</span>
              <span class="catalog-item-price">72 700 ₽</span>
              <img class="catalog-item-img" src="src/assets/watch_1.png" width="313px"/>
              <a class="link-details" href="#"><span>Подробнее</span></a>
            </li>
          </ul>
        </div>
      </div>
      <div class="banner">
        <div class="container">
          <div class="banner-wrapper">
            <div class="banner-img-column">
              <img src="src/assets/photo_banner.jpg" width="521px" height="414" alt="Баннер"/>
              <div class="slider">
                <button class="button-back"><span class="icon-back"></span></button>
                <span class="number">01</span>
                <button class="button-forward"><span class="icon-forward"></span></button>
              </div>
            </div>
            <div class="banner-text-column">
              <h2 class="section-title">Подлинное качество</h2>
              <span class="caption">Все часы производятся в Швейцарии и имеют сертификаты качества. Настоящие швейцарские часы — это предмет гордости и престижа.</span>
              <button class="show-catalog">СМОТРЕТЬ КАТАЛОГ</button>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: 'Index',
  props: {
    msg: String
  }
}
</script>

<style scoped lang="sass">
@mixin fontPlayfair
  font-family: "PlayfairDisplay", "Arial", sans-serif

@mixin fontPrata
  font-family: "Prata", "Arial", sans-serif

.container
  width: 1170px
  margin: 0 auto
  padding: 0 15px
header
  nav
    .container
      .nav-wrapper
        display: flex
        flex-direction: row
        justify-content: space-between
        align-items: center

        .logo
          display: flex
          align-content: center

          .logo-img
            margin-right: 8px

          .logo-text
            @include fontPlayfair
            font-size: 12pt
            letter-spacing: 0.2em

        .menu
          display: flex
          justify-content: space-between
          width: 26.3em

          .menu-item
            font-size: 14pt
            cursor: pointer

            a
              color: #555248
              text-decoration: none

              &:hover
                color: #ac9b0d

        .section
          display: flex
          justify-content: space-between
          width: 6.1em

          .section-item
            cursor: pointer

            a
              &:hover
                border-bottom: #ac9b0d

main
  .promotion
    height: 828px
    display: flex
    justify-content: center
    flex-direction: column

    .container
      .promotion-wrapper
        color: #1B1A17

        .promotion-season
          font-size: 45pt
          @include fontPlayfair
          margin-bottom: 8.5px

        .promotion-collection
          font-size: 30pt
          margin-bottom: 9px
          margin-top: 0
          @include fontPlayfair

        .promotion-description
          width: 19em
          font-size: 14px
          font-weight: 400
          line-height: 1.5
          margin-bottom: 40px

      .promotion-button
        width: 250px
        height: 64px
        font-weight: 500
        font-size: 12pt
        letter-spacing: 5%
        color: white
        background-color: #444240

  .bestsellers
    margin-bottom: 175px

    .container
      .bestsellers-header
        display: flex
        justify-content: center

        .section-title
          margin-left: auto

        .show-more
          align-self: flex-end
          margin-left: auto
          text-decoration: underline
          background-color: #fff
          border: none
          border-bottom: 1px solid #C4C0B6

      .catalog-list
        display: flex
        justify-content: flex-start
        flex-wrap: wrap

        .catalog-item
          display: flex
          flex-direction: column

          &-title
            @include fontPlayfair
            font-size: 14px
            letter-spacing: 0.3em
            margin-bottom: 10px

          &-price
            @include fontPlayfair
            font-size: 12px

          &-img
            margin-bottom: 19px

          .link-details
            color: #1B1A17
            font-size: 16px
            margin-left: 50px

  .banner
    .container
      .banner-wrapper
        display: flex

        .banner-img-column
          width: 600px

          .slider
            .button-back
              .icon-back
                background: url("src/assets/arrow_left.svg")
                width: 15px

              .icon-forward
                background: url("src/assets/arrow_right.svg")

        .banner-text-column
          width: 570px

          .section-title
            @include fontPlayfair
            font-size: 32px
            margin-bottom: 38px
            font-weight: 400
            line-height: 37px

          .caption
            font-size: 16px
            line-height: 150%
            margin-bottom: 45px
            display: block

          .show-catalog
            padding: 26px 38px
            background-color: #D4B098
            color: #fff
            border: none
            font-weight: 500
            font-size: 12px
            &:hover
              background-color: #ee7c2c


a
  text-decoration: none

ul
  list-style: none
</style>
