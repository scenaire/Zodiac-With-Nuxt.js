<template>
    <div class="cardWrapper">
        <b-row class="my-1">
            <b-col sm="4">
            <img :src="selectedZodiac.imgName">
        </b-col>
        <b-col sm="8">
            <p>Year: <span class="bold">{{selectedZodiac.year}}</span></p>
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

</style>