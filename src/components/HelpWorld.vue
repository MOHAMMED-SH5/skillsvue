<template>



    <p>
       city is  {{city}}
    </p>

   <p>
       street is {{street}}
    </p>



   <p>
      number is {{number}}
    </p>


   <p>
        zipcode is {{zipcode}}
    </p>


</template>


<script>
    export default{
        data()
        {
            return{ 
                
            }
        },
        props:["city","street","number","zipcode"]
    }
</script>