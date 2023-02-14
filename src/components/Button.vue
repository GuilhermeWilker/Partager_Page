<template>
  <button @click.prevent="partagerApp">{{ content }}</button>
</template>

<script>
export default {
  props: {
    content: String,
  },
  methods: {
    partagerApp() {
      addEventListener("click", () => {
        window.location.href = "https://partage-player.vercel.app/";
      });
    },
  },
};
</script>

<style scoped>
button {
  background-color: #236ad4;
  padding: 16px;

  font-size: 15px;
  font-weight: 600;
  color: white;

  border-radius: 5px;
  border: none;
  cursor: pointer;
}
</style>
