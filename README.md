1. Otvorite priloženu datoteku "db_algebra_racuni.sql" za kreiranje baze podataka u SQL Server Management Studio (SSMS) alatu. Izvedite skriptu po koracima.
2. Kreirajte novi ASP.NET MVC projekt u Visual Studiju.
3. Koristeći naredbu za scaffolding baze podataka iz VS -> Package Manager Console terminala, generirajte bazne objekte preko EF Core-a (modele i db context) putem database-first pristupa
4. Provjerite da li je sve u redu i istražite strukturu dodatih datoteka, posebice dodane klase *DbContext.
5. Dodajte dio za konfiguriranje pristupa bazi podataka kroz konfiguracijsku datoteku.

** 2. Dodati sljedeće pakete u projekt
      - Microsoft.EntityFrameworkCore.Design, .Tools, .SqlServer
      Buildati projekt
      Unutar PMC-a pokrenuti 
      dotnet tools install

** 3. U PMC pokrenuti komandu
     -> dotnet tool install
     Pa zatim
     -> dotnet ef dbcontext scaffold "Server=<tvojServer>;Database=invoices;Trusted_Connection=true;;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer --project Zadaci.Racuni

**Atribut --project nije nužan, meni nije prepoznavalo project
