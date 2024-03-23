# Автоматизация тестирования мобильных приложений

## Практическая работа 4 

Закрепить знания о том, как создавать локаторы для элементов в java-проекте
и выбирать эффективные стратегии.

## Что нужно сделать

В обоих заданиях ниже вам нужно создать локаторы для элементов в
java-проекте. Выберите максимально эффективные стратегии поиска
локаторов.

# Задание 1. Android

1. Скачайте приложение Zoom.
2. В java-проекте задайте в capabilities драйвера параметр APP с
информацией о местонахождении скачанного приложения.
3. Откройте эмулятор (разрешение экрана эмулятора должно быть не
менее 1440×2560). Если у вас такого нет, создайте (подсказка в разделе
«Советы и рекомендации»).
4. Установите на эмулятор вручную приложение Zoom и найдите локатор
кнопки Join a Meeting.
5. В java-проекте создайте элемент с найденным локатором и вызовите у
этого элемента метод click().
6. На эмуляторе вручную нажмите на кнопку Join a Meeting.
7. На этом экране найдите все элементы, которые присутствуют в текущей
визуализации (кроме виртуальной клавиатуры), скроллить экран для
визуализации нижних элементов не нужно:
Список необходимых элементов для поиска:
 
  ● Кнопка Cancel.
  ● Заголовок Join a Meeting.
  ● Поле ввода Meeting ID (класс LinearLayout).
  ● Текст Join with a personal link name.
  ● Поле ввода с текстом sdk_gphone. (класс LinearLayout).
  ● Кнопка Join.
  ● Текст под кнопкой Join.
  ● Заголовок Join Options.
  ● Текст Don’t Connect To Audio.
  ● Переключатель рядом с текстом Don’t Connect To Audio.
  
8. В java-проекте создайте и инициализируйте все элементы текущего
экрана с локаторами, которые, на ваш взгляд, максимально
эффективны, используя знания, полученные в модулях 3 и 4.
9. Первые пять элементов объявите с помощью аннотаций, остальные — с
помощью методов драйвера.
10. Проверьте, что элементы отображаются на экране с помощью вызова у
элемента метода isDisplayed().
11. Запустите ваш тест и проверьте, что он сам запускает приложение на
эмуляторе, нажимает кнопку Join a Meeting, а затем просто удачно
завершается, найдя все элементы на экране.

# Задание 2. iOS

1. Откройте на iOS-симуляторе приложение «Здоровье» (Health).
2. В java-проекте задайте в capabilities драйвера параметр BUNDLE_ID с
идентификатором приложения «Здоровье».
3. На этом экране найдите следующие элементы:

  ● Заголовок Summary.
  ● Иконка рядом с заголовком.
  ● Заголовок Favorites.
  ● Кнопка Edit.
  ● Кнопка Steps.
  ● Текст No Data.
  ● Кнопка Show All Health Data.
  ● Заголовок Get More From Health.
  ● Иконка со звёздочкой.
  ● Кнопка Get Started.
  
4. Следите за тем, что если элемент, например, кнопка, то вам необходимо
найти именно type Button, а не StaticText, который является дочерним у
кнопки и содержит текст этой кнопки. StaticText обычно является
самостоятельным типом у заголовков.
5. В java-проекте создайте и инициализируйте все элементы текущего
экрана с локаторами, которые, на ваш взгляд, максимально
эффективны, используя знания, полученные в модулях 3 и 4.
6. Первые пять элементов объявите с помощью аннотаций, остальные — с
помощью методов драйвера.
7. Проверьте, что элементы отображаются на экране с помощью вызова у
элемента метода isDisplayed().

## Советы и рекомендации

  ● Чтобы создать эмулятор, вам необходимо во вкладке AVD Manager
нажать на кнопку Create Virtual Device → выбрать подходящий по
размерам экрана эмулятор (например, Nexus 6) → нажать Next →
выбрать подходящую версию ОС (если она не установлена, то
установить) → нажать Next → нажать Finish. За дополнительной
информацией вы можете обратиться к документации.

  ● Чтобы избежать ошибки The element … does not exist in DOM anymore,
необходимо перед загрузкой экрана с этим элементом добавить явное
ожидание с помощью записи Thread.sleep(2000) и, поставив курсор в
любое место слова sleep, нажать Option + Enter и добавить в сигнатуру
метода ошибку.

## Что оценивается

  ● Решение чётко соответствует заданным условиям.
  ● Локаторы однозначно идентифицируют нужные элементы.
  ● Код компилируетс
