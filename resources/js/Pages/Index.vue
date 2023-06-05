<template>
  <BaseLayout>
    <Hero></Hero>
    <Cards></Cards>
    <Categories id="categories"></Categories>
    <Stages id="stages"></Stages>
    <ContactUs id="contact-us"></ContactUs>
  </BaseLayout>
</template>

<script>
import BaseLayout from '@/Layouts/Base';
import {Link} from '@inertiajs/inertia-vue3';
import Cards from '@/Components/Blocks/Cards';
import Hero from '@/Components/Blocks/Hero';
import Categories from '@/Components/Blocks/Categories';
import Stages from '@/Components/Blocks/Stages';
import ContactUs from '@/Components/Blocks/ContactUs';

export default {
  components: {
    BaseLayout,
    Link,
    Cards,
    Hero,
    Categories,
    Stages,
    ContactUs,
  },
}
</script>
