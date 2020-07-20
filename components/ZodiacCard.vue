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

          <Card v-if="selected != null" :selectedZodiac="selected"/>

      </div>
      
  </div>
</template>

<script>
export default {

    data() {
        return {
            selected: null,
            options: [
                {value: {name: "Rat", yinYang: "Yang", element: "Water", imgName: require("@/assets/img/zodiac0.jpg"), decs: "is persuasive, intuitive, empathetic, objective and often sought out for their counsel"}, text: 'Rat'},
                {value: {name: "Ox", yinYang: "Yin", element: "Earth", imgName: require("@/assets/img/zodiac1.jpg"), decs: "is serious, logical and methodical, intelligent, objective and good at planning"}, text: 'Ox'},
                {value: {name: "Tiger", yinYang: "Yang", element: "Wood", imgName: require("@/assets/img/zodiac2.jpg"), decs: "has high morals, self-confident, expansive and co-operative, with wide and varied interests and idealistic goals"}, text: 'Tiger'},
                {value: {name: "Rabbit", yinYang: "Yin", element: "Wood", imgName: require("@/assets/img/zodiac3.jpg"), decs: "has high morals, self-confident, expansive and co-operative, with wide and varied interests and idealistic goals"}, text: 'Rabbit'},
                {value: {name: "Dragon", yinYang: "Yang", element: "Earth", imgName: require("@/assets/img/zodiac4.jpg"), decs: "is serious, logical and methodical, intelligent, objective and good at planning"}, text: 'Dragon'},
                {value: {name: "Snake", yinYang: "Yin", element: "Fire", imgName: require("@/assets/img/zodiac5.jpg"), decs: "has leadership qualities, dynamic passion, and is decisive, self-confident, positive and assertive"}, text: 'Snake'},
                {value: {name: "Horse", yinYang: "Yang", element: "Fire", imgName: require("@/assets/img/zodiac6.jpg"), decs: "has leadership qualities, dynamic passion, and is decisive, self-confident, positive and assertive"}, text: 'Horse'},
                {value: {name: "Goat", yinYang: "Yin", element: "Earth", imgName: require("@/assets/img/zodiac7.jpg"), decs: "is serious, logical and methodical, intelligent, objective and good at planning"}, text: 'Goat'},
                {value: {name: "Monkey", yinYang: "Yang", element: "Metal", imgName: require("@/assets/img/zodiac8.jpg"), decs: "is sincere, has fixed values and opinions, is strong of will, and has eloquence of speech"}, text: 'Monkey'}, 
                {value: {name: "Rooster", yinYang: "Yin", element: "Metal", imgName: require("@/assets/img/zodiac9.jpg"), decs: "is sincere, has fixed values and opinions, is strong of will, and has eloquence of speech"}, text: 'Rooster'},
                {value: {name: "Dog", yinYang: "Yang", element: "Earth", imgName: require("@/assets/img/zodiac10.jpg"), decs: "is serious, logical and methodical, intelligent, objective and good at planning"}, text: 'Dog'},
                {value: {name: "Pig", yinYang: "Yin", element: "Water", imgName: require("@/assets/img/zodiac11.jpg"), decs: "is persuasive, intuitive, empathetic, objective and often sought out for their counsel"}, text: 'Pig'}
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
    margin: 30px auto;
}

</style>