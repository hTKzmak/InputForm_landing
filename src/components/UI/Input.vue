<template>
    <div class="input-form" v-for="info in data">
        <p>{{ info.title }}</p>
        <input :type="info.type" :placeholder="info.placeholder" v-model="info.model">
    </div>
</template>
  
<script>
export default {
    props: ['data']
}
</script>
  
<style>
.input-form {
    margin-left: 18px;
}

input {
    width: 284px;
    height: 66px;
    padding: 20px;
    margin-bottom: 30px;

    border-radius: 46px;
    border: 1px solid #EFF0F6;
    background: #FFF;
    box-shadow: 0px 2px 6px 0px rgba(19, 18, 66, 0.07);
}

@media screen and (max-width: 600px) {
    input {
        width: 60vw;
    }
}
</style>
  