<template>
<header>
  <h1 class="text-center my-5">{{ title }}</h1>
</header>
  
</template>

<script>
export default {
  name: "HeaderComponent",
  props: [                            // props per passare valori tra elementi
    'title',
    ]
}
</script>

<style lang="scss" scoped>

h1 {
  font-weight: 700;
  text-transform: capitalize;
}

</style>