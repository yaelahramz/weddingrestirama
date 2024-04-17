<template>
  <div class="funding">
    <img src="~@/assets/images/flower.png" class="flower" />
    <h2 class="h2">
      둘째, 기부를 통해 뜻깊은 날로 만들기
    </h2>
    <p>
      인생에서 가장 행복한 날,<br />
      이 크나큰 행복을 나누면 어떨까 생각했습니다.<br />
      저희가 부자는 아니지만 마음만은 부자니까!<br />
      저희보다 더 필요로 하는 분들에게<br />
      작은 도움을 드리고 싶었습니다.<br />
      저희를 축하해주고 싶은 그 마음을<br />
      장기화된 코로나로 인해<br />
      끼니를 해결하지 못하는 아이들에게<br />
      따뜻한 한 끼로 나누어주세요.<br />
      감사한 마음 잘 모아서 전하고<br />
      나누어주신 만큼 더욱 행복하게 살겠습니다.<br />
    </p>
    <Button @click="funding">기부금 전달하기</Button>

    <a
      href="https://www.kfhi.or.kr/apps/campaign/2020_stophunger_domestic_2.asp?id=540&mcode=658&utm_medium=display_ad&utm_source=youtube&utm_campaign=2020_stophunger_domestic_2&gclid=Cj0KCQiA5bz-BRD-ARIsABjT4nieWe1teUo7KT5HSTinY-IG9KFVj7BRfzI7I_YYAqapQ4jQFsqEqYIaAvqqEALw_wcB"
      target="_blank"
      class="link"
      >기부처 확인하기</a
    >
  </div>
</template>

<script>
export default {
  name: "Divider",
  methods: {
    funding() {
      window.open("https://qr.kakaopay.com/281006011189386490008935");
    },
  },
};
</script>

<script setup>
import { reactive } from 'vue'

const formData = reactive({
  name: '',
  email: '',
  message: '',
  response: ''
})

const encode = data => {
  return Object.keys(data)
    .map(key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`)
    .join('&')
}

const submitForm = () => {
  fetch('/', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: encode({
      'form-name': 'feedback',
      ...formData
    })
  })
    .then(() => {
      formData.response = '✅ Your response was successfully submitted!'
    })
    .catch(error => {
      formData.response = `❌ There was an error submitting your response: ${error.message}. Please refresh to try again.`
    })
}
</script>

<template>
  <h1>Vue 3 + Netlify Forms</h1>

  <section v-if="formData.response" class="notification">
    <h2>{{ formData.response }}</h2>
  </section>
  <form v-else class="feedback-form" name="feedback" @submit.prevent>
    <input type="hidden" name="form-name" value="feedback" />

    <div class="input-wrapper">
      <label for="name">Name</label>
      <input
        id="name"
        v-model="formData.name"
        type="text"
        placeholder="Your Name"
      />
    </div>

    <div class="input-wrapper">
      <label for="email">Email</label>
      <input
        id="email"
        v-model="formData.email"
        type="email"
        placeholder="yourname@domain.extension"
      />
    </div>

    <div class="input-wrapper">
      <label for="message">Message</label>
      <textarea
        id="message"
        v-model="formData.message"
        placeholder="What would you like to share?"
      />
    </div>

    <button type="submit" @click="submitForm">Submit</button>
  </form>
</template>

<style scoped>
.feedback-form {
  max-width: 600px;
  margin: 0 auto;
}

.input-wrapper {
  display: grid;
  grid-template-rows: auto 1fr;
  grid-row-gap: 5px;
  margin-bottom: 1rem;
  text-align: left;
}

.input-wrapper:last-child {
  margin-bottom: 0;
}

.input-wrapper input,
.input-wrapper textarea {
  font-family: var(--primaryFont);
}

.input-wrapper input {
  padding: 10px;
  font-size: 0.9rem;
}

.input-wrapper textarea {
  height: 100px;
  padding: 10px;
  font-size: 0.9rem;
}

.notification {
  border: 1px solid #222;
  border-radius: 8px;
  padding: 20px 0;
  max-width: 600px;
  margin: 0 auto;
}
</style>

<style lang="scss" scoped>
.funding {
  padding-top: 48px;
  padding-bottom: 72px;
  padding-left: $padding-vertical;
  padding-right: $padding-vertical;
  text-align: center;

  .flower {
    width: 70px;
    margin-bottom: 26px;
  }
  .h2 {
    font-size: 16px;
    font-weight: normal;
    margin-bottom: 24px;
    color: #295138;
  }
  p {
    margin-bottom: 32px;
    line-height: 24px;
    color: #202121;
  }
  .link {
    display: inline-block;
    margin-top: 24px;
    color: #295238;
  }
}
</style>
