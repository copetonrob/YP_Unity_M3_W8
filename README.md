# Unity. Модуль 3. Вебинар 8

Этот репозиторий содержит задание для восьмого вебинара

## Game Over

<img src="https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/img/GameOver.png" width="600"/>

Самая нелюбимая фраза всех игроков. Сегодня мы займемся механикой конца игры.

Если пропустил_а предыдущие вебинары, можешь использовать полностью готовый [стартовый набор](https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/webinar7.unitypackage) из седьмого вебинара. В нем есть игрок, который стреляет, есть мобы, которые преследуют игрока. Есть прицел и полоска здоровья. Но когда у игрока заканчивается здоровье, то игра просто ломается и выдает ошибку. Сегодня мы как раз это исправим. Стартовая сцена лежит в папке Assets/M3W7/Scenes/ и называется M3W7

## Инструкция

1) Открой стартовую сцену игры

2) Прежде чем сделать экран конца игры, надо немного подготовиться. Сначала создай пустой объект в канвасе и назови его PlayerUI. Выстави параметры Rect Transform так, чтобы растянуть объект на весь экран

<img src="https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/img/PlayerUI.png" width="300"/>

3) Этот объект нужен нам, чтобы сгруппировать все игровые элементы интерфейса (прицел и здоровье игрока). Перенеси эти элементы в иерархии в PlayerUI.

<img src="https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/img/PlayerUI2.png" width="300"/>

Можно временно отключить этот объект справа в инспекторе, чтобы было удобнее настраивать экран конца игры.

4) По такому же принципу создай пустой объект в канвасе и назови его GameOverScreen. Не забудь его так же растянуть на весь экран.

5) Создай новый объект UI->Image внутри объекта GameOverScreen. Назови этот объект Background, это будет наш фон. Растяни картинку на весь экран и задай ей цвет и прозрачность.

<img src="https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/img/Background.png" width="300"/>

6) Создай внутри объекта Background два объекта с текстом UI -> Text. Ты можешь использовать Text Mesh Pro, если хочешь.

7) Напиши в этих текстах "Game Over" и "Press ESC to restart"

Настрой их положение, ширину, высоту, размер шрифта и прочие настройки так, чтобы текст на экране выглядел хорошо.

Пример настроек:

<img src="https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/img/GameOverText.png" width="300"/>

8) Настало время немного попрограммировать. Нам надо изменить скрипт [PlayerHealth.cs](https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/scripts/PlayerHealth.cs) так, чтобы после конца игры интерфейс игрока с прицелом и полоской здоровья отключался, а экран конца игры включался. Расскоментируй фрагменты кода и исправь ??? на правильные команды и выражения.

9) Теперь, добавим в проект еще один скрипт [ReloadScene.cs](https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/scripts/ReloadScene.cs)

Этот скрипт перезапускает сцену, если мы нажали на клавишу Escape. Помести этот скрипт в объект GameOverScreen, чтобы он начинал отслеживать нажатие Escape только после конца игры.

<img src="https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/img/ReloadScene.png" width="300"/>

10) Перед началом игры, проверь, что у тебя включен объект PlayerUI и выключен объект GameOverScreen.

<img src="https://github.com/copetonrob/YP_Unity_M3_W8/blob/main/img/Settings.png" width="300"/>

11) Запусти проект и проверь, что все работает.

Теперь после конца игры, у игрока отключается возможность бегать и прыгать и вращать камеру. Но он все еще может стрелять, так как оружие внутри объекта Player все еще функционирует. Если мы нажмем кнопку ESC, то сцена перезапустится и игра начнется сначала.

### Дополнительные задания на подумать (можно дома):

1) Задание со звездочкой. Подумай, как отключить после конца игры возможность стрельбы.

2) Второе задание со звездочкой. Сделай так, чтобы после смерти персонажа, проигрывалась анимация падения на землю.
