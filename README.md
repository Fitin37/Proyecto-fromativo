base coreegida

create table Medicinas( UUID_medicina varchar2(50) primary key, nombreMedicina varchar2(25), nombreLab varchar2(50) );

create table Pacientes( UUID_Dui varchar2(50) primary key, nombrePaciente varchar2(25), edad varchar2(25), fechaNacimiento date, UUID_medicina varchar2(50), CONSTRAINT fk_Medicinas FOREIGN KEY (UUID_medicina) REFERENCES Medicinas (UUID_medicina) );

create table UserEnfermera( UUID_DuiEnfermra varchar2(25) primary key, Nombres VARCHAR2(50), Contrasena varchar2(150) );

insert into Medicinas(UUID_medicina,nombremedicina,nombrelab) values(SYS_GUID(),'acetaminofen','laboratorios brayan');

select * from Pacientes;

alter table Pacientes add( apellidos varchar2(25), Enfermedad varchar2(50), NumeroHabi VARCHAR2(25), NumeroCama VARCHAR2(25), HoraDetomar varchar2(50) ); insert into Pacientes(UUID_Dui,nombrepaciente,edad,fechanacimiento,uuid_medicina,apellidos,enfermedad,numerohabi,numerocama,horadetomar) values(SYS_GUID(),' brayan wilfredo','25','12/03/95','32F962A185624C65B64A0C1B54C51717','exequiel','super inteligencia','2','3','4pm');

commit;
