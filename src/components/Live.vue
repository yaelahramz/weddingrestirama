<template>
  <div class="live">
    <p class = "desc">
      Silakan nyalakan suara animasi di atas!
    </p>
    <img src="~@/assets/images/hands.png" class="hands" />
    <div>
      <p class = "header">
        Kami yang Berbahagia,<br />
      </p>
      <p :style="{ fontWeight: 'bold' }">Resti Kurniawati<br /></p>
      <p>Putri kedua dari Bapak Satam & Ibu Jubaedah</p><br />
    <img src="~@/assets/images/love.png" class="hands" />
      <p :style="{ fontWeight: 'bold' }">M Rizky Ramadhan<br /></p>
      <p>Putra kedua dari Bapak M Idris & Ibu Tati</p>
      <p>
        وَمِنْ اٰيٰتِهٖٓ اَنْ خَلَقَ لَكُمْ مِّنْ اَنْفُسِكُمْ<br /> اَزْوَاجًا لِّتَسْكُنُوْٓا اِلَيْهَا وَجَعَلَ بَيْنَكُمْ<br /> مَّوَدَّةً وَّرَحْمَةًۗ اِنَّ فِيْ ذٰلِكَ لَاٰيٰتٍ لِّقَوْمٍ يَّتَفَكَّرُوْنَ ۝٢١ <br/> QS Ar Rum 21
      </p>
      <p>
        Di antara tanda-tanda (kebesaran)-Nya ialah bahwa<br />
        Dia menciptakan pasangan-pasangan untukmu dari (jenis) dirimu sendiri<br />
        agar kamu merasa tenteram kepadanya. Dia menjadikan di antaramu <br />
        rasa cinta dan kasih sayang. Sesungguhnya pada yang demikian itu<br />
         benar-benar terdapat tanda-tanda (kebesaran Allah) bagi kaum yang berpikir.<br />
      </p>
      <p class = "header">
        Sabtu, 27 Juli 2024<br />
        09:00 WIB<br />
        Taman Wanasari Indah<br/>
        Blok B2 No.5 RT.009 RW.008<br/>
        Cibitung, Bekasi
      </p>
      <p>"<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d247.88736584041757!2d107.0981701722262!3d-6.237632739527339!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e698f62e0231a89%3A0x3d76d6b587b6cb34!2sJl.%20Taman%20Wanasari%20Indah%20No.2%2C%20Wanasari%2C%20Kec.%20Cibitung%2C%20Kabupaten%20Bekasi%2C%20Jawa%20Barat%2017520%2C%20Indonesia!5e0!3m2!1sid!2sjp!4v1712755017086!5m2!1sid!2sjp" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>"</p>
      <p>
        Hadiri secara online dan rayakan melalui obrolan.
      </p>

    </div>
    <Button @click="attendance">Saksikan</Button>
  </div>
</template>

<script>
export default {
  name: "Divider",
  methods: {
    attendance() {
      window.open("https://youtu.be/yaelahramz");
    },
  },
};
</script>

<style lang="scss" scoped>
.live {
  padding-top: 4px;
  padding-bottom: 68px;
  padding-left: $padding-vertical;
  padding-right: $padding-vertical;
  text-align: center;
  .hands {
    width: 75px;
    margin-bottom: 16px;
  }
  p {
    margin-bottom: 16px;
    line-height: 24px;
    &.desc {
      color: #295238;
      font-size: 10px;
      opacity: 0.6;
      margin-bottom: 36px;
    }
    &.header {
      color: #295238;
    }
    &:last-child {
      margin-bottom: 40px;
    }
  }
}
</style>
