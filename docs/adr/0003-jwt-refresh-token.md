# ADR-0003: JWT + Refresh Token

## Durum
Kabul edildi

## Karar
Authentication için JWT Access Token (15dk) + Refresh Token (7gün) kullanıldı.

## Sebep
- SPA (React) için stateless auth
- Access token kısa ömürlü = çalınsa bile zarar sınırlı
- Refresh token HttpOnly cookie = XSS'e dayanıklı

## Sonuçlar
Refresh token rotation uygulandı.
Reuse detection ile token theft tespiti mümkün.