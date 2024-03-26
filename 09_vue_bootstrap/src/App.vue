<!-- <template>
  <div>
    <b-badge variant="primary">Primary</b-badge>
    <b-badge variant="secondary">Secondary</b-badge>
    <b-badge variant="success">Success</b-badge>
    <b-badge variant="danger">Danger</b-badge>
    <b-badge variant="warning">Warning</b-badge>
    <b-badge variant="info">Info</b-badge>
    <b-badge variant="light">Light</b-badge>
    <b-badge variant="dark">Dark</b-badge>
  </div>

  <div>
    <b-card
      title="Card Title"
      img-src="https://picsum.photos/600/300/?image=25"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-2"
    >
      <b-card-text>
        Some quick example text to build on the card title and make up the bulk of the card's content.
      </b-card-text>

      <b-button href="#" variant="primary">Go somewhere</b-button>
    </b-card>
  </div>
</template>



<script setup>

</script>

<style scoped>

</style> -->

<template>
  <b-row>
    <b-col md="auto">
      <b-calendar v-model="value" @context="onContext" locale="en-US"></b-calendar>
    </b-col>
    <b-col>
      <p>Value: <b>'{{ value }}'</b></p>
      <p class="mb-0">Context:</p>
      <pre class="small">{{ context }}</pre>
    </b-col>
  </b-row>
</template>

<script>
  export default {
    data() {
      return {
        value: '',
        context: null
      }
    },
    methods: {
      onContext(ctx) {
        this.context = ctx
      }
    }
  }
</script>