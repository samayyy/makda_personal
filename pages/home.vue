<template>
<div>
    <home1 />
    <home2 />
    <home3 />
    <home4 />
    <home5 />
</div>
</template>

<script>
import home1 from '../components/home1'
import home2 from '../components/home2'
import home3 from '../components/home3'
import home4 from '../components/home4'
import home5 from '../components/home5'


export default {
    name: 'Home',
    components: {
        home1,
        home2,
        home3,
        home5,
        home4,
    },
    
}
</script>
