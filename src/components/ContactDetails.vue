<template>
    <div class="contact-form">
        <div class="contact-form-title">
            <h2>Contact details</h2>
            <p>Please fill your information so we can get in touch with you.</p>
        </div>
        <form class="contact-form-list">
            <Input :data="data" />
        </form>
    </div>
    <Submit title="Submit" @getInfo="getInfo"/>
</template>
  
<script>

import Input from './UI/Input.vue'
import Submit from './UI/Submit.vue'

export default {
    components: { Input, Submit },
    props: ['data', 'getInfo'],
}

</script>
  
<style>
.contact-form {
    border-radius: 34px;
    border: 1px solid #EFF0F6;
    background: #FAF8F8;
    padding: 20px 30px 90px;
    margin: 0 auto;
    width: 55%;
}

.contact-form-title::after {
    content: "";
    display: block;
    height: 1px;
    background: #D9DBE9;
}

.contact-form-title>h2,
.contact-form-title>p {
    margin-left: 18px;
}

.contact-form-title>p {
    color: #6F6C90;
}

.contact-form-list {
    margin-top: 48px;
}

@media screen and (max-width: 909px) {
    .contact-form {
        margin: 0 auto;
        width: 70%;
    }
}

@media screen and (max-width: 600px) {
    .contact-form {
        margin: 0 auto;
        width: 100%;
    }
}
</style>
  