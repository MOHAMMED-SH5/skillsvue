<template>
    <label>search data by city name  </label>
    <input type="text" v-model="searchdata">
    <HelpWorld v-for="county  in finddata" v-bind:key="county.id" :city="county.city" :street="county.street" :number="county.number" :zipcode="county.zipcode" />
</template>


<script>
import HelpWorld from '@/components/HelpWorld.vue'
    export default{
        data()
        {
            return{  
                countys:
                [
                    {
                        "city": "kilcoole",
                        "street": "new road",
                        "number": 7682,
                        "zipcode": "12926-3874"
                    },
                     {
                       "city": "kilcoole",
                        "street": "Lovers Ln",
                        "number": 7267,
                        "zipcode": "12926-3874"
                    },
                     {
                        "city": "Cullman",
                        "street": "Frances Ct",
                        "number": 86,
                        "zipcode": "29567-1452"
                    },
                     {
                        "city": "San Antonio",
                        "street": "Hunters Creek Dr",
                        "number": 6454,
                        "zipcode": "98234-1734"
                    },
                     {
                        "city": "el paso",
                        "street": "prospect st",
                        "number": 124,
                        "zipcode": "12346-0456"
                    }
                ],
                searchdata:''
            }
        },
        components:{
            HelpWorld
        },
        computed:{
            finddata:function()
            {
                return this.countys.filter(country =>{
                    return country.city.match(this.searchdata)
                })
            }
        }
    }
</script>