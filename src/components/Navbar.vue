<template>
    <nav>
        <v-toolbar app color="#1e202b">
            <v-toolbar-title class="text-uppercase grey--text">
                <img src="../assets/logo.png" />
                <span>Company Name</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn  outlined rounded color="primary" class="ma-2">
                <span>Home</span>
            </v-btn>
            <v-btn  outlined rounded color="white" class="ma-2">
                <span>News</span>
            </v-btn>
            <v-btn  outlined rounded color="white" class="ma-2">
                <span>Live cameras</span>
            </v-btn>
            <v-btn  outlined rounded color="white" class="ma-2">
                <span>Photos</span>
            </v-btn>
            <v-btn  outlined rounded color="white" class="ma-2">
                <span>Contact</span>
            </v-btn>
            <v-btn  outlined rounded color="white" class="ma-2">
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

