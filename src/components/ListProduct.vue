<template>
   <q-dialog v-model="showForm" class="backdrop-filter" persistent>
    <q-card class="form-container" style="border-radius:10px;width:600px">
      <div class="form-header">
        Add your product
      </div>
    <q-form
      @submit="onSubmit"
      @reset="onReset"
      class="q-pa-md"
    >
      <q-input
        filled
        v-model="name"
        label="What's your name? *"
        hint="First & Last Name"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type something']"
      />

      <q-input
        filled
        v-model="name"
        label="Which email address shall we use? *"
        hint="Don't worry, we're not going to spam you"
        class="q-mt-md"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type something']"
      />

       <q-input
        filled
        v-model="name"
        label="What's the name of your product? *"
        hint="This will be the listing's title"
        class="q-mt-md"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type something']"
      />

       <q-input
        filled
        v-model="name"
        label="Give us a short description of your product? *"
        hint="Up to 100 characters"
        maxlength="100"
        counter
        type="textarea"
        autogrow
        class="q-mt-md"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type something']"
      />

      <q-input
        filled
        v-model="name"
        label="Give us a long description of your product? *"
        hint="Up to 400 characters"
        maxlength="400"
        counter
        type="textarea"
        class="q-mt-md"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type something']"
      />

      <q-input
        filled
        v-model="name"
        label="Website/Product URL *"
        class="q-mt-md"
        type="email"
        lazy-rules
        :rules="[ val => val && val.length > 0 || 'Please type something']"
      />

      <q-select
        filled
        v-model="category"
        multiple
        :options="options"
        label="Which category suits your product best?"
      />

      <q-file outlined v-model="logo" label="Upload the logo" filled class="q-mt-md">
        <template v-slot:prepend>
          <q-icon name="attach_file" />
        </template>
      </q-file>
      <q-toggle v-model="accept" label="I accept the license and terms" class="q-mt-md"/>

      <div class="q-mt-md">
        <q-btn label="Submit" type="submit" class="gradiant-btn" size="md" unelevated no-caps padding="10px 40px"/>
        <q-btn label="Close" type="reset" color="primary" no-caps flat class="q-ml-sm" padding="10px 40px" @click="$emit('closeForm',false)"/>
      </div>
    </q-form>
     </q-card>
    </q-dialog>
</template>

<script>
export default {
  name: 'ListProduct',
  data(){
    return{
      showForm: false,
      name: null,
      age: null,
      category:null,
      logo:null,
      options: [
        'Analyics',
        'Cap Table',
        'Collaboration & Communication',
        'CRM',
        'Customer Support',
        'Deployment',
        'Design',
        'Development',
        'Domain names',
        'Early users',
        'eCommerce',
        'Feedback & Bugtracking',
        'Finance',
        'Forms & Surveys',
        'Funding Docs',
        'Hosting',
        'HR',
        'Idea generation',
        'Investor relations',
        'Launching',
        'Learning',
        'Legal',
        'Lodging',
        'Market research',
        'Marketing',
        'Mobile App Analytics',
        'Mockups & Wireframing',
        'MVP',
        'Naming',
        'Newsletters',
        'Outdoor Activities',
        'Outsourcing',
        'Payments',
        'Pitch & Deck',
        'Presentations',
        'Product Demo',
        'Product Management',
        'Productivity',
        'Project Management',
        'Raising Capital',
        'Revenue Models',
        'Sales',
        'Social Tools',
        'Task Management',
        'Videos'
      ],
      accept: false
    }
  },
  props: {
    showProductForm:{
      type: Boolean
    }
  },
  watch:{
    showProductForm(val){
      this.showForm = val
    }
  },
  methods: {
    onSubmit () {
      if (this.accept !== true) {
        this.$q.notify({
          color: 'red-5',
          textColor: 'white',
          icon: 'warning',
          message: 'You need to accept the license and terms first'
        })
      }
      else {
        this.$q.notify({
          color: 'green-4',
          textColor: 'white',
          icon: 'cloud_done',
          message: 'Submitted'
        })
      }
    },

    onReset () {
      this.name = null
      this.age = null
      this.accept = false
    }
  }

}
</script>

<style>
.form-header{
  background: linear-gradient(
    277.14deg,
    #25f6ff -15.2%,
    #7782ff 55.76%,
    #ff5196 113.69%
  );
  border-radius: 10px;
  color: white;
  font-weight: bold;
  padding: 16px;
  font-size: 20px;
}
.backdrop-filter{
  backdrop-filter: blur(5px);
}
.form-container{
  background: white;
    font-family: 'Poppins';

}
</style>
