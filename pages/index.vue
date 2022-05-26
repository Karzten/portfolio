<template>
  <div >
    <Header />
    <Presentation />
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Header from '~/components/UI/Header.vue'
import Presentation from '~/components/UI/Presentation.vue'
export default {
  components: {
    Logo,
    Header,
    Presentation
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/

</style>
