<template>
  <h1>{{ msg }}</h1>
  <h1>{{ obs.test }}</h1>
  <button
    @click="
      count++;
      show(count);
    "
  >
    count is: {{ count }}
  </button>
  <!-- <button v-if="test" :style="{ color: 'red' }">{{ test }}ttttttttttttt</button> -->
  <p>
    Edit <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
  <div>
    {{ fullName }}
    <br />
    <input type="text" v-model="firstName" />
    <br />
    <input type="text" v-model="lastName" />
  </div>
  <ul id="array-rendering">
    <li v-for="item in vs">
      {{ item }}
    </li>
  </ul>
  <div v-for="item in items">tes</div>
  <input v-model.number="age" type="number" />
</template>

<script>
const tt = {};
export default {
  name: "HelloWorld",
  props: {
    msg: String,
    obs: {
      type: Object,
      // required:true
      default: {
        test: "resr",
      },
    },
  },
  data() {
    return {
      count: 0,
      re: "re",
      age: "ww",
      test: false,
      firstName: "chunwen",
      lastName: "YU",

      items: [{ message: "Foo" }, { message: "Bar" }],
      vs: [1, 2, 3, 6, 4, 8],
    };
  },
  created() {
    console.log("test", this.count);
  },
  watch: {
    count() {
      console.log("ccha", this.count);
    },
    firstName() {
      console.log("fir", this.firstName);
    },
    cs() {
      console.log("cs");
    },
  },
  methods: {
    show(count) {
      console.log(count, this.test);
    },
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
  },
};
</script>
