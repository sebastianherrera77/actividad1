
Actividad 2: Auditoría de permisos de acceso
1. Objetivo

Verificar los controles de acceso en Linux mediante la identificación de permisos incorrectos y su posterior corrección.

2. Asignación de permisos incorrectos

Se ejecutaron los siguientes comandos:

bash
chmod 777 empresa/finanzas/planilla.xlsx
chmod 777 empresa/rrhh/empleados.csv

3. Auditoría de permisos

Se utilizaron los comandos:

bash
ls -l empresa/finanzas
ls -l empresa/rrhh


Se identificaron permisos 777 en ambos archivos.

4. Análisis de seguridad
¿Existe incumplimiento?

Sí. Existe un incumplimiento de seguridad porque los archivos tienen permisos 777, permitiendo que cualquier usuario pueda leer, modificar y ejecutar los archivos.

¿Qué riesgo genera?
Acceso no autorizado a información confidencial.
Modificación o eliminación de información.
Filtración de datos financieros y personales.
Pérdida de confidencialidad e integridad.
¿Qué control ISO 27001 aplica?
A.5.15: Control de acceso.
A.5.18: Derechos de acceso.
A.8.3: Restricción de acceso a la información.
5. Corrección de permisos

Se ejecutaron los siguientes comandos:

bash
chmod 640 empresa/finanzas/planilla.xlsx
chmod 640 empresa/rrhh/empleados.csv


Los permisos 640 permiten que el propietario lea y modifique los archivos, el grupo solamente pueda leerlos y los demás usuarios no tengan acceso.

6. Conclusión

La auditoría permitió identificar permisos incorrectos que representaban un riesgo para la seguridad de la información.

Se corrigieron los permisos utilizando chmod 640, aplicando el principio de mínimo privilegio y mejorando la protección de los activos de información.
