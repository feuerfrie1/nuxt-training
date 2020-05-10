<template>
  <div class="statistics__container">
    <div class="facts__card">
      <h3 class="facts__description">
        Каждый 3-й в&nbsp;стране уверен, что рак неизлечим. А&nbsp;это примерно
        48&nbsp;918&nbsp;000&nbsp;человек.
      </h3>
      <progress-bar />
      <h2 class="facts__digit">1 из 3</h2>
      <h3 class="facts__description facts__description-grey">
        Левада-Центр 2018
      </h3>
    </div>

    <div class="facts__card">
      <h3 class="facts__description">
        2,6% Россиян имеют онкозаболевания.
      </h3>
      <progress-bar />
      <h2 class="facts__digit">1 из 3</h2>
      <h3 class="facts__description facts__description-grey">
        Росстат 2018
      </h3>
    </div>

    <div class="facts__card">
      <h3 class="facts__description">
        На&nbsp;28% выросла доля выявления заболеваний на&nbsp;ранней стадии
        за&nbsp;10&nbsp;лет.
      </h3>
      <progress-bar />
      <h2 class="facts__digit">1 из 3</h2>
      <h3 class="facts__description facts__description-grey">
        МНИОИ Герцена 2018
      </h3>
    </div>

    <div class="facts__card">
      <h3 class="facts__description">
        На&nbsp;25% снизилась смертность в&nbsp;течение первого года после
        постановки диагноза.
      </h3>
      <progress-bar />
      <h2 class="facts__digit">1 из 3</h2>
      <h3 class="facts__description facts__description-grey">
        МНИОИ Герцена 2018
      </h3>
    </div>
  </div>
</template>

<script>
import ProgressBar from '@/components/ui/ProgressBar';

export default {
  components: {
    'progress-bar': ProgressBar,
  },
};
</script>

<style scoped>
.statistics__container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  max-width: 1200px;
  margin: 0 auto;
}
.facts__card {
  width: 265px;
  height: 265px;
  border: 1px solid #efefef;
  box-sizing: border-box;
  padding: 18px 18px;
}
.facts__description {
  width: 229px;
  color: #000000;
  font-weight: normal;
  font-size: 12px;
  line-height: 16px;
  margin-bottom: 56px;
  display: flex;
  justify-content: flex-end;
}
.facts__description:last-child {
  margin-top: 10px;
}
.facts__description-grey {
  color: #666666;
}
.facts__digit {
  font-weight: 600;
  font-size: 38px;
  line-height: 40px;
  color: #000000;
  margin-top: 20px;
  display: flex;
  justify-content: flex-end;
}
</style>
