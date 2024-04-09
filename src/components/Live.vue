<template>
  <div class="live">
    <p class = "desc">
      Silakan nyalakan suara animasi di atas!
    </p>
    <img src="~@/assets/images/hands.png" class="hands" />
    <div>
      <p class = "header">
        "Haruskah kita berpegangan tangan?"<br />
      </p>
      <p>
        Kami telah menjalani hidup kami sepenuhnya,<br />
        Sekarang kita akan berjalan berdampingan berpegangan tangan.<br />
        Dengan seseorang yang mengatakan aku mencintaimu<br />
        Saya akan melakukan yang terbaik untuk bahagia untuk waktu yang lama.<br />
        Berita pernikahan yang tenang tapi menyenangkan<br />
        Inilah yang kami ingin Anda ketahui.
      </p>
      <p class = "header">
        Sabtu, 27 Juli 2024<br />
        09:00 WIB<br />
      </p>
      <p>
        Ini makan keluarga kecil, jadi aku bisa melihat wajahmu dan <br />
        Meskipun kami tidak dapat berbagi rasa terima kasih dan ucapan selamat kami secara langsung,<br />
        Sebaliknya, seluruh dunia dapat berpartisipasi<br />
        Saya ingin bergabung dengan Anda di YouTube Live.<br />
        Sehingga Anda merasa bersama kami<br />
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
