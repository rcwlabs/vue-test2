<template>
  <div class="component">
      <h1>The User component</h1>
      <p>I'm the user</p>
      <button @click="changeName">Change my name</button>
      <hr>
      <div class="row">
        <div class="col-xs-12 col-sm-6">
            <user-detail 
                :name='name' 
                :age='age'
                @nameWasReset="name = $event">
            </user-detail>
          </div>
          <div class="col-xs-12 col-sm-6">
              <user-edit :age="age" @ageWasEdited="age = $event"></user-edit>
          </div>
      </div>
  </div>
</template>

<script>
import UserDetail from './UserDetail'
import UserEdit from './UserEdit'

export default {
    data: function() {
        return {
            name: 'Robert',
            age: 21
        }
    },
    methods: {
        changeName: function() {
            this.name = 'Nellie'
        }
    },
    components: {
        UserDetail,
        UserEdit
    }
}
</script>
