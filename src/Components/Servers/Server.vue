<template>
  <div>
      <p v-if="!server">Server Details are currently not updated</p>
      <p v-else>Server #{{ server.id }}: {{ server.status }}</p>
      <button class="btn btn-default" @click="resetStatus">Reset Status</button>
  </div>
</template>

<script>
import { eventBus } from '../../main';
export default {
    data() {
        return {
            server: null
        };
    },
    methods: {
        resetStatus() {
            this.server.status = 'Normal';
        }
    },
    created() {
        eventBus.$on('serverSelected', server => {
            this.server = server;
        });
    }
}
</script>

<style>

</style>