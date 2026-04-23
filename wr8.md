# МІНІСТЕРСТВО ОСВІТИ І НАУКИ УКРАЇНИ  
## КИЇВСЬКИЙ ФАХОВИЙ КОЛЕДЖ ЗВ’ЯЗКУ  

---

# ЗВІТ  
## про виконання work-case №8
### з дисципліни «Операційні системи»

---

**Виконала:**  
студентка групи **БІКС-33**  
**Сербіна Ярослава Вячеславівна**

---

**Перевірила:**  
**Сушанова Вікторія Сергіївна**

---

**Київ - 2026**

---

# Work-case №8
## Операційні системи

---

## Пункт 1: Виконання базових задач у Linux через термінал

У даному пункті розглядаються базові можливості операційної системи Linux щодо виконання повсякденних задач без використання графічного інтерфейсу. Для цього використовуються консольні утиліти.

### 1.1 Перегляд файлів і папок у терміналі

Для роботи з файловою системою в терміналі використовується консольний файловий менеджер mc (Midnight Commander). Він дозволяє переглядати, копіювати, переміщувати та видаляти файли у зручному текстовому інтерфейсі.

Встановлення та запуск:
```bash
sudo apt install mc
mc
```

<img width="829" height="571" alt="image" src="https://github.com/user-attachments/assets/b5e09443-74eb-47b2-b43a-316d8fa4bf10" />

---

<img width="821" height="585" alt="image" src="https://github.com/user-attachments/assets/49eb665e-e4aa-42b0-9d9d-9adf6e9b2c60" />

Пояснення:
Після запуску відкривається двопанельний інтерфейс, який дозволяє навігацію по файловій системі без графічної оболонки.

### 1.2 Перегляд веб-сторінок у терміналі

Для перегляду веб-сторінок використовується текстовий браузер lynx. Він відображає сайти у вигляді тексту та дозволяє навігацію за допомогою клавіатури.

Команди:
```bash
sudo apt install lynx
lynx https://wikipedia.org
```

<img width="668" height="234" alt="image" src="https://github.com/user-attachments/assets/b7f1f9c5-b8b8-4524-a3cd-77c3f581f2c3" />

---

<img width="795" height="537" alt="image" src="https://github.com/user-attachments/assets/a1791719-3911-4872-974f-b0917f889abf" />

---

<img width="808" height="554" alt="image" src="https://github.com/user-attachments/assets/6784cd1f-cb44-4e7b-81d3-5645280f4a88" />

Пояснення:
Браузер завантажує сторінку та відображає її у терміналі без графічних елементів.

### 1.3 Перегляд електронної пошти в терміналі

Для роботи з електронною поштою використовуються пакети mailutils та mutt.

Команди:
```bash
sudo apt install mailutils mutt
echo "Hello from terminal" | mail -s "Test" yaroslava
mutt
```
<img width="830" height="522" alt="image" src="https://github.com/user-attachments/assets/d465e44c-0ae1-4816-a332-132db1b47dc0" />

---

<img width="825" height="107" alt="image" src="https://github.com/user-attachments/assets/a9e3b962-617b-4a57-82dc-d20f32bc322a" />

---

<img width="815" height="558" alt="image" src="https://github.com/user-attachments/assets/75419ee3-691c-4d63-be85-5b148f4b7f2a" />

---

<img width="502" height="232" alt="image" src="https://github.com/user-attachments/assets/d2ade4df-3ff1-4d5f-af4c-7f6fa13525fe" />

Пояснення:
Команда mail дозволяє надсилати листи, а mutt - переглядати та керувати електронною поштою в терміналі.

### 1.4 Відтворення музики через термінал

Для відтворення аудіофайлів використовується консольний плеєр cmus.

Команда:
 ```bash
sudo apt install cmus
cmus
```

<img width="817" height="537" alt="image" src="https://github.com/user-attachments/assets/5adc1da1-62a2-4b9b-bf2a-d0248abc197b" />

---

<img width="812" height="597" alt="image" src="https://github.com/user-attachments/assets/7867c897-05d0-4a49-8065-c2fda157a976" />

