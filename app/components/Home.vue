<template>
  <Page>
    <ActionBar>
      <Label text="Home" class="font-bold text-lg" />
    </ActionBar>

    <GridLayout>
      <Label
        class="text-xl align-middle text-center text-gray-500"
        :text="message"
        @tap="logMessage"
      />
      <Image
        v-if="image1"
        @click=""
        src="https://www.wallpaperup.com/uploads/wallpapers/2016/10/14/1026018/c3eea88412a4f3718761e0a406dec452.jpg"
        stretch="none"
      />
      <Image
        v-if="image2"
        @click=""
        src="https://1.bp.blogspot.com/-9dyKiLdml6g/UPe81_5qlqI/AAAAAAAAcuU/_3qTICKLzPQ/s1600/tirol2.jpg"
        stretch="none"
      />
    </GridLayout>
  </Page>
</template>

<script lang="ts">
import Vue from 'nativescript-vue';

export default Vue.extend({
  data() {
    return {
      image1: true,
      image2: flase,
    };
  },
  computed: {
    message() {
      return 'Blank {N}-Vue app';
    },
  },

  methods: {
    logMessage() {
      console.log('You have tapped the message!');
    },
    img1() {
      this.image1 = false;
      this.image2 = true;
    },
    img2() {
      this.image2 = false;
      this.image1 = true;
    },
  },
});
</script>

<style>
/* .info {
    font-size: 20;
  } */
</style>
