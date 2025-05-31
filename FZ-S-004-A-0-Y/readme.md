## Использование ESP32 Marauder напрямую

**Важно:** GPS-антенна заявлена как всенаправленная, но на самом деле направленная — керамическая часть должна быть направлена в небо для корректного позиционирования.

**Поддерживаемые функции:**

- WiFi 2.4 ГГц, Bluetooth, GPS.

- Поддержка SD-карт (до 32 ГБ, формат FAT32).

**Аккумулятор:** 800 мАч, время зарядки ~2 часа.  
**Входное напряжение:** 5V/2A, выход: 5V/2.4A.

#### Меню:

1. **Sniffers (Снифферы WiFi)**
   
   - **Probe Request Sniff** — отображает MAC-адреса устройств вокруг.
   
   - **Beacon Sniff** — показывает список WiFi-сетей в реальном времени.
   
   - **Deauth Sniff** — детектирует атаки Deauth и показывает их мощность.
   
   - **EAPOL/PMKID Scan** — сканирование пакетов (требуется предварительный выбор WiFi).
   
   - **Packet Monitor** — мониторинг трафика (Beacons, Deauths, Probes).
   
   - **Scan AP** — сканирование WiFi-сетей (рекомендуется перед любыми действиями).
   
   - **Raw Capture** — отображает мощность сигнала MAC-адресов.
   
   - **Stations Sniff** — показывает устройства, подключённые к WiFi.
   
   - **Signal Monitor** — мониторинг изменения силы сигнала (RSSI).
   
   - **Wardrive** — автоматическое сохранение данных WiFi и GPS на SD-карту.
   
   - **Stations Wardrive** — автоматическое сохранение данных устройств на SD-карту.

**Все данные сохраняются в формате PCAP на SD-карту.**

2. **WiFi Attacks (Атаки WiFi)**

#### **Beacon Spam (Спам маяками WiFi)**

- **Beacon Spam List** – Спам списком WiFi-сетей.

- **Beacon Spam Random** – Случайный спам WiFi-сетями.

- **Rick Roll Beacon** – Неизвестный метод атаки.

- **Probe Req Flood** – Атака Probe Request (неизвестный метод).

- **Evil Portal (Фишинговая атака)**
  
  - - Перед использованием необходимо поместить файлы `index.html` (или другие HTML-файлы) на SD-карту.
    
    - В меню **General → Select EP HTML File** можно выбрать нужный фишинговый шаблон.
      
      - Создайте файл `ap.config.txt` в корне SD-карты.
    
    - Отсканируйте и выберите целевую WiFi-сеть (см. инструкцию ниже).
    
    - При подключении жертвы к этой сети, если они введут логин/пароль, данные будут отображены.
    
    - **Официальный гайд:** [GitHub Evil Portal Workflow](https://github.com/justcallmekoko/ESP32Marauder/wiki/evil-portal-workflow#using-configuration-file)

- **Deauth Flood (Атака деаутентификации)**
  
  - Отсканируйте и выберите WiFi (см. инструкцию ниже), затем запустите атаку.

- **AP Clone Spam (Клонирование WiFi-сетей)**
  
  - Клонирует все WiFi-сети из вашего списка.

- **Deauth Targeted (Целевая деаутентификация)**
  
  - Неизвестный метод атаки.

---

3. **WiFi General (Общие настройки WiFi)**
- **Generate SSIDs** – Генерация SSID.

- **Save/Load File** – Сохранение/загрузка из файла.

- **Add SSIDs** – Добавление SSID вручную.

- **Clear SSIDs** – Очистка списка SSID.

- **Clear APs** – Очистка списка WiFi-сетей.

- **Select APs** – Выбор WiFi-сети для атаки.

- **Select Stations** – Выбор устройств, подключённых к WiFi.

- **Select EP HTML File** – Выбор HTML-файла для фишинга.

---

## **Bluetooth (Bluetooth-атаки)**

#### **Sniffers (Сниффинг Bluetooth)**

- **Bluetooth Sniffer** – Отображает RSSI-сигналы Bluetooth-устройств.

- **BT Wardrive** – Автоматическое сохранение данных Bluetooth и GPS на SD-карту (файлы с префиксом `wardrive`).

- **Detect Card Skimmers** – Обнаружение Bluetooth-скиммеров (старые модели могут быть уязвимы к атакам).

#### **Bluetooth Attacks (Атаки через Bluetooth)**

- **Sour Apple** – Тест уязвимости Apple (поп-ап на iPhone).

- **Swiftpair Spam** – Поп-ап атака на ПК с Windows.

- **Samsung BLE SPAM** – Поп-ап атака на Samsung.

- **BLE Spam ALL** – Все вышеперечисленные атаки одновременно.

---

## **Device (Настройки устройства)**

- **Update Firmware** – Обновление прошивки (скачайте с [официального репозитория](https://github.com/justcallmekoko/ESP32Marauder/releases), версия **V6**).

- **Language** – Только английский (пока нет русского).

- **Device Info** – Информация об устройстве.

- **Settings** – Настройки (LED, сохранение PCAP и др.).

- **GPS Data** – Данные GPS (широта, долгота, высота, время UTC+0 – для России +8 часов).

- **NMEA Stream** – Реальные данные GPS (холодный старт может занять время, лучше использовать на улице, антенна должна быть направлена в небо).

---

## **Полный процесс тестирования WiFi-атак**

1. **Scan APs** (в меню Sniffers) – сканирование WiFi.

2. **Select APs** (в меню General) – выбор цели.

3. **Deauth Flood** (в меню Attacks) – запуск атаки.

### **Как выбрать WiFi для атаки?**

1. **Sniffers → Scan APs** – сканирование.

2. **General → Select APs** – выбор сети.

**Официальная документация:** [ESP32 Marauder Wiki](https://github.com/justcallmekoko/ESP32Marauder/wiki)
