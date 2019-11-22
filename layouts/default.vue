<template>
  <div class="wrapper container">
    <Sidebar />

    <main class="content">
      <Header />
      <Breadcrumbs />
      <nuxt />
    </main>
  </div>
</template>

<script>
import Sidebar from "@/components/Sidebar";
import Header from "@/components/Header";
import Breadcrumbs from "@/components/Breadcrumbs";

export default {
  components: {
    Sidebar,
    Header,
    Breadcrumbs
  }
};
</script>

<style lang="scss">
.wrapper {
  display: flex;
}
.sidebar {
  flex: 0 0 100%;
  max-width: 150px;
}
.content {
  flex: 0 0 100%;
  max-width: calc(100% - 150px);
  padding: 20px 50px;
}
</style>
