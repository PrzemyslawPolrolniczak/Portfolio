<template>
    <div class="content-box">
        <div 
        class="mini-navbar"
        :class="[background]"></div>
        <div class="content">
            <h1 class="text-center">{{title}}</h1>
            <div class="container">
                <div class="text">Etiam risus metus, cursus sit amet convallis aliquet, aliquet vitae lorem. Nullam accumsan arcu quis ex porta cursus. Vivamus tempor leo eu odio porttitor, sed ultricies lectus tempus. Quisque eget magna metus. Phasellus malesuada eros id tellus commodo, in tristique odio viverra. Nullam sem turpis, accumsan semper turpis viverra, blandit accumsan nisi. Duis rhoncus, tortor quis rutrum porta, tortor erat pulvinar ex, quis tempor augue elit ut libero. Fusce eu velit at ex aliquet vehicula quis at enim. Quisque pretium convallis fermentum. Morbi cursus aliquet mollis. Aenean sit amet sagittis est, vitae varius tellus. Nunc sit amet justo sodales quam rhoncus ornare id a magna. Vivamus vehicula et sapien a fringilla.</div>
                
            </div>
        </div>
    </div>
</template>

<script>
    module.exports= {
        name:"ContactComponent",
        data (){
            return {
                title:"Contact",
                background: this.$parent.themeColor
            }
        }
    }

</script>


<style scoped lang="scss">
@import './scss/variables.scss';
@import './scss/content_box.scss';


</style>