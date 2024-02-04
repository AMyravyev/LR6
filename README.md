# LR6
Лабораторная работа №6

**Цель работы:** изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

**Ход работы**

1. Создать аккаунт на сайте GitHub.

![reg](https://github.com/Gauliux/half-interval/assets/158781390/93670a06-f981-4beb-a5ff-fda04a0f2de6)

2. Сделать копию в личное хранилище из https://github.com/Kurtyanik/LR6.

![fork](https://github.com/Gauliux/half-interval/assets/158781390/a7e3c898-81ec-442a-a883-f73cec1f673a)

3. Установить Git.

![3](https://github.com/Gauliux/half-interval/assets/158781390/ceafd72b-d6a5-4f42-8388-7c3b98f08eeb)

4. После установки настроить клиент git, введя имя пользователя (Группа Фамилия И.О.) и email.

Изменение имени пользователя:
```sh
git config --global user.name "4217 Муравьёв А.С."
```

![1](https://github.com/Gauliux/half-interval/assets/158781390/79e53427-bc2a-40f1-a2af-f7581b940670)

Изменение электронной почты пользователя:
```sh
git config --global user.email "myravyevalexander@gmail.com"
```

![2](https://github.com/Gauliux/half-interval/assets/158781390/d8931a56-ef6c-4d79-aef2-14ccea034886)

5. Клонировать свой личный удалённый репозиторий на компьютер.

```sh
git clone https://github.com/AMyravyev/LR6.git
```

![4](https://github.com/Gauliux/half-interval/assets/158781390/faeea94d-e612-42d5-bdc6-da98b2a699cf)

6. Добавить файл через интерфейс GitHub. Подтянуть изменения в локальный репозиторий.

Добавление файла в репозиторий через интерфейс GitHub:

![5](https://github.com/Gauliux/half-interval/assets/158781390/b6906831-7549-470f-ba89-c690d8e45986)

Загрузка изменений на локальный репозиторий:
```sh
git pull
```

![6](https://github.com/Gauliux/half-interval/assets/158781390/dfd6a004-89a9-4e7d-8c55-ad4d38980a0e)

7. Получить историю операций для каждой из веток.

Для ветки master: ``` git log ```

![7](https://github.com/Gauliux/half-interval/assets/158781390/a84a050c-b7e8-44c6-b6e0-655a33e5b661)

Для ветки bracnh1: ``` git log origin/main ```

![8](https://github.com/Gauliux/half-interval/assets/158781390/9f30b495-e1a3-4871-bc03-3d9ea8d90bad)

8. Просмотреть последние изменения.

```sh
git status
```

![9](https://github.com/Gauliux/half-interval/assets/158781390/3804d394-bffe-4945-bba0-64938a5470b7)

9. Выполнить слияние в ветку master, разрешив конфликт (можно использовать специальные редакторы или графический интерфейс git).

Слияние ветки master с branch1:
```sh
git merge origin/branch1
```

![10](https://github.com/Gauliux/half-interval/assets/158781390/ab40b2ff-949c-474c-b1ca-a8f22db010bc)

Разрешение конфликта с помощью текстового редактора:

![11](https://github.com/Gauliux/half-interval/assets/158781390/92960e73-7a41-43b4-a525-86e0b2a8d069)
![12](https://github.com/Gauliux/half-interval/assets/158781390/cba88e9f-fcee-4bc1-9b6e-de5773bcd134)

Проверка состояния:
```sh
git status
```

![13](https://github.com/Gauliux/half-interval/assets/158781390/13750edc-2cf8-412c-9989-7ac8e0ed2b07)

Запись изменений:
```sh
git add mergefile.txt
git commit -m"conflict resolutuin"
```

![14](https://github.com/Gauliux/half-interval/assets/158781390/172d1348-51c0-4321-911f-032458226c92)

11. Удалить побочную ветку после успешного слияния.

```sh
git branch -D branch1
```

![15](https://github.com/Gauliux/half-interval/assets/158781390/b6e4c168-60c8-4a4d-ab0f-b7db608502d5)

12. Сделать изменения и зафиксировать их, оставляя комментарии, несколько раз.

Первое изменение:
```sh
git status
git add .
git commit -m"first change"
```

![16](https://github.com/Gauliux/half-interval/assets/158781390/fddae1fc-648f-451c-a720-b9df12e73403)

Второе изменение:
```sh
git status
git add .
git commit -m"second change"
```

![17](https://github.com/Gauliux/half-interval/assets/158781390/949ac159-ac6d-45c1-a86a-74ada9a47d2a)

Просмотр журнала:
```sh
git log
```

![18](https://github.com/Gauliux/half-interval/assets/158781390/51170583-0a01-43ab-98b5-31976fd4b823)

14. Сделать откат коммита.

```sh
git reset --hard HEAD~
```

![19](https://github.com/Gauliux/half-interval/assets/158781390/9e6da9b1-4b6f-4482-b5fc-f85ff25524ef)

Журнал изменений до:
```sh
git log
```

![18](https://github.com/Gauliux/half-interval/assets/158781390/51170583-0a01-43ab-98b5-31976fd4b823)

Журнал изменений после:
```sh
git log
```

![20](https://github.com/Gauliux/half-interval/assets/158781390/00bd0f13-2bc1-441b-a94b-87b29121ed82)

15. Создать ветку для отчёта.

```sh
git branch report
git branch
git checkout report
```

![21](https://github.com/Gauliux/half-interval/assets/158781390/c24ce696-62b7-4593-83d5-fc0d513bce40)

16. Получить историю операций в форматированном виде (сокращённый хэш + дата + имя автора + комментарий). Добавить её в отчёт и сделать финальную фиксацию изменений.

```sh
git log --pretty=format:"%h %cd - %an : %s"
```

![last](https://github.com/Gauliux/half-interval/assets/158781390/af3adf7f-aeed-4c88-ae9b-436c950bd7e9)
