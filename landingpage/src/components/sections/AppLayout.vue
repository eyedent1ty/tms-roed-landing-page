<script>
import Footer from '../Footer.vue';
import FloatingActionButton from '../FloatingActionButton.vue';
import ContactSection from './ContactSection.vue';
import ClientsSection from './ClientsSection.vue';
import AboutUsSection from './AboutUsSection.vue';
import HomeSection from './HomeSection.vue';
import NavBar from '../NavBar.vue';

export default {
    name: 'AppLayout',
    components: {
        Footer,
        FloatingActionButton,
        ContactSection,
        ClientsSection,
        AboutUsSection,
        HomeSection,
        NavBar
    },
    data(){
        return{
            windowTop: 0,
            fabVisible: false
        }
    },
    mounted() {
        window.addEventListener("scroll", this.onScroll)
    },
    beforeDestroy() {
        window.removeEventListener("scroll", this.onScroll)
    },
    methods: {
        scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        },         
        onScroll(e) {
            this.windowTop = window.scrollY;
            this.fabVisible = this.windowTop > 300;
        }
    }
};
</script>

<template>
    <div>
    <NavBar id="navBar" />
    <div id="homeSection" class="section">
        <HomeSection />
    </div>
    <div id="aboutUsSection" class="section">
        <AboutUsSection />
    </div>
    <div id="clientsSection" class="section">
        <ClientsSection />
    </div>
    <div id="contactSection" class="section">
        <ContactSection />
    </div>
    <transition name="fab-fade" mode="out-in">
        <FloatingActionButton v-if="fabVisible" @scroll-to-top="scrollToTop"/>
    </transition>
    <Footer />
    </div>
</template>

<style scoped>
.section {
    height: 100vh;
    background-color: grey;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
}

#contactSection {
    height: 50vh;
    background-color: grey;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
}

#homeSection, #clientsSection {
    background-color: #041421;
}

.fab-fade-enter-active,
.fab-fade-leave-active {
  transition: opacity 0.5s;
}

.fab-fade-enter, .fab-fade-leave-to {
  opacity: 0;
}

.fab-fade-enter-to, .fab-fade-leave {
  opacity: 1;
}
</style>

