<template>
  <section class="admin-panel">
    <div class="col">
      <div class="tab-content" id="v-pills-tabContent">
        <div
          class="tab-pane fade show active"
          id="v-pills-home"
          role="tabpanel"
          aria-labelledby="v-pills-home-tab"
        >
            <AccountInfo/>
        </div>
        <div
          class="tab-pane fade"
          id="v-pills-profile"
          role="tabpanel"
          aria-labelledby="v-pills-profile-tab"
        >tab2</div>
        <div
          class="tab-pane fade"
          id="v-pills-messages"
          role="tabpanel"
          aria-labelledby="v-pills-messages-tab"
        >.tab3</div>
        <div
          class="tab-pane fade"
          id="v-pills-settings"
          role="tabpanel"
          aria-labelledby="v-pills-settings-tab"
        >.tab4</div>
      </div>
    </div>
  </section>
</template>
<script>
    import AccountInfo from '../components/Dashboard/AccountInfo'

export default {
  name: "AdminPanel",
  components:{AccountInfo}
};
</script>

<style lang="scss" scoped>
.admin-panel {
  
}
</style>