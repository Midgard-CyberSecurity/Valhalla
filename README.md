# Valhalla ⚔️

> Custom Arch Linux Repository - Midgard CyberSecurity

Repository personale per pacchetti Arch Linux custom e personalizzati.

## 🚀 Installazione Rapida

Aggiungi al tuo `/etc/pacman.conf`:

```ini
[valhalla]
SigLevel = Optional TrustAll
Server = https://raw.githubusercontent.com/Midgard-CyberSecurity/Valhalla/main/x86_64
```

Poi aggiorna e installa:

```bash
sudo pacman -Sy
sudo pacman -S huginn  # o altro pacchetto
```

## 📦 Pacchetti Disponibili

| Pacchetto | Versione | Descrizione | Dimensione |
|-----------|----------|-------------|------------|
| **huginn** | 1.0.0-1 | Hub manager per Arch Linux | ~218 MB |

### Comandi Utili

```bash
# Lista tutti i pacchetti disponibili
pacman -Sl valhalla

# Informazioni su un pacchetto specifico
pacman -Si huginn

# Installa un pacchetto
sudo pacman -S valhalla/huginn

# Aggiorna da questa repo se già installato
sudo pacman -S valhalla/huginn --overwrite '*'
```

## ⚠️ Note Importanti

- **Signature Level**: La repo usa `SigLevel = Optional TrustAll` - i pacchetti non sono firmati GPG
- **Git LFS**: I pacchetti grandi sono ospitati su GitHub LFS
- **Limiti GitHub**: 1GB storage + 1GB bandwidth/mese (limite gratuito)
- **Uso personale**: Repository mantenuta per uso interno, usa a tuo rischio

## 🔧 Per Maintainer

### Aggiungere un nuovo pacchetto

```bash
# 1. Copia il pacchetto compilato
./scripts/add-package.sh /path/to/package.pkg.tar.zst

# 2. Commit e push
git add x86_64/
git commit -m "Add: nome-pacchetto vX.Y.Z"
git push
```

### Rimuovere un pacchetto

```bash
./scripts/remove-package.sh nome-pacchetto
git add x86_64/
git commit -m "Remove: nome-pacchetto"
git push
```

### Struttura Repository

```
.
├── x86_64/                    # Pacchetti compilati (pubblico)
│   ├── *.pkg.tar.zst          # Pacchetti (Git LFS)
│   ├── valhalla.db.tar.gz     # Database repo
│   └── valhalla.files.tar.gz  # File index
├── scripts/                    # Script gestione (locale)
├── docs/                       # Documentazione (locale)
└── pkgbuilds/                  # PKGBUILD (locale)
```

## 📚 Risorse

- [Arch Wiki - Custom Local Repository](https://wiki.archlinux.org/title/Pacman/Tips_and_tricks#Custom_local_repository)
- [Documentazione completa](./MAINTAINER.md) (solo locale)

## 📄 Licenza

Repository personale - Midgard CyberSecurity  
Pacchetti individuali mantengono le proprie licenze originali.

---

*Valhalla - Where packages go to live forever* ⚔️
