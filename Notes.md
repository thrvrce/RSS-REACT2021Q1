## Лекции

1. [Лекция по webpack 5](https://www.youtube.com/watch?v=AoPDBBbInzc&feature=youtu.be&ab_channel=RollingScopesSchool)
	- [Презентация](https://slides.com/klmmm/webpack/fullscreen)
	- [Пример кода](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbWp0NzVKM3BCOU5BV1FvaXJBWHljNDNVLWlYQXxBQ3Jtc0tsOV82dDVaaF9DMG5TX2pHUThJME9ROUg5MnFUTUdqZUtvMVdaM2E0aEI5ZDVzVjYtUm8wSVNOX1BidU90MTJ0SjJIcHJ1TjJlTXVkMkhkdWFUbThfb0NGcTNEUkZJSUxCYTJLY0c1dkxpeG5GRy1paw&q=https%3A%2F%2Fgithub.com%2Fklimenkomaksim%2Fwebpack-example)
	- <details><summary>Интересные моменты</summary>

		- Установка:
		```
		npm install webpack -- save-dev
		npm install webpack-cli -- save-dev
		```
		- [О конфиге](https://youtu.be/AoPDBBbInzc?t=505)(см. презентацию).
		- [Alias](https://youtu.be/AoPDBBbInzc?t=619) - помогают создвать переменные с путем к файлу для сокращения импортов типа ../../. (см. презентацию)
		- [Loader](https://youtu.be/AoPDBBbInzc?t=675) - позволяет вебпаку обрабатыать расширения кроме js & json. Например, ts -> js.. (см. презентацию)
		```
		rules:[{test: /\.js$/, use: 'some-loader'},]
		```
		- [Plugins](https://youtu.be/AoPDBBbInzc?t=929) - используются для расширения возможностей вебпака.(см. презентацию)
		- [Modes](https://youtu.be/AoPDBBbInzc?t=1123) - режимы работы вебпака (development, prodaction, none). Определяет на используемые оптимизации при использовани сборщика.(см. презентацию)
		- [Devserver](https://youtu.be/AoPDBBbInzc?t=1275)(см. презентацию)
		```
		npm install --save-dev webpack-dev-server
		```
		- npx create-react-app my-app разворачивает сборку webpack
		- [Скрипты сборки в pckage.json](https://youtu.be/AoPDBBbInzc?t=1868)
		- [пример loader rules](https://youtu.be/AoPDBBbInzc?t=2036)
		- loader отрабатывают с конца массива use
		- плагин сначала импортируется, потом указывается в массиве плагинов, потом используется
		- [Devserver config](https://youtu.be/AoPDBBbInzc?t=2563)
		</details>
2. [React. Base](https://www.youtube.com/watch?v=cJ9gGiH9UzA&feature=youtu.be&ab_channel=RollingScopesSchool).
	- [Офииальная документация](https://ru.reactjs.org/docs/getting-started.html)
	- [Презентация](https://docs.google.com/presentation/d/1Zl61lcoJPN81-jZhYTfjkPZkid7DLM0pGN3rK2N0ZZc/edit#slide=id.p)
	- <details><summary>Интересные моменты</summary>

		- [Create react app](https://youtu.be/cJ9gGiH9UzA?t=701).
		- [Create react app HAbr](https://habr.com/ru/company/plarium/blog/326520/)
		- [Stace class](https://youtu.be/cJ9gGiH9UzA?t=1444). setState(updater[,callback(prevstate, ptops)]). Callback вызывается после апдейта.
		- [Lifecycle](https://youtu.be/cJ9gGiH9UzA?t=1739). Все об обновлении компонентов (подробно).
			- [Lifecycle Diagram](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/).
			- [getDerivedstateFromProps](https://youtu.be/cJ9gGiH9UzA?t=2617).
			- [shoudComponentUpdate](https://youtu.be/cJ9gGiH9UzA?t=2680). Можно уравлять ледует ли обновлять компонент на основе нового значения пропсов\стэйта.
			- [getSnapshotBeforeUpdate](https://youtu.be/cJ9gGiH9UzA?t=2768).
		- [Dom event handling](https://youtu.be/cJ9gGiH9UzA?t=2893). About event handling by REACT (refs to each react event see on presentation).
		- [Key](https://youtu.be/cJ9gGiH9UzA?t=2934). Key - compontnrt identifier.
	</details>

4. [React hooks](https://www.youtube.com/watch?v=3-Zh_DAzCi0&t=11s&ab_channel=RollingScopesSchool)
	- [Code examples](https://github.com/thrvrce/react-lectures)
	- <details><summary>Интересные моменты</summary>

		- Хуки позволяют управлять\ввзаимодействовать с жизненнымм циклом или остояния компонента.
		- Код на функциональных компонентах легковеснее.
		- setState не мержит стейт, а заменяет полностью, в отличии от this.setState!
		- Функция\переменная\объект\етц передаваемая в качестве параметра useState как первоначальное значение вызывается только при первом рендере (монтировании). [пример](https://youtu.be/3-Zh_DAzCi0?t=1149)
		- **Запускается ли рендер сразу после seеState или они накапливаются?**. setState не триггерит мгновенный рендеринг. Значение локального свойства не меняется, но вот значение внутри функции-стейта изменяется. То есть при установке нового значения стейта и последующей попытке его поменять используя предыдущее значение из функции - колбэка в качестве предыдущего значения будет уже новое значение .
		- const Comp: React.FC = ()=> {} - React.FC - функциональный компонент реалкт тип.
		- в зависимостях useEffect сравнение происход по правилу ===.
		- [useCallback](https://youtu.be/3-Zh_DAzCi0?t=3854). Помогает хранить экземпляр функции сквозь рендеры. Полезно когда useEffect в зависимостях имеет функцию. Сам же useCallback меняет свое содержимое(функцию) в зависимости от изменения его собственной зависимости. В функцию полученноу после вызова useCallback можно передавать параметры.**почитать дополнительно!**
		- [useMemo](https://youtu.be/3-Zh_DAzCi0?t=4210). Возврщает результат вызова функции переданной в качестве аргумента. Тоже есть подписки. **почитать дополнительно!**
		- не стоит предавать в методы мемоизации (useCallback, useMemo) асинхронный функционал.
		- [Контекст](https://youtu.be/3-Zh_DAzCi0?t=4648).
		- [useRef](https://youtu.be/3-Zh_DAzCi0?t=5029). Возвращает mutable контейнер. Ссылка на контейнер не меняется с монтирования компонента. React не триггерит рендеры если содержимое контейнера меняется. Видимо значение .curent можно полув соседних функциях одного скоупа, ведь сам реф не меняется, а меняется только его свойство.
		- [UseRef & DOM elements](https://youtu.be/3-Zh_DAzCi0?t=5384).
		- [useReducer](https://youtu.be/3-Zh_DAzCi0?t=5507). На вход получает некую функцию - reducer и начальный state. [пример reducer'a](https://youtu.be/3-Zh_DAzCi0?t=5628)
		- [user hooks](https://youtu.be/3-Zh_DAzCi0?t=6274)
		- [пример проверки клика за пределами элемента](https://youtu.be/3-Zh_DAzCi0?t=6777)
	</details>
