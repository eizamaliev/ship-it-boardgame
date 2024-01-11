# Ship IT!

## Подготовка к игре

0. Необходимо определиться с вариантами правил игры

Доступны следующие варианты:
- С социальным взаимодействием или без
- С дополнительными картами (Кеш, OpenSource, Цепочка поставок, Слить) или без

Смотрите пункт "Варианты игры" для подробностей

1. Раздача карт "Архитектура"

Каждый игрок взакрытую получает случайную карту Архитектуры, чтобы узнать условия своей победы: какие компоненты нужно будет выложить на стол ("задеплоить"). Вот ваша задача на игру.

Данную карту нужно положить взакрытую рядом с собой.
Так как задания для игроков разные, то игрокам заранее неизвестно, какие компоненты нужны вам для победы. Данное обстоятельство предстоит выяснить по ходу игры.

Карта Архитектуры вам понадобится только в конце, чтобы подтвердить вашу победу.

2. Раздача остальных карт

При 2х игроках: возьмите по 6 карт
При 3x или 4x игроках: возьмите по 7 карт

## Ход игры

В начале каждого хода необходимо взять карту из колоды.
Далее у вас есть два варианта.

Вы можете взять еще одну карту и закончить ход.

Или вы можете сделать полноценный ход, в рамках которого вы можете совершить от одного до трех уникальных действий из списка ниже:
- Разыграть 1 карту компонента
- Разыграть любое количество других карт
- Совершить обмен

Действия можно совершать в любом порядке.
Например: сначала поменяться картами, затем сыграть карты атаки, потом выложить 1 компонент.

Если в течение вашего хода, карты в колоде закончились, то перемешайте сброс

Если в конце вашего хода у вас на столе оказывается набор компонентов, который требуется на вашей карте Архитектуры – поздравляю, вы победили. Покажите её всем остальным.

Можно продолжить игру пока не останется один проигравший.
Тот, кто проигрывает, раздает карты, а победители могут всю следующую игру звать его "Джун".

## Обмен

Как проиходит обмен?

В свой ход в рамках действия вы можете предложить какую-то карту другим игрокам. Или попросить какую-то карту для себя. Обмен не обязательно должен быть равным. Вы можете поменять одну карту на несколько или несколько на одну. Однако, нельзя менять несколько карт на несколько карт.

Важное правило: все карты меняются взакрытую. Два игрока, участвующие в обмене, кладут карты, которые будут менять, перед собой взакрытую. Как только оба игрока выложили карты, обмен считается произведенным; вам остается только взять их себе в руку.

Данное правило критично для возможности обмана других игроков: любой игрок может положить в обмен любую карту, не только ту, что он обещал.

Более того, игрок может вернуть карту, которую отдал, при помощи карты "RFC", просто запросив отданную карту обратно.

Обмен – очень полезная, но очень опасная штука!

## Атака

Атака – второе фундаментальное действие в игре.
Вы же не хотите, чтобы ваши соперники успели победить раньше вас?
Конечно нет! Тогда – нужно сломать их планы.

В игре есть два основных вида атаки:
- Ошибки нескольких видов (результат: соперник останется без компонента на столе)
- Проблема безопасности (результат: соперник отдает компонент со стола вам в руку)

От ошибок и проблем безопасности есть защита нескольких типов:
- В виде компонента (Мониторинг, Файрвол)
- В виде свойства компонента (CI, Сертификат)
- В виде ответного действия (Отговорка, Патч)

И еще у вас есть карты "sudo" для усиления атаки и защиты.

Как происходят атаки? Разберем на примерах

### Пример: атака на компонент

У Алисы на столе лежит компонент "Бекенд". Борис в свой ход его атакует картой "Ошибка".
Варианты развития событий:
- У Алисы есть карта "Отговорка", она разыгрывает её. Обе карты отправляются в сброс, компонент остается на столе у Алисы
- У Алисы нет карты защиты, она вынуждена выполнить условие карты "Ошибка". Карта "Ошибка" идет в сброс

Аналогично выглядит процесс атаки с другими картами ошибок и проблем безопасности.
Однако, обратите внимание, что от ошибок и проблем безопасности защищают разные карты!

### Пример: атака с картой sudo

У Алисы на столе лежит компонент "Бекенд". Борис в свой ход его атакует картой "Ошибка" вместе с картой "sudo".
Варианты развития событий:
- У Алисы есть карты "Отговорка" и "sudo". Она разгрывает их. Все 4 карты отправляются в сброс, компонент остается на столе у Алисы
- У Алисы есть только одна карта ("Отговорка" или "sudo") или вовсе нет карт защиты, что не защитит её от атаки с "sudo". Она вынуждена выполнить условие карты "Ошибка". Атакующие карты идут в сброс

### Пример: атака на игрока с картой CI / Сертификат

У Алисы на столе лежит компонент "Бекенд" с подложенной картой "CI". Борис в свой ход его атакует картой "Ошибка".
Варианты развития событий:
- Карты "CI" и атака отправляют в сброс, компонент остается лежать на столе

Карта "sudo" полностью меняет ситуацию.

У Алисы на столе лежит компонент "Бекенд" с подложенной картой "CI". Борис в свой ход его атакует картами "Ошибка" и "sudo".
Варианты развития событий:
- У Алисы есть карта "sudo". Карты "CI", "sudo" и карты атаки отправляются в сброс, компонент остается лежать на столе
- У Алисы нет карты "sudo". Она вынуждена выполнить условие карты "Ошибка". Карта "CI" и атакующие карты идут в сброс

### Пример: атака на игрока с картой Мониторинг / Файрвол

У Алисы на столе лежат компоненты "Бекенд" и "Мониторинг". Борис в свой ход атакует Алису картой "Ошибка".

Особенность данной ситуации в том, что карта "Мониторинг" защищает все другие компоненты от атаки (кроме себя). Следовательно, Борис может атаковать только компонент "Мониторинг".

Все остальные правила остаются без изменений.

### Пример: атака на самого себя

В некоторых случаях имеет смысл атаковать себя. Пример: у Алисы на столе компонент "Бекенд". У Бориса в руках карта "Проблема безопасности" и почти все компоненты необходимые для победы (кроме карты "Бекенд"). Сейчас ход Алисы. Она знает, что защиты от "Проблемы безопасности" у нее нет.

Если оставить компонент на столе, то Борис победит следующим ходом. Тогда Алиса атакует свой компонент и убирает его обратно себе в руку. Оттуда его будет сложнее достать!

## Варианты игры

### Игра с социальным взаимодействием

Некоторые карты, например "Ошибка", имеют специальное условие в нижней трети карты, что нужно сделать при розыгрыше. Если вы договорились играть с данным правилом, то игроку *необходимо* выпонить данное социальное действие. Если игрок забыл, не может или не хочет его выполнять – то он обязан скинуть карту с руки в сброс.

Некоторые карты могут иметь небольшие бонусы при определенных социальных условиях. Пользуйтесь ими в данном режиме игры!

Стоит отдельно отметить, что социальное взаимодействие на карте `Проблема безопасности` – просто шутка, выполнять его не нужно, и штрафовать за неисполнение – тоже.

### Игра с дополнительными картами

Есть 4 карты, которые можно добавлять или убирать из игры: "Кеш", "OpenSource", "Цепочка поставок" и "Слить". Они привносят немного хаоса и веселья! Можете играть с ними или без них.

## FAQ

### Почему карты нужно складывать в сброс рубашкой вниз (лицом наверх)?

Для того, чтобы видеть верхнюю карту при применении карты "Переиспользование".