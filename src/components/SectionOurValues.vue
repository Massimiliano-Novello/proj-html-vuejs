<script>
export default {
    name: "SectionOurValues",
    props: {
        icon: String,
        title: String,
        text: String,
        button: String
    }
}
</script>

<template>
            <div class="col-3 text-center my_card">
                <i :class="icon"></i>
                <div class="text-white card-title">
                    <h5>{{ title }}</h5>
                    <p>{{ text }}</p>
                </div>
                <button class="my_btn">{{ button }}</button>
            </div>

</template>

<style lang="scss" scoped>


.my_card {
    i {
        font-size: 2.5rem;
        color: #fcd66c;
    }

    .card-title {

        p {
            font-size: .7rem;
            font-weight: 300;
        }
    }

    .my_btn {
    background-color: #fcd66c;
    border: none;
    color: white;
}
}
</style>