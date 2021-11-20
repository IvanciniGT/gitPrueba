# Los archivos markdown

## Sobre este documento...

He escrito este documento para ayudar a las personas dedicadas al mundo de la informática a entender y familiarizarse los con conceptos del lenguaje markdown.

Para escribirlo he utilizado la propia sintaxis de markdown (asegurandome de incluir todos y cada uno de los recursos que nos brinda este lenguaje para maquetar documentos) de forma que pueda ser a su vez utilizado como una plantilla en la que consultar cómo conseguir un determinado resultado.

La última versión de este documento puede encontrarse en:
><https://recursos.iochannel.tech/markdown-intro>

Este documento está sujeto a cambios, y agradezco tu colaboración. Puedes enviarme cualquier comentario o sugerencia con respecto a este documento a:
>    Iván Osuna: <ivan@iochannel.tech>

Este archivo está bajo una licencia:
>  [Creative Commons Atribución-SinDerivadas 4.0 Internacional](http://creativecommons.org/licenses/by-nd/4.0/) ![Licencia Creative Commons](https://i.creativecommons.org/l/by-nd/4.0/80x15.png)

## Introducción a markdown

La sintaxis **markdown** permite *maquetar* [^1] un documento mediante el uso de unas ___marcas___ y unas ___reglas sintácticas___ muy simples.

Aunque no se utiliza sólo para ello, markdown es el formato estándar para documentar y dar información en los repositorios git, y es interpretado automáticamente por los principales servicios cloud de git, como:
- [github](https://github.com)
- [gitlab](https://gitlab.com)
- [bitbucket](https://bitbucket.org)

Pero markdown está siendo utilizado para escribir  documentación de distinta naturaleza. Como ejemplo para entender la amplia difusión que está teniendo esta síntaxis podríamos decir que ***Microsoft Word permite pegar directamente contenido escrito en formato markdown***, autoconvietiéndolo la sintaxis markdown a estilos de Word directamente.

A los archivos escritos según la sintaxis markdown les añadimos la extensión `.md`.

El icono habitual que utilizamos para representar archivos markdown es:

![Icono archivo markdown](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/312px-Markdown-mark.svg.png "Icono estandar de un archivo markdown")

## Uso de markdown en git 

Como hemos explicado en la [introducción](#introducción-a-markdown), los principales servicios de git en cloud buscan en cada carpeta un archivo llamado `README.md`. 
Si el archivo existe, automáticamente lo convierten a HTML aplicando unas reglas de maquetado que facilitan su lectura por personas y lo muestran por pantalla.

Los desarrolladores que colocan su código en un sistema de control de versión git, utilizan estos archivos para ayudar a entener el contenido de una determinada carpeta o repositorio al resto de personas interesadas en el proyecto.

## TL; DR

En esta tabla resumo la mayor parte de símbolos utilizados en markdown, su significado dentro de este lenguaje y ejemplos de uso. 

> En apartados posteriores detallo algunos aspectos adicionales, así como buenas prácticas al respecto de su utilización:

### Formatos de texto:

| Formato | Símbolo | Ejemplo | Estandar [^2] |
| ------- | :-----: | ------- | ---: |
| Cursiva | ```*```<br>```_``` | ```*```esto sale en cursiva```<br>```_```esto también```_```| ✓ |
| Negrita | **<br>__ | \*\*esto sale en negrita**<br>\_\_esto también__| ✓ |
| Negrita y cursiva | ***<br>___ | \*\*\*esto sale en negrita y cursiva***<br>\_\_\_esto también___| ✓ |
| Tachado | ~~| \~\~esto sale tachado~~| ✓ |
| Código | \`| \`esto sale como código` | ✓ |
| Salto de linea | \<br>| Esto es una linea\<br>Esto sería otra linea | ✓ |
| Enlace sencillo | <> | \<https://iochannel.tech> | ✓ |
| Enlace | \[alt](url) | \[Web de IOChannel](https://iochannel.tech) | ✓ |
| Enlace a título <br> del mismo documento | \[alt](#url) | \[Introducción](#introduccion-del-documento) | ✓ |
| Imágen | \![alt](url) | \![Logo de IOChannel]\(https://iochannel.tech/logo) | ✓ |
| Imágen con título | \![alt](url título) | \![Logo de IOChannel]\(https://iochannel.tech/logo "Logotipo de IOChannel" ) | ✘ |
| Referencia a nota al margen | \[^1] | véase nota [^1] | ✘ |

### Formatos de Título:

| Formato | Símbolo | Ejemplo | Estandar [^2] |
| ------- | :-----: | ------- | ---: |
| Encabezado principal <br> Título 1 | # | # Esto sería un título| ✓ |
| Encabezado secundario <br> Título 2 | ## | ## Esto sería un subtítulo| ✓ |
| Título de nivel 3 | ### | ### Esto sería un apartado | ✓ |
| Título de nivel 4 | #### | #### Esto sería un subapartado | ✓ |
| Título de nivel 5 | ##### | ##### Esto sería una sección | ✓ |
| Título de nivel 6 | ###### | ###### Esto sería una subsección | ✓ |

### Formatos de listas:

| Formato | Símbolo | Ejemplo | Estandar [^2] |
| ------- | :----- | ------- | ---: |
| Lista | -<br>*<br>+ | \- Esto es una lista<br>\- Con varios elementos<br><br>\* Esto también sería una lista<br>\* Con varios elementos | ✓ |
| Sublista | -, * o + <br>(deben aparecer indentados) | \- Esto es una lista<br>&nbsp;&nbsp;&nbsp;&nbsp;* Esto sería una sublista<br>&nbsp;&nbsp;&nbsp;&nbsp;* Con varios elementos | ✓ |
| Lista numerada | 1.<br>2.<br>3. | 1\. Esto es el primer elemento<br>2\. Esto es el segundo elemento | ✓ |
| Lista de definiciones | :| Elemento a definir<br>\: definición<br><br>Otro elemento a definir<br>\: Otra definición | ✘ |
| Lista de tareas | \- \[ ]<br>\- \[x] | \- \[x] Esta es una tarea realizada<br>\- \[ ] Esta es una tarea sin realizar | ✘ |

### Formatos especiales de bloque:

| Formato | Símbolo | Ejemplo | Estandar [^2] |
| ------- | :----- | ------- | ---: |
| Linea de separación | ---<br>*** | --- | ✓ |
| Cita | > | > Esto aparecería como una cita.<br>><br>> Que podría tener varias lineas<br>> y su \*\*propio formato** | ✓ |
| Código | \```formato<br>CONTENIDO<br>``` | \```bash<br>echo 'HOLA'<br>``` | ✘ |
| Nota al margen | \[^]: | \[\^1]: Esto es una nota al margen | ✘ |

## Formato de textos

### Negrita

Utilizamos dos caracteres asterisco `**` o guión bajo `__` para escribir algo en negrita.

***Ejemplos:***

```md    
La siguiente palabra se muestra en negrita: **palabra**.

Y esta también: __palabra__.
```
> La siguiente palabra se muestra en negrita: **palabra**.
>
> Y esta también: __palabra__.

Notas:
- ⚠️ Para evitar problemas con los guiones bajos en medio de una palabra, es aconsejable utilizar asteriscos en lugar de guiones bajos.


## Titulos

Utilizamos el carácter `#` al principio de una linea para identificarla como un título.

El número de caracteres `#` que se utilicen, denota el nivel del título. De esta forma:
- Una única almohadilla `#` establece un título de nivel 1. El más importante.
- Dos almohadillas `##` establecen un subtítulo o título de nivel 2.
- Tres almohadillas `###` establecen un título de nivel 3.
- Así sucesivamente hasta los títulos de nivel 6, identificados por 6 almohadillas: `######`

***Ejemplos:***

```md    
### Este es un título de nivel 3
#### Y este uno de nivel 4
```
>    ### Este es un título de nivel 3
>    #### Y este uno de nivel 4

Notas:
- ⚠️Es aconsejable dejar una linea en blanco antes y después de un título.
    ```md
    Si aquí hay un texto...    
    ### Este título no debería empezar aquí.❌
    Ni este texto aquí debajo.❌

    ### Este título si está bien escrito pues le precede una línea en blanco y le sigue otra linea en blanco.✅
    
    Este sería el primer párrafo dentro del apartado.✅

    ```
- ⚠️Es aconsejable dejar un espacio en blanco después del último carácter almohadilla.
    ```md    
    ### Este título sigue unas buenas prácticas.✅

    ###Este no las sigue. Esto debería evitarse.❌
    ```

- 💡Algunos procesadores de markdown (como los que se utilizan dentro de github o gitlab), generan idenficadores automáticamente para cada título. El identificador tiene por valor el texto del título en minúsculas y con los espacios en blanco transformacos a guiones.

    Ejemplo
    
    ```md
    ### Ejemplo de título

    El título de arriba puede referenciarse mediante el enlace: 
    [Ir al apartado Ejemplo de título](#ejemplo-de-título)
    ```

    >    ### Ejemplo de título
    >    [Ir al apartado Ejemplo de título](#ejemplo-de-titulo)




# Notas:

[^1]: Maquetar: Componer gráficamente un documento, asignando estilos y organizando contenido, para facilitar su lectura por personas.
[^2]: Algunos elementos de sintaxis no son maquetados por todos los procesadores de markdown. En general, incluso los no estándar aquí mostrados están disponibles por la mayoría de ellos, incluidos los utilizados en github.gitlab y bitbucket.
