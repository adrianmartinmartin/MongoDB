# MongoDB

En este repositorio se encontrarán los comandos necesarios para realizar los ejercicios propuestos.



---
## EJERCICIO 1
1. *db.articulos.find()*
2. *db.articulos.find({rubro: {$ne: 'impresora'}})*
3. *db.articulos.find({rubro: {$eq: 'mouse'}})*
4. *db.articulos.find({precio: {$gte: 5000}})*
5. *db.articulos.find({rubro: 'impresora', precio: {$gte: 3500}})*
6. *db.articulos.find({stock: {$gte: 0, $lte: 4}})*
---







## EJERCICIO 2
1. *db.articulos.find()*
2. *db.articulos.deleteMany({rubro: 'impresora'})*
   *db.articulos.deleteMany({rubro: {$eq: 'impresora'}})*
3. *db.articulos.deleteMany({_id: {$gte: 5}})*

## EJERCICIO 3
1. *db.articulos.find()
2. *db.articulos.updateOne({nombre: 'LOGITECH M90'},{$set: {precio: 350}})*
3. *db.articulos.updateOne({_id: 6},{$set: {stock: 0}})*
4. *db.articulos.updateOne({_id: 6},{$set: {proveedores: ['Martinez','Gutierrez']}})*
5. *db.articulos.updateOne({_id: 6},{$unset: {proveedores: ''}})*

## EJERCICIO 4
1. *db.articulos.find()*
2. *db.articulos.updateMany({rubro:'monitor'},{$set: {stock: 0}})*
3. *db.articulos.updateMany({stock:0},{$set: {pedir:true}})*
4. *db.articulos.updateMany({},{$unset: {pedir: ''}})*

## EJERCICIO 5
1. *db.medicamentos.find()*
2. *db.medicamentos.find({laboratorio: 'Roche', precio: {$lt: 5}})*
3. *db.medicamentos.find({$or: [{laboratorio: 'Roche'}, {precio: {$lt: 5}}]})*
4. *db.medicamentos.find({laboratorio: {$ne: 'Bayer'}})*
5. *db.medicamentos.find({$and: [{laboratorio: 'Bayer'}, {cantidad: {$ne: 100}}]})*
6. *db.medicamentos.deleteMany({$and: [{laboratorio: 'Bayer'},{precio: {$gt: 10}}]})*
7. *db.medicamentos.updateMany({laboratorio: 'Roche', precio: {$gt: 5}}, {$set: {cantidad: 200}})*
8. *db.medicamentos.deleteMany({$or: [{laboratorio: 'Bayer'}, {precio: {$lt: 3}}]})*

## EJERCICIO 6
1. *db.articulos.find()*
2. *db.articulos.find({rubro: 'impresora'},{nombre:1,precio:1})*
3. *db.articulos.find({$and: [{rubro:'impresora',precio: {$gte: 3500}}]},{nombre:1,precio:1,stock:1})*
4. *db.articulos.find({rubro:'monitor'},{nombre:1,precio:1,_id:0}).sort({precio:1})*

## EJERCICIO 7
1. *db.libros.find()*
2. *db.libros.find({'autor.nacionalidad': 'Argentina'})*
3. *db.libros.find({'autor.nombre': 'Borges'})*
4. *db.libros.find({'autor.nacionalidad': 'Española',precio: {$gte: 50}})*

## EJERCICIO 8
1. *db.alumnos.find().pretty()*
2. *db.alumnos.find({}, {apellido: 1, fechanacimiento: 1, _id: 0})*
3. *db.alumnos.find().sort({fechanacimiento:1})*
4. *db.alumnos.find({fechanacimiento: {$gte: new Date(1970, 01, 1)}})*

## EJERCICIO 9
*db.universities.aggregate([{$unwind: "$students"}, {$group: {_id: "$name", totalStudents: {$sum: "$students.number"}}}, {$sort: {totalStudents: -1}}])*


