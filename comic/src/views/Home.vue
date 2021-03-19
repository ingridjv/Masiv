<template>
  <div class="home">
    <comic />
    
  </div>
</template>

<script>
// @ is an alias to /src

import comic from '@/components/comic.vue'
export default {
  name: 'Home',
  components: {
    
    comic
  }
}
</script>
