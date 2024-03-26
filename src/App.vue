<!-- App.vue -->
<template>
  <div id="app" style="display: flex; justify-content: center; align-items: center; height: 100vh;">
    <!-- Submit Form -->
    <div>
      <input v-model="inputNumber" type="number" placeholder="Masukkan angka">
      <button @click="count">Submit</button>
      <p>Total angka: {{ totalNumber }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputNumber: null,
      totalNumber: 0
    };
  },
  methods: {
    count() {
      if (this.inputNumber !== null) {
        this.totalNumber += parseInt(this.inputNumber);
        this.inputNumber = null;
      }
    }
  }
};
</script>
