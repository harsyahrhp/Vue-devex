<template>
  
  <div class="table">
    <h1>Our Product</h1>
    <DxDataGrid
      :data-source="dataSource"

      :show-borders="true"
     
      :height="330"

    />
  </div>
</template>
<script lang="ts">
import DxFilterBuilder from 'devextreme-vue/filter-builder';
import DxButton from 'devextreme-vue/button';
import DxDataGrid from 'devextreme-vue/data-grid';
import DataSource from 'devextreme/data/data_source';
import ODataStore from 'devextreme/data/odata/store';


export default {
  components: {
    DxFilterBuilder,
    DxButton,
    DxDataGrid,
  },
  data() {
    return {
      dataSource: new DataSource({
        store: new ODataStore({
          fieldTypes: {
            Product_Cost: 'Decimal',
            Product_Sale_Price: 'Decimal',
            Product_Retail_Price: 'Decimal',
          },
          url: 'https://js.devexpress.com/Demos/DevAV/odata/Products',
        }),
        select: [
          'Product_ID',
          'Product_Name',
          'Product_Cost',
          'Product_Sale_Price',
          'Product_Retail_Price',
          'Product_Current_Inventory',
        ],
      }),
    };
  },
  methods: {
   
  },
};
</script>
<style scoped>
.table{
  padding:5rem;
}

h1{
  font-size: 50px;
}
</style>
