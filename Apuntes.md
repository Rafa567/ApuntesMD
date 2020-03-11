# Despliegue de Aplicaciones Web.

## Documentación y Control de versiones

---
![Despliegue de aplicaciones web](https://github.com/rafa567/ApuntesMD/blob/master/iesluisvelez.png)
<small> Rafael Ramos Durán </small>

## Índice
--- 
- ### Introducción
- ### Documentación con Markdown
- ### Control de versiones con git


## Introducción

### En esta Unidad aprenderemos a

- Identificar diferentes herramientas de generación de documentación.
- Utilizar diferentes formatos para la documentación.
- Utilizar herramientas colaborativas para la elaboración y mantenimiento de la documentación.
- Instalar, configurar y utilizar un sistema de control de versiones.


## Documentación con Markdown

### Cabeceras

```markdown
# Cabecera de nivel 1 (Titulo 1 <h1>)
## Cabecera de nivel 2 (Titulo 2 <h2>)
###### Cabecera de nivel 5 (Titulo 5 <h5>)
```

---
# Esto es una cabecera de nivel 1 (Titulo 1)
---
## Esto es una cabecera de nivel 2 (Titulo 2)
---
###### Esto es una cabecera de nivel 5 (Titulo 5)
---

### Listas sin orden

```markdown
- Ejemplo 1
- Ejemplo 2
  - Ejemplo 2a
  - Ejemplo  2b
```
- Ejemplo  1
- Ejemplo  2
  - Ejemplo  2a
  - Ejemplo  2b

### Lista con orden

```markdown
1. Ejemplo 1
2. Ejemplo 2
3. Ejemplo 3
   - Ejemplo 3a
   - Ejemplo 3b
```
1. Ejemplo 1
2. Ejemplo 2
3. Ejemplo 3
   - Ejemplo 3a
   - Ejemplo 3b

### Formato

```markdown

**Texto en negrita**
__Texto en negrita__

*Texto en itálica*
_Tamnbien en itálica_


**Puedes *combinar* ambos formatos**


~~Tachado~~
```
*Texto en itálica*

_Texto en itálica_

**Texto en negrita**

__Texto en negrita__

~~Este texto está tachado~~

### Lista de tareas
```markdown
- [ ] Cenar
- [ ] Dormir
- [X] Hola
```

- [ ] Comer 
- [X] Siesta
- [ ] Nada


### Enlaces

```markdown
http://github.com - automático

[GitHub](http://github.com)
```
[GitHub](http://github.com)


### Imágenes

```markdown
![GitHub Logo](/images/logo.png)

Formato: ![Texto alternativo](url)
```
![GitHub Logo](https://github.com/rafa567/ApuntesMD/blob/master/descarga.png)


### Citas

```markdown
Como dijo Obi-Wan:

> Se acabo Anakin
> la altura me da la ventaja
```
Como dijo Obi-Wan:

> Se acabo Anakin
> la altura me da la ventaja


### Código fuente

**javascript**
```javascript
var s = "Lenguaje javascript. Se realizará coloreado de sintaxis.";
alert(s); 
```

**python**
```python
s = "Lenguaje Python. Se realizará coloreado de sintaxis."
print s
```

**ninguno**
```
No se indica lenguaje. No se realizará coloreado de sintaxis. 
```


### Menciones y Referencias
- Menciones a usuarios: @usuario

- Referencias a Issues y Pull request: #numero


### Escapar caracteres
```markdown

Para la comilla invertida hay que poner \`
Para el asterisco hay que poner \*
Para el guión bajo hay que poner \_
Para la barra invertida hay que poner \\
Para la llave que cierra hay que poner \}
Para el corchete que abre hay que poner \[
Para el corchete que cierra hay que poner \]
Para la llave que abre hay que poner \{
Para el parentesis que abre hay que poner \(
Para el parentesis que cierra hay que poner \)
Para la almohadilla hay que poner \#
Para el signor de sumar hay que poner \+
Para el punto hay que poner \.
Para el guion hay que poner \-
Para la exclamación que cierra hay que poner \!
Para los dos puntos hay que poner hay que poner \:
Para la barra separatoria hay que poner \|
```
Para la barra invertida hay que poner \\

Para la comilla invertida hay que poner \`

Para el asterisco hay que poner \*

Para el guión bajo hay que poner \_

Para la llave que abre hay que poner \{

Para la llave que cierra hay que poner \}

Para el corchete que abre hay que poner \[

Para el corchete que cierra hay que poner \]

Para el parentesis que abre hay que poner \(

Para el parentesis que cierra hay que poner \)

Para la almohadilla hay que poner \#

Para el signor de sumar hay que poner \+

Para el guion hay que poner \-

Para el punto hay que poner \.

Para la exclamación que cierra hay que poner \!

Para los dos puntos hay que poner hay que poner \:

Para la barra separatoria hay que poner \|


### Tablas
```markdown
**Tabla de multiplicar del número 4**
| numero1 | numero2 | resultado |
| ------- | ------- | --------- |
| 4       | 0       | 0         |
| 4       | 1       | 4         |
| 4       | 2       | 8         |
| 4       | 3       | 12        |
| 4       | 4       | 16        |
| 4       | 5       | 20        |
| 4       | 6       | 24        |
| 4       | 7       | 28        |
| 4       | 8       | 32        |
| 4       | 9       | 36        |
| 4       | 10      | 400        |


### Usando emojis
```markdown
Ya he vuelto a casa :satisfied:
```
Ya he vuelto a casa :satisfied:


## Control de versiones con git


### Instalación de git

```bash
sudo  apt  install  git
```


### Configuración de git

```bash
git  config  --global  user.name   "Nombre y Apellidos"
git  config  --global  user.email  "nombre@mail.com"
```


### Iniciar repositorio local

```bash
git  init
```

Note: Es recomendable crear un archivo `.gitignore` con listado de carpetas y archivos a los que no se realizará seguimiento.


### Comandos básicos

```bash
git  status
git  add .
git  commit -m  "Mensaje"
```


### Clonar repositorio remoto 

```bash
git  clone   https://github.com/usuario/repositorio.git
git  clone   git@github.com:usuario/repositorio.git
```


### Vincular y desvincular repositorio remoto

```bash
git  remote  -v
git  remote  add  origin  https://github.com/usuario/repositorio.git
git  remote  rm   origin
```


### Bajar y subir contenido a repositorio remoto

```bash
git  pull  origin  master  // bajar commits
git  push  origin  master  // subir commits
```


###  Trabajo con ramas

```bash
git  branch    -va        // listado verbose, all (local y remoto)

git  branch    nuevo      // creación de rama
git  checkout  nuevo      // cambiar a dicha rama

git  checkout  -b nuevo   // equivalente a las 2 sentencias anteriores
```


### Checkout

- El comando **`checkout`** de `git` sirve para **cambiar de rama**.

```bash
git  checkout  rama
```

- También sirve para **cambiar de commit dentro de una rama**.

```bash
git  checkout  0f82
```


### Etiquetas de anotación

```bash
git tag -l                          // Listado
git tag -a v1.0 -m "Version 1.0"    // Añadir etiqueta
git tag -d v1.0                     // Eliminar etiqueta
```

- Las etiquetas deben enviarse explícitamente al repositorio remoto:

```bash
git  push  --tags
```
