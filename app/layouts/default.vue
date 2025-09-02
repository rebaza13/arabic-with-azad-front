<template>

  <div>
    <header class="header">
      <div id="menuToggle">
        <!--
    A fake / hidden checkbox is used as click reciever,
    so you can use the :checked selector on it.
    -->
        <input type="checkbox" id="menuCheckbox" />

        <!--
    Some spans to act as a hamburger.
    
    They are acting like a real hamburger,
    not that McDonalds stuff.
    -->
        <span></span>
        <span></span>
        <span></span>

        <!--
    Too bad the menu has to be inside of the button
    but hey, it's pure CSS magic.
    -->
        <ul id="menu">
          <!-- 
      We can use a label here to close upon click (when doing same page navigation), this
      does require a slight bit of JS.
      -->
          <li>
            <a href="#">
              <label for="menuCheckbox" onclick="this.parentNode.click();">سەرەکی</label>
            </a>
          </li>
          <li>
            <a href="#about">
              <label for="menuCheckbox" onclick="this.parentNode.click();">دەربارە</label>
            </a>
          </li>

          <!-- These just close the menu -->
          <li><label for="menuCheckbox"><a>زانیاری</a></label></li>
          <li><label for="menuCheckbox"><a>پەیوەندی</a></label></li>

         
        </ul>
      </div>
      <div class="header__logo">
        عەرەبی لەگەڵ <span class="header__logo-hilighted">ئازاد</span>
      </div>
      <div class="header__menu">
        <ul class="header__list">
          <li class="header__item">
            <a href="/" class="header__link">سەرەکی</a>
          </li>
          <li class="header__item">
            <a href="/" class="header__link">وانەکان</a>
          </li>
          <li class="header__item">
            <a href="/" class="header__link">ماددەکان</a>
          </li>
          <li class="header__item">
            <a href="/" class="header__link">تاقیکردنەوی ئاست</a>
          </li>

        </ul>
      </div>
      <div class="header__buttons">
        <button class="header__button">
          <a href="/" class="header__link">خۆتۆمارکردن</a>
        </button>
        <button class="header__button">
          <a href="/" class="header__link">داخڵ بوون</a>
        </button>

      </div>
    </header>
    <slot />
  </div>


</template>