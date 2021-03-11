<template>
    <header>
        <h1>
            <img 
                v-for="image in images"
                :key="image.id"
                :src="image.image"
            >
        </h1>
    </header>
</template>

<script>
    export default{
        data:function(){
            return{
                images:[
                    {
                        image:require('@/assets/images/first-view1.png')
                    },
                    {
                        image:require('@/assets/images/first-view2.png')
                    },
                ],
            }
        }
    }
</script>