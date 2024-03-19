<template>
<div>
    <Navbar/>
    
    <main class="container p-3 my-5 border rounded shadow">
       <slot></slot> 
    </main>

    <Footer/>
    
</div>
</template>

<script setup>
useHead({

    // base de mi titulo
   titleTemplate: "%s - Intro Nuxt",
   bodyAttrs: [{
        class: "text-center",
   }],
    link:[
        {
            rel: "stylesheet",
            href: "https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css",
            integrity:"sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH",
            crossorigin:"anonymous"
        }
    ],
    script:[
        {
            src: "https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" 
            
        }
    ]
})

</script>
