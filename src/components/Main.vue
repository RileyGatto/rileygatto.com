<template>
  <div class="Container" @click="toggleSection('work')">
    <h2>Work</h2>
  </div>
  <transition name="fade">
        <div v-show="sections.work">
            <div class="Container">
            <h3>Trainee IT Support Administrator</h3>
            <h4><a href="https://www.griffith.nsw.gov.au/Home" target="blank">Griffith City Council</a></h4>
            <h5>August 2025 - Current</h5>
            </div>
            <div class="Container">
            <h3>Data Analyst / Developer Internship</h3>
            <h4><a href="https://www.debortoli.com.au" target="blank">De Bortoli Wines</a></h4>
            <h5>June 2025 - June 2025</h5>
            </div>
        </div>
   </transition>

  <div class="line"></div>

  <div class="Container" @click="toggleSection('projects')">
    <h2>Projects</h2>
  </div>
  <transition name="fade">
      <div v-show="sections.projects">
        <div class="Container">
          <h3>Automated Plant Watering System</h3>
          <h4><a href="https://github.com/RileyGatto/Automated-Watering-System" target="blank">Embedded System</a></h4>
          <h5>May 2025 - June 2025</h5>
        </div>
        <div class="Container">
          <h3>NVIM Configurations</h3>
          <h4><a href="https://github.com/RileyGatto/nvim" target="blank">LUA</a></h4>
          <h5>July 2025 - July 2025</h5>
        </div>
        <div class="Container">
          <h3>AI Disable Navigation System</h3>
          <h4><a href="https://github.com/RileyGatto/Griffith-Wheelchair-Navigation-System" target="blank">Python</a></h4>
          <h5>March 2025 - May 2025</h5>
        </div>
     </div>
  </transition>

  <div class="line"></div>

  <div class="Container" @click="toggleSection('education')">
    <h2>Education</h2>
  </div>
  <transition name="fade">
      <div v-show="sections.education">
        <div class="Container">
          <h3>Bachelor of Computer Science</h3>
          <h4><a href="https://www.deakin.edu.au" target="blank">Deakin University</a></h4>
          <h5>March 2024 - Current</h5>
        </div>
        <div class="Container">
          <h3>Certificate IV Information Technology</h3>
          <h4><a href="https://www.austrg.com.au" target="blank">ATC</a></h4>
          <h5>August 2025 - Current</h5>
        </div>
        <div class="Container">
          <h3>Marian Catholic College</h3>
          <h4><a href="https://ww.catholic.edu.au" target="blank">HSC</a></h4>
          <h5>February 2018 - December 2023</h5>
        </div>
      </div>
  </transition>
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
    background-color: #242424;
    border-radius: 5px;
    margin: 10px auto;
    }

    a {
    text-decoration: none;
    
    }

    h3 {
    border-bottom: 2px solid gray;
    }

</style>
