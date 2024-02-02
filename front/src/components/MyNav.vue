<template>
    <v-layout>
        <v-navigation-drawer permanent location="left">
            <template v-slot:prepend>
                <div style="display: flex; margin: 1em; gap: 0.5em;">
                    <v-avatar>
                        <v-img :src="`https://api.dicebear.com/7.x/thumbs/svg?seed=${user}`" alt=""></v-img>
                    </v-avatar>
                    <v-text-field clearable size="small" label="Search" prepend-inner-icon="mdi-magnify"
                        variant="outlined"></v-text-field>
                </div>
            </template>

            <v-divider></v-divider>

            Chats
            <v-list density="compact" nav>
                <v-list-item prepend-icon="mdi-home-city" title="Home" value="home"></v-list-item>
                <v-list-item prepend-icon="mdi-account" title="My Account" value="account"></v-list-item>
            </v-list>

            <v-divider></v-divider>

            Contacts
            <v-list density="compact" nav>
                <v-list-item prepend-icon="mdi-home-city" title="Home" value="home"></v-list-item>
                <v-list-item prepend-icon="mdi-account" title="My Account" value="account"></v-list-item>
                <v-list-item prepend-icon="mdi-account-group-outline" title="Users" value="users"></v-list-item>
            </v-list>

        </v-navigation-drawer>
        <v-main style="height: 250px">
            <div>
                <v-toolbar>
                    <v-badge dot inline>
                        <v-avatar>
                            <v-img :src="`https://api.dicebear.com/7.x/thumbs/svg?seed=${user}`" alt=""></v-img>
                        </v-avatar>
                    </v-badge>
                    <v-list-item>
                        <v-list-item-content>
                            <v-list-item-title>Celeste Jasso</v-list-item-title>
                            <v-list-item-subtitle>Frontend Developer</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                    <v-spacer></v-spacer>

                    <v-icon icon="mdi-phone"></v-icon>
                    <v-icon icon="mdi-video-outlne"></v-icon>
                    <v-icon icon="mdi-magnify"></v-icon>
                    <v-icon icon="mdi-dots-vertical"></v-icon>

                </v-toolbar>

                <div>
                    chat
                    <v-alert icon="$vuetify" text="Hi"></v-alert>
                    <v-spacer></v-spacer>
                    <v-spacer></v-spacer>
                    <v-alert icon="mdi-acoount" text="Hello"></v-alert>
                    <div>
                        <v-text-field clearable label="Type your message..." prepend-icon="mdi-account"
                            apend-icon="mdi-send">
                            <v-icon icon="mdi-microphone"></v-icon>
                            <v-icon icon="mdi-attachment"></v-icon>
                        </v-text-field>
                        <!-- <v-text-field v-model="message" :append-icon="message ? 'mdi-send' : 'mdi-microphone'"
                            :append-inner-icon="marker ? 'mdi-map-marker' : 'mdi-map-marker-off'" :prepend-icon="icon"
                            variant="filled" clear-icon="mdi-close-circle" clearable label="Message" type="text"
                            @click:append-inner="toggleMarker" @click:append="sendMessage" @click:prepend="changeIcon"
                            @click:clear="clearMessage"></v-text-field> -->
                        <!-- <v-text-field clearable label="Type your message..." prepend-icon="$vuetify">
                            <v-icon icon="mdi-microphone"></v-icon>
                            <v-icon icon="mdi-attachment"></v-icon>
                            <v-btn>Send</v-btn>
                        </v-text-field> -->
                    </div>

                </div>
            </div>
        </v-main>
    </v-layout>
</template>

<script>
//
</script>