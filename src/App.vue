<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName()">change name</button>
    <button @click="changeAge()">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  setup() {
    // ::::: reactive ::::: 
    // const state = reactive({
    //   name: "Link",
    //   age: 25 as number | string,
    // });

    // return { ...toRefs(state) };

    // ::::: reference 
    const name = ref("Link");
    const age = ref<number | string>(25);

    return { name, age };
  },
  methods: {
    changeName(name: string) {
      this.name = name;
    },
    changeAge(age: string | number) {
      this.age = age;
    },
  },
});
</script>

<style></style>
