<template>
  <div>
    <ul class="list-group">
          <li class="list-group-item" v-for="(server) in servers" :key="server.name"><a href @click.prevent="select(server)">Server #{{ server.id }}</a></li>
    </ul>
  </div>
</template>

<script>
import { eventBus } from '../../main';
export default {
    data() {
        return {
            servers: [
                {
                    id: 1,
                    status: 'Normal'
                },
                {
                    id: 2,
                    status: 'Critical'
                },
                {
                    id: 3,
                    status: 'Unknown'
                },
                {
                    id: 4,
                    status: 'Normal'
                },
                {
                    id: 5,
                    status: 'Critical'
                }
            ],
            selected: null
        }
    },
    methods: {
        select(server) {
            eventBus.selectServer(server);
        }
    }
}
</script>

<style>

</style>