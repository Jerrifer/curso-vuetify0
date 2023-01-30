<template>
    <v-container>
        <v-layout>
            <v-flex class="dark">
                <v-btn>Text</v-btn>
                <v-btn color="primary">Text</v-btn>
                <v-btn light color="blue">Text</v-btn>
                <v-btn color="primary" flat>Sin fondo</v-btn>
                <v-btn color="warning" large>Largo</v-btn>
                <v-btn color="warning" small>pequeño</v-btn>
                <v-btn color="warning" disabled>disabled</v-btn>
                <v-btn color="info" depressed>Sin sombra</v-btn>
                <v-btn icon>
                    <v-icon>
                        mdi-heart
                    </v-icon>
                </v-btn>

                <v-btn class="success" fab>
                    <v-icon>
                        mdi-heart
                    </v-icon>
                </v-btn>

                <v-btn class="success" fab small>
                    <v-icon>
                        mdi-heart
                    </v-icon>
                </v-btn>

                <v-btn class="success" fab large>
                    <v-icon>
                        mdi-heart
                    </v-icon>
                </v-btn>

                <v-btn color="dark">
                    Text
                    <v-icon>mdi-thumb-up</v-icon>
                </v-btn>

                <v-btn color="dark">
                    Text
                    <v-icon class="ml-2">mdi-thumb-up</v-icon>
                </v-btn>

                <v-btn color="secondary">
                    Text
                    <v-icon right>mdi-thumb-up</v-icon>
                </v-btn>

                <v-btn color="secondary">
                    <v-icon left>mdi-thumb-up</v-icon>
                    Text
                </v-btn>

                <v-btn color="success" outlined>
                    <v-icon left>mdi-thumb-up</v-icon>
                    Text
                </v-btn>

                <v-btn color="success" outlined block>
                    <v-icon left>mdi-thumb-up</v-icon>
                    Text
                </v-btn>

                <v-btn color="primary" rounded>
                    <v-icon left>mdi-thumb-up</v-icon>
                    Text
                </v-btn>

                <v-btn color="primary" rounded outlined>
                    <v-icon left>mdi-thumb-up</v-icon>
                    Text
                </v-btn>

                <v-btn color="primary" rounded block>
                    <v-icon left>mdi-thumb-up</v-icon>
                    Text
                </v-btn>

                <v-btn color="primary" block fab>
                    Text
                </v-btn>

            </v-flex>
        </v-layout>
    </v-container>
</template>