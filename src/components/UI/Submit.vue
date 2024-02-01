<template>
    <button type="submit" @click="getInfo">{{ title }}</button>
</template>
  
<script>
export default {
    props: ['title'],
    methods: {
        getInfo() {
            this.$emit('getInfo')
        }
    }
}
</script>
  
<style>
button {
    font-family: 'Poppins', sans-serif;
    display: block;

    font-size: 24px;
    padding: 20px 40px 21px 40px;
    margin: 48px auto;

    color: #FFF;
    background: linear-gradient(180deg, #9E96F2 0%, #EC31F0 100%);
    box-shadow: 0px 3px 12px 0px rgba(74, 58, 255, 0.18);

    border: none;
    border-radius: 56px;

    cursor: pointer;
}

button:active {
    background: linear-gradient(180deg, #8d84f3 0%, #e44be7 100%);
}
</style>
  