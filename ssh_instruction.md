## Как создать ssh ключ на MacOS

1) Открыть терминал
2) Ввести команду: ssh-keygen

   _После этой команды будет сгенерировано два ключа: public and private_

3) В директории _/Users/username/.ssh/_ теперь есть два ключа: *__id_rsa__ (private), __ida_rsa.pub__ (public)*
4) В терминале командой _open .ssh/_ открываем папку, где лежат наши ключи
5) В любом текстовом редакторе открываем файл __ida_rsa.pub__ и копируем содержимое
6) на Github добавляем наш ключ (содержимое файла)

## Как клонировать репозиторий на свой MacOS

*Перед тем как перейти к самому клонированию, нам нужно пройти аутентификацию, чтобы мы могли клонировать репозиторий*

1) Командой ssh-add *.ssh/id_rsa* мы добавляем приватный ключ
2) Проверить список приватнызх ключей можно командой *ssh-add -l*
3) *ssh -T git@github.com* - команда для проверки соединения с сервером GitHub
4) Пример удачного подключения: *Hi ModeratorY! You've successfully authenticated, but GitHub does not provide shell access.*

**А теперь будем клонировать репозиторий:**

1) Через терминал находим ту дерикторию, куда мы будем клонировать наш репозиторий
2) Командой git clone *<ssh_ссылка_репозитория>* клонируем репозиторий к себе на компьютер

**Отправил наш файл на сервер GitHub в наш пустой репозиторий**

1) Файлы, которые мы хотим закинуть на *Github* копируем в наш локальный репозиторий
2) Находясь в дериктории нашего репозитория, вводим команду *git init* чтобы проинициализировать репозиторий
3) Дальше командой *git add .* все файлы, которые мы хотим закинуть на *GitHub*
4) командой *git commit -m "комментарий"* делаем первый комит
5) Теперь для того, чтобы *запустить наш репозиторий* на GitHub через терминал, поочерёдно вводим команды:
   **git remote add origin git@github.com:Username/namerepoz.git**
   **git branch -M main**
   **git push -u origin main**

## Заключение

*Теперь мы можем без проблем клонировать, обновлять наш репозиторий и отправлять на него файлы*