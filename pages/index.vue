<template>
  <div>
    <h1>Hello world</h1>
  </div>
</template>

<script>

export default {
  data() {
    return {
    }
  },methods:{
    async asyncData({$axios}){
      const results = await $axios.$get('URL', {progress: false}).then((res) => {return res.data})
      return {results}
    }
  }
}
</script>
