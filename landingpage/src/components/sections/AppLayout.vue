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
        window.addEventListener("scroll", this.onScroll),
        this.createObserver();
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
        },
        createObserver(){
            const observer = new IntersectionObserver((entries) => {
                entries.forEach((entry) => {
                    console.log(entry)
                    if (entry.isIntersecting) {
                        entry.target.classList.add('show');
                    }
                    else {
                        entry.target.classList.remove('show');
                    }
                });
            })

            const hiddenElements = document.querySelectorAll('.hidden');

            hiddenElements.forEach((el) => observer.observe(el));
        }
    }
};
</script>

<template>
    <div>
        <NavBar id="navBar" class="navbar" />

        <section id="homeSection" class="section hidden">
            <HomeSection />
        </section>

        <section id="aboutUsSection" class="section hidden">
            <AboutUsSection />
        </section>

        <section id="clientsSection" class="section hidden">
            <ClientsSection />
        </section>

        <section id="contactSection" class="section hidden">
            <ContactSection />
        </section>

        <transition name="fab-fade" mode="out-in">
            <FloatingActionButton v-if="fabVisible" @scroll-to-top="scrollToTop"/>
        </transition>

        <Footer />
    </div>
</template>

<style>

.section {
    height: 100vh;
    background-color: #041421;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
}

#contactSection {
    height: 50vh;
}

.hidden {
    opacity: 0;
    filter: blur(5px);
    transform: translateX(-100%);
    transition: all 2s;
}

.show {
    opacity: 1;
    filter: blur(0px);
    transform: translateX(0%);
}

.navbar {
    background-color: #4C7273;
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

.h1, .h2, .h3, .h4, .h5, .h6, h1, h2, h3, h4, h5, h6 {
    margin-top: .5rem;
    margin-bottom: .5rem;
    font-weight: 500;
    line-height: 1.2;
    color: var(--bs-heading-color);
}
</style>

