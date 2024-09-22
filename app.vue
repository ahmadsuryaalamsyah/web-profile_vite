<template>
  <Header />
  <Section />
  <Project />
  <Footer />
</template>

<script>
import Header from './components/Header.vue';
import Section from './components/Section.vue';
import Project from './components/Project.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    Header,
    Section,
    Project,
    Footer,
  },
};
</script>
