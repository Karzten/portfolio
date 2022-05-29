<template>
    <div class="skills">
        <div class="skills-title">
            <h1>Mi experiencia</h1>
        </div>
        <div class="skills-content">
            <div v-for="skill in skills" :key="skill.index" class="skills-table">
                <div class="skill">
                    <div class="skill-main">
                        <div class="skill-img">
                            <img :src='skill.image'>
                        </div>
                        <div class="skill-title">
                            <h3> {{skill.title}} </h3>
                        </div>
                    </div>
                    <div class="skill-description">
                        <p> {{skill.description}} </p>
                    </div>
                    <div class="project-button">
                        <button>
                            <span class="font-black">VER PROYECTOS</span>
                        </button>
                    </div>
                    <div class="knowledges-list" v-if="skill.knowledgesString">
                        <span>Tengo conocimientos en:</span>
                        <span>{{ skill.knowledgesString }}</span>
                    </div>
                    <div class="knowledges-list" v-else>
                        <span>
                            Tengo conocimientos en:
                        </span>
                        <div class="knowledges-list-img">
                            <div v-for="knowledge in skill.knowledges" :key="knowledge.index" class="knowledge-element">
                                <img :src="knowledge.image" alt="">
                                <span> {{ knowledge.name }}</span>
                            </div>
                        </div>
                    </div>
                    <div class="frameworks-list" v-if="skill.frameworks">
                        <span>
                            Uso los frameworks:
                        </span>
                        <div class="framework-list-img">
                            <div v-for="framework in skill.frameworks" :key="framework.index" class="framework-element">
                                <img :src="framework.image" alt="">
                                <span> {{ framework.name }}</span>
                            </div>
                        </div>
                    </div>
                    <div class="widgets-list">
                        <span>Herramientas que uso:</span>
                        <div class="widget-list-img">
                            <div v-for="widget in skill.widgets" :key="widget.index" class="widget-element">
                                <img :src="widget.image" alt="">
                                <span> {{ widget.name }}</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            skills: [
                {
                    title: 'Diseño UX/UI',
                    image: 'skills/desing.png',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto, sunt. Illum, excepturi repellat eos quo consequuntur iste tenetur ratione',
                    knowledges: [
                        {
                            name: 'UX',
                            image: null,
                        },
                        {
                            name: 'UI',
                            image: null,
                        },
                        {
                            name: 'Desing Thinking',
                            image: null,
                        },
                        {
                            name: 'Atomic Design',
                            image: null,
                        }
                    ],
                    widgets: [
                        {
                            name: 'Figma',
                            image: 'skills/widgets/figma.png',
                        },
                        {
                            name: 'Whismical',
                            image: 'skills/widgets/whismical.png',
                        },
                        {
                            name: 'Photoshop',
                            image: 'skills/widgets/photoshop.png',
                        },
                        {
                            name: 'Balsamiq',
                            image: 'skills/widgets/balsamiq.png',
                        },
                        {
                            name: 'draw.io',
                            image: 'skills/widgets/draw.png',
                        },
                        {
                            name: 'Optimal',
                            image: 'skills/widgets/optimal.png',
                        },
                    ]
                },
                {
                    title: 'Desarrollo Frontend',
                    image: 'skills/frontend.png',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto, sunt. Illum, excepturi repellat eos quo consequuntur iste tenetur ratione',
                    knowledges: [
                        {
                            name: 'HTML',
                            image: 'skills/knowledges/html.png',
                        },
                        {
                            name: 'CSS',
                            image: 'skills/knowledges/css.png',
                        },
                        {
                            name: 'JavaScript',
                            image: 'skills/knowledges/javascript.png',
                        }
                    ],
                    frameworks: [
                        {
                            name: 'Vue.js',
                            image: 'skills/frameworks/vue.png',
                        },
                        {
                            name: 'Nuxt.js',
                            image: 'skills/frameworks/nuxt.png',
                        },
                        {
                            name: 'Tailwind',
                            image: 'skills/frameworks/tailwind.png',
                        }
                    ],
                    widgets: [
                        {
                            name: 'VS Code',
                            image: 'skills/widgets/vscode.png',
                        },
                        {
                            name: 'Github',
                            image: 'skills/widgets/github.png',
                        },
                        {
                            name: 'Bitbucket',
                            image: 'skills/widgets/bitbucket.png',
                        },
                    ]
                }
            ],
            knowledges: []
        }
    },
    created(){
        this.skills.forEach(skill => {
            for (let i = 0; i < skill.knowledges.length; i++) {
                if(!skill.knowledges[i].image){
                    skill.knowledgesString = skill.knowledges.map(knowledge => knowledge.name).join(', ');
                }
            }
        });
    }
}
</script>

<style scoped>
.skills {
    font-family: 'Oxanium', sans-serif;
    margin-top: 64px;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 56px;
}
.skills-title {
    font-size: 2rem;
    font-weight: bold;
    padding: 36px;
}
.skills-content{
    display: flex;
    flex-direction: row;
    text-align: center;
    gap: 24px;
}
.skills-table{
    width: 50%;
}
.skill{
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 48px;
}
.skill-main{
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 20px;
}
.skill-title{
    font-size: 1.625rem;
    font-weight: bold;
}
.skill-description{
    font-size: 1.625rem;
}
.project-button{
    background-color: #52B96F;
    font-size: 1.625rem;
    color: #fff;
    padding: 18.5px 29px;
    border-radius: 10px;
}
.knowledges-list{
    display: flex;
    flex-direction: column;
    gap:18px;
    font-size: 1.625rem;
    width: 50%;
}
.knowledges-list-img{
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    justify-content: space-between;
    gap: 18px;
}
.knowledge-element{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    text-align: center;
    gap: 16px;
    width: 100%;
}
.knowledge-element span{
    font-weight: bold;
}
.frameworks-list{
    display: flex;
    flex-direction: column;
    gap:18px;
    font-size: 1.625rem;
    width: 50%;
}
.framework-list-img{
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    justify-content: space-between;
    gap: 18px;
}
.framework-element{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    text-align: center;
    gap: 16px;
    width: 100%;
}
.framework-element span{
    font-weight: bold;
}
.widgets-list{
    display: flex;
    flex-direction: column;
    gap:18px;
    font-size: 1.625rem;
    width: 50%;
}
.widget-list-img{
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 18px;
    justify-content: space-between;
}
.widget-element{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    text-align: center;
    gap: 16px;
}
.widget-element span{
    font-weight: bold;
}
</style>