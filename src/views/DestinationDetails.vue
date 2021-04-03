<template>
  <section class="destination">
    <div v-if="destination">
      <h1>{{ destination.name }}</h1>
      <div class="destination-details">
        <img
          :src="require(`@/assets/${destination.image}`)"
          alt="destination.name"
        />
        <p>
          {{ destination.description }}
        </p>
      </div>
    </div>
    <BaseErrorMessage
      v-else
      :data="{
        title: 'Destination Error',
        message: 'The destination page was not loaded successfully',
      }"
    />
  </section>
</template>

<script>
import store from "@/store.js";
import BaseErrorMessage from "@/components/BaseErrorMessage";

export default {
  components: {
    BaseErrorMessage,
  },
  data() {
    return {
      destinationId: this.$route.params.id,
    };
  },
  computed: {
    destination() {
      return store.destinations.find(
        (destination) => destination.id === parseInt(this.destinationId)
      );
      /*   A PROBLEM !!!
        - when the page is reloaded during destination/details/:id pages
          the "===" operator will return false because the destination.id returned from the
          sought array will somehow not return its expected data type which is a "number".
          WORKAROUND !!!
        - it will somehow work if the comparison operator is changed to "=="
         or
        - it will work by parsing the "id" from the route params into an integer
       */
    },
  },
};
</script>

<style scoped>
img {
  max-width: 800px;
  height: auto;
  width: 100%;
  max-height: 400px;
}
.destination-details {
  display: flex;
  justify-content: space-between;
}
p {
  margin: 0 40px;
  font-size: 16.5px;
  font-weight: 100;
  text-align: left;
  line-height: 1.4;
  color: rgb(68, 66, 66);
}
</style>
