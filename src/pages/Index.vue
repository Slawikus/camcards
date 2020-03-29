<template>
  <q-page padding>
    <div class="q-pb-md">
      <q-list bordered>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="bluetooth" />
          </q-item-section>

          <q-item-section>Icon as avatar</q-item-section>
        </q-item>
      </q-list>
    </div>

    <div class="q-pb-md">
      <q-list bordered>
        <q-item clickable v-ripple>
          <q-item-section avatar>
            <q-icon color="primary" name="bluetooth" />
          </q-item-section>

          <q-item-section>Icon as avatar</q-item-section>
        </q-item>
      </q-list>
    </div>
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
