<template>
    <div id="global-layout">
        <!-- <PagePreloader /> -->
        <TopHeader />
        <HeroArea />
        <!-- <MainMenu /> -->



        <component :is="layout"/>
        <!-- ***** Footer Area Start ***** -->
        <footer class="footer-area">
            <div class="container">
                <div class="row">
                    <div class="col-12">
                        <!-- Copywrite Text -->
                        <div class="copywrite-text">
                            <p><!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
    Copyright &copy;<script>document.write(new Date().getFullYear());</script> All rights reserved | This template is made with <i class="fa fa-heart-o" aria-hidden="true"></i> by <a href="https://colorlib.com" target="_blank">Colorlib</a>
    <!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
    </p>
                        </div>
                    </div>
                </div>
            </div>
        </footer>
        <!-- ***** Footer Area End ***** -->
    </div>
</template>

<script>
import PagePreloader from "../components/PagePreloader.vue"
import MainMenu from "../components/MainMenu.vue"
import TopHeader from "../components/Header.vue"
import HeroArea from "../components/HeroArea.vue"

export default {
    components: {
        PagePreloader,
        MainMenu,
        TopHeader,
        HeroArea,
    },
    mounted () {
        console.log('GlobalLayout', this)
    },
    computed: {
        layout () {
            if (this.$page.path) {
                if (this.$frontmatter.layout) {
                    // You can also check whether layout exists first as the default global layout does.
                    return this.$frontmatter.layout
                }
                return 'Layout'
            }
            return 'NotFound'
        }
    },
}
</script>