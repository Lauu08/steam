<template>
    <nav>
        <ul>
            <li>
                <NuxtLink to="/">Tienda</NuxtLink> <! -- llamar a las pages para pintarlas --!>
            </li>
            <li>
                <NuxtLink to="/comunidad">Comunidad</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/users">Usuarios (fetch)</NuxtLink>
            </li>
        </ul>
        <div
            class="user"
            @click="panelActive = !panelActive">U</div>
        <div
            class="panel"
            v-show="panelActive">
        </div>
    </nav>
</template>

<script setup>
    import { ref } from 'vue'
    const panelActive = ref(false)
</script>

<style lang="postcss">
    nav{
        @apply flex p-4;
        align-items: center;
        color: rgb(43, 43, 43);
    }
    ul{
        @apply flex p-4;
        li{
            @apply p-4;
        }
    }
    .user{
        display: flex;
        justify-content: right;
        padding: 10px;
        margin: 10px;
        
    }
    .panel{
        background-color: rgb(43, 43, 43);
        width: 300px;
        height: 300px;
    }
</style>

