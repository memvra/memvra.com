<script setup>
import HeroSection from './components/HeroSection.vue'
import ProblemSolution from './components/ProblemSolution.vue'
import FeaturesGrid from './components/FeaturesGrid.vue'
import WhyMemvra from './components/WhyMemvra.vue'
import HowItWorks from './components/HowItWorks.vue'
import InstallSection from './components/InstallSection.vue'
import SupportedTools from './components/SupportedTools.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <div class="min-h-screen bg-[#0a0a0a]">
    <HeroSection />
    <ProblemSolution />
    <FeaturesGrid />
    <WhyMemvra />
    <HowItWorks />
    <InstallSection />
    <SupportedTools />
    <FooterSection />
  </div>
</template>
