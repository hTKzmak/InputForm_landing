<template>
    <main>
        <div class="container">
            <div class="title">
                <h2>Get an estimate for Workspace</h2>
            </div>
            <div class="requirements">
                <div class="requirements-title">
                    <h1>Post Your Requirements</h1>
                    <p>Please fill the form below to receive a quote for workspace. <br /> Please add all the details
                        required.</p>
                </div>
                <ContactDetails :data="data" :getInfo="getInfo" />
            </div>
        </div>
    </main>
</template>
  
<script>
import ContactDetails from './ContactDetails.vue'

export default {
    components: { ContactDetails },
    props: ['data'],
    data() {
        return {
            data: [
                { model: '', title: 'Name', type: 'text', placeholder: 'Your Name' },
                { model: '', title: 'Phone Number', type: 'tel', placeholder: '(123) 456 - 7890' },
                { model: '', title: 'Email', type: 'email', placeholder: 'Your Mail ID' },
                { model: '', title: 'Date', type: 'text', placeholder: 'dd - mm - yyyy' },
            ]
        }
    },
    methods: {
        getInfo() {
            let info = {};
            this.data.forEach(item => {
                info[item.title] = item.model;
            });
            console.log(info);
        }
    }
}
</script>
  
<style>
.title {
    text-align: center;
    padding: 36px 0;
    margin-top: 50px;
    margin-bottom: 110px;
    border-radius: 18px;
    background: #FFF;
    box-shadow: 0px 12px 24px 0px rgba(20, 20, 43, 0.04), 0px -2px 4px 0px rgba(20, 20, 43, 0.02), 0px 3px 14px 0px rgba(74, 58, 255, 0.03);
}

.requirements-title {
    text-align: center;
    margin-bottom: 42px;
}

.requirements-title h1 {
    margin: 12px 0;
}
</style>
  