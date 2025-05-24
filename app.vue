<script setup lang="ts">

const things = ref([
  {
    id: 1,
    name: 'fuckingfast',
    link: 'https://fuckingfast.net/',
    img: 'https://placehold.co/600x400/EEE/31343C'
  },
  {
    id: 2,
    name: 'wait',
    link: 'https://fuckingfast.net/',
    img: 'https://placehold.co/600x400/EEE/31343C'
  }
])

</script>

<template>
  <main>
    <section class="head-seg">
      <h1>Maksiks' list of nifty stuffs</h1>
    </section>
    <section class="content-seg">
      <div v-for="thing in things" :key="thing.id" class="thing">
        <img :src="thing.img" :alt="thing.name" />
      </div>
    </section>
  </main>
</template>

<style>
* {
  margin: 0;
  padding: 0;
}

html, body {
  overflow-x: hidden;
}
</style>
<style scoped>
main {
  display: flex;
  flex-direction: column;

  & .head-seg {
    display: flex;
    justify-content: center;

    & h1 {

    }
  }

  & .content-seg {
    display: flex;
    justify-content: center;
  }

}
</style>