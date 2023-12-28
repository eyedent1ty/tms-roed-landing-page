<script>
export default {
    name: 'ClientsSection',
    data() {
        return {
            cards: [
                {
                    imageUrl: 'http://via.placeholder.com/640x360',
                    title: 'GreenCross Inc.',
                    description: 'One of the top businesses committed to providing premium health and wellness goods is GreenCross Incorporated. Offering a variety of goods intended to improve and encourage a healthier lifestyle, GreenCross has made a name for itself in the market because to its dedication to innovation and client satisfaction.',
                },
                {
                    imageUrl: 'https://via.placeholder.com/800x400',
                    title: 'Kerry Logistikus',
                    description: 'Dynamic logistics firm Kerry Logistikus is renowned for its all- inclusive and effective supply chain solutions. Kerry Logistikus, a logistics and distribution specialist, is essential to the smooth flow of goods, on-time delivery, and overall supply chain process optimization.',
                },
            ],
        };
    },
}
</script>

<template>
    <div class="container-fluid text-center">
        <h1 style="color: antiquewhite;">Clients of Ro-Ed Logistics and Service</h1>
        <div class="carousel-wrapper">
            <div class="carousel-container">
                <div id="carouselAutoplay" class="carousel slide carousel-fade" data-bs-ride="carousel">
                    <div :class="['carousel-item', 'fixed-width-item', index === 0 ? 'active' : '']" v-for="(card, index) in cards" :key="index">
                        <div class="card">
                            <img :src="card.imageUrl" class="card-img-top" :alt="'Card Image ' + index">
                            <div class="card-body">
                                <h5 class="card-title">{{ card.title }}</h5>
                                <p class="card-text">{{ card.description }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <button class="carousel-control-prev" type="button" data-bs-target="#carouselAutoplay" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselAutoplay" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </button>
        </div>
    </div>
</template>

<style scoped>
.carousel-wrapper {
    position: relative;
    display: flex;
    justify-content: center;
}

.carousel-container {
    width: 80%;
    max-width: 100vh;
    flex: 0 0 auto;
}

.carousel-control-prev,
.carousel-control-next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
}

.carousel-control-prev {
    left: 0;
}

.carousel-control-next {
    right: 0;
}
</style>