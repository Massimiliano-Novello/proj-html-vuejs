<script>
export default {
    name: "LastSectionMain",
}
</script>

<template>
<section class="last-section">
    <div class="content text-white text-center">
        <h2>CHANGE A LIFE TODAY</h2>
        <div class="border-title my-3"></div>
        <p>As a long a poverty, injustice & inequality persist, none of us can truly rest. It doesn't take much to change a life .Get in touch today and start making the difference</p>
        <div class="my_button">
            <button type="button" class="my_btn me-3">Volunteer
            </button>
            <button type="button" class="my_btn">Donate now</button>
        </div>
    </div> 
</section>
</template>

<style lang="scss" scoped>
.last-section {
    background-image: url(../assets/img/home-footer.jpg);
    background-size: cover;
    background-position: center;
    height: 500px;
    position: relative;

    .content {
        width: 50%;
        margin: 0 auto;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);

        .my_btn {
            border: 2px solid white;
            padding: 5px;
            background-color: transparent;
            color: white;

            &:hover {
                background-color: white;
                color: black;
                transition: 1s;
            }
        }
    }
}
</style>