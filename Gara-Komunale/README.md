# 🏆 Gara Komunale e Diturisë 2026 – Shtime

Sistem elektronik për organizimin e garës komunale akademike.

## 📦 Kërkesat

- Python 3.10+
- pip

## 🚀 Instalimi & Startimi

```bash
# 1. Instalo paketat
pip install flask flask-cors openpyxl reportlab

# 2. Starto serverin
python3 server.py
```

Pastaj hap shfletuesin te: **http://localhost:5000**

---

## 👤 Kredencialet Default të Administratorit

- **Përdoruesi:** `admin`
- **Fjalëkalimi:** `admin123`

⚠️ Ndrysho fjalëkalimin pas hyrjes së parë!

---

## 🖥️ Si Funksionon

### Për Administratorët:
1. Hyr te **Panel Administratori**
2. Kliko **"Krijo Test të Ri"**
3. Zgjidh lëndën (sistemi cakton automatikisht numrin e pyetjeve)
4. Shto pyetjet me 4 opsione (A, B, C, D) dhe shëno opsionin e saktë
5. Ruaj testin – gjenerohet automatikisht **kodi 6-shifror**
6. Shpërndaj kodin tek nxënësit
7. Monitoro rezultatet në kohë reale
8. Eksporto të dhënat si **Excel** ose **PDF**

### Për Nxënësit:
1. Hyr te **Portal Nxënësi**
2. Plotëso: Emri, Mbiemri, Klasa, Shkolla, Kodi i Testit
3. Fillo testin – kemi **60 minuta** kohë
4. Paralajmërim automatik **5 minuta** para mbarimit
5. Dorëzo testin – shfaqet rezultati menjëherë me:
   - Pikët e fituara + ID e sesionit
   - Pyetjet e gabuara me përgjigjet e sakta

---

## 🏅 Sistemi i Pikëve

| Lënda | Pyetje | Pikë/Pyetje | Total |
|-------|--------|-------------|-------|
| Matematikë | 10 | 10 | 100 |
| Fizikë | 10 | 10 | 100 |
| Kimi | 10 | 10 | 100 |
| Biologji | 20 | 5 | 100 |
| Gjuhë shqipe | 20 | 5 | 100 |
| Gjuhë angleze | 20 | 5 | 100 |
| Histori | 20 | 5 | 100 |
| Gjeografi | 20 | 5 | 100 |
| TIK | 20 | 5 | 100 |

**Tie-breaking:** Nëse dy nxënës kanë pikë të njëjta, ai që e ka përfunduar testin më shpejt renditet para.

---

## ⚡ Kapaciteti

- **245 nxënës njëkohësisht** (Flask threaded mode + SQLite WAL)
- Auto-save i çdo përgjigje
- Mbyllje automatike e testit pas 60 minutave

---

## 📁 Struktura e Projektit

```
gara-diturise/
├── server.py          # Backend Flask
├── gara.db            # Database SQLite (krijohet automatikisht)
├── public/
│   └── index.html     # Frontend i plotë
└── README.md
```
