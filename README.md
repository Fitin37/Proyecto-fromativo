# Proyecto-fromativo
base de datos a usar

CREATE TABLE medicinas(
UUID_MEDICINA varchar2(50) primary key,
nombre_medicina varchar2(25),
laboratorio_nombre VARCHAR2(50)
);

CREATE TABLE paciente(
UUID_DUI VARCHAR2(8) primary key,
nombrePaciente varchar2(50),
apllidosPaaciente varchar2(50),
Edad varchar2(25),
Enfermedad varchar2(25),
numeroDeAbitacion VARCHAR2(25),
numeroDeCama VARCHAR2(25),
fecha_nacimineto VARCHAR2(50),
HoraDeMedicina date
);

CREATE  TABLE DOCOTORES(
UUID_DUIDOCTOR VARCHAR2(80) primary key,
NombreDoctor varchar2(50),
Apellidos varchar2(50),
UUID_DUI VARCHAR2(50),
UUID_MEDICINA VARCHAR2(8),
Edad VARCHAR2(25),
CONSTRAINT fk_paciente FOREIGN KEY (UUID_DUI) references paciente(UUID_DUI),
CONSTRAINT fk_medicinas  FOREIGN KEY (UUID_MEDICINA) references medicinas(UUID_MEDICINA)
);
