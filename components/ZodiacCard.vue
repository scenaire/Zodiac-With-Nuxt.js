<template>
  <div>
      <div class="wrapper">
          <h3>Your choice</h3>
          <label>Choose Zodiac: </label>
          <b-form-select v-model="selected" :options="options" class="mb-3">
              <template v-slot:first>
                  <b-form-select-option :value="null" disabled>--- Please select an option ---</b-form-select-option>
              </template>
          </b-form-select>

        

      </div>
      
  </div>
</template>

<script>
export default {

    data() {
        return {
            selected: null,
            options: [
                {value: 'rat', text: 'Rat'},
                {value: 'ox', text: 'Ox'},
                {value: 'tiger', text: 'Tiger'},
                {value: 'rabbit', text: 'Rabbit'},
                {value: 'dragon', text: 'Dragon'},
                {value: 'snake', text: 'Snake'},
                {value: 'horse', text: 'Horse'},
                {value: 'goat', text: 'Goat'},
                {value: 'monkey', text: 'Monkey'}, 
                {value: 'rooster', text: 'Rooster'},
                {value: 'dog', text: 'Dog'},
                {value: 'pig', text: 'Pig'}
            ]
        }
    }

}
</script>

<style>

.wrapper {
    max-width: 800px;
    border: solid 2px #17a2b8;
    border-radius: 25px;
    padding: 30px 40px;
    margin: 0 auto;
}

</style>