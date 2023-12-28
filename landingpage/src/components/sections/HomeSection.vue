<script>
export default {
    name: 'HomeSection',
}
</script>

<template>
    <div class="text-center home-container">
        <div class="row">
            <div class="bg">
                <div class="main-text">
                    <h1>
                        Welcome to Ro-Ed Logistics and Services: Your trusted Partner in Efficient Trucking Solutions
                    </h1>
                </div>
                <div class="overlay"></div>
            </div>
            <div class="sub-text">
                <h3>
                    Join the Ro-Ed Logistics and Services Team! Become a Subcontractor Today!
                </h3>
                <a 
                    href="#contactSection" 
                    class="btn btn-success" 
                    tabindex="-1" 
                    role="button">
                    Contact Us Now!
                    UWU
                </a>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .home-container {
        height: 100%;
        width: 100%;
        justify-content: center;
        align-items: center;
    }

    .row {
        height: 100%;
        --bs-gutter-x: 0; 
    }

    .main-text h1{
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        text-shadow: 2px 2px 10px black;
        font-size: 2.5rem;
        font-weight: bold;
        z-index: 1;
    }

    .sub-text {
        width: 30%; 
        background-color: #041421;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        color: white;
        text-shadow: 2px 2px 10px black;
        font-weight: bold;
    }

    .bg {
        width: 70%; 
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        background: center / cover no-repeat url("../../assets/trucksBG.jpg");
    }

    .bg .overlay {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        background-color: #4c7273;
        opacity: 0.4;
        z-index: 0;
    }
</style>