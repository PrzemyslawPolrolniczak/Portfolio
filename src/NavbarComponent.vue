<!--NavbarComponent.vue-->
<template>
    <nav>
        <div class="tab"
            :class="[tab.color, tab.isActive]"
            @click="toggleActive(tab), changeTab(tab)" 
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
                    {text: 'Intro', icon: 'fa-home', color:'default', isActive: 'active', href: 'intro-component'},
                    {text: 'O mnie', icon: 'fa-user-circle', color:'blue', isActive: '', href: 'about-component'},
                    {text: 'Projekty', icon: 'fa-briefcase', color:'red', isActive: '', href: 'projects-component'},
                    {text: 'Linki', icon: 'fa-link', color:'green', isActive: '', href: 'links-component'},
                    {text: 'Kontakt', icon: 'fa-envelope', color:'yellow', isActive: '', href: 'contact-component'},
                    {text: 'English', icon: 'fa-language', color:'', isActive: '', href: 'english'},
                ],
                toggleActive(tab) {
                    this.tabs.forEach(element => {
                        element.isActive = '';
                    });
                    tab.isActive = 'active';
                }
            }
        },
        methods: {
            changeTab(tab) {
                this.$emit('changeTab', tab.href);
            }
        }
    }
</script>


<style scoped lang="scss">
    nav {
        position: fixed;
        background-color: #31373c;
        display: flex;
        flex-direction: column;
        left: 0;
        top: 0;
        bottom: 0;
        width: 150px;
        .tab {
            height: 12vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column-reverse;
            transition: all 0.5s;
            cursor: pointer;
            &:hover {
                padding-left: 20px;
                background-color: #212121;
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
                color: #31373c !important;
                &.blue {
                    background-color: rgba($color: #00B3FF, $alpha: 1.0)
                }
                &.red {
                    background-color: rgba($color: #EF233C, $alpha: 1.0)
                }
                &.green {
                    background-color: rgba($color: #91CB3E, $alpha: 1.0)
                }
                &.yellow {
                    background-color: rgba($color: #F5B700, $alpha: 1.0)
                }
                &.default {
                    background-color: rgba($color: #FFF, $alpha: 1.0)
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