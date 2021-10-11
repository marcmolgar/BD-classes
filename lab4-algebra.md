# Àlgebra relacional

## Pregunta 1:

- Fàcil, nivell tontico

## Pregunta 2:

- Molta gent selecciona els empleats que viuen a Madrid
  ``` sql
  A=EMPLEATS(CIUTAT_EMPL = 'MADRID')
  ```
  I fa la join amb DEPARTAMENTS
  
- Proveu què passa si feu això amb aquest joc de proves:
  ``` sql
  INSERT INTO  DEPARTAMENTS VALUES(3,'MARKETING',3,'VERDAGUER','VIC');
  INSERT INTO  PROJECTES VALUES (1,'IBDTEL','TELEVISIO',1000000);
  INSERT INTO  EMPLEATS VALUES (3,'ROBERTO',25000,'MADRID',3,1);
  INSERT INTO  EMPLEATS VALUES (4,’MARC’,35000,’BARCELONA’,3,1);
  ```
  És a dir, quan un departament té un empleat de Madrid i un d’una altra ciutat.

- Per aconseguir que "El resultat no ha d'incloure aquells departaments que no tenen cap empleat", penseu que si feu una join DEPARTAMENTS * EMPLEATS, els departaments que no tenen empleats no fan match amb cap empleat, i per tant no apareixen en el resultat.

## Pregunta 3:

- Recordeu que podeu fer join d'una taula amb ella mateixa, però llavors una de les dues ha de ser resultat d'un reanomenament.

- Pista: Busqueu aquells empleats tals que n'existeix un altre amb el mateix departament i diferent ciutat.

## Pregunta 4:

- Similar a l'exercici 2. La majoria busqueu els professors amb sou=100000 i feu join amb assignacions. Fixeu-vos que l'enunciat diu "despatxos que NOMÉS han estat ocupats per professors amb sou igual a 100000".

- Joc de proves per si no veieu clar el problema:
  ``` sql
  insert into professors values ('999', 'DOLORS', '323323323', 100000);
  insert into despatxos values ('Omega','128',30);
  insert into assignacions values ('999', 'Omega', '128', 1, null);
  insert into professors values ('888', 'MARC', '323323323', 50000);
  insert into assignacions values ('888', 'Omega', '128', 1, null);
  ```
  És a dir, un despatx amb una assignació d'un profe amb sou=100000 i un altre amb sou!=100000
