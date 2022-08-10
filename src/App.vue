<script setup>
import Navbar from './components/Navbar.vue'
import FullHeader from './components/FullHeader.vue'
import SmallHeader from './components/SmallHeader.vue'
import SmallProject from './components/SmallProject.vue'
import LargeProject from './components/LargeProject.vue'
import ProjectGrid from './components/ProjectGrid.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import ContactCard from './components/ContactCard.vue'
import Footer from './components/Footer.vue'

import imgUrl2 from './assets/01v.png'
import vue from './assets/icons/vue.svg' 
import php from './assets/icons/php-alt.svg' 
import bootstrap from './assets/icons/bootstrap.svg' 
import mysql from './assets/icons/mysql.svg' 
import socketio from './assets/icons/socket.io.svg' 
import electron from './assets/icons/electron.svg' 
import express from './assets/icons/express.svg' 
import node from './assets/icons/nodejs-icon.svg' 
import jquery from './assets/icons/jquery-icon.svg'
import mongo from './assets/icons/mongodb-icon.svg' 
import elastic from './assets/icons/elasticsearch.svg' 
import handlebars from './assets/icons/handlebars.svg' 
import cplusplus from './assets/icons/c-plusplus.svg' 
import puppeteer from './assets/icons/puppeteer.svg' 
var opencl = "https://upload.wikimedia.org/wikipedia/commons/b/b8/OpenCL.jpg"; 

var about = 
`
    class Carter {
        protected $skills = [
            'APIs'                  => ['openapi', 'postman', 'RESTful']
            'C / C++'               => ['opencl'],
            'CSS'                   => ['bootstrap', 'sass', 'tailwind' ],
            'JavaScript'            => ['electron', 'express', 'jquery', 'nodejs', 'vue'],
            'PHP'                   => ['composer'],
            'Python',
            'SQL',                  => ['mariadb', 'mysql', 'postgresql'],
            'System Administration' => ['active directory', 'esxi', 'mecm'],
            'MongoDB',
        ];

        public function __construct() {
            $this->name = 'Carter Roeser';
            $this->age = date("Y") - 2002;
            $this->location = 'Corvallis, OR';
            $this->interests = ['programming', 'music', 'technology'];
        }
    }`;
</script>

<template>
  <Navbar title="Carter Roeser" linkTitle="Blog" link="https://blog.cjroeser.com" />
  <div class="flex flex-col items-center">
    <FullHeader msg="Carter Roeser"/>
    <LargeProject title="Vesta Web Interface" subtitle="Hosting Control Panel" date="2017" textColor="text-indigo-400" buttonColor="bg-indigo-500" buttonHover="bg-indigo-600" link="https://vwi.cdgtech.one" :icons="[php, bootstrap, mysql, jquery]" description="PHP interface for VestaCP, providing a modern, customizable control panel featuring plugins, integrations and branding necessary for any web host. VWI has thousands of downloads and has been claimed by many customers to be an essential piece of any Vesta system."/>
    <LargeProject title="01V Web Controller" subtitle="Remote Mixer" date="2020" textColor="text-red-400" buttonColor="bg-red-500" buttonHover="bg-red-600" link="https://github.com/cdgco/01v-web-controller" :image="imgUrl2" :icons="[node, express, electron, socketio]" description="Multi-device real time remote controller for Yamaha 01V digital mixer. Portable Web App that allows multiple devices to wirelessly mix sound on a 26-year-old mixer."/>
    <LargeProject title="COE Tools" subtitle="IT Tool Management" date="2021" textColor="text-orange-400" buttonColor="bg-orange-500" buttonHover="bg-orange-600" link="https://github.com/cdgco/coetools" :icons="[php, bootstrap, mysql, jquery]" description="Dynamic tool management system for IT departments. Features an LDAP authenticated role system with users and admins, a customizable interface with light / dark mode and a drag-and-drop editor, favorite tools and tool history, tool search, sorting and categorization and embedded tool support."/>
    <ProjectGrid>
      <SmallProject title="SmartAssets" subtitle="Modern Asset Management" date="2022" textColor="text-blue-400" buttonColor="bg-blue-500" buttonHover="bg-blue-600" link="https://github.com/cdgco/SmartAssets" :icons="[node, vue, express, mongo, elastic]" description="SmartAssets is an API first asset management system, built for IT professionals with integration and expansion in mind. It features native barcode support, label printing, a built in barcode scanner, and much more."/>
      <SmallProject title="SmartLists" subtitle="Music Visualization Platform" date="2022" textColor="text-green-400" buttonColor="bg-green-500" buttonHover="bg-green-600" link="https://github.com/cdgco/smartlists" :icons="[node, handlebars, express, mongo]" description="SmartLists is a music visualization platform that allows users to view the metadata from their Spotify playlists through a range of interactive 2D, 3D, and AI generated graphs and art."/>
      <SmallProject title="Dream API" subtitle="API for Wombo Dream" date="2022" textColor="text-amber-400" buttonColor="bg-amber-500" buttonHover="bg-amber-600" link="https://cdgco.github.io/dream-api/" :icons="[node]" description="Dream API is an unofficial promise based NodeJS API for Wombo Dream, allowing you to generate AI images from Wombo Dream directly from your application."/>
      <SmallProject title="PHP REST Service" subtitle="Express-Like API Server" date="2022" textColor="text-cyan-400" buttonColor="bg-cyan-500" buttonHover="bg-cyan-600" link="https://cdgco.github.io/php-rest-service/" :icons="[php]" description="PHP REST Service is a simple, fast, and lightweight API framework for PHP, featuring regex support, JSON, XML, and plaintext responses, OpenAPI specification generation, parameter validation, custom error handling, logging, access control, formatting functions, and more."/>
      <SmallProject title="RayTracer" subtitle="Accelerated Ray Tracer" date="2019" textColor="text-teal-400" buttonColor="bg-teal-500" buttonHover="bg-teal-600" link="https://github.com/cdgco/raytracing" :icons="[cplusplus, opencl]" description="An accelerated ray tracer for comparing 3D rendering speeds for the same environment across different non-accelerated, software accelerated and hardware accelerated rendering techniques."/>
      <SmallProject title="Warranty Tool" subtitle="CLI Warranty Lookup Tool" date="2022" textColor="text-rose-400" buttonColor="bg-rose-500" buttonHover="bg-rose-600" link="https://cdgco.github.io/warrantytool/" :icons="[node, puppeteer]" description="Quickly look up Dell and HP warranties from your command line. Formats computer information and warranty list into a clean table and returns the status of the warranty."/>
    </ProjectGrid>
    <SmallHeader msg="About Me"/>
    <About :msg=about />
    <SmallHeader msg="Employ Me" />
    <Contact>
        <ContactCard title="Email" subtitle="carter@cdgtech.one" icon="envelope-o" link="mailto:carter@cdgtech.one" />
        <ContactCard title="LinkedIn" subtitle="@CarterRoeser" icon="linkedin" link="https://linkedin.com/in/CarterRoeser" />
        <ContactCard title="GitHub" subtitle="@cdgco" icon="github" link="https://github.com/cdgco" />
      </Contact>
    <Footer msg="Carter Roeser" />
    
  </div>
</template>

<script>
export default {
    created() {
      $("#app").scroll(function() {
        var scroll = $(this).scrollTop();
        if (scroll > 0 && $("#nav").css("opacity") == 0) {
          $("#nav").fadeTo(500, 1)
          console.log("fade in")
        } else if (scroll == 0 && $("#nav").css("opacity") != 0) {
          $("#nav").fadeTo(500, 0)
          console.log("fade out")
        }
      }).scroll();
    },
};
</script>