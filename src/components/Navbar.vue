<template>
    <nav>
        <v-toolbar app>
            <v-toolbar-title class="text-uppercase grey--text">
                <img src="../assets/logo.png" />
                <span>Company Name</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn falt color="gray">
                <span>Home</span>
            </v-btn>
            <v-btn falt color="gray">
                <span>News</span>
            </v-btn>
            <v-btn falt color="gray">
                <span>Live cameras</span>
            </v-btn>
            <v-btn falt color="gray">
                <span>Photos</span>
            </v-btn>
            <v-btn falt color="gray">
                <span>Contact</span>
            </v-btn>
            <v-btn falt color="gray">
                <span>Sign Out</span>
                <v-icon right>fas fa-lock</v-icon>
            </v-btn>
        </v-toolbar>
    </nav>
</template>

<script>
export default {
    
}
</script>