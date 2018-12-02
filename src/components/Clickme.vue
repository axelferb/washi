<template>
    <div>
        <div v-for="(item, index) in items" v-bind:key="index">
            <h1>
                {{item.text}}
            </h1>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Clickme',
  data () {
    return {
      items: [
          {text: 'Tjaman 1'},
          {text: 'Tjaman 2'},
          {text: 'Tjaman 3'},
          {text: 'Tjaman 4'}
      ]
    }
  }
}
</script>

<style lang="less" scoped>
    div {
        background-color: rebeccapurple;
    }
</style>

