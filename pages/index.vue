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
      <!-- Product card -->
      <flip-panel  class="flip-panel" shadow :width="productCardWidth">
        <template slot="front">
          <div class="front">
            <img src="~/assets/book.jpg" width="100%" height="100%"/>
          </div>
        </template>
        <template slot="back">
          <p>
            Fotography: Fons Peels <br/>
            Language: English <br/>
            ISBN: 9789050114806 <br/>
            Number of pages: 384 <br/>
            Dimensions: 21 x 29 cm <br/>
            Full colour, hardcover
          </p>
          <p>
            Published by KNNV Uitgeverij, november 2014
          </p>
          <p>
            This is the first detailed and complete overview of the distribution of the dragonflies and 
            damselflies of Europe.
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
      backColor: '#ecf0f1',
      height: '250px',
      productCardWidth: '275px',
      productCardHeight: '380px'
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

    justify-content: space-evenly;
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
