<template>
  <q-card>
    <q-card-section class="q-pb-none">
      <q-btn icon="o_close" flat dense v-close-popup />
    </q-card-section>

    <q-card-section>
      <q-icon :name="iconPrefix + icon" class="full-width" size="24rem"/>
    </q-card-section>

    <q-card-section>
      <div class="text-center text-uppercase text-h4">{{ caption }}</div>
    </q-card-section>
  </q-card>
</template>

<script>
  export default {
    name: 'CardFullSize',

    props: {
      icon: {
        type: String,
        required: true
      },

      caption: {
        type: String,
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
