<template>
    <input
    type="email"
    class="form-control"
    placeholder="E-mail"
    :value="email"
    @input="update($event)"
    pattern="^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$"
    :class="{
        'is-valid':
        validateEmail(email),
        'is-invalid':
       !validateEmail(email),
    }"
    />
</template>

<script>
import validateEmail from '../validate-email';

export default {
    name: 'EmailInput',
    props: ['email'],
    methods: {
        update($event) {
            this.$emit('update:email', $event.target.value)
        },
        validateEmail
    }
}
</script>

