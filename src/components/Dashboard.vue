<template>
<section class="dashboard">
    <input-container @emit-to-add="addRow"></input-container> 
    <div v-if="false" class="dashboard-tableview">
      <table-view 
        :tableData="data">
      </table-view>
    </div>
    <div class="dashboard-cardview">
      <div v-for="entry in data" :key="entry.web_server_name">
        <card-view :value="entry"> 
        </card-view>
      </div>
    </div>
  </section>
</template>

<script>
import InputContainer from './InputContainer'
import TableView from './TableView'
import CardView from './CardView'
export default {
  name: 'Dashboard',
  data(){
        const data = [
        { 'web_server_name': 'https://www.google.com/', 'test_time': 'dfd', 'status': 'Active'},
        { 'web_server_name': 'https://www.amazon.com/', 'test_time': 'dfd', 'status': 'Active'},
        { 'web_server_name': 'https://www.flipkart.com/', 'test_time': 'dfd', 'status': 'Down'},
        { 'web_server_name': 'https://www.siemens.com/', 'test_time': 'dfd', 'status': 'Active'},
        { 'web_server_name': 'https://www.apple.com/', 'test_time': 'dfd', 'status': 'Down'},
        { 'web_server_name': 'https://www.google.com/', 'test_time': 'dfd', 'status': 'Active'},
        { 'web_server_name': 'https://www.amazon.com/', 'test_time': 'dfd', 'status': 'Active'},
        { 'web_server_name': 'https://www.flipkart.com/', 'test_time': 'dfd', 'status': 'Down'},
        { 'web_server_name': 'https://www.siemens.com/', 'test_time': 'dfd', 'status': 'Active'},
        { 'web_server_name': 'https://www.apple.com/', 'test_time': 'dfd', 'status': 'Down'}
    ]
    return { data };
  },
  components: {
    InputContainer,
    TableView,
    CardView
  },
  methods: {
    addRow(link){
      let entry = {
        'web_server_name': link, 'test_time': '04-15-2021 12:30 AM', 'status': 'Active'
      }
      this.data.push(entry);
    }
  },
}
</script>

<style>
.dashboard {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100%;
  width: 100%
}
.dashboard-tableview {
  margin-top: 5em;  
}

.dashboard-cardview {
  display: flex;
  flex-direction : row;
  flex-wrap: wrap
}

</style>
