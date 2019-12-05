<template>
    <div class="root">
        <div class="shape block">
            <button class="square" @click="$emit('square')">四角</button>
            <button class="littleCurve" @click="$emit('littleCurve')">少し丸い</button>
            <button class="curve" @click="$emit('curve')">丸い</button>
        </div>
        <div class="color block"></div>
        <div class="fill block"></div>
    </div>
</template>

<script>
export default {
    name: "Select",
}
</script>
<style lang="css" scoped>
.root{
    width: 100%;
}
.block{
    width: 90%;
    height: 50px;
    margin-bottom: 15px;
    display: flex;
    justify-content: space-evenly
}

button{
    width: 70px;
    height: 30px;
    font-size: 14px;
    border: solid 1px #000;
    border-radius: 10px;
}

.square{
 border-radius: 0px;
}

.littleCurve{
  border-radius: 10px;
}

.curve{
    border-radius: 15px;
}
</style>