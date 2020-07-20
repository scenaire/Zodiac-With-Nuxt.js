<template>
    <div class="centerdiv">
        <Nav />
        <h2>Table: Chinese Zodiac Reference</h2>
        <b-form-group label="Search by:">
            <b-form-checkbox-group
                id="checkbox-group"
                v-model="selected"
                :options="options"
                name="info"
            ></b-form-checkbox-group>
        </b-form-group>

        <ZodiacTable v-if="selected.includes('zodiac')"/>
        <br>
        <ElementTable v-if="selected.includes('element')"/>

    </div>
</template>

<script>
export default {
    head() {
        return {
            title: "Chinese Zodiac Table", 
            meta: [
                {
                    hid: 'table',
                    name: 'table',
                    content: 'table for chinese zodiac'
                }
            ]
        };
    },

    data() {
      return {
        selected: [], // Must be an array reference!
        options: [
          { text: 'Zodiac', value: 'zodiac' },
          { text: 'Element', value: 'element' },
        ]
      }
    }


};

</script>

<style>

.centerdiv {
    text-align: center;
    margin: 100px ;
}

</style>