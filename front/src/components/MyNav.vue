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
                barra
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
                    <!-- <div>
                        <v-container>
                            <v-row justify="center">
                                <v-col cols="8">
                                    <v-chat>
                                        <v-chat-message v-for="(message, index) in messages" :key="index"
                                            :color="message.isCurrentUser ? 'primary' : 'grey lighten-3'"
                                            :mine="message.isCurrentUser">
                                            {{ message.text }}
                                        </v-chat-message>
                                    </v-chat>
                                    <v-text-field v-model="newMessage" @keydown.enter.prevent="sendMessage"
                                        placeholder="Type your message..."></v-text-field>
                                </v-col>
                            </v-row>
                        </v-container>
                    </div> -->
                    <v-alert icon="$vuetify" text="Hi"></v-alert>
                    <div>
                        <v-text-field clearable size="small" label="Type your message..." variant="outlined"></v-text-field>
                        <v-icon icon="mdi-microphone"></v-icon>
                        <v-icon icon="mdi-attachment"></v-icon>
                        <v-btn>Send</v-btn>
                    </div>

                </div>
            </div>
        </v-main>
    </v-layout>
</template>

<script setup>
//
// export default {
//     data() {
//         return {
//             messages: [
//                 { text: "Hello", isCurrentUser: false },
//                 { text: "Hi there!", isCurrentUser: true },
//             ],
//             newMessage: "",
//         };
//     },
//     methods: {
//         sendMessage() {
//             if (this.newMessage.trim() === "") return;

//             this.messages.push({
//                 text: this.newMessage,
//                 isCurrentUser: true,
//             });

//             setTimeout(() => {
//                 this.messages.push({
//                     text: "Received your message!",
//                     isCurrentUser: false,
//                 });
//             }, 500);

//             this.newMessage = "";
//         },
//     },
// };

</script>