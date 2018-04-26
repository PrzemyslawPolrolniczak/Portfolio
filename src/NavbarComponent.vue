<!--NavbarComponent.vue-->
<template>
    <nav>
        <div class="tab">Intro<i class="fas fa-home"></i></div>
        <div class="tab">O mnie<i class="fas fa-user-circle"></i></div>
        <div class="tab">Projekty<i class="fas fa-briefcase"></i></div>
        <div class="tab">Linki</div>
        <div class="tab">Kontakt</div>
        <div class="tab">ENG</div>        
    </nav>
</template>

<script>
    module.exports = {
        name: 'NavbarComponent',
        data(){
            return {}
        }
    }
</script>


<style scoped lang="scss">
    nav {
        position: fixed;
        // background-color: #2c3e50;
        background-color: #212121;
        display: flex;
        flex-direction: column;
        // justify-content: space-around;
        left: 0;
        top: 0;
        bottom: 0;
        width: 150px;
        .tab {
            background-color: #212121;
            height: 12vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column-reverse;
            transition: all 0.5s;
            cursor: pointer;
            &:hover {
                background-color: red;
            }
            i {
                font-size: 3em;
            }
        }
    }
</style>