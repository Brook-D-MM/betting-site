<template>
  <md-card class="md-card-profile">
    <div class="md-card-avatar">
      <img class="img" :src="cardUserImage" />
    </div>

    <md-card-content>
      <h6 class="category text-gray">Founder Of Betting Site</h6>
      <h4 class="card-title">Aung Min Khant Oo</h4>
      <p class="card-description">
       Sometimes, we need to relax and chill in our social life. Then, why don't watch football match?
       It is somekind of relaxation and if u want chill more!!! Bet the football matches in my site!!!
       Good luck Have Fun all   
      </p>
      <md-button class="md-round md-success">Follow</md-button>
    </md-card-content>
  </md-card>
</template>
<script>
export default {
  name: "user-card",
  props: {
    cardUserImage: {
      type: String,
      default: require("@/assets/img/amko1.jpeg")
    }
  },
  data() {
    return {};
  }
};
</script>
<style></style>