---

<img width="814" height="363" alt="image" src="https://github.com/user-attachments/assets/eba1a0be-95cb-4019-bf47-1bd74a1907c0" />

---

<img width="833" height="571" alt="image" src="https://github.com/user-attachments/assets/3c400378-a15f-43a1-8c7b-4e5a9b768852" />

---

<img width="875" height="125" alt="image" src="https://github.com/user-attachments/assets/c8a49073-f01c-4084-bcf1-cc76aa5284e7" />

Пояснення:
Після запуску відкривається інтерфейс медіаплеєра, який дозволяє керувати музикою без графічного середовища.

### 1.5 Завантаження торрентів через термінал

Для роботи з торрентами використовується transmission-cli. Він дозволяє завантажувати файли через magnet-посилання або .torrent файли.

Команда:
```bash
sudo apt install transmission-cli
transmission-cli "magnet:?xt=urn:btih:6a3d3b5b5c3c1d3f5c6b6e5d4f3a2b1c0d9e8f7a""
```

<img width="679" height="169" alt="image" src="https://github.com/user-attachments/assets/fb3e9c73-fb79-46f9-a0aa-087360fbee6e" />

---

<img width="888" height="624" alt="image" src="https://github.com/user-attachments/assets/23f15d68-2e18-4550-8160-752c631659d4" />

Пояснення:
Після запуску клієнт підключається до tracker-ів та peer-ів і починає завантаження даних.

### 1.6 Планування задач (cron)

Для автоматизації задач використовується планувальник cron.

Команда:
```bash
crontab -e
```
Доданий запис:
```bash
* * * * * echo "TEST CRON" >> /home/yaroslava/cron_test.txt
```

<img width="848" height="626" alt="image" src="https://github.com/user-attachments/assets/25021ce0-87b9-453e-b0c3-05bc4b237671" />

---

<img width="613" height="236" alt="image" src="https://github.com/user-attachments/assets/66ad19ff-00fa-4479-a60d-f67491e80e4e" />

Пояснення:
Команда дозволяє автоматично виконувати дію кожну хвилину - у даному випадку запис у файл.

### 1.7 Перегляд зображень у терміналі

Для перегляду зображень використовується програма feh.

Команди:
```bash
wget https://upload.wikimedia.org/wikipedia/commons/3/3f/Fronalpstock_big.jpg -O image.jpg
feh image.jpg
```

<img width="817" height="347" alt="image" src="https://github.com/user-attachments/assets/51641989-6978-4aff-b599-fe9116197da2" />

---

<img width="414" height="33" alt="image" src="https://github.com/user-attachments/assets/92bafc7c-96a7-4f6a-81d9-71b5457ee246" />

---

<img width="902" height="861" alt="image" src="https://github.com/user-attachments/assets/747d10e8-98cc-4018-8dba-6dd0f205812d" />

Пояснення:
Програма відкриває зображення у мінімальному вікні без графічного редактора.

## Пункт 2: Адміністративні інструменти Linux
### 2.1 Робота з текстом (редактори файлів)

Для створення та редагування текстових файлів використовується редактор nano.

Команди:
```bash
sudo apt install nano
nano file.txt
```

<img width="669" height="211" alt="image" src="https://github.com/user-attachments/assets/bcdc58d5-7934-4c17-8b7d-de585bf686c4" />

---

<img width="910" height="163" alt="image" src="https://github.com/user-attachments/assets/053b2d49-f93e-4ad9-aab0-224d7046c1db" />

Пояснення:
Редактор дозволяє вводити, змінювати та видаляти текст у файлі.

Перевірка:
```bash
cat file.txt
```

<img width="442" height="143" alt="image" src="https://github.com/user-attachments/assets/64c3147c-c480-4a12-bd9d-116758c2359d" />

Видалення файлу:
```bash
rm file.txt
```

<img width="435" height="103" alt="image" src="https://github.com/user-attachments/assets/2cf992a8-1bb9-476a-8fce-a64c948d64b3" />

### 2.2 Моніторинг системи

