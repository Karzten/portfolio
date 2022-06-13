<template>
    <div class="about-me">
        <div class="about-me-title">
            <h1>Hola. Mi nombre es Homero, un gusto</h1>
        </div>
        <div class="about-me-content">
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Architecto, sunt. Illum, excepturi repellat eos quo consequuntur iste tenetur ratione, 
               saepe debitis officia placeat error corporis laboriosam. Deserunt facilis veniam aliquam!. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Architecto, sunt. Illum, excepturi repellat eos quo consequuntur iste tenetur ratione, 
               saepe debitis officia placeat error corporis laboriosam. Deserunt facilis veniam aliquam!
            </p>
        </div>
    </div>
</template>

<style scoped>
.about-me {
    font-family: 'Oxanium', sans-serif;
    background-color: #52B96F;
    margin-top: 64px;
    padding: 42px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 24px;
    color: #fff;
}
.about-me-title {
    font-size: 2rem;
    font-weight: bold;
}
.about-me-content {
    font-size: 1.625rem;
}
@media screen and (min-width: 300px) and (max-width: 600px) {
    .about-me-title {
        font-size: 1.6rem;
    }
    .about-me-content {
        font-size: 1.1rem;
    }
}
@media screen and (min-width: 601px) and (max-width: 768px) {
    .about-me-title {
        font-size: 2rem;
    }
    .about-me-content {
        font-size: 1.25rem;
    }
}
@media screen and (min-width: 769px) and (max-width: 1024px) {
    .about-me-title {
        font-size: 2.2rem;
    }
    .about-me-content {
        font-size: 1.5rem;
    }
}
</style>