<template>
  <div class="home-techstack mlr-main">
    <div class="home-techstack-title">
      <h2 class="t-section-title t-purple">FULLSTACK DEV</h2>
      <h2 class="t-section-title t-white">TECHNOLOGY LOVER</h2>
    </div>
    <div class="techstack-item grid" v-for=" item in this.techstackItems" :key="item.title">
      <div class="techstack-item-type">{{ item.type }}</div>
      <div class="techstack-item-info">
        <h3 class="techstack-item-info-title">{{ item.title }}</h3>
        <p class="techstack-item-info-desc">{{ item.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import animations from '@/animations/gsap'

export default {
  name: 'HomeTechstack',
  methods: {
    enterLeftAnimation: (el) => {
      animations.enterFadeInX(el)
    },
    enterAnimation: (el) => {
      animations.enterFadeInY(el)
    }
  },
  mounted () {
    const techstackItems = document.querySelectorAll('.techstack-item')
    for (var i = 0; i < techstackItems.length; i++) {
      animations.enterFadeInY(techstackItems[i])
    }
    animations.enterFadeInX('.home-techstack-title')
  },
  data: () => {
    return {
      techstackItems: [
        {
          type: 'backend',
          title: 'C# and ASP.NET',
          description: 'I develop desktop applications using C# which is my favourite programming language. I love it’s syntax and just the way the code is written. It’s relatively easy to learn and realiable modern programming language. Apart from desktop applications I also develop backend of web applications using the ASP.NET framework.'
        },
        {
          type: 'frontend',
          title: 'Vue.js',
          description: 'This whole website runs on Vue.js. I develop reactive and modern websites and web applications using Vue. It’s overall very good javascrip framework and fairly easy to learn and use.'
        },
        {
          type: 'frontend',
          title: 'HTML and (S)CSS',
          description: 'I mean, seriously. What kind of web developer does not use HTML and CSS?'
        },
        {
          type: 'databases',
          title: 'MS SQL and MongoDB',
          description: 'For my web applications as a database I mainly use the SQL database MS SQL, but in some cases I use MongoDB.'
        },
        {
          type: 'design',
          title: 'Figma',
          description: 'For designing all my websites and web applications I use Figma. I think it’s the best tool for web design available right now.'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
