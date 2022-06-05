<template>
    <footer>
        <div class="footer-container">
            <div class="contact-section">
                <div class="work-together">
                    TRABAJEMOS JUNTOS
                </div>
                <div class="contact-text">
                    Si estás interesado en mi perfil, envíame un e-mail
                </div>
                <div class="contact-button">
                    <button>
                        CONTÁCTAME
                    </button>
                </div>
            </div>
            <div class="social-network">
                <a href="">
                    <img src="social/behance.png" alt="behance">
                </a>
                <a href="https://www.linkedin.com/in/luis-homero-zegarra-fern%C3%A1ndez-031a41200/">
                    <img src="social/linkedin.png" alt="linkedin">
                </a>
            </div>
            <span>Diseñado y codeado por mí. Copyright by KarztenDev</span>
        </div>
    </footer>
</template>

<style scoped>
    footer{
        background-color: #52B96F;
        padding: 25px 20px;
        text-align: center;
        margin-top: 100px;
    }
    .footer-container{
        display: flex;
        flex-direction: column;
        font-family: 'Oxanium', sans-serif;
        font-weight: 600;
        font-size: 1.625rem;
        gap: 56px;
        color: #fff;
    }
    .social-network{
        display: flex;
        flex-direction: row;
        gap: 16px;
        justify-content: center;
    }
    .contact-section{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        background-color: #278E44;
        border-radius: 12px;
        align-items: center;
        padding: 24px 32px;
        position: relative;
        top: -80px;
    }
    .contact-text{
        width: 25%;
        text-align: center;
        font-weight: 300;
    }
    .contact-button button{
        background-color: #278E44;
        border-radius: 12px;
        border: 2px solid #fff;
        color: #fff;
        font-size: 1.425rem;
        font-weight: 900;
        padding: 16px;
    }
    .contact-button button:hover{
        background-color: #fff;
        border: 2px solid #fff;
        color: #278E44;
    }
</style>