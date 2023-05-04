<template>
    <nav>
        <h1 class=""><a :href="`${home}.html`">{{ home }}</a></h1>
        <ul class="nav-items">
            <a v-for= "page in pages" :href="`${page}.html`" >{{ page }}</a>
        </ul>
    </nav>
</template>

<script>
export default{
    props:['casa'],
    data(){
        return {
            home: 'Meowtel 😸',
            kitties: 'Kitties',
            pages:['Kitties', 'About Us', 'Contact']
        }
    }
}
</script>