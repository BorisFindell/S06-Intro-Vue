<template>
    <div id="benving">
        <h3>{{title}}</h3>
        <p>{{description}}</p>
        <button @click="$emit('comenzar')">Començar</button>  
    </div>
    
</template>

<script>
export default {
    name:"Benving",
    data() {
        return {
            title: "Benvinguts/des!",
            description: "Feu click al boton per començar!",
        }
    },
    emits:['comenzar']
    
    
}
</script>


<style scoped>
#benving{
    background-color: rgb(211, 236, 167, 0.8);
    padding:5rem;
    height:100vh;
    width: 50vw;
    text-align: center;
    margin: 0% 25% 0% 25%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-flow: column;
}
button{
    padding:1rem;
    font-size: 1.2rem;
    background-color: rgba(255, 255, 255, 0.5);
    color:black;
    cursor:pointer;
    border-radius: 50px;
    border-style:solid;
}
h3{
    font-size:3rem;
    color: maroon
}
p {
    font-size: 1.5rem;
}
</style>