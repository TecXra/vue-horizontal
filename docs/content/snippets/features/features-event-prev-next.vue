<template>
  <div>
    <vue-horizontal @prev="onPrev" @next="onNext">
      <component-example v-for="i in [1,2,3,4,5,6,7,8,9,10,11,12]" :key="i">
        <h3>Event {{ i }}</h3>
      </component-example>
    </vue-horizontal>

    <pre>{{prev}}</pre>
    <pre>{{next}}</pre>
  </div>
</template>

<script>
export default {
  data() {
    return {
      prev: 'no-event',
      next: 'no-event',
    }
  },
  methods: {
    onPrev() {
      this.prev += '- clicked prev'
    },
    onNext() {
      this.next += '- clicked next'
    }
  }
}
</script>
