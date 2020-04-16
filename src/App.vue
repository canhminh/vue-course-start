<template>
  <div class="container">
    <d-header></d-header>
    <hr />
    <div class="row">
      <div class="col-xs-12 col-sm-6">
        <d-server-list></d-server-list>
      </div>
      <div class="col-xs-12 col-sm-6">
        <d-server />
      </div>
    </div>
    <hr />
    <d-footer></d-footer>
  </div>
</template>

<script>
import Header from './Components/Header/Header.vue';
import Footer from './Components/Footer/Footer.vue'
import ServerList from './Components/Servers/ServerList.vue';
import Server from './Components/Servers/Server.vue';
export default {
    components: {
        'd-header': Header,
        'd-footer': Footer,
        'd-server-list': ServerList,
        'd-server': Server
    }
}
</script>

<style>
</style>
