Generador de Correspondencia

Esta aplicación genera documentos personalizados a partir de una plantilla y un archivo de datos en formato CSV. Utiliza los campos delimitados por {{ }} en la plantilla para reemplazarlos con los valores correspondientes del archivo CSV.

Ejemplo
Archivo de Datos: datos.csv

DNI,NOMBRES,CARGO,FECHA_INICIO,FECHA_CESE

123,Juan,Gerente,01/01/2020,01/01/2021

456,Ana,Jefe,02/02/2020,02/02/2021

459,David,Jefe,02/02/2021,02/02/2022


Plantilla: plantilla.docx
-------------------------------------------------------------------------------------------------------------
  Estimado {{ NOMBRES }} identificado con {{DNI}},                                                          
                                                                                                            
  Le informamos que su cargo de {{ CARGO }} comenzó el {{ FECHA_INICIO }} y finalizará el {{ FECHA_CESE }}. 
                                                                                                            
  Atentamente,                                                                                              
  La Empresa                                                                                                
                                                                                                            
------------------------------------------------------------------------------------------------------------

Documentos Generados
La aplicación generará tres documentos basados en la plantilla, reemplazando los campos delimitados por {{ }} con los valores correspondientes del archivo de datos CSV. Por defecto, el nombre del archivo tomará los datos de la primera columna.

Por ejemplo:

123.docx
456.docx
459.docx
Cada documento contendrá información personalizada como se muestra a continuación:

123.docx
-------------------------------------------------------------------------------------------------------------
  Estimado Juan identificado con 123,                                                                        
                                                                                                            
  Le informamos que su cargo de Gerente comenzó el 01/01/2020 y finalizará el 01/01/2021.                    
                                                                                                            
  Atentamente,                                                                                              
  La Empresa                                                                                                
                                                                                                            
------------------------------------------------------------------------------------------------------------


456.docx
-------------------------------------------------------------------------------------------------------------
  Estimado Ana identificado con 456,                                                                        
                                                                                                            
  Le informamos que su cargo de Jefe comenzó el 02/02/2020 y finalizará el 02/02/2021.                      
                                                                                                            
  Atentamente,                                                                                              
  La Empresa                                                                                                
                                                                                                            
------------------------------------------------------------------------------------------------------------


459.docx
-------------------------------------------------------------------------------------------------------------
  Estimado David identificado con 459,                                                                      
                                                                                                            
  Le informamos que su cargo de Jefe comenzó el 02/02/2021 y finalizará el 02/02/2022.                      
                                                                                                            
  Atentamente,                                                                                              
  La Empresa                                                                                                
                                                                                                            
------------------------------------------------------------------------------------------------------------

Notas
Los campos delimitados por {{ }} en la plantilla deben coincidir con las cabeceras del archivo de datos CSV, evitando el uso de espacios.
Asegúrate de que los nombres de las columnas en el CSV y los marcadores en la plantilla coincidan exactamente para garantizar una correcta sustitución de valores.

Cómo Ejecutar
Coloca el archivo datos.csv y la plantilla plantilla.docx en el mismo directorio 

Ejecuta la aplicación.
Los documentos generados se guardarán en el mismo directorio que elijas, utilizando los valores de la primera columna en este caso (DNI) como nombre de archivo.
