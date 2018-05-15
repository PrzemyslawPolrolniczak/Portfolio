<template>
    <div class="content-box">
        <div class="mini-navbar"></div>
        <div class="content">
            <h1 class="text-center">{{title}}</h1>
            <div class="container">
                <div class="photo"><img src="./assets/me.jpg" alt=""></div>
                <div class="text">Etiam risus metus, cursus sit amet convallis aliquet, aliquet vitae lorem. Nullam accumsan arcu quis ex porta cursus. Vivamus tempor leo eu odio porttitor, sed ultricies lectus tempus. Quisque eget magna metus. Phasellus malesuada eros id tellus commodo, in tristique odio viverra. Nullam sem turpis, accumsan semper turpis viverra, blandit accumsan nisi. Duis rhoncus, tortor quis rutrum porta, tortor erat pulvinar ex, quis tempor augue elit ut libero. Fusce eu velit at ex aliquet vehicula quis at enim. Quisque pretium convallis fermentum. Morbi cursus aliquet mollis. Aenean sit amet sagittis est, vitae varius tellus. Nunc sit amet justo sodales quam rhoncus ornare id a magna. Vivamus vehicula et sapien a fringilla.</div>
                
            </div>
        </div>
    </div>
</template>

<script>
    module.exports= {
        name:"AboutComponent",
        data (){
            return {
                title:"O mnie"
            }
        }
    }

</script>


<style scoped lang="scss">
@import './scss/variables.scss';

    h1 {
        font-size: 55px;
        line-height: 100px;
    }
    .content-box {
        padding-left: 50px;
        background-color: #596770;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        width: 80%;
        height: 80%;
        .mini-navbar {
            background-color: #31373c;
            position: fixed;
            top: 0;
            left: 0px;
            bottom: 0;
            width: 51px;
        }
        .content {
            overflow-y: auto;
            width: 100%;
            height: 100%;
        }
    }
    .container {
        display: grid;
        grid-template-columns: 50% 50%;
        .text {
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: left;
            padding-right: 20%;
        }
        .photo {
            img {
                max-width: 50%;
            }
        }
    }
    
</style>