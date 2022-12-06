<template>
    
    <div>
        <h2>{{ anime.id }}</h2>
            <ul>
                <li>anime: {{ anime.anime }}</li>
                <li>developer: {{ anime.developer }}</li>
                <li>genre {{ anime.genre }}</li>
                <li>rating{{ anime.rating }} </li>
            </ul>
    </div>
</template>

<script>

export default{
    name: 'company ',
    props:{
        anime : Array
    }
}
</script>

<style scoped>



h2 {
    margin: 2px;
    font-size: 2em;
    text-align: center;
}

li {
    font-style: italic;
    font-family: 'Times New Roman', Times, serif;
    font-size: 1.3em;
}

div {
    background-color: #E5CFFB;
    color: black;
    padding: 1.5em;
    border-style: groove;
}


</style>