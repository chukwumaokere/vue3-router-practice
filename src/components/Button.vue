<template>
  <button :class="className" :style="{backgroundColor: color, color: textcolor}">{{text}}</button> 
</template>

<script>
export default {
    props: {
        text: String,
        color: String,
        textcolor: String,
        className: String,
    },
    /*
    setup(props){
        return {
            styleObject: { backgroundColor: props.color, color: textcolor }
        }
    }
    */
   setup(props){
       let btnstyle = "background-color:"+props.color+";color:"+props.textcolor+";";
       return {
           btnstyle,

       }
   }
}
</script>

<style>
    button{ 
        padding: 12px 20px;
        font-size: 1.2rem;
        border: none;
        border-radius: 8px;
    }
    .client-green{ 
        background-color: #24b35f !important;
    }
    .client-red{
        background-color: rgb(163, 25, 25) !important;
    }
    .hello{ 
        font-size: 30rem;
    }
</style>