<template>
  <MainScreen
    v-if="statusMatch === 'default'"
    @onStart="onHandleBeforeStart($event)"
  />
  <InteractScreen v-if="statusMatch === 'match'" />
</template>

<script>
import MainScreen from "./components/MainScreen.vue";
import InteractScreen from "./components/InteractScreen.vue";
export default {
  name: "App",
  data() {
    return {
      statusMatch: "default",
    };
  },
  components: {
    MainScreen,
    InteractScreen,
  },
  methods: {
    onHandleBeforeStart(config) {
      console.log("runnung handle before start,", config);
      this.statusMatch = "match";
    },
  },
};
</script>
