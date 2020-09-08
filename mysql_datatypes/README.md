# MySQL DataTypes:
MySQL has a variety of datatypes,  
- Numeric data types
- Boolean data type
- String data types
- Date and Time data types
- Spatial data types

## > Numeric Data Types:
| Numeric Data Types	| Description                               | Specs                    |
| ------------------- | :---------------------------------------- | :------------------------|
| TINYINT             | A very small integer                      | Integer (-128 to 127) |
| SMALLINT	          | A small integer                           | Integer (-32768 to 32767) |
| MEDIUMINT	          | A medium-sized integer                    | Integer (-8388608 to 8388607) |
| INT	                | A standard integer                        | Integer (-2147483648 to 214748-3647) |
| BIGINT	            | A large integer                           | Integer (-9223372036854775808 to 9223372036854775807) |
| DECIMAL	            | A fixed-point number                      | "DOUBLE" stored as string |
| FLOAT	              | A single-precision floating point number  | Decimal (precise to 23 digits) |
| DOUBLE	            | A double-precision floating point number  | Decimal (24 to 53 digits) |
| BIT	                | A bit field                               | 1 bit |

## > Boolian data types:
MySQL doesn't have its own `Boolian` data type. MySQL uses `TINYINT` to represent `Boolian` data types.  

## > String data types:
In MySQL, a string can hold anything from a small text to a binary data such as images or files.  

| string Data Types 	| Description                                                                  | Specs                    |
| ------------------- | :--------------------------------------------------------------------------- | :------------------------|
| CHAR	              | A fixed-length nonbinary (character) string                                  | String (0 - 255) |
| VARCHAR	            | A variable-length non-binary string                                          | String (0 - 255) |
| BINARY	            | A fixed-length binary string                                                 | - |
| VARBINARY	          | A variable-length binary string                                              | - |
| TINYBLOB	          | A very small BLOB (binary large object)                                      | - |
| BLOB	              | A small BLOB                                                                 | String (0 - 65535) |
| MEDIUMBLOB	        | A medium-sized BLOB                                                          | String (0 - 16777215) |
| LONGBLOB	          | A large BLOB                                                                 | String (0 - 4294967295) |
| TINYTEXT	          | A very small non-binary string                                               | String (0 - 255) |
| TEXT	              | A small non-binary string                                                    | String (0 - 65535) |
| MEDIUMTEXT	        | A medium-sized non-binary string                                             | String (0 - 16777215) |
| LONGTEXT	          | A large non-binary string                                                    | String (0 - 4294967295) |
| ENUM	              | An enumeration; each column value may be assigned one enumeration member     | One of preset options |
| SET	                | A set; each column value may be assigned zero or more SET members            | Selection of preset options |

## > Date and Time data types:

| Date & Time Data Types	| Description                                         | Specs                    |
| ----------------------- | :-------------------------------------------------- | :------------------------|
| DATE	                  | A date value in CCYY-MM-DD format                   | YYYY-MM-DD |
| TIME	                  | A time value in hh:mm:ss format                     | HH:MM:SS |
| DATETIME	              | A date and time value inCCYY-MM-DD hh:mm:ssformat   | YYYY-MM-DD HH:MM:SS |
| TIMESTAMP	              | A timestamp value in CCYY-MM-DD hh:mm:ss format     | YYYYMMDDHHMMSS |
| YEAR	                  | A year value in CCYY or YY format                   | CCYY or YY |

## > Spatial data types:
MySQL supports many spatial data types that contain various kinds of geometrical and geographical values,  

| Date & Time Data Types	| Description                             |
| ----------------------- | :-------------------------------------- |
| GEOMETRY	              | A spatial value of any type |
| POINT	                  | A point (a pair of X-Y coordinates) |
| LINESTRING	            | A curve (one or more POINT values) |
| POLYGON	                | A polygon |
| GEOMETRYCOLLECTION	    | A collection of GEOMETRYvalues |
| MULTILINESTRING	        | A collection of LINESTRINGvalues |
| MULTIPOINT	            | A collection of POINTvalues |
| MULTIPOLYGON	          | A collection of POLYGONvalues |















