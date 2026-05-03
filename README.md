# 🏦 FEMABank

Mini banka ve kredi yönetim sistemi. ASP.NET Core 9, EF Core, MSSQL, React.

## 🏗️ Mimari

Clean Architecture (4 katman):
- **Domain:** Entity'ler, value object'ler, domain event'ler
- **Application:** Use case'ler, MediatR handler'lar, DTO'lar
- **Infrastructure:** EF Core, Identity, external servisler
- **Api:** Controller'lar, middleware, Swagger

## 🚀 Çalıştırma

### Gereksinimler
- .NET 9 SDK
- Docker Desktop

### Kurulum

```bash
# 1. Repo'yu clone'la
git clone https://github.com/[username]/FEMABank.git
cd FEMABank

# 2. Docker ile DB'yi başlat
docker-compose up -d

# 3. Migration'ları uygula
dotnet ef database update --project src/FEMABank.Infrastructure --startup-project src/FEMABank.Api

# 4. API'yi çalıştır
dotnet run --project src/FEMABank.Api
```

### Swagger UI
`https://localhost:5001/swagger`

## 📦 Modüller

| Modül | Açıklama | Durum |
|-------|----------|-------|
| 1 | Foundation + Authentication | 🚧 In Progress |
| 2 | Customer Management | ⏳ Planned |
| 3 | Bank Accounts | ⏳ Planned |
| 4 | Money Transfer | ⏳ Planned |
| 5 | Loan Application | ⏳ Planned |
| 6 | Payment Schedule | ⏳ Planned |

## 🏛️ Mimari Kararlar

[ADR dökümanlarına bak](docs/adr/)

## 🧪 Test

```bash
dotnet test
```