<template>
<div id="app">

    <div v-loading="isLoading" class="controlled-area">
        <pre>{{ msg }}</pre>
    </div>

    <div class="control-area">
        <el-button :icon="isLoading ? 'el-icon-video-pause' : 'el-icon-video-play'" tabindex="1" @click="toggle">
            {{ isLoading ? '有点晕 停车' : '爱的魔力转圈圈' }}
        </el-button>
    </div>

</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({})
export default class App extends Vue {

    private isLoading: boolean = false

    private msg: string = `
        生生繁华于枯荑
        萋萋空翠自灵犀
        辉星皓夜苍千顷
        此宵风醉月舞萤
    `

    private toggle() {
        this.isLoading = !this.isLoading
    }

}
</script>

<style lang="sass" scoped>
#app
    .controlled-area
        min-width: 500px
        max-width: 60vw
        min-height: 400px
        margin: 30px
        padding: 50px
        font-size: 22px
        line-height: 32px
        box-shadow: 0 0 10px 10px rgba(171, 174, 182, .2)

    .control-area
        text-align: center
</style>
