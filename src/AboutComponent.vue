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
@import './scss/content_box.scss';

.mini-navbar {
    background-color: $color2;
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
            padding: 5px;
            border: 1px solid $color2;
            max-width: 50%;
        }
    }
}
</style>