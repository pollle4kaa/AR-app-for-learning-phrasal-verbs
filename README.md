# AR-приложение для изучения фразовых глаголов
Работу выполняла ученица школы №548: Ситникова Полина Юрьевна (10Ц)

Руководитель: Гришин Пётр Анатольевич (учитель информатики)
## Комментарий
Приложение создано в Unity при помощи плагина Vuforia Engine для Android-устройств.
## Краткое описание
Phrase - приложение для изучение фразовых глаголов английского языка. Известно, что учить иностранные языки легче, если делать это при помощи ассоциаций. Данный метод подходит для изучения слов как максимально приближенный к естественным процессам запоминания.
## Функционал приложения
#### На главном экране приложения доступно 3 кнопки: "Начать", "Информация" и "О приложении"
Кнопка "Начать" включает камеру устройства. Чтобы увидеть анимированную 3D модель, нужно сфокусировать камеру на любом изображении  из набора фразовых глаголов.

Кнопка "Информация" предлагает пользователю ознакомиться с тем, что такое фразовый глагол.

Кнопка "О приложении" хранит в себе краткое описание приложения и инструкцию.

![scenes](https://user-images.githubusercontent.com/125691054/219877529-b74a4a86-79f7-4e7a-98d1-e02ff265769f.png)

#### Набор фразовых глаголов, представленных в приложении, и их ассоциативные анимированные 3D модели:
- run away
- sit down
- leave off
- look for
- knock out

![metki_modeli](https://user-images.githubusercontent.com/125691054/219875896-9304ddf6-dfd2-4e4b-aaa0-01728063342f.png)



## Описание проведенных испытаний
При фокусировке и распознавании камерой необходимые нам фразы приложение успешно воспроизводит 3Д модель с анимацией для наглядного понимания лексического значения фразового глагола;

Приложение автономно (не зависит от интернета);

Приложение построено не на клиент-серверной архитектуре, следовательно ему не нужен доступ к серверу ;

В дальнейшем планируется создать клиент-серверную архитектуру, при помощи которой, добавляя фразовые глаголы, клиенту не нужно будет скачивать новую версию файла;

Из-за отсутствия клиент-серверной архитектуры, после добавления нового фразового глагола клиенту необходимо скачать новую версию файла.
## Архитектура программы 
Приложение создано в Unity для Android-устройств при помощи плагина Vuforia Engine.

В папке Scenes хранятся файлы с 4-мя сценами (1 сцена - главный экран (меню) и 3 сцены для кнопок: "Начать", "Информация" и "О приложении").

В папке 3d models хранятся файлы с 5-ью 3D моделями и папки с их текстурами, материалами и анимациями.

В папке Sprites хранятся файлы (изображения), используемые для кнопок.

В папке Scripts хранится файл - программный код, написанный на C#

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class LoadScenes : MonoBehaviour
{
    // Start is called before the first frame update
    public void ChangeScenes(int _number)
    {
        SceneManager.LoadScene(_number);
    }
}
```
