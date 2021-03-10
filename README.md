# Skillfactory-module-d9_11-YeSergey (API блога - Python, Django, djangorestframework)
Для работы с приложением:
1. Скачайте приложение.
2. В cmd ввести: cd путь до папки с проектом;
3. Создать окружение: python –m venv имя_окружения;
4. Войти в окружение: имя_окружения\Scripts\activate.bat
5. Установить библиотеки: pip install -r requirements.txt;
6. Создан сюперюзер: с логином pws_admin и паролем sf_password
7. Запустить сервер: python manage.py runserver.

На HEROKU создан сюперюзер: с логином pws_admin и паролем sf_password.
https://vw-9-11.herokuapp.com/
https://vw-9-11.herokuapp.com/categories/
https://vw-9-11.herokuapp.com/admin/

Задание:

API приложение:
Добавить модель "Category". Установить отношение между моделями "Post" и "Category". Для простоты лучше исходить из того, что к посту может относиться только одна категория, но к одной категории может относиться множество постов.
Категория должна быть необязательным параметром поста. При удалении категории у всех связанных постов категория должна становиться равной null, то есть обнуляться.
Добавить категории в API, то есть создать обработчики и сериализаторы (полезно будет освежить память о вложенных связях в DRF).
Маршруты вашего приложения должны быть связаны с обработчиками списка категорий и единичной категорией: https://YOUR_HOST/categories/ и https://YOUR_HOST/categories/<int:pk> соответственно.
При этом на запрос GET по адресу https://YOUR_HOST/categories/ сервер должен отвечать списком всех категорий и входящих в них постов. По запросу POST на этот адрес должна создаваться новая категория, а информация о ней должна возвращаться в качестве ответа сервера с HTTP статусом 201 (created).

На запрос GET по адресу https://YOUR_HOST/categories/<int:pk> сервер должен отображать информацию только об одной категории, id которой был передан в запросе.
