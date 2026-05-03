# ADR-0002: MSSQL + EF Core

## Durum
Kabul edildi

## Karar
Database olarak MSSQL, ORM olarak EF Core Code-First kullanıldı.

## Sebep
- Şirket stack'i MSSQL
- EF Core type-safe, refactor dostu
- Code-First migration ile DB versiyonlama kolay

## Alternatifler
- PostgreSQL (open source, ama şirket stack'i değil)
- Dapper (daha performanslı ama daha fazla manuel SQL)

## Sonuçlar
EF Core'un ürettiği SQL'i LogTo ile monitor edeceğiz.
N+1 problemlerini Include stratejisi ile önleyeceğiz.