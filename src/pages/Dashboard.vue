<template>
  <div>
    <div class="content" >
      <div class="md-collapse">
          <div class="md-autocomplete">

            <md-autocomplete class="search" v-model="selected_league" type="text"
              :md-options="employees">
              <label>Search...</label>
            </md-autocomplete>
           
          </div>          
      </div>
      <div class="md-layout">
        <div class="md-layout md-gutter">
          <div class="md-layout-item" v-for="(item, index) in searchLeague" :key="index" >
            <fixture :fixture="item" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Fixture from "../components/UiComponent/Fixture.vue";

export default {
  name: "Dashboard",
  components: {
    Fixture
  },
 
  data() {
    return {
      fixtures: [
        {
          title: 'London Derby',
          time: '3:30 AM',
          team_A: 'chelsea',
          team_B: 'man u',
          suggest_team: 'chelsea',
          picture: require('../assets/img/premier.jpg'),
          card:'premier',
        },
        {
          title: 'Laliga',
          time: '3:30 AM',
          team_A: 'Madrid',
          team_B: 'Barca',
          suggest_team: 'Madrid',
          picture: require('../assets/img/laliga.jpg'),
          card:'laliga',
        },
        {
          title: 'Bundesliga',
          time: '4:30 AM',
          team_A: 'Dort',
          team_B: 'Schalke',
          suggest_team: 'Dort',
          picture: require('../assets/img/Bundesliga.jpg'),
          card: 'bundesliga',
        },
      ],
      selected_league: ''
    }
  },
 computed: {
  searchLeague:function() {
      return this.fixtures.filter(fixture =>{
        return  fixture.card.match(this.selected_league)
      }
      )
      
    }
 },
 
};
</script>
<style>
.md-content {
  width: 200px;
  height: 200px;
  display: inline-flex;
  justify-content: center;
  align-items: center;
}
</style>
