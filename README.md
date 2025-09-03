# 🏦 NBS IPS QR Generator

Progressive Web App (PWA) za generisanje QR kodova za trenutna plaćanja u Srbiji preko NBS IPS (Instant Payment System) sistema.

## 🎯 Opis

Ova aplikacija omogućava kreiranje QR kodova koji se mogu skenirati u bilo kojoj banking aplikaciji u Srbiji za brza i sigurna plaćanja. QR kodovi su generisani prema zvaničnoj NBS specifikaciji za IPS plaćanja.

## ✨ Funkcionalnosti

- 📱 **Progressive Web App** - može se instalirati na telefon
- 🔒 **Potpuna privatnost** - svi podaci se čuvaju lokalno na vašem uređaju
- 🌐 **Offline rad** - radi bez internet konekcije nakon prvog učitavanja
- ⚡ **Trenutna plaćanja** - kompatibilno sa svim banking aplikacijama u Srbiji
- 💾 **Pamćenje podešavanja** - jednom unesete svoje podatke
- 📤 **Deljenje QR kodova** - preuzimanje i deljenje generisanih QR kodova
- 🇷🇸 **Srpski jezik** - kompletna lokalizacija

## 🖥️ Kako koristiti

### 1. Početno podešavanje
1. Idite na tab **"Podešavanja"**
2. Unesite svoje podatke:
   - Ime i prezime
   - Broj računa (format: 000-0000000000000-00)
   - Šifru plaćanja (289 za bezgotovinska plaćanja)
   - Adresu i mesto (opciono)
3. Kliknite **"Sačuvaj podešavanja"**

### 2. Generisanje QR koda
1. Idite na tab **"Generator"**
2. Unesite:
   - Iznos u RSD
   - Svrhu plaćanja
3. Kliknite **"Generiši QR kod"**
4. Koristite **"Preuzmi QR kod"** ili **"Podeli QR kod"**

### 3. Plaćanje
Osoba koja plaća treba da:
1. Otvori svoju banking aplikaciju
2. Skenira generisani QR kod
3. Potvrdi plaćanje

## 🚀 Pokretanje

Aplikacija radi direktno u browser-u. Jednostavno otvorite `ips-qr-generator.html` fajl.

### Lokalno pokretanje
```bash
# Klonirajte repozitorijum
git clone https://github.com/cukovicmilos/qrmitant.git

# Otvorite fajl u browser-u
open ips-qr-generator.html
```

### Web server (opciono)
```bash
# Python 3
python -m http.server 8000

# Node.js (sa npx)
npx serve .

# Zatim idite na http://localhost:8000
```

## 📁 Struktura projekta

```
qrmitant/
├── ips-qr-generator.html    # Glavna HTML aplikacija
├── manifest.json            # PWA manifest fajl
├── sw.js                   # Service Worker za offline funkcionalnost
├── .gitignore              # Git ignore fajl
└── README.md               # Ovaj fajl
```

## 🛠️ Tehnologije

- **HTML5** - struktura aplikacije
- **Tailwind CSS** - stilizovanje (CDN)
- **Vanilla JavaScript** - funkcionalnost
- **QR Code Generator** - generisanje QR kodova
- **Service Worker** - offline podrška
- **localStorage** - čuvanje podešavanja
- **Web Share API** - deljenje QR kodova
- **Canvas API** - crtanje i eksportovanje QR kodova

## 🔐 Privatnost i sigurnost

- ✅ **Bez slanja podataka na internet** - sve se izvršava lokalno
- ✅ **Bez čuvanja podataka na serverima** - koristi localStorage
- ✅ **Bez praćenja korisnika** - nema analitiku ili cookie-je
- ✅ **Open source kod** - transparentan i proveren

## 🏛️ NBS IPS Standard

Aplikacija generiše QR kodove prema zvaničnoj NBS specifikaciji:
```
K:PR|V:01|C:1|R:račun|N:ime|I:iznos|SF:šifra|S:svrha
```

Gde:
- `K:PR` - tip transakcije (plaćanje)
- `V:01` - verzija protokola
- `C:1` - valuta (1 = RSD)
- `R` - broj računa primaoca (bez crtice)
- `N` - ime primaoca (latinica)
- `I` - iznos (RSD + zarez)
- `SF` - šifra plaćanja
- `S` - svrha plaćanja (latinica)

## 🏦 Kompatibilnost

QR kodovi rade sa svim banking aplikacijama u Srbiji koje podržavaju NBS IPS, uključujući:
- Banca Intesa
- Komercijalna banka
- Raiffeisen Bank
- UniCredit Bank
- AIK Banka
- Erste Bank
- I sve ostale banke koje podržavaju NBS IPS

## 📱 PWA Instalacija

Aplikacija može da se instalira kao PWA:
1. Otvorite aplikaciju u browser-u
2. Kliknite dugme **"📱 Instaliraj aplikaciju"** (ako se pojavi)
3. Ili koristite browser opciju "Add to Home Screen"

## 💖 Donacije

Ako vam je aplikacija korisna, možete podržati autora donacijom od 50 RSD preko tab-a **"Donirajte"**.

## 👨‍💻 Autor

**Miloš Ćuković / chulechux**
- Website: [mustrabecka.com](https://mustrabecka.com/vibe-coding-story/)

## 📄 Licenca

Ovaj projekat je open source. Slobodno ga koristite, menjajte i delite.

## 🐛 Problemi i predlozi

Ako imate problema ili predloge za poboljšanje:
1. Otvorite [Issue](https://github.com/cukovicmilos/qrmitant/issues) na GitHub-u
2. Ili kontaktirajte autora direktno

## 🔄 Verzije

- **v1.0** - Početna verzija sa osnovnim funkcionalnostima PWA-a

---

**Napomena:** Aplikacija je namenjena za legitimno korišćenje u skladu sa NBS IPS pravilnikom. Autor nije odgovoran za zloupotrebe.
