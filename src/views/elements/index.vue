<template>
  <div class="elements-container">
    {{ elementType }} setting page
    1. 通过path判断哪一种组件
    2. 每一种组件，展示的字段和添加时候的字段都不一样，可以用一个dict去存一下
    3. 进入页面，将组件的所有结果用Table Render出来
    4. 右上角弄一个添加按钮，添加的话，按照配置里面需要的字段添加好，添加时候规则就是非空就行
    5. 至于添加的那个页面如何出现，随你们了，可以本来隐藏的，点了添加就出现~
  </div>
</template>

<script>

export default {
  name: 'Elements',
  data() {
    return {
      elementType: undefined,
      elementList: [],
      elementsSettings: {
        cpu: {

        },
        memory: {

        }
      }
    }
  },
  computed: {
  },
  created() {
    this.elementType = this.$route.name.toLowerCase()
  }
}
</script>
