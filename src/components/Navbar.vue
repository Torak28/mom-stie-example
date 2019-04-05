<template>
    <div id='Navbar'>
        <div>
            <b-navbar toggleable="lg" type="dark" variant="info">
                <b-navbar-brand href="#">SiteName</b-navbar-brand>

                <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                    <b-nav-item href="#Text1">{{json.textToDisplay1.name}}</b-nav-item>
                    <b-nav-item href="#Text2">{{json.textToDisplay1.name}}</b-nav-item>
                </b-navbar-nav>
                </b-collapse>
            </b-navbar>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Navbar',
    props: ['json']
}
</script>


<style scope>
</style>

