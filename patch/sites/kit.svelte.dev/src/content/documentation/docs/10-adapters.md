---
title: Адаптеры
---

Прежде чем развернуть готовое приложение SvelteKit на сервере или сервисе, его необходимо адаптировать под то окружение, в котором оно будет работать. Адаптеры - это небольшие плагины, которые берут собранное приложение и выдают оптимизированную для конкретной платформы сборку.

Например, чтобы запустить приложение как простой Node-сервер, необходимо использовать адаптер `@sveltejs/adapter-node`:

```js
// svelte.config.js
import node from '@sveltejs/adapter-node';

export default {
	kit: {
		adapter: node()
	}
};
```

В таком случае, команда [`svelte-kit build`](#svelte-kit-cli-svelte-kit-build) сгенерирует приложение Node внутри папки `build`, которое можно запустить автономно. Также адаптерам можно передать параметры , например настроить выходной каталог в `adapter-node`:

```diff
// svelte.config.js
import node from '@sveltejs/adapter-node';

export default {
	kit: {
-		adapter: node()
+		adapter: node({ out: 'my-output-directory' })
	}
};
```

Для бессерверных платформ существует множество официальных адаптеров...

- [`adapter-begin`](https://github.com/sveltejs/kit/tree/master/packages/adapter-begin) — для [Begin](https://begin.com)
- [`adapter-cloudflare-workers`](https://github.com/sveltejs/kit/tree/master/packages/adapter-cloudflare-workers) — для [Cloudflare Workers](https://developers.cloudflare.com/workers/)
- [`adapter-netlify`](https://github.com/sveltejs/kit/tree/master/packages/adapter-netlify) — для [Netlify](https://netlify.com)
- [`adapter-vercel`](https://github.com/sveltejs/kit/tree/master/packages/adapter-vercel) — для [Vercel](https://vercel.com)

...и другие:

- [`adapter-node`](https://github.com/sveltejs/kit/tree/master/packages/adapter-node) — для создания автономных приложений Node
- [`adapter-static`](https://github.com/sveltejs/kit/tree/master/packages/adapter-static) — для пререндера приложения и получения статического сайта

> API адаптеров всё ещё находится в разработке и, вероятно, изменится до версии 1.0.
