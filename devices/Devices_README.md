# Axonius Devices API Calls
###### All API calls utlize the /api/devices endpoint

## Collection Variables: 

1. `ax_fields` - Axonius fields used for column headers - Required
2. `ax_filter` - Axonius AQL used to filter devices
3. `ax_assest_entity_split` - true/false - explode each row for each adapter connected to assest - Required 
4. `ax_field_to_split_by` - Axonius field used to explode additional rows - Not Required
5. `ax_device_id` - Axonius Device ID for device specific operations


## Workflows for API Calls

#### Export CSV
* Utilize Saved Queries `GET` Request to identify data needed for the API Call.
   * data > attributes > view > fields = `ax_fields` Collection Variable 
   * data > attributes > query > filter = `ax_filter` Collection Variable
* If using `ax_field_to_split_by` ensure you are using the correct Request Body when issuing Call.