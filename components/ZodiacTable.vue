<template>
    <div>
        <div class="container">
            <b-table striped hover :items="items"></b-table>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            items: [
                {id: 0, name: "Rat", yinYang: "Yang", element: "Water", imgName: "/img/zodiac0.jpg"},
                {id: 1, name: "Ox", yinYang: "Yin", element: "Earth", imgName: "/img/zodiac1.jpg"},
                {id: 2, name: "Tiger", yinYang: "Yang", element: "Wood", imgName: "/img/zodiac2.jpg"},
                {id: 3, name: "Rabbit", yinYang: "Yin", element: "Wood", imgName: "/img/zodiac3.jpg"},
                {id: 4, name: "Dragon", yinYang: "Yang", element: "Earth", imgName: "/img/zodiac4.jpg"},
                {id: 5, name: "Snake", yinYang: "Yin", element: "Fire", imgName: "/img/zodiac5.jpg"},
                {id: 6, name: "Horse", yinYang: "Yang", element: "Fire", imgName: "/img/zodiac6.jpg"},
                {id: 7, name: "Goat", yinYang: "Yin", element: "Earth", imgName: "/img/zodiac7.jpg"},
                {id: 8, name: "Monkey", yinYang: "Yang", element: "Metal", imgName: "/img/zodiac8.jpg"},
                {id: 9, name: "Rooster", yinYang: "Yin", element: "Metal", imgName: "/img/zodiac9.jpg"},
                {id: 10, name: "Dog", yinYang: "Yang", element: "Earth", imgName: "/img/zodiac10.jpg"},
                {id: 11, name: "Pig", yinYang: "Yin", element: "Water", imgName: "/img/zodiac11.jpg"},
            ]
        }
    }
}
</script>

<style>
.container{
    margin: 0 auto;
}
</style>