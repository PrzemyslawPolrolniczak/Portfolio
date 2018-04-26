<!--NavbarComponent.vue-->
<template>
    <nav>
        <div class="tab" v-for="tab in tabs" :key="tab.id">{{tab.text}}<i class="fas" :class="tab.icon"></i></div>        
    </nav>
</template>

<script>
    module.exports = {
        name: 'NavbarComponent',
        data(){
            return {
                tabs: [
                    {text: 'Intro', icon: 'fa-home'},
                    {text: 'O mnie', icon: 'fa-user-circle'},
                    {text: 'Projekty', icon: 'fa-briefcase'},
                    {text: 'Linki', icon: 'fa-link'},
                    {text: 'Kontakt', icon: 'fa-envelope'},
                    {text: 'English', icon: 'fa-language'},                    
                ]
            }
        }
    }
</script>


<style scoped lang="scss">
    nav {
        position: fixed;
        // background-color: #2c3e50;
        background-color: #31373c;
        // background-color: #31373c;
        display: flex;
        flex-direction: column;
        // justify-content: space-around;
        left: 0;
        top: 0;
        bottom: 0;
        width: 150px;
        .tab {
            background-color: #31373c;            
            height: 12vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column-reverse;
            transition: all 0.5s;
            cursor: pointer;
            &:hover {
                background-color: #212121;
                padding-left: 20px;
            }
            &:last-of-type {
                position: absolute;
                left: 0;
                right: 0;
                bottom: 0;
            }
            i {
                font-size: 3em;
                margin-bottom: 5px;
            }
        }
    }
</style>