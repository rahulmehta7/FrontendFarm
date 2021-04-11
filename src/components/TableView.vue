<template>
    <section>

        <b-table
            :data="tableData"
            :columns="columns"
            :checked-rows.sync="checkedRows"
            checkable
            :checkbox-position="checkboxPosition">

            <b-table-column field="web_server_name" sortable v-slot="props">
                {{ props.row.web_server_name }}
            </b-table-column>
            <b-table-column field="test_time" sortable v-slot="props">
                {{ props.row.test_time }}
            </b-table-column>
            <b-table-column field="status"  sortable v-slot="props">
                {{ props.row.status }}
            </b-table-column>

            <template #bottom-left>
                <b>Total checked</b>: {{ checkedRows.length }}
            </template>
        </b-table>

    </section>
</template>

<script>
    export default {
        data() {
            return {
                checkboxPosition: 'left',
                checkedRows: [],
                columns: [

                    {
                        field: 'web_server_name',
                        label: 'WebServer Name',
                    },
                    {
                        field: 'test_time',
                        label: 'Test Done',
                    },                    
                    {
                        field: 'status',
                        label: 'Current Status',
                    }
                ]
            }
        },
        props: {
            tableData: {
                type: Array,
                required: true,
            },
        },
    }
</script>
<style>
</style>