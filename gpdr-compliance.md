# Apache Iceberg and GDPR's "the right to be forgotten"

Data lakes used to have problems with ACID transactions when using Apache Hive, and compliance with privacy laws such as GDPR has been a bottleneck.

In order to delete client records to comply with these laws, you had to re-create the table excluding those target records for removal. You needed to use external processes with file systems to deal with the compliance issue.

Iceberg has implemented ACID guarantees on data lakes, and it is now easy to comply with "right to be forgotten" as you would delete a record on an OLTP database with SQL scripts. Still, to be fully compliant with GDPR, you have to ensure that historical versions will also be cleaned up.

The challenge is that in a data pipeline, there are cases where you need to retain the historical versions for some time. How you as a data steward deal with both of these issues is to apply fine-grained access control on your data lake.

There is a need to communicate the SLAs with your clients that when they want their data to be deleted, soft deletes can be done right away but historical versions will be retained for some time, allowing them to expire based on their retention time, but only certain people should be able to access historical versions.

These are possible steps on how Apache Iceberg can be leveraged to comply with GDPR:
1. Communicate your SLAs regarding the client's right to be forgotten
2. Set up fine-grained access control on who can access historical versions on your data lake 

    ↪️ Data Engineers, Stewards, Compliance Officers (have access to historical versions) 

    ↪️ Data Analysts and other downstream users (have access only to the current version)

3. Soft delete client records so that the current snapshot will have those records removed
4. Hard delete by allowing the historical snapshots' retention period to expire