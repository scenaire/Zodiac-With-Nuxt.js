<template>
    <div class="cardWrapper">
        <b-row class="my-1">
            <b-col sm="4">
            <img :src="selectedZodiac.imgName">
        </b-col>
        <b-col sm="8">
            <p>Chinese Zodiac: <span class="bold">{{selectedZodiac.name}}</span></p>
            <p>Yin/Yang: <span class="bold">{{selectedZodiac.yinYang}}</span></p>
            <p>Element: <span class="bold">{{selectedZodiac.element}}</span></p>
            <p>Description: <span class="bold">{{selectedZodiac.decs}}</span></p>
        </b-col>
        </b-row>
    </div>
</template>

<script>
export default {

    props: {
        selectedZodiac: {
            type: Array,
            required: true
        }

    }

}
</script>

<style>

.cardWrapper {
    width: 600px;
    margin: 20px auto;
    padding: 20px;
    border-radius: 25px;
    background: linear-gradient(90deg, rgba(217,236,242,1) 0%, rgba(226,213,218,1) 31%, rgba(230,203,207,1) 69%, rgba(255,140,140,1) 100%);
    text-align: left;
}

.bold {
    font-weight: bold;
}

img {
    border-radius: 10px;
}

</style>