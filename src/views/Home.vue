<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <Nature :sites="natures"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Nature from '@/components/Nature.vue'

export default {
  name: 'Home',
  components: {
    Nature
  },
  data(){
    return {
      natures: [
        {
          nameImg: 'santorini.jpg',
          country: 'Grecia',
          state: 'Santorini',
          area: '26.570',
          maxLength: '26.800', 
        },
        {
          nameImg: 'sahara.jpg',
          country: 'Africa',
          state: 'Sahara',
          area: '50.000',
          maxLength: '100.000', 
        }
      ]
    }
  }
}
</script>
