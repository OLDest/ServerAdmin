# ServerAdmin

[Русский](#русский) · [English](#english)

Official website: https://serveradmin.su/  
Current version: **1.1.0.373**  
Download: https://download.agbis.co/download/admin_tools/ServerAdmin/ServerAdmin-1.1.0.373.zip  
CRC: https://download.agbis.co/download/admin_tools/ServerAdmin/ServerAdmin-1.1.0.373.zip_crc  
SHA-256: `042B801474525AABAC1B8C2CD0E3E4C268B25A06AB26E6ECD4E709B36B1C63AC`


Privacy policy: [English](https://serveradmin.su/en/privacy/) · [Русский](https://serveradmin.su/privacy/) · [Repository copy](PRIVACY.md)

## Screenshots

![ServerAdmin workspace](https://serveradmin.su/assets/screenshots/vcl-workspace.png?v=1.1.0.373)

![Server monitoring](https://serveradmin.su/assets/screenshots/vcl-monitoring.png?v=1.1.0.373)

![Embedded VM console](https://serveradmin.su/assets/screenshots/vcl-console.png?v=1.1.0.373)

![Web dashboard](https://serveradmin.su/assets/screenshots/web-dashboard.png?v=1.1.0.373)

## Русский

**ServerAdmin** — бесплатное Windows-приложение для управления серверами Proxmox и виртуальными машинами Windows из единого интерфейса.

### Возможности

- Подключение нескольких серверов Proxmox и объединение их в группы.
- SSH-доступ через Pageant, SSH-ключ или пароль.
- Запуск, остановка, перезагрузка, пауза и удаление виртуальных машин.
- Изменение процессоров, памяти, дисков, сети и CD/DVD виртуальных машин.
- Создание и восстановление резервных копий.
- Управление хранилищами, ISO-образами и расписаниями Proxmox.
- Мониторинг серверов, ВМ, хранилищ и ZFS.
- История показателей в CSV, инциденты, webhooks и настраиваемые пороги.
- Массовые операции с серверами и виртуальными машинами.
- Встроенные RDP, VNC, SSH и консоль.
- Агент DevOpsTasks для Windows VM: PowerShell, передача файлов, сведения о системе и снимки экрана.
- Web-интерфейс и фоновая служба ServerAdminJobService.
- История и контроль выполняемых задач.

### Требования

- Windows 10 или Windows 11.
- Microsoft Edge WebView2 Runtime.
- Сетевой доступ к Proxmox.
- Pageant с SSH-ключом либо SSH-пароль.
- QEMU Guest Agent для автоматической установки агента в Windows VM.

### Быстрый старт

1. Скачайте архив.
2. Распакуйте весь каталог.
3. При использовании ключа запустите Pageant.
4. Запустите `ServerAdmin.exe`.

Полная инструкция: https://serveradmin.su/guide/

### Лицензия

ServerAdmin распространяется бесплатно и предоставляется «как есть», без явных или подразумеваемых гарантий. Пользователь самостоятельно принимает риски, связанные с установкой и использованием приложения.

Исходный код в этом репозитории не публикуется.

---

## English

**ServerAdmin** is a free Windows application for managing Proxmox servers and Windows virtual machines from one interface.

### Features

- Multiple Proxmox servers and server groups.
- SSH access using Pageant, an SSH key, or a password.
- VM start, stop, reboot, pause, deletion, and hardware editing.
- CPU, memory, disk, network, and CD/DVD configuration.
- Backup creation and restoration.
- Storage, ISO image, and Proxmox schedule management.
- Server, VM, storage, and ZFS monitoring.
- CSV history, incidents, webhooks, and configurable thresholds.
- Bulk operations for servers and virtual machines.
- Embedded RDP, VNC, SSH, and console access.
- DevOpsTasks Windows VM agent: PowerShell commands, file transfer, system information, and screenshots.
- Web interface and ServerAdminJobService background service.
- Task history and task control.

### Requirements

- Windows 10 or Windows 11.
- Microsoft Edge WebView2 Runtime.
- Network access to Proxmox.
- Pageant with an SSH key, or an SSH password.
- QEMU Guest Agent for automatic Windows VM agent installation.

### Quick start

1. Download the archive.
2. Extract the entire directory.
3. Start Pageant when using an SSH key.
4. Run `ServerAdmin.exe`.

Full guide: https://serveradmin.su/en/guide/

### License

ServerAdmin is distributed free of charge and provided “as is”, without express or implied warranties. Users assume all risks related to installing and using the application.

Source code is not published in this repository.

## Support

Feedback form: https://serveradmin.su/#contact
