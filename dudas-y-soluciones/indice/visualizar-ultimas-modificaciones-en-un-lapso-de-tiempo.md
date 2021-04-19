---
description: >-
  Ver todos los cambios de un periodo de tiempo a través del plugin Dataview de
  Obsidian
---

# Visualizar ultimas modificaciones en un lapso de tiempo

### Consulta

> @pituxmat Hola, muy buenas. ¿Alguien sabe como buscar en obsidian un grupo de documentos por fecha? Por ejemplo, los últimos 3 días, algo así como: "last 3 days" y que muestre todos los documentos de los últimos tres días. ¡Gracias!

### Dataview

Usando el plugin Dataview [https://github.com/blacksmithgu/obsidian-dataview](https://github.com/blacksmithgu/obsidian-dataview) es posible listar las ultimas modificaciones durante un periodo de tiempo, para ello procedemos a tener en una nueva nota donde deseamos tener la extracción de los datos. 

![Ejemplo de arbol de directorios](../../.gitbook/assets/image%20%284%29.png)

El directorio Notes corresponde al directorio donde deseas realizar la búsqueda.

```text
```dataview
LIST FROM "Notes/Directorio" WHERE file.mtime >= date(today) - dur(1 day)
sort date desc
```
```

Si deseamos extraer especificamente por un periodo de tiempo podemos hacer uso de:

* month: Para extraer la cantidad de meses.
* day: Durante cierta cantidad de dias. 
* hour: Durante cierta cantidad de horas.

Resultado de la consulta a 1 dia desde la fecha actual, que son cambios que estuve realizando para mi blog. 

![Resultado de la consulta](../../.gitbook/assets/image%20%283%29.png)

Si deseamos que nos extraiga de los ultimos 7 dias solo debemos de cambiar el valor respectivo.

{% hint style="info" %}
Conoces otra manera de solucionar este problema? Comparte con la comunidad, por medio de [_**Telegram**_](https://t.me/ObsidianEs) o el [_**GITHUB**_](https://github.com/Snifer/Obsidian) de este repositorio. 
{% endhint %}





