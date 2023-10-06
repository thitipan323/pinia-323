<template>
  <navbar_product />
  <div class="container">
    <router-view />
  </div>

  <h1 >รายการสินค้าตัวอย่างที่สมมุติทุกอย่างไม่มีอันไหนของจริง</h1>
  
<img src="https://th.bing.com/th/id/R.ee87e6dfbc3c654194896d509d637412?rik=eTnr0C8PHdHLaA&riu=http%3a%2f%2fbouassa.org%2fen%2fwp-content%2fuploads%2f2016%2f03%2fneedyou.jpg&ehk=Sv%2fl22AmohmztaNb2WPwLj29HFuCqBvaGfcqGk6Xz1c%3d&risl=&pid=ImgRaw&r=0&sres=1&sresct=1" alt="">
</template>


<script setup>
import { onMounted } from 'vue'
import navbar_product from './components/navbar_product.vue';

// useProductStore
import { useProductStore } from './store/product'
const product_store = useProductStore()

//useCartStore
import { useCartStore } from './store/cart';
const cart_store = useCartStore()


onMounted(() => product_store.fetch_products())
onMounted(() => cart_store.loadFromLocalStorage())



</script>

<style lang="scss" scoped>
h1{
  text-align: center;
}

img{
  max-width: 540px;
  min-height: 540px;
  margin-left: 35rem;
}
</style>