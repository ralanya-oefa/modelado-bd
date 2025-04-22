# Biblioteca

## Listado de Entidades

### material (MAP)
- PK_MATERIAL **(PK)**
- FK_AREA_MATERIAL **(FK)**
- TITULO
- AUTOR
- ISBN
- PIE DE IMPRENTA
- SUSTENTO
- ENLACE WEB
- OBSERVACIONES
- TITULO DE REVISTA
- EDITORIAL
- ISSN
- SUSTENTO
- OBSERVACIONES

### editorial (GEP)
- 

### area_material (GEP)
- PK_AREA_MATERIAL **(PK)**
- TX_DESCRIPCION

### difusion (MVD)
- PK_DIFUSION **(PK)**
- TX_TITULO
- FK_MATERIAL_DIFUSION **(FK)**

### medio difusion (GEP)
- PK_MEDIO_DIFUSION **(PK)**
- TX_NOMBRE

## Relaciones
1. Uno o ningún **material** tiene **difusion** (_0/1  - M_).
2. Un **medio difusion** tiene **difusion** (_1 - M_).

## Comentario de las tablas

### editorial
| Descripción | Comentario de las columnas |
| ----------- |----------------------------|
| Almacena los datos de editoriales y repositorios institucionales externos | -El campo |
