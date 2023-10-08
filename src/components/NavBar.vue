<template>
    <nav>
        <img class="logo" src="../assets/logo_temporaneo.jpg"
            @click="$emit('change_view', 'home')">
        <!-- <div class="menu" 
            :class="deleting ? 'deleting' : ''"
            v-if="show" 
            >
            <ul >
                <li>
                    <i class="bi bi-x-lg" 
                        v-on:click="outAnim()">
                    </i>
                </li>
                <li @click="$emit('change_view', 'home')"
                    :class="current_page == 'home' ? 'current' : ''">Home</li>
                <li @click="$emit('change_view', 'gallery')"
                    :class="current_page == 'gallery' ? 'current' : ''">My work</li>
                <li @click="$emit('change_view', 'about_me')"
                    :class="current_page == 'about_me' ? 'current' : ''">About me</li>
                <li @click="$emit('change_view', 'contacts')"
                    :class="current_page == 'contacts' ? 'current' : ''">Contacts</li>
            </ul>
        </div> -->
    </nav>
</template>

<script>
export default {
    name: 'NavBar',
    props: {
        current_page: String
    },
    data() {
        return {
            show: false,
            deleting: false,
            // pagina_corrente: this.current_page
        }
    },
    methods: {
        outAnim: function() {
            this.deleting=true;
            this.clock = setTimeout(() => {
               this.show=false;
               this.deleting=false;
            }, 2000);
        }
    }
}
</script>

<style lang="scss" scoped>
.logo {
    height: 100%;
    width: auto;
    padding-top: 5px;
    margin-right: 10px;
}
nav {
    height: 50px;
    width: 100%;
    display: flex;
    justify-content: flex-end;
    .menu {
        animation: slide_in 2s;
    }
}
ul {
    text-align: right;
    list-style: none;
    height: 100vh;
    color: white;
    background-color: rgba(0, 0, 0, 0.4);
    li {
        width: 100px;
        padding-right: 10px;
        padding-top: 5px;
        height: 30px;
        i {
            float: left;
        }
    }
}

.deleting {
    animation: slide_out 2s;
}
.current {
    border-right: 5px solid red;
    font-weight: bold;
}

@keyframes slide_in {
    0% {
        position: relative;
        left: 100px;
    }
    100% {
        position: relative;
        left: 0;
    }
}
@keyframes slide_out {
    0% {
        position: relative;
        left: 0;
    }
    100% {
        position: relative;
        left: 200px;
    }
}
</style>