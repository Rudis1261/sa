<template>
  <h1 v-if="size == 'lg'">{{ msg }}</h1>
  <h2 v-else-if="size == 'md'">{{ msg }}</h2>
  <h3 v-else-if="size == 'sm'">{{ msg }}</h3>
  <h4 v-else>{{ msg }}</h4>
</template>

<script>
export default {
  name: 'Title',
  props: {
    msg: String,
    size: String
  }
}
</script>