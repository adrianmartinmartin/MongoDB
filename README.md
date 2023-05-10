# MongoDB

En este repositorio se encontrarán los comandos necesarios para realizar los ejercicios propuestos.


EJERCICIO 1
1. db.articulos.find()
2. db.articulos.find({rubro: {$ne: 'impresora'}})
3. db.articulos.find({rubro: {$eq: 'mouse'}})
4. db.articulos.find({precio: {$gte: 5000}})
5. db.articulos.find({rubro: 'impresora', precio: {$gte: 3500}})
6. db.articulos.find({stock: {$gte: 0, $lte: 4}})

EJERCICIO 2
1. db.articulos.find()
2. db.articulos.deleteMany({rubro: 'impresora'})
   db.articulos.deleteMany({rubro: {$eq: 'impresora'}})
3. db.articulos.deleteMany({_id: {$gte: 5}})

EJERCICIO 3
1. db.articulos.find()
2. db.articulos.updateOne({nombre: 'LOGITECH M90'},{$set: {precio: 350}})
3. db.articulos.updateOne({_id: 6},{$set: {stock: 0}})
4. db.articulos.updateOne({_id: 6},{$set: {proveedores: ['Martinez','Gutierrez']}})
5. db.articulos.updateOne({_id: 6},{$unset: {proveedores: ''}})
