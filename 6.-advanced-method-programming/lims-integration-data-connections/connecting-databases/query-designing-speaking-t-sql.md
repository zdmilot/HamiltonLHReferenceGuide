# Query Designing: Speaking T-SQL

Here’s a clear breakdown of operations in different scenarios:

<details>

<summary><strong>READ (SELECT)</strong></summary>

* To retrieve data from a table.
*   Example:

    ```sql
    SELECT * FROM job WHERE assay = 'HBV';
    SELECT barcode FROM job WHERE assay = 'HBV';
    ```

</details>

<details>

<summary><strong>WRITE (INSERT)</strong></summary>

* To add new data into a table.
*   Example (with `id` column being auto-incremented):

    ```sql
    INSERT INTO job (barcode, assay)
    VALUES (10003, 'HBV');
    ```

</details>

<details>

<summary><strong>UPDATE</strong></summary>

* To modify existing data in a table.
*   Example:

    ```sql
    UPDATE assay
    SET big_dye_vol = 10
    WHERE assay = 'HIV';
    ```

</details>

<details>

<summary><strong>DELETE</strong></summary>

* To remove data from a table.
*   Example:

    ```sql
    DELETE FROM worklist
    WHERE id = '4' AND job_id = '2';
    ```

**Important Note**: When deleting data, if you do not include a `WHERE` clause, it will remove all rows in the table, which can be very dangerous.

*   Example without a `WHERE` clause (this would delete the entire table content):

    ```sql
    DELETE FROM worklist;
    ```

</details>

