<template>
    <div>
        <header class="header" :class="scrolled ? 'scroll' : ''">
            <nav class="nav">
                <a href="#" class="logo">Homero Zegarra</a>
                <button class="nav-toggle" :aria-label="showSidebar ? 'Cerrar menú' : 'Abrir menú'" @click="openRespMenu()">
                    <IconBurgerMenu :animate="showSidebar" />
                </button>
                <ul class="nav-menu" :class="{'nav-menu_visible': showSidebar}">
                    <li class="nav-menu-item"><router-link to="/" class="nav-menu-link nav-link nav-menu-link_active">Inicio</router-link></li>
                    <li class="nav-menu-item"><router-link to="/" class="nav-menu-link nav-link">Sobre mí</router-link></li>
                    <li class="nav-menu-item"><router-link to="/" class="nav-menu-link nav-link">Proyectos</router-link></li>
                    <li class="nav-menu-item"><router-link to="/" class="nav-menu-link nav-link">Contacto</router-link></li>
                </ul>
            </nav>
        </header>
    </div>
</template>

<script>
export default {
    data(){
        return {
            showSidebar: false,
            scrolled: false
        }
    },
    components: {
        IconBurgerMenu: () => import('@/components/Icons/IconBurgerMenu.vue'),
    },
    methods: {
        openRespMenu() {
            this.showSidebar = !this.showSidebar
        },
        handleScroll () {
            if (typeof window !== 'undefined') {
                this.scrolled = window.scrollY > 0;
            }
        }
    },
    created () {
        if (typeof window !== 'undefined') {
            window.addEventListener('scroll', this.handleScroll);
        }

    },
    destroyed () {
        if (typeof window !== 'undefined') {
            window.removeEventListener('scroll', this.handleScroll);
        }
    }
}
</script>

<style scoped>
.header{
    padding: 0.5rem 1.25rem;
    font-family: 'Oxanium', sans-serif;
    font-weight: bold;
    height: 80px;
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background-color: #fff;
}

.scroll {
    box-shadow: 0 0 16px 0 rgba(0,0,0,.13);
    transition: background 0.3s,border 0.3s,border-radius 0.3s,box-shadow 0.3s;
    z-index: 3;
}

.nav{
    display: flex;
    justify-content: space-between;
}
.logo {
    font-size: 2.5rem;
    line-height: 65px;
}

.nav-menu {
    display: flex;
    flex-direction: row;
    gap: 48px;
}

.nav-menu-item{
    font-size: 1.5rem;
    line-height: 65px;
    text-transform: uppercase;
    width: max-content;
}

.nav-menu-link:hover,
.nav-menu-link_active{
    color: #52B96F;
    transition: 0.5s;
}

.nav-toggle{
    width: 35px;
    height: 35px;
    line-height: 60px;
    display: none;
}

@media (max-width: 1024px) {
    .header{
        height: 65px;
    }
    .logo {
        font-size: 2rem;
        line-height: 50px;
    }

    .nav-menu {
        flex-direction: column;
        gap: 20px;
        background-color: #fff;
        position: fixed;
        left: 100%;
        top: 65px;
        width: 100%;
        height: calc(100% - 60px);
        overflow-y: auto;
        align-items: center;
        padding: 20px 0;
        transition: left 0.5s;
    }

    .nav-menu-item{
        line-height: 70px;
    }

    .nav-menu-link:hover,
    .nav-menu-link_active{
        color: #52B96F;
        transition: 0.5s;
    }

    .nav-toggle{
        display: block;
    }

    .nav-menu_visible{
        left: 0;
    }

    .nav-toggle:focus:not(:focus-visible){
        outline: none;
    }
}

@media (max-width: 768px) {
  .logo {
    font-size: 1.75rem;
    line-height: 50px;
  }
}

@media (max-width: 320px) {
  .logo {
    font-size: 1rem;
    line-height: 50px;
  }
}
</style>
