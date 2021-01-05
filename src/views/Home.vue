<template>
    <div class="home">
        <div class="header">
            <h1 class="title">2048</h1>
            <div class="controls">
                <div class="controls_list">
                    <div class="controls_score">
                        <div class="controls_score-label">Score</div>
                        <div class="controls_score-text">0</div>
                    </div>
                    <div class="controls_score">
                        <div class="controls_score-label">Best</div>
                        <div class="controls_score-text">0</div>
                    </div>
                </div>
                <div class="controls_game"></div>
            </div>
        </div>
        <!-- controls -->
        
        <div class="game-container">
        <grid></grid>
        </div>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Grid from "@/components/grid.vue"; // @ is an alias to /src

@Options({
  data() {
    return {
      score: 0,
    };
  },
  components: {
    Grid,
  },
})
export default class Home extends Vue {}
</script>
<style lang="less" scoped>
.home {
    min-height: 100vh;
    background: #faf8ef;
    color: #776e65;
    padding: 0.4rem 0.3rem;
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .title {
        font-size: 1rem;
        font-weight: 800;
    }
    .controls {
        .controls_list {
            display: flex;
            align-items: baseline;
            justify-content: space-between;
            .controls_score {
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                background: #BBAC9F;
                width: 1.2rem;
                height: 1.1rem;
                margin-left: .1rem;
                border-radius: .1rem;
                &-label {
                    font-size: .26rem;
                    margin-bottom: 0.1rem;
                    color: #eee4da;
                    font-weight: 800;
                }
                &-text {
                    color: #fff;
                    font-size: .5rem;
                    font-weight: 800;
                }
            }
        }
        
        .controls_game {
            .controls_game-btn {
                padding: 0.1rem 0.18rem;
                background: transparent;
                color: #f9d49a;
                outline: 1px solid #f9d49a;
                appearance: none;
                border: 2px solid transparent;
                box-shadow: inset 0 0 0px 2px #d4a8cf;
                letter-spacing: 0.1em;
                font-weight: bold;
                font-size: 0.4rem;
                text-transform: lowercase;
            }
        }
        // .controls_score {
        //     display: flex;
        //     flex-direction: column;
        //     align-items: center;
        //     justify-content: center;
        //     min-width: 50%;
        //     padding: 0.2rem;
        //     background: linear-gradient(90deg, #f9d49a, #d4a8cf);
        //     &-label {
        //         font-size: 0.3rem;
        //         margin-bottom: 0.1rem;
        //     }
        //     &-text {
        //         color: #4a3647;
        //         color: #4a3647;
        //         font-size: 0.6rem;
        //     }
        // }
    }
    .game-container {
        display: flex;
        justify-content: center;
        margin-top: 0.8rem;
    }
}
</style>
