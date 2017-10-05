<template>
  <div class="grid">
    <kendo-datasource
      ref="datasource"
      :type="'odata'"
      :pageSize="20"
      :transportRead="'https://demos.telerik.com/kendo-ui/service/Northwind.svc/Customers'"
    ></kendo-datasource>
    <kendo-grid
      :height="550"
      :dataSourceRef="'datasource'"
      :groupable='true'
      :sortable='true'
      :pageable-refresh='true'
      :pageable-page-sizes='true'
      :pageable-button-count="5">
      <kendo-grid-column
        field="ContactName"
        title="Contact Name"
        :width="250">
      </kendo-grid-column>
      <kendo-grid-column
        field="ContactTitle"
        title="Contact Title">
      </kendo-grid-column>
      <kendo-grid-column
        field="CompanyName"
        title="Company Name">
      </kendo-grid-column>
      <kendo-grid-column
        field="Country"
        title="Country"
        :width="150">
      </kendo-grid-column>
    </kendo-grid>
  </div>
</template>

<script>
export default {
  name: 'grid'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .grid {
    padding: 10px;
  }
</style>
