## Как создать ветку 

   1) Открыть терминал
   2) Находясь в репозитеории ввести команду *git branch namebranch* - создание новой ветки
   3) Командой *git branch --all*  проверить наличие веток в репозитории

# Как переключаться между ветками 

   1) Командой *git log* - можно посмотреть в какой конкретно ветке вы находитесь 
   
     *Пример:* 
     *username@MacBook-Pro-username namerepozitories % **git log***
     *commit 48a98fd99911c3560384f0811bda0185d01f6e4b (**HEAD -> main, origin/main, origin/HEAD**)*

   1) Командой *git checkout namebranch* переключиться в ветку с названием **namebranch**
   2) Снова командой  *git log* посмотрим в какой ветке мы находимся
   
     *Пример:* 
     *username@MacBook-Pro-username namerepozitories % **git log***
     *commit 48a98fd99911c3560384f0811bda0185d01f6e4b (**HEAD -> example_1, origin/main, origin/HEAD, main**)*

# Как отправить ветку на сервер

   1) проверить что вы находить в ветке, которую хотите отправить командой *git log**
   2) Командой **git add .** *(подготовка для комита всех файлов)* или 
               **git add namefile** *(подготовка для комита выбранного файла)* подготовить файлы для комита
   3) Закомитить файл(-лы) *git commit -m "your_commit"* 
   4) Отправить изменения на сервер: *git push*
