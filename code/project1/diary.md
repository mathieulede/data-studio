## Diary

### Circle packing
https://stackoverflow.com/questions/21068151/generating-visually-pleasing-circle-pack

### Bin packing
https://github.com/jakesgordon/bin-packing/

### Memory error
The csv files have millions of rows and merging produces a memory error. Have to do the merge in PSQL.
https://stackoverflow.com/questions/31765123/pandas-dataframe-merge-memoryerror

```sql
CREATE TABLE buildings (
    BUILDING_CITY             varchar(80),
    BUILDING_ID               varchar(10),
    BUILDING_NAME             varchar(80),
    BUILDING_STATE            varchar(10),
    BUILDING_ZIP              varchar(40)
);

CREATE TABLE fine_arts (
    FAARTIST_SURNAME              varchar(120),
    FAP_DEFINITION                varchar(40),
    FINEARTS_DATE                 varchar(40),
    FINEARTS_APPRAISAL            varchar(40),
    FINEARTS_BUILDING_ID          varchar(40),
    FINEARTS_DEACCESSIONED        varchar(40),
    dim_width_inches              varchar(20),
    dim_height_inches             varchar(20)
);

copy buildings from '/Users/mathieurudaz/Desktop/ds-tests/FACIT/buildings.csv' delimiter ',' CSV HEADER;

copy fine_arts from '/Users/mathieurudaz/Desktop/ds-tests/FACIT/fine_arts.csv' delimiter ',' CSV HEADER;

copy (
SELECT * 
FROM fine_arts
LEFT JOIN buildings on buildings.BUILDING_ID = fine_arts.FINEARTS_BUILDING_ID
) to '/Users/mathieurudaz/Desktop/ds-tests/FACIT/merge.csv' delimiter ',' csv header;
```