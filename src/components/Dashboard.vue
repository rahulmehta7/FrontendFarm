<template>
<div class="dashboard">
    <input-container @emit-to-add="addRow"></input-container> 
    <div class="dashboard-tableview">
      <table-view 
        :tableData="data">
      </table-view>
    </div> 
  </div>
</template>

<script>
import InputContainer from './InputContainer'
import TableView from './TableView'
export default {
  name: 'Dashboard',
  data(){
        const data = [
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
    TableView
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
}
.dashboard-tableview {
  margin-top: 5em;  
}

</style>
