<template>
  <q-card>
    <q-card-section class="q-pb-none">
      <q-btn icon="o_close" flat dense v-close-popup />
    </q-card-section>

    <div class="fixed-center">
      <q-card-section>
        <q-icon :name="iconPrefix + card.icon" class="full-width" size="24rem"/>
      </q-card-section>

      <q-card-section>
        <div class="text-center text-uppercase text-h4">{{ card.caption }}</div>
      </q-card-section>
    </div>
  </q-card>
</template>

<script>
  export default {
    name: 'CardFullSize',

    props: {
      card: {
        type: Object,
        required: true
      },
    },

    data() {
      return {
        iconPrefix: 'o_'
      }
    }
  }
</script>
