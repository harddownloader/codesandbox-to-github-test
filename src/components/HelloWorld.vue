<template>
  <div class="hello">
    {{ name }}
    {{ getNewName }}
    {{ inputVal }}
    <input type="text" v-model="inputVal" />
    <button @click="this.changeName">Change Name</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data: () => ({
    name: "john",
    inputVal: null,
  }),
  methods: {
    changeName() {
      this.name = this.input;
    },
  },
  computed: {
    getNewName() {
      return this.name;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
