<script>
import SectionOurValues from './SectionOurValues.vue';
import SectionCauses from './SectionCauses.vue';
import SectionArticles from './SectionArticles.vue';
import LastSectionMain from './LastSectionMain.vue';
export default {
    name: "AppMain",
    components: {
        SectionOurValues,
        SectionCauses,
        SectionArticles,
        LastSectionMain
    },
    data () {
        return {
            cards: [
                {
                    icon: "fa-solid fa-droplet",
                    title: "Clean water",
                    text: "Nullam convallis, orci in cogue aliquet, diam mauris cursus urna, id maximus lectus magna maximus",
                    button: "Learn more"
                },
                {
                    icon: "fa-solid fa-stethoscope",
                    title: "Vaccinations",
                    text: "Nullam convallis, orci in cogue aliquet, diam mauris cursus urna, id maximus lectus magna maximus",
                    button: "Learn more"
                },
                {
                    icon: "fa-solid fa-graduation-cap",
                    title: "Education",
                    text: "Nullam convallis, orci in cogue aliquet, diam mauris cursus urna, id maximus lectus magna maximus",
                    button: "Learn more"
                },
                {
                    icon: "fa-solid fa-wheat-awn",
                    title: "Farming",
                    text: "Nullam convallis, orci in cogue aliquet, diam mauris cursus urna, id maximus lectus magna maximus",
                    button: "Learn more"
                },
            ]
        }
    }
}
</script>

<template>
<main>
    <!-- MOMENT SECTION -->
    <section class="section-moment row g-0">
        <div class="left container col-lg-7 col-md-6 p-4">
            <h3 class="fw-normal">EVERY MOMENT COUNTS</h3>
            <hr>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet placeat, ullam debitis voluptates facere quis laborum?</p>
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui ab numquam facere optio deleniti voluptas nisi. Quos ipsam corporis eaque, quaerat illum pariatur repellendus. </p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae quas repellat repellendus</p>
            <button type="button" class="btn btn-warning">Our Missions</button>
        </div>
        <div class="rigth col-lg-5 col-md-6">
            <div class="rigth-content text-white fs-5">
                <div class="text-center">
                    <i class="fa-regular fa-heart me-2"></i>
                    <span>2032</span>
                    <p class="fs-6">Volunters worldwide</p>
                </div>
                <div class="text-center">
                    <i class="fa-solid fa-globe me-2"></i>
                    <span>132</span>
                    <p>Active Project</p>
                </div>
                <div class="text-center">
                    <i class="fa-solid fa-dollar-sign me-2"></i>
                    <span>3.8M</span>
                    <p>Donated</p>
                </div>
            </div>
        </div>
    </section>
    <!-- /MOMENT SECTION -->

    <!-- VALUES SECTION -->
    <section class="section-values">
        <header></header>
        <div class="content-values pb-4">
            <div class="container">

                <div class="title text-center">
                    <h2 class="text-white">OUR VALUES</h2>
                    <div class="border-title my-3"></div>
                    <p class="text-white">Think big. Act bigger</p>
                </div>
                <!-- Card -->
                <div class="row content-card">
                    <SectionOurValues v-for="(item, index) in cards" :key="index" :icon="item.icon" :title="item.title" :text="item.text" :button="item.button"/>
                </div>
                <!-- /Card -->
            </div>             
        </div>
    </section>
    <!-- /VALUES SECTION -->

    <!-- CAUSES SECTION -->
    <SectionCauses />
    <!-- /CAUSES SECTION -->

    <!-- SECTION ARTICLES -->
    <SectionArticles />
    <!-- /SECTION ARTICLES -->

    <!-- ULTIMA SEZIONE -->
    <LastSectionMain />
    <!-- /ULTIMA SEZIONE -->


</main>
</template>

<style lang="scss" scoped>
main {
    .section-moment {
        .left {

            hr {
                color: blue;
                width: 150px;
            }

            p {
                font-size: .9rem;
            }
        }

        .rigth {
            background-image: url(../assets/img/home-content-bg-1.jpg);
            background-size: cover;
            position: relative;

            .rigth-content {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
            }
        }
    }

    .section-values {
     header {
        height: 100px;
        background-image: url(../assets/img/home-content-bg-2.jpg);
        background-size: cover;
        opacity: .9;
    }
    .content-values {
        background-image: url(../assets/img/home-content-bg-2.jpg);
        background-size: cover;
        background-position: center;

        .title {

            .border-title {
                border-bottom: 2px solid orange;
                width: 70px;
                margin: 0 auto;
            }
        }

        .content-card {
            padding:  50px 0 100px;
        }

    }
}
}

</style>