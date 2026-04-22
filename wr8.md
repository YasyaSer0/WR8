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

sudo apt install mc
mc

<img width="829" height="571" alt="image" src="https://github.com/user-attachments/assets/b5e09443-74eb-47b2-b43a-316d8fa4bf10" />

<img width="821" height="585" alt="image" src="https://github.com/user-attachments/assets/49eb665e-e4aa-42b0-9d9d-9adf6e9b2c60" />

Пояснення:
Після запуску відкривається двопанельний інтерфейс, який дозволяє навігацію по файловій системі без графічної оболонки.

### 1.2 Перегляд веб-сторінок у терміналі

Для перегляду веб-сторінок використовується текстовий браузер lynx. Він відображає сайти у вигляді тексту та дозволяє навігацію за допомогою клавіатури.

Команди:
 
sudo apt install lynx
lynx https://wikipedia.org


<img width="668" height="234" alt="image" src="https://github.com/user-attachments/assets/b7f1f9c5-b8b8-4524-a3cd-77c3f581f2c3" />

<img width="795" height="537" alt="image" src="https://github.com/user-attachments/assets/a1791719-3911-4872-974f-b0917f889abf" />

<img width="808" height="554" alt="image" src="https://github.com/user-attachments/assets/6784cd1f-cb44-4e7b-81d3-5645280f4a88" />

Пояснення:
Браузер завантажує сторінку та відображає її у терміналі без графічних елементів.


### 1.3 Перегляд електронної пошти в терміналі

Для роботи з електронною поштою використовуються пакети mailutils та mutt.

Команди:

sudo apt install mailutils mutt
echo "Hello from terminal" | mail -s "Test" yaroslava
mutt

<img width="830" height="522" alt="image" src="https://github.com/user-attachments/assets/d465e44c-0ae1-4816-a332-132db1b47dc0" />

Пояснення:
Команда mail дозволяє надсилати листи, а mutt — переглядати та керувати електронною поштою в терміналі.

### 1.4 Відтворення музики через термінал

Для відтворення аудіофайлів використовується консольний плеєр cmus.

Команда:

sudo apt install cmus
cmus

<img width="817" height="537" alt="image" src="https://github.com/user-attachments/assets/5adc1da1-62a2-4b9b-bf2a-d0248abc197b" />

<img width="812" height="597" alt="image" src="https://github.com/user-attachments/assets/7867c897-05d0-4a49-8065-c2fda157a976" />

<img width="814" height="363" alt="image" src="https://github.com/user-attachments/assets/eba1a0be-95cb-4019-bf47-1bd74a1907c0" />

<img width="833" height="571" alt="image" src="https://github.com/user-attachments/assets/3c400378-a15f-43a1-8c7b-4e5a9b768852" />

<img width="875" height="125" alt="image" src="https://github.com/user-attachments/assets/c8a49073-f01c-4084-bcf1-cc76aa5284e7" />

Пояснення:
Після запуску відкривається інтерфейс медіаплеєра, який дозволяє керувати музикою без графічного середовища.

### 1.5 Завантаження торрентів через термінал

Для роботи з торрентами використовується transmission-cli. Він дозволяє завантажувати файли через magnet-посилання або .torrent файли.

Команда:

sudo apt install transmission-cli
transmission-cli "magnet:?xt=urn:btih:..."

<img width="826" height="534" alt="image" src="https://github.com/user-attachments/assets/b841a10a-c3db-4b1e-b573-cc719f5ed7ba" />

<img width="824" height="534" alt="image" src="https://github.com/user-attachments/assets/39ea3163-bbdc-441b-93b3-467ce04b3d7e" />

Пояснення:
Після запуску клієнт підключається до tracker-ів та peer-ів і починає завантаження даних.

### 1.6 Планування задач (cron)

Для автоматизації задач використовується планувальник cron.

Команда:

crontab -e

Доданий запис:

* * * * * echo "TEST CRON" >> /home/yaroslava/cron_test.txt

Пояснення:
Команда дозволяє автоматично виконувати дію кожну хвилину — у даному випадку запис у файл.

### 1.7 Перегляд зображень у терміналі

Для перегляду зображень використовується програма feh.

Команди:

wget https://upload.wikimedia.org/wikipedia/commons/3/3f/Fronalpstock_big.jpg -O image.jpg
feh image.jpg

Пояснення:
Програма відкриває зображення у мінімальному вікні без графічного редактора.

## Пункт 2: Адміністративні інструменти Linux
### 2.1 Робота з текстом (редактори файлів)

Для створення та редагування текстових файлів використовується редактор nano.

Команди:

sudo apt install nano
nano file.txt

Пояснення:
Редактор дозволяє вводити, змінювати та видаляти текст у файлі.

Перевірка:

cat file.txt

Видалення файлу:

rm file.txt
### 2.2 Моніторинг системи

Для моніторингу процесів та ресурсів системи використовується htop.

Команда:

sudo apt install htop
htop

Пояснення:
Програма відображає всі процеси системи, використання CPU, RAM та дозволяє керувати процесами (завершення, пошук тощо).

Альтернатива:

top
## Пункт 3: Пасхалки Linux (розважальні команди)

У Linux існують додаткові утиліти, які не є критично важливими для роботи системи, але демонструють її можливості у розважальному форматі.

### 3.1 Паровоз (sl)
sudo apt install sl
sl

Пояснення:
На екрані з’являється анімація паровоза. Це “жартівлива” утиліта, яка реагує на часту помилку введення ls як sl.

### 3.2 Корова, що говорить (cowsay)
sudo apt install cowsay
cowsay "Hello Yaroslava"

Пояснення:
Програма виводить текст у вигляді “мовлення” ASCII-корови.

### 3.3 Matrix-ефект (заміна Star Wars)
sudo apt install cmatrix
cmatrix

Пояснення:
На екрані відображається анімація “падаючих символів”, як у фільмі Matrix.
