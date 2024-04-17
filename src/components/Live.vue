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
        Di antara tanda-tanda (kebesaran)-Nya ialah bahwa
        Dia menciptakan pasangan-pasangan untukmu dari (jenis) dirimu sendiri
        agar kamu merasa tenteram kepadanya. Dia menjadikan di antaramu
        rasa cinta dan kasih sayang. Sesungguhnya pada yang demikian itu
         benar-benar terdapat tanda-tanda (kebesaran Allah) bagi kaum yang berpikir.
      </p>
      <p class = "header">
        Sabtu, 27 Juli 2024<br />
        09:00 WIB<br />
        Taman Wanasari Indah<br/>
        Blok B2 No.5 RT.009 RW.008<br/>
        Cibitung, Bekasi
      </p>
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
