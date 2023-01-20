<template>
    <div>
        <header>
            <Navbar/>
        </header>
        <main class="container p-3 my-5 border rounded shadow text-center">
            <slot></slot>
        </main>
        
        <Footer/>
    </div>
</template>

<script setup>
    useHead({
        titleTemplate:"%s - Aprendiendo Nuxt",
        
        link: [
            {
                rel:"stylesheet",
                href: "https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css",
                integrity: "sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3",
                crossorigin: "anonymous"
            }
        ],
        script: [
            {
                src: "https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js",
            }
        ]
    })
    const currentYear = new Date().getUTCFullYear();
</script>