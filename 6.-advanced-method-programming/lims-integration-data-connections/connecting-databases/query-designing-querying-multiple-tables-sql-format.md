# Query Designing : Querying MULTIPLE tables (SQL Format):

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td><h3>Full Inner Join</h3><p>Selects all rows from both tables as long as there is a match between the columns in both tables.</p><p></p><p></p><p><br></p></td><td></td><td><a data-footnote-ref href="#user-content-fn-1">Full inner Join Example</a></td><td><a href="../../../.gitbook/assets/innerjoin2.png">innerjoin2.png</a></td></tr><tr><td><h3>Left Join</h3><p>Selects all rows from the left table (table1), with the matching rows in the right table (table2). The result is NULL in the right side when there is no match. <br><br></p></td><td></td><td><a data-footnote-ref href="#user-content-fn-2">Left Join Example</a></td><td><a href="../../../.gitbook/assets/leftjoin.png">leftjoin.png</a></td></tr><tr><td><h3>Right Join</h3><p>Selects all rows from the right table (table2), with the matching rows in the left table (table1). The result is NULL in the left side when there is no match.</p><p><br></p></td><td></td><td><a data-footnote-ref href="#user-content-fn-3">Right Join Example</a></td><td><a href="../../../.gitbook/assets/rightjoin.png">rightjoin.png</a></td></tr><tr><td><h3>Full Outer Join</h3><p>Selects all rows from the right table (table2), with the matching rows in the left table (table1). The result is NULL in the left side when there is no match.</p></td><td></td><td><p></p><p></p><p><a data-footnote-ref href="#user-content-fn-4">Full Outer Join Example</a></p></td><td><a href="../../../.gitbook/assets/fullOuterJoin.png">fullOuterJoin.png</a></td></tr><tr><td></td><td></td><td></td><td></td></tr><tr><td></td><td></td><td></td><td></td></tr></tbody></table>

If you want to connect more than 2 table, simply add more JOINS to the query!

<figure><img src="../../../.gitbook/assets/image (23) (1) (1) (1).png" alt="" width="290"><figcaption></figcaption></figure>



```sql
SELECT t1.column, t2.column, t3.column, t4.column
FROM table1 AS t1
JOIN table2 AS t2 ON t1.column_name=t2.column_name
JOIN table3 AS t3 ON t1.column_name=t3.column_name
JOIN table4 AS t4 ON t2.column_name=t4.column_name
WHERE t1.some_column = value;
```

> **HINT:** Tired of typing the table names all the time?! Use an “ALIAS” and give it a nickname with “…AS \[alias]”!

## Example Query

<figure><img src="../../../.gitbook/assets/image (24) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Let’s say your protocol just scanned your pcr plate: Barcode read was 10001

```sql
SELECT w.well_id, a.big_dye_vol
FROM worklist AS w
JOIN job AS j ON w.job_id = j.job_id
JOIN assay AS a ON j.assay = a.assay
WHERE j.barcode = ‘10001’
```

this would give you the following result set:&#x20;

<figure><img src="../../../.gitbook/assets/image (25) (1) (1) (1).png" alt="" width="170"><figcaption></figcaption></figure>

## Other Types of Querys

### lternate to JOIN using IN or NOT IN (Oracle)

```sql
-- Alternate to JOIN using IN or NOT IN (Oracle)
SELECT se.sequence_name, se.id_sequence, si.s_id_lida, f.id_fraction, f.id_sample, 
si.s_name, f.f_vialbarcode, f.f_keep, f.f_vialtare, f.f_pos2, f.f_processed1, 
f.f_processed2, f.f_volume, f.f_weight, si.s_mass 
FROM fraction f, sample_in si, sequence se 
WHERE se.id_sequence IN 
(SELECT DISTINCT se.id_sequence 
FROM fraction f, sample_in si, sequence se 
WHERE f.f_rackbarcode2 = 'srv002008' 
AND f.f_weight != 0 
AND f.f_keep = 1 
AND f.f_volume > 0 
AND f.f_processed1 = 1 
AND f.f_processed2 = 0 
AND f.id_sample = si.id_sample 
AND se.id_sequence = si.id_sequence)
AND f.f_keep = 1 
AND f.id_sample = si.id_sample 
AND si.id_sequence = se.id_sequence 
ORDER BY f.f_pos2;
```

**Result**: 15 different fields of data based on ten different selection criteria across 3 different tables from 1 barcode.



### Data Conversion with SQL

```sql
-- Data Conversion with SQL
SELECT to_char(smiles(m.ctab)) AS smile_str 
FROM lida_medchem_results r, lida_medchem_moltable m 
WHERE r.cdbregno = 49909 
AND r.cdbregno = m.cdbregno;
```

**Result**: Smile string value `CCN(C)Cc1ccc(cc1)NC(=O)c2ccc3c(c2)n(cn3)C` from ISIS nomenclature in column `m.ctab`.

```sql
-- Converting customer number
SELECT hex(dp_select.cst) AS tempA 
FROM dp, dp_select 
WHERE dp.p = dp_select.p 
AND dp.name = 'QX4087653';
```

**Result**: Customer number as hexadecimal value, later converted to integer to solve issue of leading zeroes (e.g., `004` vs. `4`).

[^1]: ```sql
    SELECT table1.column1, table2.column2
    FROM table1
    JOIN table2
    ON table1.column_name = table2.column_name;
    ```

    Note: You begin using `<table>.<column>`.

[^2]: ```sql
    SELECT table1.column1, table2.column2
    FROM table1
    LEFT JOIN table2
    ON table1.column_name=table2.column_name;
    ```

[^3]: ```sql
    SELECT table1.column1, table2.column2
    FROM table1
    RIGHT JOIN table2
    ON table1.column_name=table2.column_name;
    ```

[^4]: ```sql
    SELECT table1.column1, table2.column2
    FROM table1
    FULL OUTER JOIN table2
    ON table1.column_name=table2.column_name;
    ```
