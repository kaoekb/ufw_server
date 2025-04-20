# 🔐 Ansible: UFW Firewall Setup for VPN Servers

Этот проект настраивает безопасный фаервол `ufw` на нескольких VPN-серверах с помощью Ansible.

---

## 📁 Структура проекта

```
ufv_server/
├── hosts.ini             # Инвентарь (список серверов)
├── ufw.yml               # Основной плейбук
├── .gitignore            # Исключения
└── roles/
    └── ufw/
        ├── tasks/
        │   └── main.yml
        ├── vars/
        │   └── main.yml
        ├── defaults/
        │   └── main.yml
        └── handlers/
            └── main.yml
```

---

## ✅ Возможности

- Установка и включение UFW
- Задание правил для TCP и UDP портов
- Rate limiting для SSH-порта

---

## 🚀 Быстрый старт

### 1. Заполни файл инвентаря `hosts.ini`

```ini
[vpn_servers]
server1 ansible_host=192.168.1.10 ansible_port=22 ansible_user=root
server2 ansible_host=192.168.1.11 ansible_port=22 ansible_user=root
```

---

### 2. Запуск

```bash
ansible-playbook -i hosts.ini ufw.yml --ask-vault-pass
```

---

## 📜 Лицензия

MIT

---

© Kacidrat, 2025