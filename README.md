# Metagenomica
Metagenomica, tarea 8.1, Juan Soto
Curso de Bioinformática aplicada al análisis de datos genómicos

Se trabajó con un set de datos de muestras de suelo rizosférico recolectados en sitios de bosque nativo (N) y mixto (M) de Quercus (Q) y de Juniperus (J), partiendo desde lecturas de secuenciación forward y reverse obtenidos por Illumina MiSeq.El procesamiento bioinformatico de los datos se realizó con AMPtk.

En primer lugar se pre-procesaron los reads,ensamblando las dos lecturas (R1 y R2), eliminando primers y secuencias de un largo menor a 200 pb. 
POsteriormente se filtraron las secuencias por calidad y se agruparon las secuencias en OTUs (Operational Taxonomic Units).
Luego se corrigio el index bleed (indices asignados a lecturas erroneas) filtrando la tabla de OTUs con un umbral de 0,005%.
Finalmente se asignó una taxonomía a los OTUs, utilizando la base de datos UNITE

Al comparar los resultados obtenidos al filtrar las secuencias menores a 200 pb con el resultado que se obtiene filtrando secuencias menores a 300 pb se observa que si se filtra a 300 pb se piede mucha información de los datos, obteniendo una cantidad de OTUs muy inferior a la obtenida filtrando a 200 pb. Mediante la filtración a 200 pb se obtuvieron 1257 OTUs de fungi, en cambio, al filtrar con 300 se obtuvieron sólo 329 OTUs, por lo que en este caso es más correcto utilizar una filtración de 200 pb.

