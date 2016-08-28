# [Wolf Launcher](https://telegram.me/pika_launcher)
(سورس مخصوص سوپر گپ نیز هست)

**An advanced and powerful launcher cli bot based on [yagop/telegram-bot](https://github.com/yagop/telegram-bot) licensed under the [GNU General Public License](https://github.com/SEEDTEAM/TeleSeed/blob/master/LICENSE)**.


[![https://telegram.me/Telewolf_ch](https://img.shields.io/badge/💬_telegram-channel-green.svg)](https://telegram.me/Telewolf_ch) 

# مزایا

* **آپتایم 99 درصدی ربات شما**
* **! آپتایم 100 درصدی خود ربات لانچر**
* **افزایش دقت ربات آنتی اسپم و آنتی تبلیغ شما**
* **بهبود کیفیت گروه های ربات**
* **!و یا نام های مشابه steady.sh افزایش دقت ربات در ریپلی ها به دلیل حذف عامل آن یعنی**

# توضیحات

خیلی از شما دوستان یک مشکل بزرگ دارید که رباتتون افلاین میشه و خیلی مشکلات ایجاد میکنه و باید بدانید 
! که یه ربات خوب به پلاگین و سورسش نیست ، بلکه به مدت آنلاین بودنش هست 

 این ربات به دلیل اینکه از ورژن سه تله سید ساخته شده و سوپرگروه ساپورت نمی کنه ، خودش هرگز اف نمیشه مگر به خاطر سرور خودتون باشه

* **مرحله اول**

خب اول از همه سورس فایل منیجر تله سید رو نصب کنید
>###**[file-manager-bot](https://www.github.com/telewolf653/server-manager)**
>>حتما ایدی ربات لانچر رو داخلش به عنوان ادمین قرار بدید
>>>این ربات نقش کنترل سرور شما رو داره که ربات لانچر ما به اون وصل میشه
>>>>ربات فایل منیجر را داخل همون یوزر از سرور ران کنید که ربات آنتی اسپمتون داخلش ران هست


* **مرحله دوم** 

به پوشه رباتتون اضافه کنید که نقش یک لانچ رو داشته باشه **[etc](https://telegram.me/luaforyou/6* در این قسمت شما باید یک فایل به نام 

>##[Download etc file](https://telegram.me/luaforyou/6)
>> فایل رو به پوشه اصلی رباتتون اضافه کنید 
>>>اسم یوزر سرور خودتون رو جاش بزارید **serveruser** به جای pika.conf پوشه را باز کنید و داخل فایل 
>>>> !دست نزنید telegrambotpath نکته : به 

**!خیلی از شما به اشتباه فکر میکنید باید به جای این کلمه داخل این پوشه ، اسم پوشه ربات خودتون رو بزارید که کاملا اشتباه هست**

* **مرحله سوم**

:بعد از انجام مراحل بالا ، ترمینال رو باز کنید و دستورات زیر را داخل ترمینال وارد کنید

`cd botfile name`  **botfile name = اسم پوشه اصلی ربات**

>`sed -i "s/serveruser/$(whoami)/g" etc/pika.conf`
>>مثل قبل نام یوزر سرور را قرار دهید ، **serveruser** به جای 

سپس

`sed -i "s_telegrambotpath_$(pwd)_g" etc/pika.conf`

`sudo cp etc/pika.conf /etc/init/`

:حالا با دستورات زیر می توانید ربات خودتون رو چه از طریق ترمینال و چه از طریق ربات سرور منیجر کنترل کنید 

`sudo start pika` _to start pikabot_

`sudo stop pika` _to stop pikabot_

`sudo restart pika` _to restart and make new process for pikabot_

 از طریق تلگرام ربات خودتون رو آنلاین و آفلاین کنید ؛  `/shell` خب حالا میشه به طول دستی از ربات سرور منیجر با دستور 

!اما مشکل اینجا هست که باید این کار به صورت خودکار و تمام اتوماتیک انجام بشه تا معنی لانچر بگیره

* **مرحله چهارم**

:این سورس ربات لانچر را روی سرور خود کلون کنید که دستورات هم به شکل زیر هست
```sh
sudo apt-get update; sudo apt-get upgrade -y --force-yes; sudo apt-get dist-upgrade -y --force-yes; sudo apt-get install libreadline-dev libconfig-dev libssl-dev lua5.2 liblua5.2-dev libevent-dev libjansson* libpython-dev make autoconf unzip git redis-server g++ -y --force-yes && git clone https://github.com/blackwolfadmin/pika_launcher_bot.git && cd pika_launcher_bot && chmod +x launch.sh && ./launch.sh install && ./launch.sh
```

!خب حالا داخل ربات خودتون رو سودو کنید که 99.5 درصد بلد هستید

!اما با این تفاوت که باید خود ربات رو داخل خودش سودو کنید یعنی ایدی ربات لانچر را داخل کافینگ  به عنوان  سودو  قرار دهید

* **مرحله پنجم**

 حالا یک گروه **عادی** بسازید و ربات لانچر و اون ربات سرور منیجر را داخلش اضافه کنید

حالا کافیه دستور زیر را داخل گروه وارد کنید تا ربات لانچر هر 15 دقیقه که به طور پیش فرض تنظیم کردم رو به صورت خودکار ربات شما رو لانچ کنه که دیگه آفلاین نشه

>`/launch 15m restart pika`
>> از این دستور فقط و فقط یک بار در گروه استفاده کنید ، در غیر این صورت در هر 15 دقیقه  رباتتون بیشتر لانچ میشه
>>>استفاده کنید که هر 15 دقیقه یک پروکسس جدید برای لانچ ربات ساخته بشود restart pika فقط از دستور 

**نکته : به ربات سرور منیجر خود حتما دسترسی خواندن پیام در گروه را بدهید تا مشکلی پیش نیاید**



امید وارم براتون مفید باشه و مشکل شما دوستان رو حل کنه 


سوالی داشتید در خدمتم 

موفق باشید
