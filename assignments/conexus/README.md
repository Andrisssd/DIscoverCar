## Task 1 - SQL vaicājumi
---
### Schema
```sql
CREATE TABLE IF NOT EXISTING Employee (
	'ID' int not null,
	'Department' int not null,
	'ChiefId'int null,
	'Name' varchar(255) not null,
	'Salary'decimal not null,
	PRIMARY KEY ('ID')
	CONSTRAINT 'fk_Employee_Employee' FOREIGN KEY ('ChiefId') REFERANCES Employee ('ID'),
	CONSTRAINT 'fk_Employee_Department' FOREIGN KEY ('DepartmentID') REFERANCES Department ('ID'),
)
CREATE TABLE IF NOT EXISTS Department (
	'ID' int not null,
	'Name' varchar(255) not null,
	PRIMARY KEY ('ID')
)
```

1. Uzrakstiet SQL pieprasījumu, kas atgriež darbiniekus ar maksimālo atalgojumu savā departamentā.
2. Uzrakstiet SQL pieprasījumu, kas noskaidro departamenta vadītājus.
3. Uzrakstiet SQL pieprasījumu, kas sakārto departamentus pēc efektivitātes (darbinieku skaits pret kopējām
izmaksām).
4. Uzrakstiet SQL pieprasījumu, kas noskaidro katram departamentam darbinieku hierarhijas maksimālo līmeni.

---

## Task 2 - Izvēlieties programmēšanas valodu (vēlams izmantot C++/C#) un atbildiet uz jautājumiem:

---

1. Uzrakstiet funkciju, kas, saņemot veselo skaitļu masīvu, pārceļ visas nulles uz masīva beigām, saglabājot pārējo
skaitļu kārtību. Mēģiniet izmantot pēc iespējas mazāk papildus atmiņas.
Piemērs: [5, 0, 8, 3, 0] => [5, 8, 3, 0, 0].

2. Ko var noskaidrot ar pārbaudi, ja x – vesels skaitlis: x & (x - 1) == 0 ?

3. Uzrakstiet funkciju, kas masīvam noskaidro mediānu (elements, kas sadala kopu divās vienādās daļās: skaitļi,
mazāki par mediānu, un skaitļi, lielāki par mediānu).
