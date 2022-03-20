<template>
  <div>
    <button class="btn btn-success" @click="increaseCounter">+ Arttır</button>
    <button class="btn btn-danger" @click="decreaseCounter">- Azalt</button>
    <hr />
    <button class="btn btn-success" @click="increment({x : 10})">+ Arttır</button>
    <button class="btn btn-danger" @click="decrement">- Azalt</button>
    <hr />
    <button class="btn btn-success" @click="incAsync({time : 1000})">+ Async Arttır</button>
  </div>
</template>

<script>
import { mapMutations, mapActions } from "vuex";

export default {
  methods: {
    ...mapMutations(["increaseCounter", "decreaseCounter"]),
     ...mapActions(["increment", "decrement","incAsync"]),

    // decrement(){
    //   this.$store.dispatch("decrement")
    // },
    // increment(){
    //   this.$store.dispatch("increment")
    // }
    // incrementCounter(){
    //   //this.$emit("counterEvent", 1);
    //   // this.$store.state.counter++;
    //   this.$store.commit("increaseCounter");
    // },
    // decrementCounter(){
    //   //this.$emit("counterEvent", -1);
    //   // this.$store.state.counter--;
    //   this.$store.commit("decreaseCounter");

    // }
  },
};
</script>

<style>
</style>
