
<template>
    <div class="Companybox">
        
        <div v-for="anime in companies" :key="anime.id" >
                
                <Company :anime="anime"/>
        </div>
    </div>
</template>
<script>
import Company from './Company.vue';
    export default{
        name: 'Companybox',
        components: {
            Company
        },
        props: {
            companies: Array
        }
    }

</script>
<style>

.Companybox{

    background-color: rgb(164, 250, 175);
    padding: 1em;
    color: rgb(255, 184, 184);
}
</style>