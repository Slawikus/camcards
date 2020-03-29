<template>
  <q-page class="flex flex-center">
    <p>Text</p>
  </q-page>
</template>

<script>
import Card from 'components/Card';

export default {
  name: 'PageIndex',

  components: {
    Card
  },

  data () {
    return {
      cards: [
        {
          icon: 'Docs',
          caption: 'quasar.dev'
        },
        {
          icon: 'Docs',
          caption: 'quasar.dev'
        }
      ]
    }
  }
}
</script>
