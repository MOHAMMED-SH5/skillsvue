<template>

    <!-- return name -->
    <p>
       {{name}}
    </p>

    <!-- return age -->
    <p v-if="age>0 && age<20">
      age is small {{age}}
    </p>

     <p v-else-if="age>20 && age<50">
      age is suit {{age}}
    </p>

    <p v-else-if="age>50 && age<100">
      age is big {{age}}
    </p>


      <!-- return gender according male or fmale -->
    <p>
      {{gender ? 'male':'fmale'}}
    </p>


    <!-- return firsname and  lastmame  -->
    <p>
      {{fullname[0].firsname}} {{fullname[0].lastmame}}
    </p>

    <!-- return img using v-bind  -->
    <div class="d-flex justify-content-center">
      <img  class="w-25 mb-5" :src="imgurl" alt="">
    </div>

      <!-- return value  in input  -->
      <input type="emailvalue" name="" v-model="emailvalue" id="">
      <p>the email is ::{{emailvalue}}</p>

      <!-- use function -->
      <label for="">name</label>
      <input type="text" v-model="namevalue">
      <label for="">family</label>
      <input type="text" v-model="familyvalue">
      <p>
        {{fullnameis()}}
      </p>
    
</template>

<script>
export default {
 data() {
    return {
        name:'mohammed',
        family:'shalayel',
        age:51,
        gender:true,
        fullname:[
          {
            firsname:'mohammed',
            lastmame:'shalayel'
          }
        ],
        imgurl:"https://i2.wp.com/pic.i7lm.com/wp-content/uploads/2020/03/5-64.jpg",
        emailvalue:'',
        namevalue:'',
        familyvalue:'',
      }
   },
   methods:{
    fullnameis:function()
    {
      return this.namevalue+' '+this.familyvalue
    }
   }
}
</script>

<style>

</style>