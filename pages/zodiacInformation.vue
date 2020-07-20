<template>
    <div class="centerdiv">
        <Nav />
        <h2>Chinese Zodiac Information</h2>
        <br>
        <label>Search by: </label>
        <b-form-radio-group
            v-model="selected"
            :options="options"
            class="mb-3"
            value-field="item"
            text-field="name"
        ></b-form-radio-group>

        <div class="mt-3">Selected: <strong>{{ selected }}</strong></div>
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            selected: '',
            options: [
                {item: 'year', name: 'Year'},
                {item: 'zodiac', name: 'Zodiac'}
            ]
        }
    }
}
</script>

<style>

</style>