Для моніторингу процесів та ресурсів системи використовується htop.

Команда:
```bash
sudo apt install htop
htop
```

<img width="890" height="494" alt="image" src="https://github.com/user-attachments/assets/01170f9e-cccc-4882-b9e4-ce3ce2f175ec" />

---

<img width="932" height="756" alt="image" src="https://github.com/user-attachments/assets/b33ed016-c428-4761-8151-c1a0c4914412" />

Пояснення:
Програма відображає всі процеси системи, використання CPU, RAM та дозволяє керувати процесами (завершення, пошук тощо).

Альтернатива:

```bash
top
```

<img width="902" height="727" alt="image" src="https://github.com/user-attachments/assets/f0a30c21-d1a1-48d4-ac1c-e367aaebecad" />

## Пункт 3: Пасхалки Linux (розважальні команди)

У Linux існують додаткові утиліти, які не є критично важливими для роботи системи, але демонструють її можливості у розважальному форматі.

### 3.1 Паровоз (sl)

```bash
sudo apt install sl
sl
```

Пояснення:
На екрані з’являється анімація паровоза. Це “жартівлива” утиліта, яка реагує на часту помилку введення ls як sl.

### 3.2 Корова, що говорить (cowsay)

```bash
sudo apt install cowsay
cowsay "Hello Yaroslava"
```

<img width="892" height="569" alt="image" src="https://github.com/user-attachments/assets/e9f43cfb-cfa5-4faf-ad52-dbdf055c05a0" />

---

<img width="564" height="242" alt="image" src="https://github.com/user-attachments/assets/db60b17c-4339-4504-9158-50433d3ad1e0" />

Пояснення:
Програма виводить текст у вигляді “мовлення” ASCII-корови.

### 3.3 Matrix-ефект 

```bash
sudo apt install cmatrix
cmatrix
```

<img width="874" height="556" alt="image" src="https://github.com/user-attachments/assets/df8b32d4-aeb5-42f5-9b62-7faa79875c05" />

---

<img width="370" height="40" alt="image" src="https://github.com/user-attachments/assets/327c91eb-7d24-4987-8845-7918f3210108" />

---

<img width="918" height="749" alt="image" src="https://github.com/user-attachments/assets/0b2baba6-3fb6-4459-8ebd-2dc847e9169f" />

Пояснення:
На екрані відображається анімація “падаючих символів”, як у фільмі Matrix.

### 3.4 Кольоровий текст (lolcat + figlet)
```bash
sudo apt install lolcat figlet
echo "Hello Yaroslava" | lolcat
figlet "Linux" | lolcat
figlet "Yaroslava" | lolcat
```
<img width="914" height="682" alt="image" src="https://github.com/user-attachments/assets/ae6be3e8-2814-4d38-b245-6aa0412792a2" />

---

<img width="880" height="632" alt="image" src="https://github.com/user-attachments/assets/1340fff7-7a16-4280-9f19-88ed3d8b370d" />

---

<img width="616" height="48" alt="image" src="https://github.com/user-attachments/assets/e0513d93-6b45-41a1-bc18-1b47671a388f" />

---

<img width="573" height="342" alt="image" src="https://github.com/user-attachments/assets/60d0856d-ee94-4f33-a832-2fb54ae2f8a3" />

Пояснення:
- figlet створює великий ASCII-текст, а lolcat додає кольори.
- Використання | демонструє передачу даних між командами.

## Conclusion

In this work, the capabilities of the Linux operating system without a graphical user interface were explored. It was demonstrated that most common tasks, such as file management, web browsing, email handling, multimedia playback, torrent downloading, task scheduling, and image viewing, can be successfully performed using only terminal-based tools.

Additionally, essential administrative utilities for text editing and system monitoring were studied, showing how efficiently system resources and processes can be managed from the command line.

Finally, several interactive and entertaining terminal applications were tested, highlighting the flexibility and versatility of the Linux environment.

Overall, this work confirms that the Linux terminal provides powerful and efficient tools for both practical system administration and user interaction, even in resource-limited environments.
