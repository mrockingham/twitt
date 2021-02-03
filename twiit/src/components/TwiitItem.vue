<template>
    <div class="twiit-item">
        <div class="profile-twiit">
            <div class="twiit-user">
                @{{username}}
            </div>
            <div class="twiit-content">
                {{ twiit.content}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "twiitItem",
    props:{
        username:{
            type: String,
            required: true
        },
        twiit:{
            type:Object,
            required: true
        }
    }
}
</script>

<style >
.twiit-item{
    padding: 20px;
    background-color: white;
    border-radius: 5px;
    border: 1px solid #dfe3e8;
    box-sizing: border-box;
    cursor: pointer;
    transition: all 0.25s ease;
    }

.twiit-item:hover{
    transform: scale(1.1, 1.0)
}

.twiit-user{
    font-weight: bold;
}
</style>