<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import FullHeader from './components/FullHeader.vue'
import Project from './components/Projects.vue'
import ProjectB from './components/ProjectsB.vue'
</script>

<template>
  <FullHeader msg="Carter Roeser" />
  <ProjectB title="Vesta Web Interface" subtitle="Hosting Control Panel" link="" description="PHP interface for VestaCP, providing a modern, customizable control panel featuring plugins, integrations and branding necessary for any web host. VWI has thousands of downloads and has been claimed by many customers to be an essential piece of any Vesta system." date="2017" image="https://cdgtech.one/images/VWI-HWI.png" gradColor="" color="indigo" builtwith="" />
  <Project title="01V Web Controller" subtitle="Remote Mixer" date="2020" link="" description="Multi-device real time remote controller for Yamaha 01V digital mixer. Portable Web App that allows multiple devices to wirelessly mix sound on a 26-year-old mixer." image="https://cdgtech.one/images/IMG_9989.jpg" color="red" gradColor="red" builtwith="" />
  <ProjectB title="COE Tools" subtitle="IT Tool Management" date="2021" link="" description="Dynamic tool management system for IT departments. Features an LDAP authenticated role system with users and admins, a customizable interface with light / dark mode and a drag-and-drop editor, favorite tools and tool history, tool search, sorting and categorization and embedded tool support." gradColor="" image="https://github.com/cdgco/coetools/raw/master/docs/light-home.png?raw=true" color="yellow" builtwith="" />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
