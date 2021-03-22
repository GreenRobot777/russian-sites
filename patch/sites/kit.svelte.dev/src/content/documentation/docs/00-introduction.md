---
title: Введение
---

###   Важное замечание  

> SvelteKit ещё в ранней стадии разработки, и некоторые вещи могут поменяться, когда мы дойдём до релиза 1.0. Этот документ всё ещё дорабатывается. Если у вас появятся вопросы, обратитесь за помощью в русскоязычный [канал в Telegram](https://t.me/sveltejs).
>
> Прочтите [руководство по миграции ](migrating) для помощи при переходе с Sapper.

### Что такое SvelteKit?

SvelteKit — это фреймворк для создания невероятно производительных web-приложений. Прямо сейчас вы смотрите на одно из них! 

Вот два наших основных принципа:

* Каждая страница вашего приложения является компонентом [Svelte](https://ru.svelte.dev)
* Вы создаёте новые страницы путём добавления компонентов в директорию `src/routes` вашего проекта. Они будут рендериться на сервере, так что время первой загрузки приложения для пользователя будет максимально быстрым, а уже затем клиентское приложение возьмёт на себя бразды правления.

Создание приложения, соответствующего лучшим современным трендам вроде разделения кода, поддержки автономного режима, гидрации — чрезвычайно сложная задача. SvelteKit делает все эти скучные вещи за вас, чтобы вы могли сконцентрироваться только на творческой части.

Чтобы понять это руководство, знать Svelte не обязательно, но желательно. Если коротко, Svelte — это фреймворк, который компилирует ваши компоненты в высокооптимизированный ванильный JavaScript. Прочтите [вводную статью в блоге](https://ru.svelte.dev/blog/svelte-3-rethinking-reactivity) и [учебник](https://ru.svelte.dev/tutorial), чтобы узнать о нём побольше.

### Начало работы

Самый простой способ начать создавать приложение SvelteKit — запустить команду `npm init`:

```bash
mkdir my-app
cd my-app
npm init svelte@next
npm install
npm run dev
```

Это создаст новый проект в каталоге `my-app`, установит его зависимости и запустит сервер на [localhost:3000](http://localhost:3000). Попробуйте поредактировать файлы, чтобы увидеть, насколько всё просто работает — быть может вам вообще не понадобиться читать оставшуюся часть этого руководства!