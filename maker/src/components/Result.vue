<template>
    <div class="root">
      <div class="resultContainer">
        <button
        :class="[{white: fontColorWhite},{fillColor: fill}]"
        :style="styles">ボタン
        </button>
      </div>
      <div class="cssCodeContainer">
          <div class="cssCode">
              <p>border-style: solid</p>
              <p>border-width: 1px</p>
              <p>border-color: {{ color }};</p>
              <p>border-radius: {{ shape }}px;</p>
              <template v-if="fontColorWhite">
                <p>color: white;</p>
              </template>
              <template v-if="!fontColorWhite">
                <p>color: black;</p>
              </template>
              <template v-if="fill">
                <p>background-color: {{ color }};</p>
              </template>
          </div>
      </div>
    </div>
</template>

<script>
export default {
  name: "Result",
  props:{
    shape: {
      type: String,
      default: "10",
    },
    color:{
      type: String,
      dafault: "",
    },
    fill: {
      type: Boolean,
      dafault: "",
    },
    fontColorWhite: {
        type: Boolean,
        default: false,
    }
  },
  methods: {
    // バインドするスタイルを生成
  },
  computed: {
      styles () {
      return {
        '--shape': this.shape + "px",
        '--color': this.color,
      }
    }
  }

}
</script>
<style lang="css" scoped>

.root{
    width: 100%;
    height: 100%;
}
.resultContainer{
    width: 100%;
    height: 48%;
    display: flex;
    justify-content: center;
    align-items: center;
    border: solid 1px #000;
    border-radius: 10px;
    margin-bottom: 4%;
}

button{
    --shape: 10px;
    --color: black;
    width: 100px;
    height: 30px;
    font-size: 15px;
    border: solid 1px #000;
    border-radius: var(--shape);
    color: black;
    border-color: var(--color);
}

.cssCodeContainer{
    width: 100%;
    height: 48%;
    border: solid 1px #000;
    border-radius: 10px;
    background-color: gray;
    color: white;
}

.cssCode{
    width: 95%;
    margin: auto;
}

.white{color: white;}
.fillColor{background-color: var(--color);}
</style>