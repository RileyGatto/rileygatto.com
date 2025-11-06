<template>
  <div class="Container" @click="toggleSection('work')">
    <h2>Work</h2>
  </div>
  <transition name="fade">
        <div v-show="sections.work">
            <div class="Container">
            <h3>Trainee IT Support Administrator</h3>
            <h4>Griffith City Council</h4>
            <h5>August 2025 - Current</h5>
            </div>
            <div class="Container">
            <h3>Data Analyst / Developer Internship</h3>
            https://google.com
            <h5>June 2025 - June 2025</h5>
            </div>
        </div>
   </transition>

  <div class="line"></div>

  <div class="Container" @click="toggleSection('projects')">
    <h2>Projects</h2>
  </div>
  <div v-show="sections.projects">
    <div class="Container">
      <h3>Automated Plant Watering System</h3>
      <h4>Embedded System</h4>
      <h5>May 2025 - June 2025</h5>
    </div>
    <div class="Container">
      <h3>NVIM Configurations</h3>
      <h4>LUA</h4>
      <h5>July 2025 - July 2025</h5>
    </div>
    <div class="Container">
      <h3>AI Disable Navigation System</h3>
      <h4>Python</h4>
      <h5>March 2025 - May 2025</h5>
    </div>
  </div>

  <div class="line"></div>

  <div class="Container" @click="toggleSection('education')">
    <h2>Education</h2>
  </div>
  <div v-show="sections.education">
    <div class="Container">
      <h3>Bachelor of Computer Science</h3>
      <h4>Deakin University</h4>
      <h5>March 2024 - Current</h5>
    </div>
    <div class="Container">
      <h3>Certificate IV Information Technology</h3>
      <h4>ATC</h4>
      <h5>August 2025 - Current</h5>
    </div>
    <div class="Container">
      <h3>Marian Catholic College</h3>
      <h4>HSC</h4>
      <h5>February 2018 - December 2023</h5>
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue';

const sections = reactive({
  work: false,
  projects: false,
  education: false
});

function toggleSection(section) {
  sections[section] = !sections[section];
}
</script>

<style scoped>
    .fade-enter-active, .fade-leave-active {
    transition: all 0.3s ease;
    }
    .fade-enter-from, .fade-leave-to {
    opacity: 0;
    transform: translateY(-10px);
    }

    .Container {
    background-color: rgba(255, 255, 255, 0.87);
    color: black;
    border-radius: 10px;
    margin: 10px auto;
    padding: 5px;
    cursor: pointer;
    }

    .line {
    width: 10px;
    height: 100px;
    background-color: #FFEE8C;
    border-radius: 5px;
    margin: 10px auto;
    }

    a {
    text-decoration: none;
    color: black;
    }

    h3 {
    border-bottom: 2px solid gray;
    }
</style>