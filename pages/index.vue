<template>
  <div >
    <Header />
    <body>
      <Presentation />
      <AboutMe />
      <Skills />
      <Projects />
      <Footer />
    </body>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Header from '~/components/UI/Header.vue'
import Presentation from '~/components/UI/Presentation.vue'
import AboutMe from '~/components/sections/AboutMe.vue'
import Skills from '~/components/sections/Skills.vue'
import Footer from '~/components/sections/Footer.vue'
import Projects from '~/components/sections/Projects.vue'
export default {
  components: {
    Logo,
    Header,
    Presentation,
    AboutMe,
    Skills,
    Projects,
    Footer
  }
}
</script>

<style>
/* body {
  display: flex;
  flex-direction: column;
  gap: 80px;
} */
</style>
