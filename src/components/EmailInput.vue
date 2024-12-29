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
        email && /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/.test(email),
        'is-invalid':
        email && !/^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/.test(email),
    }"
    />
</template>

<script>
export default {
    name: 'EmailInput',
    props: ['email'],
    methods: {
        update($event) {
            this.$emit('update:email', $event.target.value)
        }
    }
}
</script>

