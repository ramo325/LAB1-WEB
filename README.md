# LAB2-WEB
# Muzička Streaming Aplikacija - LAB 2

## Podaci o studentima i timu:
- Ramo Kozlić
- Emir Đelilbašić

---

## Logički tok kreiranja aplikacije:
Aplikacija je nadograđena sa in-memory arhitekture na relacionu bazu podataka. Kreiran je novi entitet `Izdavac` i povezan sa postojećim modelom `Album`. Implementirani su MVC i REST kontroleri za rad sa podacima, te forme za unos i izmjenu unutar Thymeleaf view-a.

---

## Opis novog modela i relacije:
- **Model Izdavac:** Sadrži atribute `id`, `naziv`, `drzava`, `godinaOsnivanja` i listu povezanih albuma.
- **Relacija:** 1:N između `Izdavac` i `Album`.

---

## Opis funkcionalnosti kontrolera:
1. **`IzdavacController` (Obični MVC Controller):**
   - GET `/izdavaci`: Prikazuje tabelu svih izdavača i formu za dodavanje novog.
   - POST `/izdavaci/add`: Čuva novog izdavača u bazi.
   - GET `/izdavaci/edit/{id}`: Otvara formu za izmjenu postojećeg izdavača.
   - POST `/izdavaci/update`: Spasava ažurirane podatke izdavača u bazi.

2. **`IzdavacRestController` (REST Controller):**
   - GET `/api/izdavaci`: Vraća listu svih izdavača iz baze u čistom **JSON** formatu.
   - GET `/api/izdavaci/{id}`: Vraća podatak o pojedinačnom izdavaču po ID-u u JSON formatu.

---

## Konfiguracija Baze Podataka:
Korištena je *lokalna MySQL baza podataka*. 
- *Database Name:* muzickadb
- *Driver:* com.mysql.cj.jdbc.Driver
- *ORM Framework:* Spring Data JPA / Hibernate
- *DDL postavka:* spring.jpa.hibernate.ddl-auto=update 

---

## Izvori i korišteni alati:
1. **Službena dokumentacija:** [Spring Boot Reference Documentation](https://spring.io/projects/spring-boot)
2. Projekat sa vježbi
