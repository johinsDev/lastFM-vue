<template lang="pug">
  div#app
    section.section
      nav.nav.has-shadow
        .container
          input.input.is-large(
              type="text",
              placeholder="Buscar canciones",
              v-model="searchQuery"
            )
          a.button.is-danger.is-large(@click="clean('searchQuery')", v-if="searchQuery") &times;
          p(v-if="totalSearch")
            small {{ searchMessage }}
      
      .container.tracks
        .columns
          .cloumn(v-for="t in tracks") {{ t.name }} - {{ t.artist }}
</template>

<script>
const tracks = [
  { name: 'Muchacha', artist: 'Luis alberto Spineta' },
  { name: 'Hoy aca en el baile', artist: 'El pepo' },
  { name: 'I was made for lowing you', artist: 'Kis' }
];

export default {
  name: 'app',
  data () {
    return {
      searchQuery: '',
      tracks: []
    }
  },
  computed: {
    totalSearch() {
      return this.tracks.length;
    },
    searchMessage() {
      return `Encontrados: ${this.totalSearch}`
    }
  },
  methods: {
    search() {
      if (this.searchQuery){
        this.tracks = tracks;
      } else {
        this.tracks = [];
      }
    },
    clean(data) {
      this[data] = '';
    }
  },
  watch: {
    searchQuery() {
      this.search();
    }    
  }
}

</script>

<style lang="scss">
  @import './scss/main.scss';
  
  .tracks {
    margin-top: 4rem;
  }
</style>
