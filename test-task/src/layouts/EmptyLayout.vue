<template>
    <section class="empty-layout">
        <LoginModal/>
    </section>
</template>

<script>
import LoginModal from '../components/Auth/LoginModal'
export default {
    name:'EmptyLayout',
    components:{LoginModal}
}
</script>
<style lang="scss" >
.empty-layout {
  background: linear-gradient(#5ef9c0a6 24%, #2f89cad9);
  overflow-x:hidden ;
}
</style>