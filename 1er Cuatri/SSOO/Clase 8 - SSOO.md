# Memoria Virtual
La memoria virtual esta paginada, la RAM tambien, cada frame de la MV puede estar solo en MV o en MV y RAM.
#### Paginación bajo demanda:
Al inicializar un proceso solo tenemos las estructuras iniciales en MP, las paginas necesarias son cargadas cuando se necesitan, en demanda.
Sigue siendo paginacion, sigue habiendo tabla de paginas.
Tiene numero de pagina, frame, bit de precencia y de modificado.

Si la presencia es 0, significa que es invalida o no esta en MP, si es 1 esta en memoria y es valida.
El bit de modificado indica que paginas de memoria fueron modificadas, Si se quiere sustituir, hay que bajar a disco las modificaciones.