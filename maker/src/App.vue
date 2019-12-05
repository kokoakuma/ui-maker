<template>
  <div id="app">
    <div class="headerContainer">
      <Header/>
    </div>
    <div class="mainContainer">
      <div>
        <Select
        @square='square'
        @littleCurve='littleCurve'
        @curve='curve'
        @black='black'
        @red='red'
        @green='green'
        @blue='blue'
        @yellow='yellow'
        @navy='navy'
        @fontBlack='fontBlack'
        @fontWhite='fontWhite'
        @doFill='doFill'
        @notFill='notFill'
        />
      </div>
      <div>
        <Result
        :shape='shape'
        :color='color'
        :fill='fill'
        :fontColorWhite='fontColorWhite'
        />
      </div>
    </div>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Select from './components/Select.vue'
import Result from './components/Result.vue'

export default {
  name: 'app',
  components: {
    Header,
    Select,
    Result,
  },
  data: function() {
    return {
    shape:"",
    color:"",
    fill:false,
    fontColorWhite:false,
    };
  },
  methods: {
    square() { this.shape = '0' },
    littleCurve() { this.shape = '10' },
    curve() { this.shape = '15' },
    black() { this.color = 'black'},
    red() { this.color = '#e74c3c'},
    green() { this.color = '#2ecc71'},
    blue() { this.color = '#3498db'},
    yellow() { this.color = '#f1c40f'},
    navy() { this.color = '#2c3e50'},
    fontBlack() { this.fontColorWhite = false},
    fontWhite() { this.fontColorWhite = true},
    doFill() { this.fill = true},
    notFill() { this.fill = false},
    },
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}

#app {
  top: 0;
  margin: 0px;
  width: 100%;
  padding: 0;
}

.headerContainer{
  margin: 0;
  padding:0;
}

.mainContainer{
  width: 700px;
  margin: auto;
  display: flex;
  margin-top: 15px;

}

.mainContainer div{
  width: 50%;
}
</style>
