<template>
  <div>
      <div class="wrapper">

          <h3>Your choice</h3>
          <b-alert show variant="info" v-if="showAlert == true"><p><strong>Warning!</strong> Year must be number with value >= 1900</p></b-alert>
          
            <b-row class="my-1">
            <b-col sm="3">
                <label>Enter a year: </label>
            </b-col>
            <b-col sm="6">
                <b-form-input v-model="yearSelected" type="number" placeholder="Your birth's year in AD"></b-form-input>
            </b-col>
            <b-button variant="info" @click="calculatedYear(yearSelected)" type="submit">Submit</b-button>
            </b-row>

            <YearCard v-if="showCard == true" :selectedZodiac="selectedZodiac"/>


      </div>
      
  </div>
</template>

<script>
export default {

    data() {
        return {
            yearSelected: null,
            selectedZodiac: null,
            showCard: false,
            showAlert: false
        }
    },


    methods: {
        calculatedYear: function (year) {

            if (this.yearSelected >= 1900) {
                this.showCard = true;
                this.showAlert = false;
            } else {
                this.showAlert = true;
                this.showCard = false;
            }

            var m = year % 12;
            switch(m) {
                case 4: this.selectedZodiac = {year: this.yearSelected, name: "Rat", yinYang: "Yang", element: "Water", imgName: require("@/assets/img/zodiac0.jpg"), decs: "is persuasive, intuitive, empathetic, objective and often sought out for their counsel"}; break; 
                case 5: this.selectedZodiac = {year: this.yearSelected, name: "Ox", yinYang: "Yin", element: "Earth", imgName: require("@/assets/img/zodiac1.jpg"), decs: "is serious, logical and methodical, intelligent, objective and good at planning"}; break;
                case 6: this.selectedZodiac = {year: this.yearSelected, name: "Tiger", yinYang: "Yang", element: "Wood", imgName: require("@/assets/img/zodiac2.jpg"), decs: "has high morals, self-confident, expansive and co-operative, with wide and varied interests and idealistic goals"}; break;
                case 7: this.selectedZodiac = {year: this.yearSelected, name: "Rabbit", yinYang: "Yin", element: "Wood", imgName: require("@/assets/img/zodiac3.jpg"), decs: "has high morals, self-confident, expansive and co-operative, with wide and varied interests and idealistic goals"}; break;
                case 8: this.selectedZodiac = {year: this.yearSelected, name: "Dragon", yinYang: "Yang", element: "Earth", imgName: require("@/assets/img/zodiac4.jpg"), decs: "is serious, logical and methodical, intelligent, objective and good at planning"}; break;
                case 9: this.selectedZodiac = {year: this.yearSelected, name: "Snake", yinYang: "Yin", element: "Fire", imgName: require("@/assets/img/zodiac5.jpg"), decs: "has leadership qualities, dynamic passion, and is decisive, self-confident, positive and assertive"}; break;
                case 10: this.selectedZodiac = {year: this.yearSelected, name: "Horse", yinYang: "Yang", element: "Fire", imgName: require("@/assets/img/zodiac6.jpg"), decs: "has leadership qualities, dynamic passion, and is decisive, self-confident, positive and assertive"}; break;
                case 11: this.selectedZodiac = {year: this.yearSelected, name: "Goat", yinYang: "Yin", element: "Earth", imgName: require("@/assets/img/zodiac7.jpg"), decs: "is serious, logical and methodical, intelligent, objective and good at planning"}; break;
                case 1: this.selectedZodiac = {year: this.yearSelected, name: "Rooster", yinYang: "Yin", element: "Metal", imgName: require("@/assets/img/zodiac9.jpg"), decs: "is sincere, has fixed values and opinions, is strong of will, and has eloquence of speech"}; break;
                case 2: this.selectedZodiac = {year: this.yearSelected, name: "Dog", yinYang: "Yang", element: "Earth", imgName: require("@/assets/img/zodiac10.jpg"), decs: "is serious, logical and methodical, intelligent, objective and good at planning"}; break;
                case 3: this.selectedZodiac = {year: this.yearSelected, name: "Pig", yinYang: "Yin", element: "Water", imgName: require("@/assets/img/zodiac11.jpg"), decs: "is persuasive, intuitive, empathetic, objective and often sought out for their counsel"}; break;
                default: this.selectedZodiac = {year: this.yearSelected, name: "Monkey", yinYang: "Yang", element: "Metal", imgName: require("@/assets/img/zodiac8.jpg"), decs: "is sincere, has fixed values and opinions, is strong of will, and has eloquence of speech"}; break;
            }
        },

    }
  
}
</script>

<style>


</style>