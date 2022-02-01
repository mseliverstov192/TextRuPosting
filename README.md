# TextRuPosting

Requires at least: 4.7  
Tested up to: 5.9  
Requires PHP: 7.2  
Stable tag: 1.0.0  
License: [MIT](LICENSE)  
Tags: textruposting, textru  
Contributors: textru  

Плагин для взаимодействия WP-сайта с биржей контента text.ru

## Description
При работе плагин взаимодействует посредством открытого API с программной платформой [text.ru](https://text.ru).
И в процессе работы отправляет следующие данные:
- токен пользователя, полученный со страницы [https://text.ru/api-check]();
- url сайта;
- идентификатор сайта в системе [text.ru](https://text.ru);
- идентификатор владельца токена в системе [text.ru](https://text.ru);
- IP адрес сервера, на котором располагается ваш сайт;
- другие ранее полученные от text.ru данные - например, идентификаторы заказов, документов;

Плагин получает от программной платформы [text.ru](https://text.ru):
- данные по вашим заказам, для которых при создании заказа указан сайт;
- данные прикреплённых к заказам документов, включая их тексты;
- токен пользователя и идентификатор владельца токена (при указании нового токена или его изменении).

Плагин публикует выбранные документы заказа в черновики Wordpress.

### Изменения, вносимые плагином
При установке плагина создаётся новая таблица базы данных
wp_textru_orders 
для хранения временных данных.
Её структуру можно посмотреть в файле
text.ru.posting.php.

Также добавляются три опции:
- textru_token: токен пользователя, полученный со страницы [https://text.ru/api-check]();
- textru_site_id: идентификатор сайта в системе [text.ru](https://text.ru);
- textru_customer_id: идентификатор владельца токена в системе [text.ru](https://text.ru);

### Принцип работы плагина
При работе плагин взаимодействует посредством открытого API с программной платформой [text.ru](https://text.ru).
И в процессе работы отправляет следующие данные:
- токен пользователя, полученный со страницы [https://text.ru/api-check]();
- url сайта;
- идентификатор сайта в системе [text.ru](https://text.ru);
- идентификатор владельца токена в системе [text.ru](https://text.ru);
- IP адрес сервера, на котором располагается ваш сайт;
- другие ранее полученные от text.ru данные - например, идентификаторы заказов, документов;

Плагин получает от программной платформы [text.ru](https://text.ru):
- данные по вашим заказам, для которых при создании заказа указан сайт;
- данные прикреплённых к заказам документов, включая их тексты;
- токен пользователя и идентификатор владельца токена (при указании нового токена или его изменении).

Плагин публикует выбранные документы заказа в черновики Wordpress.

### Разработка плагина
После внесения изменений в код плагина необходимо пересобрать файлы скриптов и стилей для фронтенда.
Для этого:
- установите dev-зависимости командой
  npm install
- осуществите сборку файлов командой
  npm run build
- для отслеживания изменений в коде в режиме реального времени используйте команду
  npm run watch