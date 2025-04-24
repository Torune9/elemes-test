<template>
  <!-- Navigation -->
  <NavBar />
  <!-- Main Content -->
  <main>
    <MainLayout />
  </main>
  <!-- Mobile Bottom Navigation -->
  <MobileBottomNav />
  <!-- Footer -->
  <FooterSection />
</template>

<script setup>
import NavBar from './components/navigation/NavBar.vue';
import MobileBottomNav from './components/navigation/MobileBottomNav.vue';
import MainLayout from './layouts/MainLayout.vue'
import FooterSection from './components/pages/FooterSection.vue';
</script>