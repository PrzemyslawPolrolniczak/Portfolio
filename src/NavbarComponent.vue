<!--NavbarComponent.vue-->
<template>
    <nav>
        <div class="tab"
            :class="[tab.background, tab.isActive]"
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
                    {text: 'Intro', icon: 'fa-home', background:'default', isActive: 'active', href: 'intro-component'},
                    {text: 'O mnie', icon: 'fa-user-circle', background:'blue', isActive: '', href: 'about-component'},
                    {text: 'Projekty', icon: 'fa-briefcase', background:'red', isActive: '', href: 'projects-component'},
                    {text: 'Linki', icon: 'fa-link', background:'green', isActive: '', href: 'links-component'},
                    {text: 'Kontakt', icon: 'fa-envelope', background:'yellow', isActive: '', href: 'contact-component'},
                    {text: 'English', icon: 'fa-language', background:'', isActive: '', href: 'english'},
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
                this.$emit('changeTab', [tab.href, tab.background]);
            }
        }
    }
</script>


<style scoped lang="scss">
@import './scss/variables.scss';

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
                    color: $color1;
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
                background-color: rgba($color: $color1, $alpha: 1.0);
                &.blue {
                    background-color: rgba($color: $color2, $alpha: 1.0)
                }
                &.red {
                    background-color: rgba($color: $color3, $alpha: 1.0)
                }
                &.green {
                    background-color: rgba($color: $color4, $alpha: 1.0)
                }
                &.yellow {
                    background-color: rgba($color: $color5, $alpha: 1.0)
                }
            }
            &.blue:hover {
                color: $color2;
            }
            &.red:hover {
                color: $color3;
            }
            &.green:hover {
                color: $color4;
            }
            &.yellow:hover {
                color: $color5;
            }
        }
    }
</style>