# ADR-0001: Clean Architecture Kullanımı

## Durum
Kabul edildi

## Bağlam
Projenin test edilebilir, bakımı kolay ve katmanlar arası bağımlılıkları 
net olan bir yapıya ihtiyacı var.

## Karar
4 katmanlı Clean Architecture kullanıldı:
Domain → Application → Infrastructure → Api

## Sebep
- Domain business logic'i altyapıdan izole
- Her katman bağımsız test edilebilir
- ORM değişimi Infrastructure'da kalır, domain etkilenmez

## Alternatifler
- Basit Layered Architecture (daha az boilerplate ama daha az izolasyon)
- Vertical Slice Architecture (feature-based, büyük ekiplerde iyi)

## Sonuçlar
Daha fazla proje ve klasör ama uzun vadede daha temiz kod.