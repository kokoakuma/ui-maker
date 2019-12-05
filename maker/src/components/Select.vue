<template>
    <div class="root">
        <h5>ボタンの形</h5>
        <div class="shape block">
            <button class="square" @click="$emit('square')">四角</button>
            <button class="littleCurve" @click="$emit('littleCurve')">少し丸い</button>
            <button class="curve" @click="$emit('curve')">丸い</button>
        </div>
        <h5>ボタン枠線の色</h5>
        <div class="color block">
            <button class="black" @click="$emit('black')">ブラック</button>
            <button class="red" @click="$emit('red')">レッド</button>
            <button class="green" @click="$emit('green')">グリーン</button>
            <button class="blue" @click="$emit('blue')">ブルー</button>
            <button class="yellow" @click="$emit('yellow')">イエロー</button>
            <button class="navy" @click="$emit('navy')">ネイビー</button>
        </div>
        <h5>塗り潰し</h5>
        <div class="fill block">
            <button class="fill" @click="$emit('doFill')">塗りつぶす</button>
            <button class="notFill" @click="$emit('notFill')">しない</button>
        </div>
        <h5>ボタンの文字の色</h5>
        <div class="font-color block">
            <button class="fontBlack" @click="$emit('fontBlack')">文字が黒</button>
            <button class="fontWhite" @click="$emit('fontWhite')">文字が白</button>
        </div>
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
    margin-bottom: 45px;
    display: flex;
    justify-content: space-evenly
}

button{
    width: 30%;
    height: 30px;
    font-size: 14px;
    border: solid 1px #000;
    border-radius: 10px;
}

.color{
    flex-wrap: wrap;
}

.color button{
    margin-bottom: 15px;
}

.square{border-radius: 0px;}
.littleCurve{border-radius: 10px;}
.curve{border-radius: 15px;}

.black{color: black; border-color: black;}
.red{color: #e74c3c; border-color: #e74c3c;}
.green{color: #2ecc71; border-color: #2ecc71;}
.blue{color: #3498db; border-color: #3498db;}
.yellow{color: #f1c40f; border-color: #f1c40f;}
.navy{color: #2c3e50; border-color: #2c3e50;}
</style>