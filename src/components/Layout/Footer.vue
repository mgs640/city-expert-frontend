<template>
    <v-card height="150">
        <v-footer
            app
            absolute
            class="font-weight-medium"
        >
            <v-col
                class="text-center"
                cols="12"
            >
                {{ new Date().getFullYear() }} - {{ $t('APP_NAME') }}
            </v-col>
        </v-footer>
    </v-card>
</template>
