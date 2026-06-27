# Herramientas

Herramientas instaladas en Ubuntu Noble ARM64 sobre la Nintendo Switch.

## Instaladas via apt

```bash
sudo systemctl stop packagekit
sudo apt install nmap gobuster nikto sqlmap john netcat-traditional tmux tshark wireshark hydra ncrack whatweb dirb default-jre -y
```

| Herramienta | Uso |
|---|---|
| nmap | Escaneo de puertos y servicios |
| gobuster | Fuerza bruta de directorios web |
| nikto | Escáner de vulnerabilidades web |
| sqlmap | Detección y explotación de SQL injection |
| john | Cracking de hashes |
| netcat-traditional | Conexiones TCP/UDP, reverse shells |
| tmux | Multiplexor de terminal |
| tshark | Captura de tráfico (CLI) |
| wireshark | Captura de tráfico (GUI) |
| hydra | Fuerza bruta de credenciales |
| ncrack | Fuerza bruta de autenticación en red |
| whatweb | Identificación de tecnologías web |
| dirb | Fuerza bruta de directorios web |
| default-jre | Java Runtime (necesario para algunas herramientas) |

## Metasploit

Instalado via instalador oficial:

```bash
curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall
chmod +x msfinstall
sudo ./msfinstall
```

## SecLists

```bash
sudo git clone https://github.com/danielmiessler/SecLists /usr/share/seclists
```

> ℹ️ SecLists no está disponible via apt en Ubuntu — git clone es el método de instalación.

## Wireshark — captura sin root

```bash
sudo usermod -aG wireshark $USER
```

Cerrar sesión y volver a entrar para que el cambio tenga efecto.
