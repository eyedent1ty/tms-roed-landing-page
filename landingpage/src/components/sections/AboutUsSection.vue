<script>
export default {
    name: 'AboutUsSection',
}
</script>

<template>
        <div class="text-center home-container">
            <div class="row">
                <div class="sub-text">
                    <div class="logo-and-title">
                        <img
                        src="../../assets/company_logo.png"
                        height="50"
                        alt="company logo"
                        />
                        <h1>ABOUT US</h1>
                    </div>
                    <h3>
                        Discover the Opportunities: Partner 
                        with Ro-Ed Logistics and Services for 
                        Profitable Subcontracting.
                    </h3>
                </div>
                <div class="bg">
                    <div class="main-text">
                        <h1>
                            In the world of trucking, Ro-Ed Logistics and 
                            Services operates as a subcontractor, maintaining 
                            and owning its own fleet of vehicles. Ro-Ed's 
                            dedication to effective logistics is essential in 
                            bridging industries and organizations. Ro-Ed is a 
                            subcontractor that accepts applications from 
                            people looking for subcontracting possibilities in 
                            addition to transporting items with its owner-operated 
                            vehicles. Join our team and experience 
                            the trucking industry where opportunity and 
                            dependability meet.
                        </h1>
                    </div>
                    <div class="overlay"></div>
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

    .sub-text h1, .sub-text img {
        margin-right: 10px;
    }

    .logo-and-title {
        display: flex;
        align-items: center; 
        justify-content: center; 
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