<template>
    <div class="root">
      <button 
      :style="styles">ボタン</button>
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
      type: String,
      dafault: "",
    },
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
    display: flex;
    justify-content: center;
    align-items: center;
    border: solid 1px #000;
}

button{
    --shape: 10px;
    --color: black;
    width: 70px;
    height: 30px;
    border: solid 1px #000;
    border-radius: var(--shape);
    color: var(--color)
}
</style>