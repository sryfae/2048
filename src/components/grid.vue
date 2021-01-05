<template>
<div class="game-board">
    <div class="grid">
        <div class="grid-cell"
            v-for="(value, index) in Array.from({length: 16})" :key="index"></div>
    </div>
</div>
</template>
<script lang="ts">
import { Options, Vue } from 'vue-class-component';
@Options({

})
export default class Grid extends Vue{}
</script>
<style lang="less" scoped>
.game-board {
    position: relative;
    width: 85vw;
    height: 85vw;
    border-radius: 6px;
    // box-shadow: 0 0 .2rem 0 #f9d49a;
    background: #BBAC9F;
    .grid {
        display: flex;
        flex-wrap: wrap;
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        padding: 5px;
        .grid-cell {
            flex-shrink: 0;
            width: 25%;
            height: 25%;
            padding: 5px;
            background: rgba(238, 228, 218, 0.35);
            background-clip: content-box;
        }
    }
}
</style>