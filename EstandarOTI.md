# Estándar OTI OEFA
<img src="https://pifa.oefa.gob.pe/mfiscamb/images/oefa-logo-header.png" alt="Logo de OpenAI" width="40%" height="40%">
<!-- ![OEFA](https://pifa.oefa.gob.pe/mfiscamb/images/oefa-logo-header.png) -->

## Aplicación a tablas
La nomenclatura de las tablas se realizan conforme al siguiente formato:

### Según su naturaleza
| Abreviatura   | Nombre     |
|---------------|------------|
| MA            | Maestro    |
| MV            | Movimiento |
| TM            | Temporal   |
| GE            | General    |


### Según su estructura
| Abreviatura   | Nombre    |
|---------------|-----------|
| P             | Plano     |
| C             | Cabecera  |
| D             | Detalle   |

### Ejemplo de combinaciones
- MAP: Maestra Plana
- MVC: Movimiento Cabecera
- MVD: Movimiento Detalle
- TMP: Temporal Plano 

## Aplicación a los campos
| TIPO DATO  | CONTENIDO     | NOMENCLATURA |
|------------|---------------|--------------|
| NUMBER     | Número        | NU           |
| INTEGER    | Número        | NU           |
| FLOAT      | Número        | NU           |
| BLOB       | Binario       | BL           |
| CLOB       | Texto Grande  | CL           |
| NCLOB      | Texto Grande  | CL           |
| DATE       | Fecha         | FE           |
| TIMESTAMP  | Fecha         | FE           |
| RAW        | Binario       | RW           |
| VARCHAR2   | Texto         | TX           |
| CHAR       | Texto         | TX           |
| NVARCHAR2  | Texto         | TX           |
| NCHAR      | Texto         | TX           |

### Ejemplo de nombre de campos
- TX_DESCRIPCION
- FE_FECHA_REGISTRO
- FE_FECHA_HORA_MODIFICA
- BL_FOTO_POSTULANTE

### Comentarios en la campos de la tabla
| CASO | EJEMPLO |
|------|---------|
| Cuando el campo de la tabla es un dato confidencial, es necesario que se especifique para que quede registrado en la Base de Datos. | COMMENT ON COLUMN <br> ESQUEMA.TABLA.CODIGO_DECLARACION_JURADA_TX IS Código de la declaración jurada.Dato (CONFIDENCIAL)'; |
| Cuando se trate de un campo Primary key, y si este utiliza una secuencia, en el comentario deberá indicar el nombre de la secuencia. | COMMENT ON COLUMN <br>ESQUEMA.TABLA.ID_ACTA_NU IS 'Identificador del registro en la tabla de Actas Secuencia: NOMBRE SECUENCIA'; |
| Cuando se trate de un campo identificador de llave foránea (Foreign Key), en el comentario deberá indicar la tabla a la que tiene referencia. | COMMENT ON COLUMN <br>ESQUEMA.TABLA.ID_UNIDAD_FISCAL_NU IS 'Foránea de la tabla Unidad Fiscalizadora'; |
| Cuando se trate un campo del tipo flag o booleano, se debe especificar los posibles valores que contendrá.| COMMENT ON COLUMN <br> ESQUEMA.TABLA.ACTIVO IS 'Flag indicador si el registro se encuentra Activo = 1 o No_Activo = 0'; |

## Aplicación a constraints
| Tipo de Constraints | Prefijo |
| --------------------|---------|
| Primary Key         | PK      |
| Foreign Key         | FK      |
| Unique              | UK      |
| Check Constraint    | CK      |
