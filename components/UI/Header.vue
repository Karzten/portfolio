<template>
    <div>
        <header class="">
            <div class="logo">
                Homero Zegarra
            </div>
            <div class="menu-options">
                <router-link to="/">Inicio</router-link>
                <router-link to="/about">Sobre mí</router-link>
                <router-link to="/contact">Proyectos</router-link>
                <router-link to="/contact">Contacto</router-link>
            </div>
        </header>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
header{
    padding: 0.5rem 1.25rem;
    font-family: 'Oxanium', sans-serif;
    font-weight: bold;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.logo {
    font-size: 2.5rem;
}
.menu-options{
    font-size: 1.5rem;
    display: flex;
    flex-direction: row;
    gap: 48px;
    justify-content: center;
}
</style>