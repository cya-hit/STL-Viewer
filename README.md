# This is a static HTML frontend project for reconstructing .stl files
You can mount it independently on an Nginx server, while other frontend pages can redirect to this mounted interface. (Note to handle cross-origin issues during mounting) Here's an example of frontend redirection to this page:

``` html
<el-table-column label="Preview" width="70">
  <template v-slot="scope">
    <span v-if="scope.row.finish_time !== null">
      <a :href="'/cardiacSTLViewer/model.html?dataid='+scope.row.data_id+'&type=1'" target="_blank">Preview</a>
    </span>
  </template>
</el-table-column>

