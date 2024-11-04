<template>
    <div>
      <h2>Contactez-nous</h2>
      <form @submit.prevent="handleSubmit">
        <div class="mb-3">
          <label for="name" class="form-label">Nom</label>
          <input type="text" id="name" class="form-control" v-model="formData.name" required />
        </div>
        <div class="mb-3">
          <label for="email" class="form-label">Email</label>
          <input type="email" id="email" class="form-control" v-model="formData.email" required />
        </div>
        <div class="mb-3">
          <label for="subject" class="form-label">Sujet</label>
          <input type="text" id="subject" class="form-control" v-model="formData.subject" required />
        </div>
        <div class="mb-3">
          <label for="message" class="form-label">Message</label>
          <textarea id="message" class="form-control" v-model="formData.message" required></textarea>
        </div>
        <button type="submit" class="btn btn-primary">Envoyer</button>
      </form>
  
      <div v-if="submitted" class="mt-4">
        <h3>Informations soumises :</h3>
        <p><strong>Nom :</strong> {{ formData.name }}</p>
        <p><strong>Email :</strong> {{ formData.email }}</p>
        <p><strong>Sujet :</strong> {{ formData.subject }}</p>
        <p><strong>Message :</strong> {{ formData.message }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ContactFormComponent',
    data() {
      return {
        formData: {
          name: '',
          email: '',
          subject: '',
          message: '',
        },
        submitted: false,
      };
    },
    methods: {
      handleSubmit() {
        this.submitted = true;
        // Vous pouvez également réinitialiser le formulaire si nécessaire
        // this.formData = { name: '', em
      },
    },
  };
  </script>  