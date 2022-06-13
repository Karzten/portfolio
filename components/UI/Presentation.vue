<template>
    <div class="presentation">
        <div class="presentation-title">
            <h1>Desarrollador Frontend y Diseñador UX/UI</h1>
        </div>
        <div class="presentation-subtitle">
            <h2>Me gusta diseñar y programar para hacer realidad mis ideas</h2>
        </div>
        <div class="presentation-image">
            <img src="@/assets/images/presentation-image.png" alt="Laptop verde" width="662px" height="580px">
        </div>
    </div>
</template>

<style scoped>
.presentation {
    font-family: 'Oxanium', sans-serif;
    margin-top: 120px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 24px;   
    text-align: center;
    padding: 0 20px;
}
.presentation-title {
    font-size: 2.5rem;
    font-weight: bold;
}
.presentation-subtitle {
    font-size: 1.625rem;
}
@media screen and (min-width: 300px) and (max-width: 600px) {
    .presentation {
        margin-top: 100px;
    }
    .presentation-title {
        font-size: 1.6rem;
    }
    .presentation-subtitle {
        font-size: 1.1rem;
    }
}
@media screen and (min-width: 601px) and (max-width: 768px) {
    .presentation-title {
        font-size: 2rem;
    }
    .presentation-subtitle {
        font-size: 1.25rem;
    }
}
@media screen and (min-width: 769px) and (max-width: 1024px) {
    .presentation-title {
        font-size: 2.2rem;
    }
    .presentation-subtitle {
        font-size: 1.5rem;
    }
}
</style>