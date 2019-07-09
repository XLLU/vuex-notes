<template lang="html">
    <div class="ui form">
        <div class="ui field">
            <textarea
            rows="5"
            placeholder="Write something... "
            v-model="entity.body"
            v-on:input="update(entity)">
            </textarea>
        </div>
    </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  props: [
    'entity'
  ],
  methods: {
    ...mapActions([
      'update'
    ])
  }
}

</script>

<style lang="css">

</style>
