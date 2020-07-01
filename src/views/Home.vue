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
        },
        {
          nameImg: 'machu.jpg',
          country: 'Perú',
          state: 'Machu Pichu',
          area: '50.000',
          maxLength: '100.000', 
        },
        {
          nameImg: 'patagonia.jpg',
          country: 'Argentina',
          state: 'Patagonia',
          area: '50.000',
          maxLength: '100.000', 
        },
        {
          nameImg: 'asm-1.jpg',
          country: 'Paises Bajos',
          state: 'Ámsterdam',
          area: '50.000',
          maxLength: '100.000', 
        }

      ]
    }
  }
}
</script>
