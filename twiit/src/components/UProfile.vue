<template>
<div class='user-profile'>
    <div class="profile-panel">
    <h1 class='profile-username'>@{{user.username}}</h1>
    <div class="admin-badge" v-if="user.isAdmin">Admin
    </div>
    <div class="user-follower-count">
        <strong>Followers: </strong> {{followers}}
        </div>
    </div>
</div>
</template>

<script>
export default {
    name:'UProfile',
    data(){
        return{
            followers: 0,
            user:{
                id: 1,
                username:'MichaelRock',
                firstName: 'Michael',
                lastName:'Rock',
                email:'mike@mike.com',
                isAdmin: true
            }
        }
    },
    watch:{
        followers(newFollowerCount, oldFollowerCount){
            if(oldFollowerCount < newFollowerCount) {
                console.log(`${this.user.username} has gained a follower!`)
            }
        }
    },
    computed:{
        fullName(){
            return `${this.user.firstName} ${this.user.lastName}`
        }
    },
    methods:{
        followUser(){
            this.followers++;
        }
    },
    mounted(){
        this.folowUser()
    }

}
</script>


<style>
.user-profile{
    display: grid;
    grid-template-columns: 1fr 3fr;
    width: 100%;
    padding: 50px 5%;
}
.profile-panel{
    display: flex;
    flex-direction: column;
    margin-right: 50px;
    padding: 20px;
    background-color: white;
    border-radius: 5px;
    border: 1px solid #DFE3E8;
    }
h1{
    margin: 0;
}

.admin-badge{
    background: rgb(255, 123, 0);
    color: white;
    border-radius: 5px;
    margin-right: auto;
    padding: 0 10px;
    font-weight: bold;
}

</style>