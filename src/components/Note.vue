<template lang="html">
  <div class="item">
    <div class="meta">{{ updated(entity) }}</div>

    <div class="content">
      <div class="header">
        {{ header(entity) || 'New Note'}}
      </div>

      <div class="extra">
        <editor
        v-bind:entity="entity">
        </editor>
        <i class="right floated trash alternate icon"
        @click="destroy(entity)">
        </i>
      </div>
      {{ words(entity) }}字
    </div>
  </div>
</template>

<script>
import Editor from './Editor'
import { mapGetters, mapActions } from 'vuex'

export default {
  computed: {
    ...mapGetters([
      'updated',
      'words',
      'header'
    ])
  },
  props: [
    'entity'
  ],
  components: {
    Editor
  },
  methods: {
    ...mapActions([
      'destroy'
    ])
  }
}
</script>

<style lang="css">

</style>
