<template>
  <div class="about-quote grid mlr-main">
    <div class="about-quote-content">
      <p class="about-quote-text">“Aliquam pretium, turpis ac congue feugiat, risus urna volutpat diam, in faucibus libero elit elementum mi. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae.”</p>
      <span class="about-quote-author">- Someone really smart</span>
    </div>
  </div>
</template>

<script>
import animations from '@/animations/gsap'

export default {
  name: 'AboutQuote',
  data: () => {
    return {

    }
  },
  mounted () {
    animations.enterFadeInY('.about-quote-content')
  },
  beforeDestroy () {
    this.marqueeScrollTrigger.scrollTrigger.kill()
  }
}
</script>

<style scoped>

</style>
