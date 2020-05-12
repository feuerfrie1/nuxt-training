<template>
  <div>
    <footer class="footer page__footer">
      <div class="footer__container">
        <h2 class="footer__title">
          Спасибо всем, кто помог&nbsp;состояться этому&nbsp;проекту
        </h2>
        <ul class="footer__list">
          <li class="footer__list-item">
            <a href class="footer__link">Главная</a>
          </li>
          <li class="footer__list-item">
            <a href class="footer__link">Истории</a>
          </li>
        </ul>
        <div class="footer__container-link">
          <a href class="container__link">Мы в Инстаграме и Youtube</a>
          <p
            href
            class="container__link container__link_another-black"
            @click="popupHandler"
          >
            Поделитесь &#8599;
          </p>
        </div>
      </div>
      <div class="footer__copyright">
        <p class="footer__copyright-text">Рак Лечится 2020</p>
        <p class="footer__copyright-text">
          Сделано студентами Яндекс Практикум
        </p>
      </div>
      <overlay v-if="popupShown" @overlayClick="popupHandler"></overlay>
      <popup v-if="popupShown" @closePopup="popupHandler">
        <h2 class="popup__title">Поделитесь</h2>
        <ul class="popup__list">
          <li>
            <a href class="popup__link">
              <img src="../static/facebook.svg" alt class="popup__link-icon" />
            </a>
          </li>
          <li>
            <a href class="popup__link">
              <img src="../static/twitter.svg" alt class="popup__link-icon" />
            </a>
          </li>
          <li>
            <a href class="popup__link">
              <img src="../static/vk.svg" alt class="popup__link-icon" />
            </a>
          </li>
          <li>
            <a href class="popup__link">
              <img src="../static/ok.svg" alt class="popup__link-icon" />
            </a>
          </li>
          <li>
            <a href class="popup__link">
              <img src="../static/instagram.svg" alt class="popup__link-icon" />
            </a>
          </li>
          <li>
            <a href class="popup__link">
              <img src="../static/youTube.svg" alt class="popup__link-icon" />
            </a>
          </li>
        </ul>
      </popup>
    </footer>
  </div>
</template>

<script>
import PopUp from '@/components/PopUp';
import Overlay from '@/components/ui/Overlay';
export default {
  components: {
    popup: PopUp,
    overlay: Overlay,
  },
  methods: {
    popupHandler() {
      this.popupShown = !this.popupShown;
    },
  },
  data() {
    return {
      popupShown: false,
    };
  },
};
</script>

<style scoped>
.footer {
  min-height: 356px;
  background-color: #fbfbfb;
  color: #000000;
  max-width: 100%;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
}
.page__footer {
  margin: 0;
}
.footer__container {
  margin: 60px 60px 0;
  min-height: 108px;
  display: flex;
  justify-content: space-between;
}
.footer__title {
  max-width: 340px;
}
.footer__container-link {
  display: flex;
  justify-content: space-between;
  flex-direction: column;
}
.footer__list {
  padding: 0;
  list-style: none;
  display: flex;
  justify-content: space-between;
  min-width: 188px;
  margin-right: calc(35%);
}
.footer__list-item {
  max-width: 76px;
}
.footer__link {
  text-decoration: none;
  color: currentColor;
}
.footer__container-link {
  min-width: 300px;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 24px;
}
.container__link {
  text-decoration: none;
  color: currentColor;
}
.container__link_another-black {
  color: #121212;
}
.footer__copyright {
  margin: 0 60px 60px;
  display: flex;
  justify-content: space-between;
  color: #898989;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 18px;
}
.popup__title {
  max-width: 200px;
  margin: 40px auto 0;
  text-align: center;
}
.popup__list {
  list-style: none;
  max-width: 388px;
  display: flex;
  justify-content: space-between;
  margin: 100px auto 100px;
  padding: 0;
}
.popup__link {
}
.popup__link-icon {
}
</style>
