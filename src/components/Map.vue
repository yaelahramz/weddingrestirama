<template>
  <div class="map">
    <div></div>
    <div class="map-container" ref="gal">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d247.88736584041757!2d107.0981701722262!3d-6.237632739527339!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e698f62e0231a89%3A0x3d76d6b587b6cb34!2sJl.%20Taman%20Wanasari%20Indah%20No.2%2C%20Wanasari%2C%20Kec.%20Cibitung%2C%20Kabupaten%20Bekasi%2C%20Jawa%20Barat%2017520%2C%20Indonesia!5e0!3m2!1sid!2sjp!4v1712755017086!5m2!1sid!2sjp" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
    <div class="cover">
      <div class="navi-apps">
        <a v-bind:href="tmapUrl">
          <div class="ico_comm ico_tmap"><img src="~@/assets/images/icons/tmap.png"/></div>
          <div class="link">T맵</div>
        </a>
      </div>
      <div class="navi-apps">
        <a v-bind:href="kakaoTaxiUrl">
          <div class="ico_comm ico_taxi"><img src="~@/assets/images/icons/kakaot.png"/></div>
          <div class="link">카카오택시</div>
        </a>
      </div>
      <div class="navi-apps">
        <a v-bind:href="navermapUrl">
          <div class="ico_comm ico_navermap"><img src="~@/assets/images/icons/navermap.png"/></div>
          <div class="link">네이버맵</div>
        </a>
      </div>
      <div class="navi-apps">
        <a v-bind:href="kakaomapUrl">
          <div class="ico_comm ico_kakaomap"><img src="~@/assets/images/icons/kakaomap.png"/></div>
          <div class="link">카카오맵</div>
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.map {
  margin-top: 18px;
  margin-bottom: 18px;
}

.navi-apps {
  align-content: center;
  position: relative;

  .ico_comm img {
    vertical-align: middle;
    width: 40px
  }

  div {
    text-align: center;
    padding-top: 10px;
  }

  a{
    text-decoration: none;
  }
}

.cover {
  display: flex;
  justify-content: space-between;
  margin: 22px 10% 22px 10%;
}

.link {
  color: #295238;
}

</style>
