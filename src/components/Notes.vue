<template lang="html">
    <div class="ui container notes">
        <h4 class="ui horizontal divider header">
            <i class="paw icon"></i>
            VueX Notes
        </h4>
        <a class="ui right floated basic vilet button"
          v-on:click="create">
            Add Note
        </a>
        <div class="ui divided items">
            <note
            v-for="(entity,key) in entities"
            v-bind:entity="entity"
            v-bind:key="key">
            </note>
        </div>
    </div>

</template>

<script>
import Note from './Note'
import { mapGetters, mapActions } from 'vuex'

export default {
  created () {
    this.initial()
  },
  create () {
    this.create()
  },
  methods: {
    ...mapActions([
      'initial',
      'create'
    ])
  },
  computed: {
    ...mapGetters([
      'entities'
    ])
  },
  components: {
    Note
  }
}
</script>

<style lang="css">

</style>
