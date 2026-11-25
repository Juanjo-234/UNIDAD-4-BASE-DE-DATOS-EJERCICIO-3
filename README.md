# UNIDAD-4-BASE-DE-DATOS-EJERCICIO-3
1. Configuración Inicial y Base de Datos
Se establece la codificación a UTF8 y se configura el esquema público por defecto.

Se define la creación de la base de datos principal llamada historiaclinicaelectronicaclinicamedica utilizando la configuración regional de España (Spanish_Spain.1252).

2. Estructura de las Tablas y sus Campos
El script define la creación de 7 tablas relacionales principales:

especialidad: Almacena las diferentes especialidades médicas disponibles.

id_especialidad: Identificador único de la especialidad (clave primaria).

nombre: Nombre de la especialidad médica.

medico: Contiene la información personal y de contacto de los profesionales de la salud.

numero_matricula: Número de matrícula profesional del médico (clave primaria).

nombre y apellido: Datos personales del médico.

telefono: Teléfono de contacto.

medico_especialidad: Tabla intermedia que relaciona a los médicos con sus respectivas especialidades.

numero_matricula y id_especialidad: Claves primarias compuestas.

nombre_especialidad: Nombre de la especialidad asociada.

tipo_especialidad: Categoría o tipo de especialidad.

paciente: Registra los datos de los pacientes atendidos en la clínica.

numero_historial_clinica: Número de historial clínico único del paciente (clave primaria).

dni: Documento nacional de identidad.

nombre y apellido: Datos personales.

obra_social: Cobertura médica o prepaga del paciente.

domicilio: Dirección de residencia.

turno: Gestiona las citas médicas, consultas o turnos agendados.

numero_turno: Identificador único del turno (clave primaria).

fecha y hora: Fecha y horario programados para la atención.

estado: Estado actual del turno (ej. completado, cancelado, pendiente).

diagnostico: Diagnóstico médico resultante de la consulta.

numero_historial_clinica y numero_matricula: Claves foráneas que relacionan el turno con el paciente y el médico correspondiente.

medicamento: Almacena el catálogo de fármacos disponibles para prescripción.

codigo_alfanumerico: Código único del medicamento (clave primaria).

monodroga: Principio activo del medicamento.

fabricante: Laboratorio o fabricante.

nombre_comercial: Nombre comercial del fármaco.

receta: Registra los medicamentos recetados en el contexto de una consulta.

numero_turno y codigo_alfanumerico: Claves primarias compuestas que vinculan la receta con el turno y el medicamento específico.

dosis: Cantidad a administrar.

frecuencia: Intervalo de tiempo en que debe tomarse.

duracion: Tiempo total que debe mantenerse el tratamiento.

3. Restricciones y Claves
Claves Primarias (PRIMARY KEY): Se configuran para garantizar la unicidad de los registros en cada tabla (ej. especialidad_pkey, medico_pkey, paciente_pkey, turno_pkey, etc.).

Claves Foráneas (FOREIGN KEY): Se establecen para mantener la integridad referencial, vinculando los datos de los médicos con sus especialidades, los turnos con los pacientes y médicos correspondientes, y las recetas con los turnos y medicamentos recetados.

IMAGEN DE EJEMPLO DE CONSULTA:
<img width="1383" height="365" alt="image" src="https://github.com/user-attachments/assets/03708aa1-d065-492e-b5c2-ca14da237f09" />
