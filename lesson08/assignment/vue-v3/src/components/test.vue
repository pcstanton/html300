<template>
<div>
<h2>The Register</h2>
<p>A simple v-model register for binding your full name. </p>
<select v-model="selected">
<option disabled value="">Select Title</option>
<option>Mr.</option>
<option>Mrs.</option>
<option>Miss. </option>
</select>
<span>{{ selected }}</span> <br>
<input type="text" v-model="first_name" placeholder="Enter first name">
<p>{{first_name}}</p>
<input type="text" v-model="last_name" placeholder="Enter last name">
<p>{{last_name}}</p>
<button>Output Full Name</button>
<p>{{selected |capitalize}} {{last_name |capitalize}} {{first_name |capitalize}}</p>
</div>
</template>

<script>
export default {
        name: 'test',
        data() {
            return {
                selected: '',
                first_name: '',
                last_name: ''
            }
        },
        filters: {
            capitalize: function(value) {
                if (!value) return ''
                value = value.toString()
                return value.charAt(0).toUpperCase() + value.slice(1)
            }
        }
    } 
</script>