<template >
  <q-page class="flex flex-center"  style="background-color:#f1f1f4;">
    <Keyboard/>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';
import Keyboard from 'src/components/Keyboard.vue';

export default defineComponent({
  name: 'IndexPage',
   components: {
    Keyboard
  },

})
</script>
