<template>
  <div class="about">
    <h2 class="about__title">#РАКЛЕЧИТСЯ</h2>
    <p class="about__subtitle">О проекте</p>
    <div class="about__container">
      <p class="about__founder">
        Этот проект был создан благотворительным&nbsp;фондом
        Константина&nbsp;Хабенского.
      </p>
      <div class="about__description">
        <div class="about__switch">
          <p class="about__cancer" @click="showCancer">Рак Лечится</p>
          <p class="about__story" @click="showStory">Фонд&nbsp;Хабенского</p>
        </div>
        <div class="about__texts">
          <p class="about__text" v-if="cancerShown">
            Есть вещи, которые не лечатся. Особенности характера, страстные
            увлечения, привычки, ставшие частью нашего «я», фобии, которые мы
            приобрели в детстве. Список можно продолжать до бесконечности, но
            одна болезнь в него точно не войдет. Эта болезнь — рак. Рак лечится,
            и лучшее доказательство — люди с их неизлечимыми особенностями,
            которые сумели победить рак.
          </p>
          <p class="about__text" v-if="cancerShown">
            Рак лечится — проект Благотворительного Фонда Константина Хабенского
            и Leo Burnett Moscow. С его помощью мы надеемся изменить отношение
            людей к раку и заставить каждого поверить: онкологическое
            заболевание — это не приговор.
          </p>
          <p class="about__fond" v-if="storyShown">
            Благотворительный Фонд Константина Хабенского с 2008 года помогает
            детям с онкологическими и другими тяжелыми заболеваниями головного
            мозга. Фонд не только поддерживает семью заболевшего ребенка в самый
            сложный момент, оплачивая обследования, лечение и медицинские
            препараты, но и в целом меняет систему оказания помощи детям с
            опухолями мозга в России.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    showCancer() {
      this.cancerShown = true;
      this.storyShown = false;
    },
    showStory() {
      this.cancerShown = false;
      this.storyShown = true;
    },
  },
  data() {
    return {
      cancerShown: '',
      storyShown: '',
    };
  },
};
</script>

<style scoped>
.about {
  background-color: #613a93;
  color: #ffffff;
  padding: 60px;
  box-sizing: border-box;
  min-height: 650px;
}
.about__title {
  margin: 0 auto 0;
  max-width: 720px;
  text-align: center;
  font-style: normal;
  font-weight: 800;
  font-size: 64px;
  line-height: 77px;
}
.about__subtitle {
  margin: 70px 0 0;

  font-style: normal;
  font-weight: 600;
  font-size: 32px;
  line-height: 36px;
}
.about__container {
  margin: 32px 0;
  display: flex;
  justify-content: space-between;

  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 22px;
}
.about__founder {
  max-width: 340px;
  color: #dedede;
}
.about__description {
  flex-basis: 830px;
  display: flex;
  justify-content: space-between;
}
.about__switch {
  max-width: 154px;
  display: flex;
  flex-direction: column;
}
.about__cancer {
  text-align: right;
  margin-bottom: 10px;
}
.about__story {
  color: #dedede;
}
.about__texts {
  display: flex;
  flex-direction: column;
  max-width: 640px;
}
.about__text {
  margin: 0 0 20px;
  color: #dedede;
}
/* .about__fond {
  display: none;
} */
</style>
