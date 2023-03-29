# MySQL Cheatsheet

## Basics

Alle Datenbanken zeigen
> show databases;

Neue Datenbank db erstellen
> create dabase db;

Datenbank benutzen
> use db;

Umfang der Datenbank zeigen
> show tables;

Variablen von zB Tabelle Anzeigen
> show columns from lala;

Datentypen:
> varchar, integer, date, bool(?)


Tabelle anschauen
> select * from lala limit 100;

Auswahl
> select * from lala where Var1='bla';

## Erstellen

Neue Tabelle erstellen
> create table lala(
> var1 type(max),
> varn type(max));

### Special cases beim Tabelle erstellen
Variable soll immer nur einmal vorkommen
> var1 type(max) unique,
> 
> var1 type(max) primary key,

Variable muss angegeben werden
> var1 type(max) not null,

Variable darf ausgelassen werden
> var1 type(max) null,

Variable muss bestimmte Bedinungen erfüllen
(wird wie Variable hinzugefügt)
>constraint chk_var1 check (var1 <> 0),
>
>constraint chk_var1 check (var1 in ('bla', 'blaa', 'blaaa'),

Eintrag in Table erstellen
>insert into lala (
var1, varn)
values ('bla', 'blaa');


## Verändern

Einzelnen Eintrag verändern
> update lala set var1='bla1' where var1='bla';

neue Spalte hinzufügen
> alter table lala add dummy type;

eine Spalte löschen
> alter table lala drop dummy;


Kommentare im Script
> \#
> 
> */ asdf */


commiten
> commit;
