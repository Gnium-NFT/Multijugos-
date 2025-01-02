De bd3ebdfc1a63c4fa980c455f155f96110ea8f959 
lunes 17 de septiembre de 2001 00:00:00
De: GreggJEduardoPH <gphgnium@gmail.com>
Fecha: jueves, 2 de enero de 2025 03:15:12 -0600
Asunto: [PATCH 1/2] Actualización del README.md

@steveluscher #27 #1
@WilfredAlmeida #2 #8
---
 README.md | 2 +-
 1 archivo modificado, 1 inserción(+), 1 eliminación(-)

diff --git a/README.md b/README.md
índice fbd046d..82dd506 100644
--- a/README.md
+++b/README.md
@@ -1,4 +1,4 @@
-# cliente-ping-thing
+ # ping-cosa-cliente
 Cliente Node JS para contribuir con tiempos de ping a la función Ping de Validators.app.
 
 ## Notas de instalación

Desde 07e65f36de208720e18d90b6116225f0f2fb03f3 Lun 17 Sep 00:00:00 2001
De: GreggJEduardoPH <gphgnium@gmail.com>
Fecha: jueves, 2 de enero de 2025 03:20:07 -0600
Asunto: [PATCH 2/2] Crear npm-gulp.yml

@Gnium-NFT
---
 .github/workflows/npm-gulp.yml | 28 ++++++++++++++++++++++++++++
 1 archivo modificado, 28 inserciones(+)
 modo de creación 100644 .github/workflows/npm-gulp.yml

diferencia --git a/.github/workflows/npm-gulp.yml b/.github/workflows/npm-gulp.yml
nuevo modo de archivo 100644
índice 0000000..f8aa8bb
--- /dev/null
+++ b/.github/workflows/npm-gulp.yml
@@ -0,0 +1,28 @@
+nombre: NodeJS con Gulp
+
+en:
+ empujar:
+ ramas: [ "principal" ]
+ solicitud_extracción:
+ ramas: [ "principal" ]
+
+trabajos:
+ construir:
+ se ejecuta en: ubuntu-latest
+
+ estrategia:
+ matriz:
+ versión del nodo: [18.x, 20.x, 22.x]
+
+ pasos:
+ - usos: acciones/checkout@v4
+
+ - nombre: Usar Node.js ${{ matrix.node-version }}
+ usos: acciones/setup-node@v4
+ con:
+ versión del nodo: ${{ matrix.node-version }}
+
+ - nombre: Construir
+ ejecutar: |
+ instalación de npm
+ trago
