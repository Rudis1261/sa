<template>
  <div class="gome">
    <div class="container text-center">
      <Title size="md" msg="Soon to be the home Strydom Accounting" />
      <Title size="sm" msg="More details to follow shortly" />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Title from '@/components/Title.vue'

export default {
  name: 'Home',
  components: {
    Title
  }
}
</script>