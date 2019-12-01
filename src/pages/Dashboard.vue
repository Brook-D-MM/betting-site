<template>
  <div class="content">
    <div class="md-layout">
     
    <md-content class="md-primary">Primary</md-content>
    <p><h1>Vs</h1></p>
    <md-content class="md-accent">Accent</md-content>
    </div>
  <div class="card-expansion">
    <md-card>
      <md-card-media>
        <img src="../assets/img/premier.jpg" alt="People">
      </md-card-media>

      <md-card-header>
        <div class="md-title">Title goes here</div>
        <div class="md-subhead">Subtitle here</div>
      </md-card-header>

      <md-card-expand>
        <md-card-actions md-alignment="space-between">
          <div>
            <md-button>Action</md-button>
            <md-button>Action</md-button>
          </div>

          <md-card-expand-trigger>
            <md-button class="md-icon-button">
              <md-icon>keyboard_arrow_down</md-icon>
            </md-button>
          </md-card-expand-trigger>
        </md-card-actions>

        <md-card-expand-content>
          <md-card-content>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio itaque ea, nostrum odio. Dolores, sed accusantium quasi non, voluptas eius illo quas, saepe voluptate pariatur in deleniti minus sint. Excepturi.
          </md-card-content>
        </md-card-expand-content>
      </md-card-expand>
    </md-card>
    

</template>

<script>
import {
  
} from "@/components";

export default {
  name: 'PaperContent',
  name: 'CardExpansion'
  
   
 
};
</script>
<style lang="scss" scoped>
  .md-content {
    width: 200px;
    height: 200px;
    display: inline-flex;
    justify-content: center;
    align-items: center;
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
</style>
