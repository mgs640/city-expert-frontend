<template>
    <v-col
            cols="12"
            sm="6"
            md="4"
            lg="3"
    >
        <router-link :to="{ name: 'PublicTestShowPage', params: { test_id: test.id }}">
            <v-img
                    :aspect-ratio="16/9"
                    :src="test['image_url']"
                    class="test-image"
                    :class="test['status']"
            ></v-img>
        </router-link>

        <div class="d-flex justify-center mb-6">
            <v-btn icon disabled style="margin-right: 10px">
                <v-icon>mdi-thumb-up</v-icon>
                <span>{{ test['likes'] }}</span>
            </v-btn>
            <v-btn icon disabled>
                <v-icon>mdi-thumb-down</v-icon>
                <span>{{ test['dislikes'] }}</span>
            </v-btn>
        </div>

    </v-col>
</template>

<script>
    export default {
        name: 'PublicTestListItem',
        props: [
            'test',
        ],
    }
</script>

<style>
    .test-image {
        border-bottom-width: 5px;
        border-bottom-style: solid;
    }

    .test-image.correct_answer {
        border-bottom-color: lawngreen;
    }

    .test-image.show_answer {
        border-bottom-color: red;
    }

    .test-image.in_process {
        border-bottom-color: lightgrey;
    }
</style>