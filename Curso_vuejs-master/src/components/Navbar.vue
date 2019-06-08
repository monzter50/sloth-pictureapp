<template>
    <nav class="main-navbar">
        <LogoApp/>
        <search-app></search-app>
        <notification></notification>     
    </nav>
</template>

<script>
import LogoApp from './LogoApp';
import Notification from './Notification';
import SearchApp from './SearchApp';

export default {
    name:'Navbar',
    components: {
        LogoApp,
        Notification,
        SearchApp
    }
}
</script>
