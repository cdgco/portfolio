<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import FullHeader from './components/FullHeader.vue'
import ProjectA from './components/ProjectsA.vue'
import ProjectB from './components/ProjectsB.vue'
import imgUrl1 from './assets/vwi.png'
import imgUrl2 from './assets/01v.png'
import imgUrl3 from './assets/coetools.png'
</script>

<template>
  <div>
    <FullHeader msg="Carter Roeser" />
    <ProjectB title="Vesta Web Interface" subtitle="Hosting Control Panel" link="https://vwi.cdgtech.one" description="PHP interface for VestaCP, providing a modern, customizable control panel featuring plugins, integrations and branding necessary for any web host. VWI has thousands of downloads and has been claimed by many customers to be an essential piece of any Vesta system." date="2017" image=imgUrl1 color="indigo" builtwith="" />
    <ProjectA title="01V Web Controller" subtitle="Remote Mixer" date="2020" link="https://github.com/cdgco/01v-web-controller" description="Multi-device real time remote controller for Yamaha 01V digital mixer. Portable Web App that allows multiple devices to wirelessly mix sound on a 26-year-old mixer." image=imgUrl2 color="red" builtwith="" />
    <ProjectB title="COE Tools" subtitle="IT Tool Management" date="2021" link="https://github.com/cdgco/coetools" description="Dynamic tool management system for IT departments. Features an LDAP authenticated role system with users and admins, a customizable interface with light / dark mode and a drag-and-drop editor, favorite tools and tool history, tool search, sorting and categorization and embedded tool support." image=imgUrl3 color="yellow" builtwith="" />
  </div>
</template>
