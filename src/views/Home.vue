<template>
  <div class="home">
    <h1 class="title">2048</h1>
    <!-- controls -->
    <div class="controls">
      <div class="controls_game">
        <button data-js="newGame" class="controls_game-btn"> New Game </button>
      </div>
      <div class="controls_score">
        <div class="controls_score-label">Score </div>

        <div class="controls_score-text" >0</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Options({
  components: {
    HelloWorld,
  },
})
export default class Home extends Vue {}
</script>
<style lang="less" scoped>
.home {
  height: 100vh;
  background: linear-gradient(to top, #160140, #261535);
  padding: .4rem .3rem;
  .title {
    text-align: center;
    color: #f9d49a;
    font-size: 1rem;
    font-weight: 800;
    margin-bottom: .6rem;
  }
  .controls {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    .controls_game {
      .controls_game-btn {
        padding: .1rem .18rem;
        background: transparent;
        color: #f9d49a;
        outline: 1px solid #f9d49a;
        appearance: none;
        border: 2px solid transparent;
        box-shadow: inset 0 0 0px 2px #d4a8cf;
        letter-spacing: 0.1em;
        font-weight: bold;
        font-size: .4rem;
        text-transform: lowercase;
      }
    }
    .controls_score {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-width: 50%;
      padding: .2rem;
      background: linear-gradient(90deg, #f9d49a, #d4a8cf);
      &-label {
        font-size: .3rem;
        margin-bottom: .1rem;
      }
      &-text {
        color: #4a3647;
        color: #4a3647;
        font-size: .6rem;
      }
    }
  }
}
</style>
