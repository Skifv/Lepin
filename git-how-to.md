<center><b>Создание ssh ключа</b></center>

*  Создается в папке `C:\Users\Skif\.ssh`
*  Есть ли ключи? `ls ~/.ssh`
*  Создать новый ключ `ssh-keygen -t ed25519 -C "lepin.vd@phystech.edu"`
*  Просмотреть приватный ключ `cat ~/.ssh/id_ed25519` 
*  Просмотреть приватный ключ  `cat ~/.ssh/id_ed25519.pub`

<center><b>Как добавить ключ в аккаунт на GitHub</b></center>

Наведите на вашу иконку в правом верхнем углу, выберите пункт `Settings`, найдите слева пункт `SSH and GPG keys`, нажмите на кнопку `New SSH key`.

Откроется окно, в котором можно ввести название в поле `Title`. В поле `Key` нужно вставить публичный ключ. Его можно получить при помощи команды на вашем компьютере `cat ~/.ssh/id_ed25519.pub`. Скопируйте ключ из терминала, и вставьте его, после чего нажмите `Add SSH key`.

После этого ключ должен отражаться в списке ключей. Чтобы проверить правильно ли вы всё сделали вызовите команду:

`ssh -T git@github.com`

<center><b>Клонирование репозитория</b></center>

Нажмите на кнопку `Code`. В ней выбираем вкладку `SSH`. В строке ниже есть строчка, которая начинается с `git@github.com...` — это адрес вашего репозитория по протоколу SSH. Клонировать репозиторий можно при помощи команды, где в `<url>` вставьте адрес репозитория: 

```git
git clone <url>
```

После этого в текущей папке появится папка с названием вашего репозитория. Отлично!

