<template>
    <div class="card">
        <div class="info">
            <h1 class="title">Título de proyecto</h1>
            <p class="description">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                Eius esse corporis, velit porro impedit laudantium accusamus! Id velit, 
                illum magni rem mollitia blanditiis iste maiores optio ipsa, est dolorem 
                fugit.
            </p>
            <button class="button">Ver más</button>
        </div>
    </div>
</template>

<style scoped>
.card {
  border-radius: 16px;
  margin: 0 auto;
  width: 540px;
  max-width: 100%;
  min-height: 300px;
  box-shadow: 0px 3px 5px -1px rgba(0, 0, 0, 0.2),
    0px 5px 8px 0px rgba(0, 0, 0, 0.14),
    0px 1px 14px 0px rgba(0, 0, 0, 0.12);
  overflow: hidden;
  background-image: url(@/static/project/default.jpg);
  background-size: cover;
}
.info {
  position: relative;
  width: 100%;
  height: 300px;
  background-color: #fff;
  transform: translateY(100%)
    translateY(-88px)
    translateZ(0);
  transition: transform 0.5s ease-out;
}
.info:before {
  z-index: -1;
  display: block;
  position: absolute;
  content: ' ';
  width: 100%;
  height: 100%;
  overflow: hidden;
  filter: blur(10px);
  background-size: cover;
  opacity: 0.25;
  transform: translateY(-100%)
    translateY(88px)
    translateZ(0);
  transition: transform 0.5s ease-out;
}
.card:hover .info,
.card:hover .info:before {
  transform: translateY(0) translateZ(0);
}

.title {
  margin: 0;
  padding: 24px;
  font-size: 40px;
  font-weight: bold;
  line-height: 1;
  color: rgba(0, 0, 0, 0.87);
}
.description {
  margin: 0;
  padding: 0 24px 24px;
  font-size: 18px;
  line-height: 1.5;
}
.button {
    color: white;
    background-color: #52B96F;
    padding: 12px 16px;
    border-radius: 12px;
    margin-left: 24px;
}
.button:hover,
.button:focus {
    color: white;
    background-color: #3b814f;
    cursor: default;
}
h1 {
  margin-bottom: 0.5em;
  font-weight: inherit;
  line-height: 1.2;
  color: #1c5b72;
  font-size: 2.618em
}

@media (min-width:800px) {
  h1 {
    font-size: 4.236em;
    font-weight: 300
  }
}

p {
  margin-bottom: 1.3em;
  line-height: 1.618
}

@media (min-width:800px) {
  p {
    font-size: 1.3em
  }
}

a {
  color: #e03616;
  text-decoration: none
}
</style>