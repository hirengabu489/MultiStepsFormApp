<template>
  <div>
    <p class="text-3xl font-bold mb-9 mt-3">General Information</p>
    <div>
      <div>
        <label class="font-bold text-2xl" for="name">Your good name?</label>
        <br />
        <input v-bind:value="formValue.name" type="text" name="name" id="name"
          class="text-2xl p-2 border-2 rounded border-green-300 mt-4 mb-4" @input="onChange" />
      </div>
      <div>
        <label class="font-bold text-2xl" for="dob">When were you born?</label>
        <br />
        <input v-bind:value="formValue.dob" type="date" name="dob" id="dob"
          class="text-2xl p-2 border-2 rounded border-green-300 mt-4 mb-4" @input="onChange" />
      </div>
      <div>
        <label class="font-bold text-2xl" for="age">How old are you?</label>
        <br />
        <input type="text" name="age" id="age" class="text-2xl p-2 border-2 rounded border-green-300 mt-4 mb-4"
          v-bind:value="formValue.age" @input="onChange" />
      </div>
      <div>
        <label class="font-bold text-2xl" for="email">Where we can send you e-mails?</label>
        <br />
        <input type="text" name="email" id="email" class="text-2xl p-2 border-2 rounded border-green-300 mt-4 mb-4"
          v-bind:value="formValue.email" @input="onChange" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Information',
  props: {
    formValue: {
      email: String,
      name: String,
      dob: String,
      age: Number,
    }
  },
  emits: ['formValueChange'],
  methods: {
    onChange(e) {
      this.$emit('formValueChange', {
        label: 'information',
        data: {
          ...this.formValue,
          [e.target.name]: e.target.value
        }
      })
    }
  }
}
</script>
