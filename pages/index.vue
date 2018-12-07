<template>
  <div>
    <Parallax />
    <Description />
  </div>
</template>

<script>
import Parallax from '~/components/top/Pararallax.vue'
import Description from '~/components/top/Description.vue'
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Parallax,
    Description,
    Logo,
    VuetifyLogo
  }
}
</script>
