# Metagenomica
Metagenomica, tarea 8.1, Juan Soto
Curso de Bioinformática aplicada al análisis de datos genómicos

Se trabajó con un set de datos de muestras de suelo rizosférico recolectados en sitios de bosque nativo (N) y mixto (M) de Quercus (Q) y de Juniperus (J), partiendo desde lecturas de secuenciación forward y reverse obtenidos por Illumina MiSeq.El procesamiento bioinformatico de los datos se realizó con AMPtk.

En primer lugar se pre-procesaron los reads,ensamblando las dos lecturas (R1 y R2), eliminando primers y secuencias de un largo menor a 200 pb. 
POsteriormente se filtraron las secuencias por calidad y se agruparon las secuencias en OTUs (Operational Taxonomic Units).
Luego se corrigio el index bleed (indices asignados a lecturas erroneas) filtrando la tabla de OTUs con un umbral de 0,005%.
Finalmente se asignó una taxonomía a los OTUs, utilizando la base de datos UNITE

Al comparar los resultados obtenidos al filtrar las secuencias menores a 200 pb con el resultado que se obtiene filtrando secuencias menores a 300 pb se observa que si se filtra a 300 pb se pierde mucha información de los datos, obteniendo una cantidad de OTUs muy inferior a la obtenida filtrando a 200 pb. Mediante la filtración a 200 pb se obtuvieron 1257 OTUs de fungi, en cambio, al filtrar con 300 se obtuvieron sólo 329 OTUs, por lo que en este caso es más correcto utilizar una filtración de 200 pb.

# Metagenomica, parte dos
Metagenomica, tarea 8.2, Juan Soto

Los resultados del archivo .biom obtenidos en la tarea 8.1 fueron analizados en R. El archivo tarea_82 en la carpeta principal contiene los analisis realizados paso por paso y resultados obtenidos. Como resultado no se detectaron diferencias significativas de diversidad alfa (riqueza) entre hospederos ni tratamiento. Pero, al analizar la diversidad beta mediante el analisis Adonis se observa que efectivamente hay diferencias significativas de la composición comunitaria entre hospederos (p-value = 0,029) y además entre los tratamientos (p-value = 0,017) con un nivel de significancia de 0,05, lo que también se observa en el analisis NMDS, por lo que, si bien la diversidad alfa no difiere entre hospederos y tratamientos, la composición comunitaria de hongos (diversidad beta) si presentan diferencias significativas entre los dos hospederos y los tratamientos.
