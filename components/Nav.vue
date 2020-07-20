<template>

    <div>
        <b-navbar fixed="top" toggleable="lg" type="dark" variant="info">
            <b-navbar-brand href="/">Chinese Zodiac</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                    <b-nav-item to="/zodiacTable">Table</b-nav-item>
                    <b-nav-item to="/zodiacInformation">Infomation</b-nav-item>
                </b-navbar-nav>
            </b-collapse>
        </b-navbar>
    </div>
    
</template>

<style>

</style>