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
