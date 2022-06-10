<template>
    <div class="projects">
        <div class="projects-title">
            <h1>Mis proyectos</h1>
        </div>
        <div class="projects-filter">
            <button>
                <span>Todos</span>
            </button>
            <button>
                <span>Diseño UX/UI</span>
            </button>
            <button>
                <span>Desarrollo Frontend</span>
            </button>
        </div>
        <div class="projects-cards">
            <Card />
        </div>
    </div>
</template>

<script>
import Card from '@/components/UI/Card.vue'
export default {
    components: {
        Card
    }
}
</script>

<style scoped>
.projects{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 48px;
    font-family: 'Oxanium', sans-serif;
}
.projects-title{
    font-size: 2rem;
    font-weight: bold;
    text-align: center;
    margin-top: 50px;
}
.projects-filter{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 20px;
}

.projects-filter button{
    color: #52B96F;
    border: 2px solid #52B96F;
    border-radius: 16px;
    padding: 16px;
    font-size: 1.625rem;
    font-weight: bold;
}

.projects-cards{
    display: grid;
    grid-template-columns: repeat(3, minmax(200px, 1fr));
    grid-gap: 32px;
    margin: 0px 20px;
    align-items: center;
    @media screen and (max-width: 1024px){
        grid-template-columns: repeat(2, minmax(200px, 1fr));
    }
    @media screen and (max-width: 600px){
        grid-template-columns: repeat(1, minmax(200px, 1fr));
    }
}
</style>