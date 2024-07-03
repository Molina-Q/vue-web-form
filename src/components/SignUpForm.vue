<template>
    <form>
        <label for="email">Email:</label>
        <input v-model="email" type="email" id="email" required>

        <label for="password">Password:</label>
        <input v-model="password" type="password" id="password" required>

        <label for="role">Role:</label>
        <select id="role" v-model="role">
            <option value="">-- None --</option>
            <option value="developer">Web Developer</option>
            <option value="designer">Web Designer</option>
        </select>

        <div class="terms">
            <input v-model="terms" type="checkbox" required>
            <label>Accept terms and conditions</label>
        </div>

    </form>

    <p>Email: {{ email }}</p>
    <p>Password: {{ password }}</p>
    <p>Role: {{ role }}</p>
    <p>Terms accepted: {{ terms ? 'Yes' : 'No' }}</p>
</template>

<script>
export default {
    data() {
        return {
            email: '',
            password: '',
            role: '',
            terms: false,
        }
    }
}
</script>

<style>
form {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}

label {
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}

input,
select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
}

input[type="checkbox"] {
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 2px;
}
</style>