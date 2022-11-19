# LR6
Лабораторная работа №6
Певым шагом мы создаем копию репозитория https://github.com/Kurtyanik/LR6/ в личном хранилище.

![200065624-f956e2eb-c260-442a-8209-e93db56d0b59](https://user-images.githubusercontent.com/64597960/202860025-59a426ec-4c9b-435f-83fa-0a1379a5d3b8.jpg)
Затем настраиваем клиент git, вводим имя пользователя и email.

Комманды: git config --global user.name ; git config --global user.emai
![Screenshot_2](https://user-images.githubusercontent.com/64597960/202860077-11e8e2ea-9f5a-4561-bb26-9c2684b54eaa.png)


Клонируем удалённый репозиторий на компьютер.

Комманда: git clone.

![Screenshot_3](https://user-images.githubusercontent.com/64597960/202860103-9a1601d5-aeaf-4830-9930-d816e6c6c5ba.png)

Проверяем, что при клонировании репозитория, все файлы из удаленного репозитория перешли в локальный.

Команда: git pull.

![Screenshot_5](https://user-images.githubusercontent.com/64597960/202860124-7836e24c-145c-4802-b33c-7ceb0a6f355c.png)

Добавляем файл через интерфейс GitHub.

Нажимаем на кнопку Add file, затем на Create new file.

![Screenshot_1](https://user-images.githubusercontent.com/64597960/202860172-e01a826e-3f4e-4943-bfe8-3d08652ed340.jpg)

С помощью появившегося интерфейса вводим название файла и его содержимое.

![Screenshot_2](https://user-images.githubusercontent.com/64597960/202860199-f90ac502-dcc7-4edc-9764-694b1fe1209c.jpg)

Прописываем комментарий к коммиту и соответственно делаем сам коммит
![Screenshot_3](https://user-images.githubusercontent.com/64597960/202860268-d9e4e443-12aa-4619-a631-9ee3a1095254.jpg)

В итоге файл появляется в репозитории на GitHub
![Screenshot_6](https://user-images.githubusercontent.com/64597960/202860284-f89916b0-9957-48e2-8b43-2ef394200991.png)

Поддтягиваем изменения с удаленного репозитория в локальный.

Комманда: git pull.

![Screenshot_7](https://user-images.githubusercontent.com/64597960/202860311-56aae202-75ac-4515-900c-2c22506aa20e.png)

Посмотрим коммиты веток

Коммиты ветки master. Комманда: git log.
![Screenshot_8](https://user-images.githubusercontent.com/64597960/202860326-6e1ba24b-5d1a-4141-9923-2fd8033f370c.png)

Переходим на вторую ветку branch1. Команда: git checkout branch1

![Screenshot_9](https://user-images.githubusercontent.com/64597960/202860360-219e8d3f-e42e-4a64-b5fe-32e3754a7f1e.png)

Коммиты ветки branch1. Комманда: git log
![Screenshot_10](https://user-images.githubusercontent.com/64597960/202860374-1759eebe-3e5b-475b-a129-bc31e55ba261.png)

Подробно рассмотрим коммиты ветки branch1. Комманда: git log -p.
![Screenshot_11](https://user-images.githubusercontent.com/64597960/202860396-0e54c18c-38ae-45e3-b5bb-eebb4708e110.png)

Возвращаемся обратно на ветку master. Команда: git checkout master.
![Screenshot_12](https://user-images.githubusercontent.com/64597960/202860408-0430b888-8a62-4e15-becd-ebbea50a0626.png)

Выполняем слияние ветки branch1 в ветку master. Комманда: git merge branch1.
![Screenshot_13](https://user-images.githubusercontent.com/64597960/202860424-b1a553b8-30eb-4187-bc72-9e90ae66f289.png)

Разрешаем возникший конфликт: в теории конфликт возник из-за того, что файл mergefile.txt не отслеживается. Добавим его с помощью команды git add, после чего проверим с помощью git status
![Screenshot_15](https://user-images.githubusercontent.com/64597960/202860559-e28cddf8-a3d7-41aa-bfce-93511d90cc75.png)

![Screenshot_14](https://user-images.githubusercontent.com/64597960/202860535-6ae53645-2721-45b9-9780-9983e7d3a49f.png)

Создаем коммит. Команда: git commit -m "merge conflict of branch1->master resolved".
![Screenshot_16](https://user-images.githubusercontent.com/64597960/202860573-aaa7a7b3-cf1c-4ef7-a489-73e74e89ce1a.png)

Пушим (отправляем) наши локальные изменения в удаленный репозиторий. Команда: git push.
![Screenshot_17](https://user-images.githubusercontent.com/64597960/202860585-55227821-bfcc-40cd-9b00-0c41ed1b13f0.png)

Удаляем (локально) побочную ветку после успешного слияния. Удаляем ветку branch1 локально. Команда: git branch -d branch1.
![Screenshot_18](https://user-images.githubusercontent.com/64597960/202860620-7d8d5aa8-2f08-4010-9800-3da6e680fe60.png)

Проверяем, что локальная ветка удалена. Команда: git branch -a
![Screenshot_19](https://user-images.githubusercontent.com/64597960/202860640-52ee1be4-f230-41b1-b7f4-49d46ad73260.png)

Добавляем (папку и файлы) изменения и фиксируем их (коммитим). Каждому изменения приписываем комментарий. Создаем папку и переходим в нее. Команды: mkdir changes; cd changes/.
![Screenshot_20](https://user-images.githubusercontent.com/64597960/202860653-83a644c4-9c70-493f-a529-71e3d45cbd53.png)

Создаем файл, соержащий в себе данные о папке. Команда: echo "package LR6.changes;" > package-info.java.
![Screenshot_21](https://user-images.githubusercontent.com/64597960/202860672-e93c9afb-9cdd-4a02-b3c6-b54b6c7a179a.png)

Добавляем файл в отслеживаемые. Команда: git add package-info.java.
![Screenshot_22](https://user-images.githubusercontent.com/64597960/202860690-f7f2f5e6-b364-4da5-8741-cc8301e36896.png)

Создаем коммит. Команда: git commit -m "added new directory plus package-info".
![Screenshot_23](https://user-images.githubusercontent.com/64597960/202860704-dab379b2-9f42-4152-8986-4778d8c885ca.png)

Создаем пустой файл. Команда: echo "" > empty.txt.
![Screenshot_24](https://user-images.githubusercontent.com/64597960/202860719-75986447-7443-4492-a0f3-64af3b95d254.png)

Добавляем файл в отслеживаемые. Команда: git add empty.txt.
![Screenshot_25](https://user-images.githubusercontent.com/64597960/202860731-56ec6e75-c974-40f4-896c-79af979355bf.png)

Создаем коммит. Команда: git commit -m "empty.txt added"
![Screenshot_26](https://user-images.githubusercontent.com/64597960/202860741-d7398494-9565-42cf-8c1e-c1c44f4e2fdc.png)

Сделаем откат последнего коммита. Найдем идентификатоор последнего коммита. Команда: git log. После нахождения его id прописываем его в команду git revert. После чего получаем такое сообщение:
![Screenshot_27](https://user-images.githubusercontent.com/64597960/202860883-cda8e114-fa46-4073-9fa7-5a276b04fc22.png)

Отправка коммитов. Команда: git push.
![Screenshot_28](https://user-images.githubusercontent.com/64597960/202860909-c19aebf8-dfb8-4291-a947-7b3b4be19a38.png)

Проверяем, что все запушили. Команда: git status.
![Screenshot_29](https://user-images.githubusercontent.com/64597960/202860930-60ed3296-80b8-46a0-8e75-88d7dca8f681.png)

Создаем ветку для отчёта. Создаем ветку report. Комманда: git branch report.
![Screenshot_30](https://user-images.githubusercontent.com/64597960/202860945-175af024-0e91-470a-9e3e-8c940eedaaa4.png)

Переходим на ветку report. Команда: git checkout report.
![Screenshot_31](https://user-images.githubusercontent.com/64597960/202860953-ed86fa60-805c-4a69-afef-f633ab9cb829.png)

Создаем пустой файл отчета — README.md. Команда: echo "" > READEME.md.
![Screenshot_32](https://user-images.githubusercontent.com/64597960/202860956-8655cbaa-d616-4af4-bfea-c7a4d080ce3c.png)

Добавляем отчет в систему контроля версий. Команда: git add README.md.
![Screenshot_33](https://user-images.githubusercontent.com/64597960/202860974-209a1de5-5527-4a18-9f15-388719daad38.png)

Получаем итоговую историю операций в форматированном виде (сокращённый хэш - дата, имя автора : комментарий). Комманда: git log --pretty=format:"%h - %ar, %an : %s".
![Screenshot_4](https://user-images.githubusercontent.com/64597960/202861125-815c2e09-2539-46e1-ae3f-f003a0d15140.jpg)

Оформляем отчёт в файле README.md. После редактирования отчета, его нужно будет сохранить и закоммитить git commit. В конце работы необходимо будет запушить все локальные изменения в сетевое хранилище GitHub командой git push.

Все снимки экрана, используемые в этом отчете находятся в папке screenshots.


