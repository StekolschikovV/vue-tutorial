<template>
    <div>
        <input type="text" :value="mess" @input="onInput">
    </div>
 
</template>

<script>
export default {
  props: ["mess"],
  methods: {
    onInput(event) {
      this.$root.$emit("mess-send", event.target.value);
    }
  },

};
</script>
