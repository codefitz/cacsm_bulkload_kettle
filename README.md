# CA Cloud Service Management Bulk Load CIs

Pentaho Kettle script for bulk uploading of CIs to CA Cloud Service Management

I no longer have access to Cloud Service Management so these are provided "as is". Contributions and improvements welcome. Happy to assist with bug-squashing and implementation in a limited capacity.

## How To

Tested on Bamboo Only.

Install Kettle from here: http://community.pentaho.com/projects/data-integration

### Bulk Import

* Use **main_ci_import.kjb** to import bulk CIs from a text file (see sample *cis.csv*).
* Replace user login details in **tf_import_ci.ktr** input step:
 * userName
 * userPassword
 * responseFormat - leave as "json"
 * url

* Update HTTP Post step with http login details

### Bulk Relate

* Use **main_ci_relate.kjb** to relate CIs to each other from text file input (see sample *ci_rels.csv*).
* Replace user login details in **tf_relate_ci.ktr** input step:
 * userName
 * userPassword
 * responseFormat - leave as "json"
 * url

* Update HTTP Post step with http login details
