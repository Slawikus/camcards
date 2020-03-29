<template>
  <q-list bordered>
    <q-item clickable v-ripple>
      <q-item-section avatar>
        <q-icon color="primary" :name="iconPrefix + icon" />
      </q-item-section>

      <q-item-section>{{ caption }}</q-item-section>
    </q-item>
  </q-list>
</template>

<script>
export default {
  name: 'Card',

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
