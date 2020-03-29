<template>
  <q-page padding>
    <div
      v-for="card in cards"
      :key="card.id"
      class="q-pb-md"
      @click="showFullSizeCard(card)"
    >
      <Card
        :icon="card.icon"
        :caption="card.caption" />
    </div>

    <q-dialog v-model="showFullSizeCardDialog" full-height full-width>
      <CardFullSize :card="fullSizeCard" />
    </q-dialog>
  </q-page>
</template>

<script>
import Card from 'components/Card';
import CardFullSize from 'components/CardFullSize';

export default {
  name: 'PageIndex',

  components: {
    Card, CardFullSize
  },

  methods: {
    showFullSizeCard(selectedCard) {
      this.setFullSizeCard(selectedCard);
      this.showFullSizeCardDialog = true;
    },

    setFullSizeCard(card) {
      this.fullSizeCard = card;
    }
  },

  data() {
    return {
      showFullSizeCardDialog: false,

      fullSizeCard: {
        id: 1,
        icon: 'free_breakfast',
        caption: "Let's make a break"
      },

      cards: [
        {
          id: 1,
          icon: 'free_breakfast',
          caption: "Let's make a break"
        },
        {
          id: 2,
          icon: 'play_circle_outline',
          caption: 'Good to go'
        },
        {
          id: 3,
          icon: 'desktop_access_disabled',
          caption: 'Away from keyboard'
        },
        {
          id: 4,
          icon: 'how_to_vote',
          caption: "Let's vote"
        },
        {
          id: 5,
          icon: 'volume_off',
          caption: 'I cannot hear you'
        },
        {
          id: 6,
          icon: 'mic_off',
          caption: 'Mute'
        },
        {
          id: 7,
          icon: 'volume_up',
          caption: 'More volume'
        },
        {
          id: 8,
          icon: 'volume_down',
          caption: 'Less volume'
        },
        {
          id: 9,
          icon: 'hearing',
          caption: 'Bad sound quality'
        },
        {
          id: 10,
          icon: 'thumb_up_alt',
          caption: 'Yes'
        },
        {
          id: 11,
          icon: 'thumb_down_alt',
          caption: 'No'
        },
        {
          id: 12,
          icon: 'event',
          caption: "Let's discuss elsewhere"
        },
        {
          id: 13,
          icon: 'pan_tool',
          caption: 'I need to speak'
        },
        {
          id: 14,
          icon: 'directions_run',
          caption: 'I need to go'
        },
        {
          id: 15,
          icon: 'emoji_people',
          caption: 'Bye'
        },
        {
          id: 16,
          icon: 'emoji_objects',
          caption: 'I have an idea'
        }
      ]
    }
  }
}
</script>
