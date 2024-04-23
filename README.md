Команды git

pwd - Командная строка выведет путь к папке, в которой вы сейчас находитесь.

cd ~ - перейти к домашней директории

ls - Вывести содержимое директории

cd 'имя папки' - Сменить директорию

cd .. - переход на уровень выше

touch - создать файл

mkdir - создать директорию

mkdir -p - создать структуру директорий

mkdir ~ - создать директорию внутри домашней

touch ../../имя файла - создаст файл в родительской директории

cp - копирование файлов

cp что копируем куда копируем (cp popa.txt nedir/)

cp data.txt ~ - копируем в дом директ

mv - перемещение файлов и папок

mv имя файла путь (mv popa.txt firpro/zalupa
)

cat - чтение файла

cat имя файла

rm name file - удаление файла

rmdir - удалить папку если пуста

rm -r имя папки - удалить все данные в этой папке

&& - несколько команд сразу
$ mkdir second-project && cd second-project && touch index.html style.css
# создаём папку second-project,
# переходим в папку second-project
# и создаём в ней два файла: index.html и style.css 

буква + двойной ТАВ - список всех команд на эту букву

cd ~/doubleTab - список всех доступных директорий

git version - версия git

$ git config --global user.name "User Namovich" 
# имя или ник нужно написать латиницей и в кавычках

$ git config --global user.email username@yandex.ru
# здесь нужно указать свой настоящий email 

$ git config --list - вывод конфига гит

Сделать папку репозиторием — git init

«Разгитить» папку, если что-то пошло не так, — rm -rf .git

Разберём подробнее, что такое -rf:
ключ -r (от англ. recursive — «рекурсивно») позволяет удалять папки вместе с их содержимым;
ключ -f (от англ. force — «заставить») избавит вас от вопросов вроде «Вы точно хотите 
удалить этот файл? А этот? И этот тоже?».

git status - состояние репы

Команда git status выведет:
название текущей ветки: On branch master или On branch main;
сообщение о том, что в репозитории ещё нет коммитов: No commits yet;
сообщение, которое говорит: «чтобы что-нибудь закоммитить (то есть зафиксировать), 
нужно сначала это создать» — nothing to commit (create/copy files and use "git add" to track).

Состояние untracked значит, что Git ещё не хранит информацию о версиях файла
и не может отследить, как он изменялся.

Мы хотим отслеживать состояние обоих, поэтому можем использовать команду
git add --all (от англ. add — «добавить» + от англ. all — «всё»). Ключ, или флаг, --all 
позволяет подготовить к сохранению все файлы в репозитории.

git add . # добавить всю текущую папку

$ git commit -m 'Мой первый коммит!' - добавить коммит
git 

Сделать коммит» значит сохранить текущую версию файла. 

Если провести аналогию, команду git add можно сравнить с добавлением товаров в корзину
в интернет-магазине, а коммит — с оформлением и оплатой заказа.

Коммит — это одна из основных сущностей в Git (и в других системах контроля версий). 
Коммит гарантирует, что изменения будут сохранены в истории и при необходимости 
к ним можно будет «откатиться». Это как если бы вы могли выполнить операцию Ctrl+Z 
для целой папки (репозитория).

Коммит (по названию команды git commit) — это по сути список файлов с их контентом.

Сначала команда git add сообщает Git, какие именно файлы нужно сохранить и какую их версию.
Затем с помощью команды git commit происходит само сохранение. 

git log - история изменений

ls -la .ssh/ # вывели список созданных ключей 

ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub" - 
Для генерации SSH-пары

ls -a ~/.ssh - проверка ген ключейьл

# скопировать содержимое ключа в буфер обмена:git
$ clip < ~/.ssh/id_rsa.pub
# для ed25519:
$ clip < ~/.ssh/id_ed25519.pub 

$ ssh -T git@github.com - проверка правильности ключа

Привязать удалённый репозиторий к локальному — git remote add
git remote add origin git@github.com:%ИМЯ_АККАУНТА%/first-project.git 

На Windows (в Git Bash) и Linux для этого используется сочетание Ctrl+Shift+V

Убедиться, что репозитории связаны, — git remote -v

Отправить изменения на удалённый репозиторий — git push

shift + ins - вставить текст в bash

Чтобы другие пользователи, а также потенциальные клиенты или работодатели могли понять,
 что представляет собой проект, его нужно описать. Такое описание принято указывать в файле README.md
