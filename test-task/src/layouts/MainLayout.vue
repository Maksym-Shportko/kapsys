<template>
  <section class="main-layout">
    <main>
      <TheNavbar/>
      <div class="container-fluid pl-5 pr-0">
        <div class="row">
          <div class="col-md-2 pr-0">
            <TheSidebar />
          </div>
          <div class="col-md-10 pl-0 admin-panel-wrapper" >
            <router-view />
          </div>
        </div>
      </div>
    </main>
  </section>
</template>

<script>
import TheNavbar from "../components/Base/TheNavbar";
import TheSidebar from "../components/Base/TheSidebar";
export default {
  name: "MainLayout",
  components: { TheSidebar, TheNavbar },
};
</script>


<style lang="scss" scoped>
.main-layout {
  overflow: hidden;
}
.admin-panel-wrapper {
  background: #e4edf5;
  border-left: 1px solid #bdb7b7;;
}
</style>