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
                {element: "Wood", decs: "has high morals, self-confident, expansive and co-operative, with wide and varied interests and idealistic goals"},
                {element: "Fire", decs: "has leadership qualities, dynamic passion, and is decisive, self-confident, positive and assertive"},
                {element: "Earth", decs: "is serious, logical and methodical, intelligent, objective and good at planning"},
                {element: "Metal", decs: "is sincere, has fixed values and opinions, is strong of will, and has eloquence of speech"},
                {element: "Water", decs: "is persuasive, intuitive, empathetic, objective and often sought out for their counsel"},
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