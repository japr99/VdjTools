# VdjTools

Vamos a llamar a VirtualDJ, VDJ.

Esta utilidad solo es compatible con VDJ 2023 y 2024.

Esta utilidad solo soporta los formatos de audio: mp3, wav, aiff y flac.

Esta utilidad guarda los datos, tag's cues, loops, etc., en el ID3Tag del audio para poder ser recuperado en la base de datos de VDJ.

Esta utilidad también elimina duplicados en los playlists de VDJ 2023. Si usa VDJ 2024, se deshabilitará, ya está incluido en esta versión.

Para guardar los datos en el audio lo primero que hacemos es un playlist con las canciones que queremos procesar, como se ve en la imagen hay cues, saltos loops, todos ellos se guardarán en el archivo de audio con sus tags en formato VDJ, los tags normales del audio no se verán afectados.

Seleccione 'Desabilita HotPlug' para que el playlist sea movido a la carpeta de preferencias de VDJ si esta usando VDJ 2024.

![VDJ a IDTag](https://github.com/japr99/VdjTools/assets/60424156/2fa2b79f-e5c1-4d97-9682-781a7c583426)

Después de crear el playlist abrimos VdjTools y seleccionamos 'VDJ a IDTag', la aplicación buscará en la carpeta de preferencias de VDJ los playlists a cargar. Si VdjTools detecta 2 carpetas de preferencias de VDJ, una en 'Documentos' y otra en '/Library/Application/Support/VirtualDJ' si es MAC, '\AppData\Local\VirtualDJ' si es PC, VdjTools no continuará, no se puede tener 2 carpetas de VDJ en el root del sistema, son restos de viejas instalaciones. En VDJ, desde 'opciones de configuración', esquina inferior derecha, pulse sobre el engranaje, se abrirá la carpeta de preferencias de VDJ, esta es la buena, la que esté en otro lugar sobra.

Seleccione el playlist o playlists a procesar.

![VDJ a IDtag](https://github.com/japr99/VdjTools/assets/60424156/604aaf28-b357-44b4-ae7b-e0833b930ac0)

Ejecute el proceso, TENGA PACIENCIA, LAS BASES DE DATOS DE VDJ PUEDEN SER MUY GRANDES Y PUEDE TARDAR.

'Omitir fecha última modificación' comprueba la fecha de la base de datos con los datos de IDTag. Si ya están en el archivo de audio, simplemente, si tienen la misma fecha no se modificará el archivo de audio (este tema es un poco relativo, VDJ mueve mucho este valor).

Seleccione 'Omitir fecha última modificación' si quiere escribir de todas formas en el archivo de audio.

Cuando termine de procesar se creará un resumen en pantalla y un log en el escritorio.

![VDJ a IDtag porcesado](https://github.com/japr99/VdjTools/assets/60424156/9e31a275-0d3d-4151-b951-6334a74401a9)

Si todo ha ido bien, los datos estarán guardados en el archivo de audio, lo comprobaremos con Mp3Tag, en mi caso, como se ve se ha creado un nuevo tag llamado VDJ_SONG, aquí se ha guardado toda la información de la base de datos de VDJ.

![mp3tag1](https://github.com/japr99/VdjTools/assets/60424156/f27e31d7-4fad-4d07-8e5f-c87e0d4bf5f0)
![mp3tag2](https://github.com/japr99/VdjTools/assets/60424156/8b3b4b23-e16f-4155-9e1f-ed5831004cdf)

No manipule los datos, puede tener alguna sorpresa como perder la base de datos de VDJ al importar los datos, los datos aunque no lo parezca están en un formato especial.

Ahora voy a eliminar los cues y la información de estas 2 canciones, en VDJ para hacer la importación, como se ve en la imagen las canciones tienen los cues y demás datos eliminados.

![carga_playlist IDTag a VDJ](https://github.com/japr99/VdjTools/assets/60424156/82687f05-aae0-4ee4-866a-cfdc59de0570)

Cierro VDJ y vamos a importar los datos del IDTag del audio a la base de datos de VDJ.

Abrimos VDJTools y seleccionamos 'IDTag a VDJ' y seleccionamos el playlist a procesar, igualmente que en el anterior proceso 'Omitir fecha última modificación' funciona pero al revés que el proceso anterior, seleccionado esta opción no comprueba fechas e importa los datos.

![IDTag a VDJ](https://github.com/japr99/VdjTools/assets/60424156/79b426a8-ca7d-41bd-af26-6578c6d421da)

Ejecutamos el proceso, si todo ha funcionado como debe, tendremos un resumen en pantalla y un log en el escritorio.

Se habrá creado una copia de la base de datos de VDJ 'database.xml' con la fecha y la hora dentro de la carpeta VDJ_Backup dentro de las preferencias de VDJ, en cualquier momento puede reemplazar esta copia por la nueva, renombrándola a 'database.xml' y moviéndola a la carpeta 'VirtualDJ', reemplazando la existente, tenga cuidado al manipular los archivos, siempre cree una copia de la carpeta 'VirtualDJ' en el escritorio por posibles desastres.

![IDTag a VDJ procesado](https://github.com/japr99/VdjTools/assets/60424156/90ff58c2-a9f3-4267-aa33-5f2a007938c2)

Ahora podemos comprobar que la información de los cues y demás datos se han recuperado.

![recuperado](https://github.com/japr99/VdjTools/assets/60424156/8c53de3c-0a30-4dbd-b8ea-9e5e74c5601d)

Eliminar duplicados solo funciona en VDJ 2023, elimina los duplicados de los playlists, seleccione 'Eliminar duplicados', seleccione los playlists a procesar, al ejecutar el proceso se creará una copia de la carpeta VDJ_Backup dentro de las preferencias de VDJ, en cualquier momento puede reemplazar esta copia por la nueva. Ahora los playlists de VDJ ya no tienen duplicados, esta función está deshabilitada si VDJTools detecta que está usando la nueva versión de VDJ 2024 que ahora mismo está en fase BETA, en la cual se han eliminado los 'playlists' y se han cambiado por archivos xml dentro de la carpeta 'MyList'.

Espero que no tengáis problemas con temas de antivirus o permisos, esta app solo la he probado en mis equipos y maquinas virtuales.

Si tenéis algún problema o alguna idea podéis dejarla en los comentarios.

Mis hobbies, la música y la programación.

Enlace de descarga:

https://drive.google.com/drive/folders/1-3vE2N7NWW1UEE8Vfeg-qnTyyn-A-igJ?usp=sharing


si no se entiende, usa el traductor Web, lo mismo hago yo para aprender Python.





