<template>
  <div>
    <textarea
      ref="area"
      v-model="tweet"
      :style="styles"
    />
  </div>
</template>

<script lang="ts">
import { Vue, Component, Watch } from 'vue-property-decorator'

@Component({})
export default class extends Vue {
  tweet = ''
  height =''
  $refs!: {
    area: HTMLInputElement
  }

  @Watch('tweet', { immediate: true })
  onChangeWatch (): void {
    this.resize()
  }

  get styles (): { height: string} {
    return {
      height: this.height
    }
  }

  resize (): void {
    // 文字列が横に長くなるだけでもtextareaが縦に長くなるので不適切
    // this.height = this.$refs.area.scrollHeight + 'px'
    this.height = 'auto'
    this.$nextTick(() => {
      this.height = this.$refs.area.scrollHeight + 'px'
    })
  }
}
</script>

<style lang="scss" scoped>

</style>
