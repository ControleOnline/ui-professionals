<template>
  <People :context="context" :myCompany="myCompany" v-if="context" />
</template>

<script>
import People from "@controleonline/ui-people/src/vue/components/People/List.vue";
import { mapGetters, mapActions } from "vuex";

export default {
  components: {
    People,
  },
  computed: {
    ...mapGetters({
      myCompany: "people/currentCompany",
    }),
  },
  data() {
    return {
      context: "professional",
    };
  },
  created() {},
};
</script>
