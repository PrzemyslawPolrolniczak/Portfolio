<!--NavbarComponent.vue-->
<template>
    <nav>
        <div class="tab"
            :class="[tab.color, tab.isActive]"
            @click="toggleActive(tab)" 
            v-for="tab in tabs" 
            :key="tab.id">
            {{tab.text}}
            <i class="fas" 
                :class="[tab.icon]"></i>
        </div>        
    </nav>
</template>

<script>
    module.exports = {
        name: 'NavbarComponent',
        data(){
            return {
                tabs: [
                    {text: 'Intro', icon: 'fa-home', color:'default', isActive: 'active'},
                    {text: 'O mnie', icon: 'fa-user-circle', color:'blue', isActive: ''},
                    {text: 'Projekty', icon: 'fa-briefcase', color:'red', isActive: ''},
                    {text: 'Linki', icon: 'fa-link', color:'green', isActive: ''},
                    {text: 'Kontakt', icon: 'fa-envelope', color:'yellow', isActive: ''},
                    {text: 'English', icon: 'fa-language', color:'', isActive: ''},
                ],
                toggleActive(tab) {
                    this.tabs.forEach(element => {
                        element.isActive = '';
                    });
                    tab.isActive = 'active';
                }
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
                padding-left: 20px;
            }
            &:last-of-type {
                position: absolute;
                left: 0;
                right: 0;
                bottom: 0;
                &.active {
                    cursor: pointer;
                    padding-left: 0;
                    background-color: #31373c;
                }
                &:hover {
                    padding-left: 0;
                    background-color: #212121;
                }
            }
            i {
                font-size: 3em;
                margin-bottom: 5px;
            }
            &.active {
                cursor: initial;
                padding-left: 20px;
                background-color: #212121;
                &.blue {
                    color: #00B3FF; //55C1FF
                }
                &.red {
                    color: #EF233C;
                }
                &.green {
                    color: #91CB3E;
                }
                &.yellow {
                    color: #F5B700;
                }
                &.default {
                    color: #fff;
                }
            }
            &.blue:hover {
                color: #00B3FF;
            }
            &.red:hover {
                color: #EF233C;
            }
            &.green:hover {
                color: #91CB3E;
            }
            &.yellow:hover {
                color: #F5B700;
            }
            &.default:hover {
                color: #fff;
            }
        }
    }
</style>