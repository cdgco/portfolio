<script setup>
import { ref } from 'vue'

defineProps({
  title: String,
  subtitle: String,
  description: String,
  date: String,
  image: String,
  color: String,
  gradColor: String,
  builtwith: String
})
</script>

<template>
  <div class="flex content-start border-b">
    <div class="containter m-auto xl:w-3/6 lg:w-5/6 p-10 font-sans text-left">
      <h2 :class="'text-'+color+'-400'" class="font-normal pb-2 text-2xl">{{subtitle}}</h2>
      <span class="inline-flex items-baseline"><h1 class="font-extrabold text-3xl">{{title}}</h1> <h2 class="pl-2 font-bold text-gray-500 text-md">{{ date }}</h2></span>
      <div class="grid grid-cols-3 gap-8 pt-10">
          <div class="col-span-3 sm:col-span-1 relative inline-grid">
            <img :src="image" class="rounded-2xl shadow">
            <button type="button" :class="['bg-'+color+'-500', 'hover:bg-'+color+'-600' ]" class="absolute shadow bottom-6 -right-3 z-20 rounded-lg text-white font-medium transition-colors duration-150 cursor-pointer hover:bg-primary-600 focus:bg-primary-600 inline-flex items-center flex-row-reverse px-5 py-2">
            <span class="w-4 h-4 inline-flex items-center ml-1">
              <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg" class="stroke-2 inline-block h-4 w-4">
                <g>
                  <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                  <polyline points="15 3 21 3 21 9"></polyline><line x1="10" y1="14" x2="21" y2="3"></line>
                </g>
              </svg>
            </span> Check it out <!----></button>
          <div :class="'from-'+color+'-700'" class="overlay bg-gradient-to-tl via-transparent absolute w-full h-full rounded-2xl"></div>
        </div>
        <div class="col-span-3 sm:col-span-2 text-gray-600 relative">
            <p>{{ description }}</p>
            <div class="absolute bottom-0 right-0 text-sm font-medium p-2 inline-flex items-center">
                <p class="h-full pr-4">BUILT WITH</p>
                <img class="rounded-lg shadow h-10 w-10" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAFAAAABQCAYAAACOEfKtAAAAAXNSR0IArs4c6QAAAERlWElmTU0AKgAAAAgAAYdpAAQAAAABAAAAGgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAUKADAAQAAAABAAAAUAAAAAAx4ExPAAAFtElEQVR4Ae3b+W8WRRgH8Gdfjp4EaLkE+/ZujcYo4hGNf4lnKliFmmpTbRo5JGiCinggKpFUKGBBDSbGGAOIR1SIMYqAYLkECqJyQ1UKbd/xed733aSV993uPrMzs42zv/TYmdl5Pv3Ott3DiW/pF2A3tkCM3dN2TApYQMkgWEALKCkg2d0m0AJKCkh2twm0gJICkt1tAi2gpIBkd5tACygpINndJtACSgpIdh8p2V9r9xvHADxT68AIJ/hh/+kHeGqvgBM9wft69Rg2gDcg3ru3ODB2VHC9HrzkWfdT+HgEOyzOgdcXAnRI4M3cKWDbOa8c8fdFHvC6NN44RvIuJwTMQrxvzvKBhuoZacBaxFuPyRs/OviyJbx6xPtaIR7hRhawuiCFV8TAu4J4j+4S8OWZofIjvz+SgIS3YYYDxRJ4n5+Wx/EzQuQAK/NTyZvAwOvF5M3ZLWCrJjwCjhRgBeJR8ibmBD/n9SFeA+JtOeUnN+G1iQxgeRpvEhPvsZ8FbNKMF5kEluYBvIfJm8zA6xcCGhHv05PhpSrISMYTGEe89yXwHke8TwzhGU8g4VHypuQGP+clMHlNewR8/GeQvITf1lgCS3JTvzCmMvGaEe+jP8IHCTqiEcBpabxpTLwn8arKhxHAI2ztgFMRj5bttXnBl63AZduCeBt/D5oTde21Al6Tk8IrYeK1/iLggwjhaU3glDRenIn3dKeADSfUJYk7spYETk7jleYHX7ZU2Lx9Ajp+45aotp9ywEmjU8u2jIk3vzMB646rRZAZXSmgi1fOxFu4LwFrIoxH8MoAJ2Ly1uNv24oC3rJdtD8Bq47JZENPXyWAE9J4VUy85xCvrUsPgOxRQr8rVzwqdT2vmom3+EACVmbBG4OznVPmwEheqGHtcQFdl2TJBvcPFbCI8HDZ1hTyKnzhYAJWHB08QferwhEAa6c7MH0sb+wlOHbYeDS3UJfwI6UO1DLxqMA3j7hcgz8S3jq8ucTFW3ooAcuzjD34SMG/ChVwySEBm08Gf2/nZY8CCxBvjUTyXvlVwLLDwWH89ggVsA/t6J7EZ6f8I76KBb6WpUAXb8Y43rJdhmPT+Cq3UAFpor04X7qluPX00BN//bAASkimLR+T147Ju5WJtxzHXppl7EzH434vdECaSBIRb2p/4YH4Bhb4Ei75TFsezqr9ZgduY+K9dUQAnU50bEoAaeJXcP70ZMBXZ64uhAp8MUuBSTxM3u3ject2BY79/MGrj6kKUxmgi/gwPV4xAPHto9kLzMXZrEa8O5h4K3HsxRrxqEZHx+uuOQjzDi7Jzm6AZw9kTkcSD9vcWcRLXluXgEX7M4+tKn3aAOlA9KABLetMGwGvRry7mHirEG+hATyqRekSHojlhUfp5OK1HzOHpxVwIKb7eXJp3+TA3czk0f+2C/Biq8lNWwL/WyThtRFeMe+c14F48/Ayv+nNGCAVzqNLkV1OmKZLHd8YIAE8hH/ifHuWl6K6uAMLamR+BOH8AIwB0vSTiPj0/HYm4kxEnFttFtEoICH2YBLpFYTvzvGSWI+X0FqrzCEaByTES4j44A4B35/nIc7Gq9QtlWYQIwHoIj4ggdhQ7kBzhX7EyAASIr2ORUn8gZnERgRs0owYKUBC/BsRKYk7LvCW8xMI2FhOI+nZIgdIZf+FiPcj4k4mYnNlDBrK/seAVHp3H8B9iLjrIi+JLVUxmF2qHjGSCXTLvkiIPwrYzURsrY5BfdwdTc3HSANSyRcQ8V5E3NPNS+LcmhjMUogYeUAX8R5E3MtEnI+IdSVqEhjqkwlqppga9XwvACE2VQAw3nwFetQknhf+ox1aLumrhDU99rBYwqaRvI5vAb10fOyzgD6QvJpYQC8dH/ssoA8kryYW0EvHxz4L6APJq4kF9NLxsc8C+kDyamIBvXR87LOAPpC8mlhALx0f+yygDySvJv8C/XLIi5hrhdgAAAAASUVORK5CYII=">
            </div>
        </div>
        
      </div>
    </div>
  </div>
</template>
<style scoped>
</style>
