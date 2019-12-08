<template>
  <div class="card-expansion">
    <md-card>
      <md-card-media>
        <img :src="fixture.picture" alt="People" />
      </md-card-media>

      <md-card-header>
        <div class="md-title">{{fixture.title}}</div>
        <div class="md-subhead">{{fixture.time}}</div>
      </md-card-header>

      <md-card-expand>
        <md-card-actions md-alignment="space-between">
          <div>
            <md-button class="md-primary">{{fixture.team_A}}</md-button>Vs
            <md-button class="md-primary">{{fixture.team_B}}</md-button>
          </div>
          <md-card-expand-trigger>
            <md-button class="md-icon-button">
              <md-icon>keyboard_arrow_down</md-icon>
            </md-button>
          </md-card-expand-trigger>
        </md-card-actions>

        <md-card-expand-content>
          <md-card-content>Two Teams are both strong. But i want to suggest for u to bet {{fixture.suggest_team.toUpperCase()}}</md-card-content>
          <md-card-actions>
            <p class="caption">Bet one team</p>
          </md-card-actions>
        </md-card-expand-content>
      </md-card-expand>
    </md-card>
  </div>
</template>

<script>
export default {
  name: "Fixture",
  props: {
    fixture: {
      type: Object
    }
  },
  data() {
    return {
      image: require("@/assets/img/premier.jpg")
    };
    result:''
  },
  
};
</script>

<style lang="scss" scoped>
img {
  height: 185px !important;
}

.card-expansion {
  height: 480px;
}

.md-card {
  width: 300px;
  margin: 5px;
  display: inline-block;
  vertical-align: top;
}
.md-button {
  width: 50px;
  text-align: center;
  color: yellow;
}

.md-layout-item {
  height: 40px;

  &:after {
    width: 100%;
    height: 100%;
    display: block;
    background: md-get-palette-color(red, 200);
    content: " ";
  }
}
</style>