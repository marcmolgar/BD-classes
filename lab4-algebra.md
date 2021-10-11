#Àlgebra relacional

Pregunta 1:
- Fàcil, nivell tontico

Pregunta 2:
- Molta gent selecciona els empleats que viuen a Madrid
  A=EMPLEATS(CIUTAT_EMPL = 'MADRID')
  I fa la join amb DEPARTAMENTS
- Proveu què passa si feu això amb aquest joc de proves:
  INSERT INTO  DEPARTAMENTS VALUES(3,'MARKETING',3,'VERDAGUER','VIC');
  INSERT INTO  PROJECTES VALUES (1,'IBDTEL','TELEVISIO',1000000);
  INSERT INTO  EMPLEATS VALUES (3,'ROBERTO',25000,'MADRID',3,1);
  INSERT INTO  EMPLEATS VALUES (4,’MARC’,35000,’BARCELONA’,3,1);
  És a dir, quan un departament té un empleat de Madrid i un d’una altra ciutat.
- Per aconseguir que "El resultat no ha d'incloure aquells departaments que no tenen cap empleat", penseu que si feu una join DEPARTAMENTS*EMPLEATS, els departaments que no tenen empleats no fan match amb cap empleat, i per tant no apareixen en el resultat.

Pregunta 3:
