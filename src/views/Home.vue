<template>
  <div class="home">
    <img
      alt="Vue logo"
      src="../assets/logo.png"
    >
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
    <p>{{vv}}</p>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

@Component({
  components: {
    HelloWorld
  }
})
export default class Home extends Vue {
  @Prop() vv!: string;
  mounted() {
    console.log("页面打开了!");
    this.vv = "哈哈";
    console.log(this.vv);
  }
}
</script>
