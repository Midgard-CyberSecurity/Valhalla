# Valhalla - Custom Arch Linux Repository

Repository personale per pacchetti Arch Linux.

## Installazione

Aggiungi al tuo `/etc/pacman.conf`:

```ini
[valhalla]
SigLevel = Optional TrustAll
Server = https://raw.githubusercontent.com/Midgard-CyberSecurity/Valhalla/main/x86_64
```

Aggiorna e installa:

```bash
sudo pacman -Sy
sudo pacman -S nome-pacchetto
```

## Pacchetti Disponibili

```bash
# Lista pacchetti disponibili
pacman -Sl valhalla

# Info su un pacchetto
pacman -Si nome-pacchetto
```

## Pacchetti Inclusi

- **huginn** - Hub manager per Arch Linux

---

*Repository mantenuta personalmente. Usa a tuo rischio.*
