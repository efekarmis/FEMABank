# ADR-0004: Result Pattern

## Durum
Kabul edildi

## Karar
Business hataları için exception yerine Result<T> pattern kullanıldı.

## Sebep
- Method imzaları dürüst (başarısız olabileceği belli)
- Exception sadece gerçek exceptional durumlar için
- Performans (exception throw maliyetli)

## Sonuçlar
Tüm handler'lar Result<T> döndürür.
Controller'da Result → HTTP status code mapping yapılır.