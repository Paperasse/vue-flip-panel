<template>
    <div class="container">
      <!-- Default settings -->
      <flip-panel class="flip-panel">
        <template slot="front">
          <h3>Default settings</h3>
          <p>
            Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, ...
          </p>
        </template>
        <template slot="back">
          <h3>Back</h3>
          <p>
            Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur
          </p>
        </template>
      </flip-panel>
      <!-- Shadow, no border -->
      <flip-panel  class="flip-panel" :frontColor="frontColor" shadow :border="false">
        <template slot="front">
          <h3>Front</h3>
          <p>
            Properties set for "shadow", "no border", background color of front
          </p>
        </template>
        <template slot="back">
          <h3>Back</h3>
          <p>
            Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur
          </p>
        </template>
      </flip-panel>
    </div>
</template>

<script>
import FlipPanel from '~/components/FlipPanel.vue'

export default {
  components: {
    FlipPanel
  },
  data() {
    return {
      frontColor: '#fdcb6e',
      shadow: true,
      height: '250px',
      flipText: 'Meer..'
    }
  },
}
</script>

<style scoped>
  .container {
    padding: 0;
    margin: 20;
    padding-top: 20px;
    list-style: none;
  
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
  
    -webkit-flex-flow: row wrap;
    flex-flow: row wrap;
    -ms-flex-flow: row wrap;
  }

  .flip-panel {
    margin-left: 20px;
  }
  p, h3 {
    padding: 10px;
  }

  p {
    font-size: .9rem;
  }
</style>
