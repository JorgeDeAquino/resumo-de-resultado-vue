<template>
  <div class="result_container">
    <p>
      Your Result
    </p>
    <div class="result_note_number">
      <h2>{{ media }}</h2>
      <p>of 100</p>
    </div>
    <div class="result_text">
      <h2>Great</h2>
      <p>You scored higher than 65% of the people who have taken these test.</p>
    </div>
  </div>
</template>

<script>
import data from '../../json/data.json';
export default {
  name: 'YorResult',
  data() {
    return {
      scores: [],
      media: null,
    }
  },
  created() {
    this.scores = data.map(item => parseInt(item.score));
  },
  mounted() {
    this.calculaMedia();
  },
  methods: {
    calculaMedia() {
      let media = 0;
      for (let i = 0; i < this.scores.length; i++) {
        media += this.scores[i];
      }
      this.media = Math.round(media / this.scores.length);
    }
  }
}
</script>

<style scoped src="./Result.scss" lang="scss"></style>
