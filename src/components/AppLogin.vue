<template>
    <v-container>
        <v-form @submit.prevent="submit">
            <v-text-field
                    v-model="name"
                    :rules="nameRules"
                    :counter="25"
                    label="Name"
                    required
            ></v-text-field>
            <v-text-field
                    v-model="password"
                    label="password"
                    type="password"
                    required
            ></v-text-field>
            <v-checkbox
                    v-model="checkbox"
                    label="Do you agree?"
                    required
            ></v-checkbox>

            <v-btn
                    color="green"
                    type="submit"
            >
                submit
            </v-btn>
            <v-btn @click="clear">clear</v-btn>
        </v-form>
    </v-container>
</template>

<script>
    import axios from 'axios'

    export default {
        name: "AppLogin",
        data: () => ({
            valid: true,
            name: '',
            nameRules: [
                v => !!v || 'Name is required',
                v => (v && v.length <= 10) || 'Name must be less than 10 characters'
            ],
            password: '',
            checkbox: false
        }),

        methods: {
            submit () {
                console.log("Hello User!");
            },
            clear () {
                this.$refs.form.reset()
            }
        }
    }
</script>

<style scoped>

</style>