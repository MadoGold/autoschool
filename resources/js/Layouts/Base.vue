<template>
  <div class="wrapper">
    <Header></Header>

    <slot/>

    <Footer></Footer>
  </div>
</template>

<script>
import BreezeApplicationLogo from '@/Components/ApplicationLogo.vue';
import {Link} from '@inertiajs/inertia-vue3';
import Header from '@/Components/Blocks/Header';
import Footer from '@/Components/Blocks/Footer';


export default {
  components: {
    BreezeApplicationLogo,
    Link,
    Header,
    Footer,
  },
}
</script>
