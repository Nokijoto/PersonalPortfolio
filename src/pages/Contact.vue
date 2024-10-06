<script setup>

</script>

<template>
  <div class="wrapper">
    <h1>Contact</h1>
    <form>
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" id="name" name="name" placeholder="Your Name">
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" name="email" placeholder="Your Email">
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea id="message" name="message" placeholder="Your Message"></textarea>
      </div>
      <button type="submit">Send</button>
    </form>
  </div>
</template>

<style scoped>

.wrapper {
  display: flex;
  flex-direction: column;
  align-items: left;
  gap: 1rem;
  margin-left: 2rem;
  margin-right: 2rem;
}
.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  margin-bottom: 10px;
}

button {
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #3e8e41;
}

button:focus {
  outline: none;
}

h1 {
  font-size: 2rem;
  font-weight: bold;
  font-family: Sigmar One,serif;
  margin-bottom: 1rem;
}
</style>