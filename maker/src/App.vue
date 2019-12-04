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
        />
      </div>
      <div>
        <Result
        :shape='shape'
        :color='color'
        :fill='fill'
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
    };
  },
  methods: {
    square() {
      this.shape = '0'
    },
    littleCurve() {
      this.shape = '10'
    },
    curve() {
      this.shape = '15'
    }
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
