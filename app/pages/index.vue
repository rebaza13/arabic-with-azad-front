<template>
  <div class="hero">
   <div class="hero__image-container">
        <div class="hero__img">
          <img :src="photo" alt="">
        </div>
        <div class="hero__img-circle1"></div>
        <div class="hero__img-circle2"></div>
      </div>
    <div class="hero__content">
      <h1 class="hero__title">فێربوونی <span class="hero__title--highlight">زمان</span></h1>
      <p class="hero__subtitle">پلاتفۆرمێک بۆ فێربونی عەرەبی</p>
      <div class="hero__description">ڕێگایەک بۆ باشترکردنی زمانەوانی عربی لەڕێگەی چەند بژاردەیەکی دیاریکراو ئاست بەرز.</div>
      <button class="hero__button">دەستپێکردن
        <img :src="arrow" class="hero__button-arrow-left"></img>
        <img :src="arrow" class="hero__button-arrow-right"></img>
      </button>
      
    </div>

     
  </div>
</template>

<script setup lang="ts">
import arrow  from '~/assets/images/left-arrow.png'
import photo from '~/assets/images/photo.jpg'
</script>