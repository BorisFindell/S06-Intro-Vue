<template>
    <div id="benving">
        <h3>{{title}}</h3>
        <p>{{description}}</p>
        <button @click="$emit('començar')">Començar</button>  
    </div>
    
</template>

<script>
export default {
    name:"Benving",
    data() {
        return {
            title: "Benvinguts/des!",
            description: "This project is a demo for a future project. Click start to see what's under construction! ",
        }
    },
    emits:['començar']
    
    
}
</script>