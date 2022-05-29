<template>
  <div >
    <Header />
    <Presentation />
    <AboutMe />
    <Skills />
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Header from '~/components/UI/Header.vue'
import Presentation from '~/components/UI/Presentation.vue'
import AboutMe from '~/components/sections/AboutMe.vue'
import Skills from '~/components/sections/Skills.vue'
export default {
  components: {
    Logo,
    Header,
    Presentation,
    AboutMe,
    Skills
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
