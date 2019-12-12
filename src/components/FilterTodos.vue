<template>
  <div>
     <div class="input-field col s12 z-depth-1">
       <div class="waves-effect waves-teal btn-flat">Filter Todos</div>
      <select @change="filterTodos($event)" class="browser-default">
        <option value="200">200</option>
        <option value="100">100</option>
        <option value="50">50</option>
        <option value="20">20</option>
        <option value="10">10</option>
        <option value="5">5</option>
      </select>
      <!-- <label>Materialize Select</label> -->
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "FilterTodos",
  methods: mapActions(["filterTodos"])
};
</script>

<style>
select {
  margin-top: 20px;
  padding: 6px;
  border: #004d40 1px solid;
}
</style>