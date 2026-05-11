# Looker Content Ogooga

Aplicație de analiză trafic și conversie pentru SuperCazino, Casino.com.ro și JocPăcănele.

🔗 **[Deschide aplicația](#)** ← înlocuiește cu URL-ul de GitHub Pages după deployment

---

## Update săptămânal (~ 2 minute)

1. Exportă CSV-urile din Looker (câte unul per site, per intervalul dorit)
2. Pe GitHub.com, mergi în `data/current/`
3. **Înlocuiește** fișierul vechi cu cel nou (același nume)
4. Pune o **copie cu data** în `data/archive/` (ex: `SC_30d_2026-05-18.csv`)

Gata. Aplicația preia datele noi la următoarea deschidere.

---

## Structura fișierelor

```
/data/current/
  SC_7d.csv      ← SuperCazino, 7 zile
  SC_30d.csv     ← SuperCazino, 30 zile
  SC_365d.csv    ← SuperCazino, 365 zile
  CCR_7d.csv     ← Casino.com.ro, 7 zile
  CCR_30d.csv
  CCR_365d.csv
  JP_7d.csv      ← JocPăcănele, 7 zile
  JP_30d.csv
  JP_365d.csv
  SC_gsc.csv     ← GSC opțional (dacă îl ai)
  CCR_gsc.csv
  JP_gsc.csv

/data/archive/
  SC_30d_2026-05-11.csv   ← copii istorice cu data în nume
  ...
```

Dacă un fișier lipsește, secțiunea respectivă e ascunsă automat în aplicație.

---

## Cadență recomandată

| Când | Ce încarci |
|------|-----------|
| Luni dimineața | 3 × 7 zile (SC, CCR, JP) |
| 1 ale lunii | 3 × 30 zile |
| 1 ale trimestrului | 3 × 365 zile |
