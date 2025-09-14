Resolución de Conflicto en Git

1. Creación del conflicto
- En la rama1 se modificó el archivo src/controllers/user.controller.js con

console.log("Cambio desde rama1"); 

tambien en la rama 2 se modifico
console.log("Cambio desde rama2");

al momento de la ejecucion de estos comandos:
git checkout main
git merge rama2

git mostro esto
<<<<<<< HEAD
console.log("Cambio desde rama1");
=======
console.log("Cambio desde rama2");
>>>>>>> rama2

lo que hice fue quitarle los <<<<<<<<, ========, y los >>>>>>>>
para que quedase asi:
HEAD
console.log("Cambio desde rama1");

console.log("Cambio desde rama2");
rama2
seguido de eso le puse
console.log("Versión final después de resolver el conflicto");

y por ultimo en la terminal de power shell le puse este comando para concluir
git add src/controllers/user.controller.js
git commit -m "Conflicto resuelto entre rama1 y rama2"




