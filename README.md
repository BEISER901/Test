# 🎮 Project Documentation

## 📖 О проекте

Этот проект представляет собой модульную игровую систему, построенную на Unity, с разделением логики на независимые подсистемы:

- Gameplay Core
- UI Framework
- Tool / Weapon System
- Database Layer (Local + Supabase)
- Rendering Extensions (URP)
- Bot AI Framework
- Custom Editor Tools

Архитектура ориентирована на масштабируемость и переиспользование компонентов.

---

# 📚 Project Architecture Tree (README Navigation)

## 🧭 UI System

* [UISystem](#uisystem)
* [UISystemAction](#uisystemaction)
* [UISysEvents](#uisysevents)

## 🧩 Text System

* [TMPFormater](#tmpformater)
* [ITMPFL](#itmpfl)

## 🎯 Aim System

* [AimController](#aimcontroller)

## 👁 Dynamic Face System

* [DynamicFace](#dynamicface)
* [DynamicEye](#dynamiceye)

## 🎮 Player System

* [BasePlayer](#baseplayer)
* [PlayerToolBase](#playertoolbase)

### 🤖 Player Bot System

* [PlayerBot](#playerbot)
* [BaseBotBehavior](#basebotbehavior)

## 🧠 Database System

* [LocalDB](#localdb)
* [SupabaseAPI](#supabaseapi)
* [DBMeta](#dbmeta)
* [UserScore](#userscore)

## ✨ Rendering / Outline System

* [OutlineTarget](#outlinetarget)
* [IgnoreTargetOutline & IIgnoreOutline](#ignoretargetoutline--iignoreoutline)

---

# 📌 Classes

---

## UISystem

Глобальная система управления UI-экранами, навигацией и анимациями.

---

## UISystemAction 

Компонент-bridge для управления UISystem через UI кнопки и события.

---

## UISysEvents

Связка Animator ↔ UISystem для синхронизации UI-анимаций и переходов.

---

## TMPFormater

Система динамической подстановки значений в TextMeshPro через `{Key}`.

---

## ITMPFL

Маркерный интерфейс источников данных для TMPFormater.

---

## AimController

Система прицеливания: ввод, угол, сила, состояния и AimEvents.

---

## DynamicFace

Система управления направлением взгляда на основе приоритетных интересов.

---

## DynamicEye

Процедурная система глаз и зрачков с привязкой к DynamicFace.

---

## BasePlayer

Базовый игрок: физика, скин, инструменты, анимации и синхронизация движения.

---

## PlayerToolBase {#playertoolbase}

Базовый класс инструмента игрока: aim, анимации, звук, стрелка направления.

---

## PlayerBot

Игрок-бот: расширение BasePlayer с AI, умиранием и физическим поведением.

---

## BaseBotBehavior

Базовый слой AI логики бота + debug режим и waypoint система.

---

## LocalDB

Центральная система локальной БД + Supabase синхронизация + SQLite слой.

---

## SupabaseAPI

API слой: авторизация, RPC, Postgrest, обновление пользовательских данных.

---

## DBMeta

Низкоуровневый SQLite слой выполнения SQL команд и логирования.

---

## UserScore

Модель лидерборда (Supabase).

---

## OutlineTarget {#outlinetarget}

Система регистрации Renderers для outline-эффекта.

---

## IgnoreTargetOutline & IIgnoreOutline

Механизмы исключения объектов из outline системы.

---

## 🪟 UI Screens

- Menu
- Shop
- Start Game
- Leaderboard
- Loading Screens

---

## 🌐 Localization

- TMP-based localization system
- `TMPFL` label system
- Dynamic text formatting

---

## 🔘 Interactive UI

- Buttons system
- Scroll systems
- Tab navigation
- UI animations

---

# 🎨 Rendering / Graphics

## 🖌️ Renderer Features

URP Renderer Extensions:

- `OutlineFeature`
- Stencil masking
- Post-processing effects

---

## ✨ Outline System

- `OutlineMask.shader`
- `OutlineComposite.shader`
- `OutlineBlur.shader`

Используется для выделения объектов.

---

# 🎮 Game Content

## 🗺️ Scenes

- Authentication
- Game
- PreLoadingGame
- Test

---

## 🎭 Animations

- Player animations
- UI transitions
- Tool effects
- Camera animations

---

## 🧱 Prefabs Structure

Система prefab-архитектуры:

- UI prefabs
- Player prefabs
- Tool prefabs
- Bot prefabs

---

## 🎨 Art / Assets

- UI Icons
- Backgrounds
- Characters
- Weapons
- Environment objects

---

## 👕 Skins System

- `Skin.cs`
- Character variants
- Animation-driven skins

---

## 🛠️ Tools System (Weapons & Items)

Унифицированная система предметов:

- Harpoon
- Katana
- Shield
- Teleporter
- Boxing Glove
- HotDog Blaster

Основано на:
- `ToolDefinition`
- ScriptableObject architecture

---

# 🧰 Systems

## 🪟 Modal System

- `ModalSystem`
- Error / Alert / Loader presets
- Dynamic modal spawning

---

## 📊 Inventory / Tools System

- `ToolInventory`
- `ToolInventoryUI`
- Editor integration

---

## 🔤 TMP Formatter System

Расширение TextMeshPro:

- `TMPFormater`
- Label attributes
- Dynamic text processing

---

## 🧪 Debug / Test System

- `TestSRC`
- Physics experiments
- Animation tests
- Raycast systems

---

# 🧑‍💻 Editor / Dev Tools

## 🧑‍💻 Editor Extensions

- Custom inspectors
- Camera editors
- Tool editors

---

## 🖼️ Preview Tools

- PngPrefabPreviewer
- Asset preview generation

---

# 📁 Legacy / Old Code

## 🗃️ OLD System

Старые системы (не используются):

- Audio system legacy
- Old location streaming
- Old UI screens
- Experimental mechanics

---

# 📦 Plugins / Third-party

## 🔌 Android / Platform Plugins

- Native SQLite libraries
- Android ABI support (arm64, x86)

---

## 📚 External Libraries

- Supabase SDK
- Newtonsoft.Json
- Reactive Extensions
- Websocket client

---

# 🚀 Build / Deployment

## 📱 Platforms

- Android
- Windows
- WSA (UWP)
- Linux (via native libs)

---

## 📦 Build Settings

- URP pipeline
- Adaptive Performance support
- StreamingAssets database

---

# 🧾 StreamingAssets

- `Objects.db`
- `Session.db`

Используется для локального хранения данных.

---

# 🧩 ScriptBoy / Extensions

- EButton Attributes system
- Editor utilities
- Test framework

---

# 📌 Known Issues

- OLD folder содержит устаревшие системы
- Требуется рефакторинг UI legacy экранов
- Некоторые тестовые сцены не используются в билд

---

# 🗺️ Roadmap

- [ ] Рефакторинг OLD системы
- [ ] Вынос Tool System в отдельную библиотеку
- [ ] Оптимизация UI system
- [ ] Полная миграция на модульную архитектуру
- [ ] Документация API

---

# Документация

***

## [Assets/_Project/UI/UISystem](Assets/_Project/UI/UISystem)
## UISystem {#uisystem}

[./UISystem.cs](Assets/_Project/UI/UISystem/UISystem.cs)

`UISystem` — глобальная система управления UI-экранами, основанная на списке `UIInfo`, поддерживающая навигацию по UI-дереву, анимационные переходы, инстансинг префабов и управление состоянием интерфейса через пути (path + hash).

---

### 📦 Возможности

* Управление UI через список `UIInfo`
* Иерархическая навигация по UI (Next / Back)
* Поддержка путей (`UIPath`) и расширенных путей с hash-данными
* Автоматическое создание и уничтожение UI префабов
* Поддержка анимационных переходов между UI:

  * GoLeft / GoRight Open / Close
  * Static Open / Close
* Система callback’ов завершения анимаций
* Блокировка raycast во время анимации
* Автоматическая синхронизация с `Canvas` и `Camera.main`
* Поддержка `SendMessage` событий UI (`UIUpdate`)
* Режим работы в Edit Mode (`ExecuteAlways`)
* Инструменты редактора для управления UI

---

### Класс

```csharp
[ExecuteAlways]
public class UISystem : MonoBehaviour, ISingleton<UISystem>
```

---

### Поля

#### uiList

Список всех UI-экранов системы. Каждый элемент описывает:

* префаб UI
* активный view
* анимации
* действия UI

```csharp
public List<UIInfo> uiList = new List<UIInfo>();
```

---

#### autoApplyAnyPrefabOverrides

Автоматически применяет изменения префабов UI (только в Editor).

```csharp
public bool autoApplyAnyPrefabOverrides = false;
```

---

#### IsAnimating

Флаг состояния анимации UI (блокирует взаимодействие с UI во время переходов).

```csharp
public bool IsAnimating { get; set; }
```

---

### Свойства

#### UIPath

Текущий путь UI без hash-данных.

```csharp
public string UIPath { get; set; }
```

---

#### UIFullPath

Полный путь UI включая hash-данные (служебное состояние навигации).

```csharp
public string UIFullPath { get; set; }
```

---

#### CurrentUI

Текущий активный UI-экран, найденный по последнему элементу пути.

```csharp
public UIInfo CurrentUI { get; set; }
```

---

#### LastUI

Предыдущий UI-экран до перехода.

```csharp
public UIInfo LastUI { get; }
```

---

#### Instance

Singleton-доступ к системе UI.

```csharp
public static UISystem Instance { get; set; }
```

---

### Методы

#### UpdateUI(UIInfo, bool)

Основной метод переключения UI.

* уничтожает неактивные UI
* создаёт новый UI из префаба
* управляет анимацией переходов
* вызывает callback после завершения перехода

```csharp
public void UpdateUI(UIInfo _new, bool animating = true)
```

---

#### SwitchUI(UIInfo, bool, string, Action)

Внутренний метод переключения UI с поддержкой анимаций и callback’ов завершения.

```csharp
void SwitchUI(UIInfo uiInfo, bool active, string animation = "", Action onReadyToChangeCallback = null)
```

---

#### SetUI(string)

Устанавливает UI по строковому пути.

```csharp
public void SetUI(string uiName)
```

---

#### Next(string, bool)

Переход к следующему UI в иерархии.

```csharp
public void Next(string path, bool saveHash)
```

---

#### ToBack(bool)

Возврат к предыдущему UI в пути.

```csharp
public void ToBack(bool saveHash)
```

---

#### ClearHash()

Очищает hash-часть UI пути.

```csharp
public void ClearHash()
```

---

#### ApplyPrefabs()

(только Editor)

Применяет изменения экземпляров префабов UI обратно в ассеты.

```csharp
public void ApplyPrefabs()
```

---

### Краткое поведение

`UISystem` — это централизованная система управления интерфейсом, которая:

* строит UI как дерево экранов
* переключает экраны через пути
* поддерживает анимационные переходы
* автоматически создаёт и удаляет UI префабы
* блокирует ввод во время анимаций
* синхронизирует UI с Canvas и камерой

## UISystemAction {#uisystemaction}

[./Components/UISystemChanger.cs](Assets/_Project/UI/UISystem/UISystem/Components/UISystemChanger.cs)

`UISystemAction` — вспомогательный компонент для управления `UISystem` из UI-кнопок и событий. Предоставляет набор методов-обёрток, которые позволяют переключать UI, переходить назад по истории и вызывать UI-действия по имени.

---

### 📦 Возможности

* Переключение UI по ID (SetUI)
* Переход к предыдущему UI (Back)
* Поддержка переходов с hash-данными и без них
* Переход к следующему UI по пути (Next)
* Вызов UI-экшенов по имени
* Использование через Unity UI Events (Button.onClick и т.д.)

---

### Класс

```csharp
public class UISystemAction : MonoBehaviour
```

---

### Методы

#### ChangeToByID(string id)

Переключает текущий UI на экран с указанным ID через `UISystem.SetUI`.

```csharp
public void ChangeToByID(string id)
```

---

#### ToBack()

Возвращает на предыдущий UI без сохранения hash-данных.

```csharp
public void ToBack()
```

---

#### ToBackWithHash()

Возвращает на предыдущий UI с сохранением hash-данных.

```csharp
public void ToBackWithHash()
```

---

#### ToBack(bool saveHash)

Возвращает на предыдущий UI с контролем сохранения hash-данных.

```csharp
public void ToBack(bool saveHash)
```

---

#### Next(string path)

Переходит к следующему UI по указанному пути без сохранения hash.

```csharp
public void Next(string path)
```

---

#### NextWithHash(string path)

Переходит к следующему UI по пути с сохранением hash-данных.

```csharp
public void NextWithHash(string path)
```

---

#### Next(string path, bool saveHash)

Переход к следующему UI с контролем сохранения hash-данных.

```csharp
public void Next(string path, bool saveHash)
```

---

#### CallAction(string name)

Вызывает UI-действие из текущего UI (`UIInfo.UIActions`) по имени.

```csharp
public void CallAction(string name)
```

---

### Краткое поведение

`UISystemAction` — это bridge-компонент между Unity UI (кнопками, событиями) и системой `UISystem`, позволяющий:

* управлять навигацией UI без кода
* вызывать UI события по строковому имени
* использовать систему UI в инспекторе через OnClick / Events
* упрощать работу дизайнеров и геймдизайнеров без доступа к логике UISystem

## UISysEvents {#uisysevents}

[./Components/UISysEvents.cs](Assets/_Project/UI/UISystem/Components/UISysEvents.cs)

`UISysEvents` — вспомогательный компонент для интеграции UI-анимаций с системой `UISystem`. Используется как мост между `Animator` и логикой смены UI, позволяя вызывать callback в момент завершения анимации или готовности к переключению интерфейса.

---

### 📦 Возможности

* Доступ к `Animator` UI-элемента
* Передача callback’а завершения анимации (`ReadyToChangeCallback`)
* Интеграция с `UISystem.SwitchUI`
* Вызов событий из Animation Events (Unity Animator)
* Связь UI-анимаций с логикой смены экранов

---

### Класс

```csharp
public class UISysEvents : MonoBehaviour
```

---

### Свойства

#### animator

Возвращает компонент `Animator`, привязанный к текущему UI-объекту.

```csharp
public Animator animator => GetComponent<Animator>();
```

---

### Поля

#### ReadyToChangeCallback

Callback, вызываемый после завершения UI-анимации или в момент, когда UI готов к переключению.

```csharp
public Action ReadyToChangeCallback;
```

---

### Методы

#### ReadyToChange()

Вызывает `ReadyToChangeCallback`, уведомляя `UISystem` о завершении анимации и готовности UI к смене состояния.

Обычно вызывается через Animation Event внутри Unity Animator.

```csharp
public void ReadyToChange()
```

---

### Краткое поведение

`UISysEvents` используется как связующее звено между анимациями UI и системой `UISystem`, позволяя:

* синхронизировать смену экранов с анимациями
* безопасно завершать UI-переходы
* запускать callback после окончания анимации
* интегрировать Animator через Animation Events

***

## [Assets/_Project/System/TMPFormaterSystem](Assets/_Project/System/TMPFormaterSystem)
## TMPFormater {#tmpformater}
[./TMPFormater.cs](Assets/_Project/System/TMPFormaterSystem/TMPFormater.cs)

`TMPFormater` — Unity-компонент для автоматической подстановки значений из объектов (`ITMPFL`) в текст TextMeshPro с использованием шаблонов вида `{Variable}`.

---

### 📦 Возможности

- Автоматическая подстановка значений в TMP_Text
- Поддержка полей и свойств (public / private)
- Использование кастомного атрибута `TMPFL.Label.Label`
- Поиск источников данных в родительских объектах
- Работа в режиме Edit Mode (`ExecuteAlways`)
- Рекурсивное форматирование (подстановка до полного разрешения)

### Класс
```csharp
[RequireComponent(typeof(TMP_Text))]
[ExecuteAlways]
public class TMPFormater : MonoBehaviour
```

### Поля 
#### text
Шаблон строки, используемый системой `TMPFormater` для генерации итогового текста в `TMP_Text`.

Внутри строки могут использоваться плейсхолдеры вида `{Key}`, которые будут заменены значениями из объектов `ITMPFL`.
```csharp
public string text = "";
```

### Свойства
#### objectsForFormating { get; }
Возвращает массив объектов, реализующих интерфейс `ITMPFL`, найденных в родительских объектах текущего GameObjec
```csharp
public ITMPFL[] objectsForFormating { get; }
```
#### tmp { get; }
Возвращает массив объектов, реализующих интерфейс `ITMPFL`, найденных в родительских объектах текущего GameObjec
```csharp
public ITMPFL[] objectsForFormating { get; }
```

### Методы
#### Format(string, object[])
Форматирует строку, заменяя плейсхолдеры вида `{Key}` на значения из объектов, реализующих систему `ITMPFL`.
```csharp
public string Format(string input, object[] ITMPFs)
```

## ITMPFL {#itmpfl}
[./ITMPFL.cs](Assets/_Project/System/TMPFormaterSystem/ITMPFL.cs)

`ITMPFL` — маркерный интерфейс, используемый системой `TMPFormater` для обозначения объектов, которые могут предоставлять данные для динамического форматирования текста в `TMP_Text`.

Интерфейс не содержит методов или свойств, а служит исключительно для поиска и группировки компонентов-источников данных через `GetComponentsInParent<ITMPFL>()`.

### Интерфейс
```csharp
public interface ITMPFL
```

## [Assets/Rendering/RendererFeatures/Outline](Assets/Rendering/RendererFeatures/Outline)
## OutlineTarget
[./Auxiliary/OutlineTarget.cs](Assets/Rendering/RendererFeatures/Outline/Auxiliary/OutlineTarget.cs)

`OutlineTarget` — Unity-компонент, который регистрирует все `Renderer` в дочерних объектах и хранит их в статическом словаре для системы обводки (outline). Используется как целевой объект, который должен быть выделен эффектом обводки.

---

### 📦 Возможности

- Автоматическая регистрация всех `Renderer` в дочерних объектах
- Фильтрация объектов, исключённых из outline через:
  - `IgnoreTargetOutline`
  - `IIgnoreOutline`
- Хранение связки `Target → Renderers` в статическом словаре
- Автоматическое удаление данных при выключении объекта
- Поддержка runtime системы выделения объектов

---

### Класс
```csharp
public class OutlineTarget : MonoBehaviour
```

### Поля 
#### RenderersMap
Статический словарь, который хранит соответствие между `OutlineTarget` и списком `Renderer`, участвующих в системе обводки.
```csharp
public static readonly Dictionary<OutlineTarget, List<Renderer>> RenderersMap = new();
```
#### color
Цвет обводки для данного объекта.
```csharp
public Color color;
```
#### weight
Толщина (сила) обводки для данного объекта.
```csharp
public float weight;
```

### Методы
#### OnEnable()
Вызывается при активации объекта.

Собирает все `Renderer` в дочерних объектах, исключая те, которые находятся под компонентами `IgnoreTargetOutline` или `IIgnoreOutline`. После этого сохраняет список рендереров в статический словарь `RenderersMap` для дальнейшего использования системой обводки.
```csharp
void OnEnable()
```
#### OnDisable()
Вызывается при деактивации объекта.

Удаляет текущий `OutlineTarget` из `RenderersMap`, очищая его данные из системы обводки.
```csharp
void OnDisable()
```

## IgnoreTargetOutline & IIgnoreOutline {#ignoretargetoutline--iignoreoutline}
[./Auxiliary/IgnoreTargetOutline.cs](Assets/Rendering/RendererFeatures/Outline/Auxiliary/IgnoreTargetOutline.cs)

`IgnoreTargetOutline` и `IIgnoreOutline` — маркерные инструменты системы обводки, используемые для исключения объектов и их дочерних иерархий из обработки `OutlineTarget`.

Они позволяют гибко управлять тем, какие части сцены не должны участвовать в системе выделения (outline), даже если находятся внутри целевого объекта.

---

### 📦 Возможности

- Исключение объекта и всех его дочерних объектов из системы обводки
- Работает на уровне всей иерархии (parent → children)
- Поддержка двух способов игнорирования:
  - Компонент `IgnoreTargetOutline`
  - Интерфейс `IIgnoreOutline`
- Автоматическое применение при сборе `Renderer` в `OutlineTarget`
- Простая интеграция без дополнительной логики

---

### Класс
#### IgnoreTargetOutline
Маркерный компонент, который используется системой обводки для исключения объекта и всех его дочерних объектов из обработки `OutlineTarget`.

Если компонент присутствует в иерархии, то все Renderer внутри этого объекта и его дочерних объектов не будут добавлены в систему `RenderersMap`.
```csharp
public class IgnoreTargetOutline : MonoBehaviour
```
### Интерфейсы
#### IIgnoreOutline
Маркерный интерфейс, используемый системой обводки для исключения объекта и всех его дочерних объектов из обработки `OutlineTarget`.

Если компонент реализует `IIgnoreOutline`, то весь объектный поддерево (включая дочерние объекты) будет проигнорировано при сборе Renderer в `OutlineTarget`.
```csharp
public interface IIgnoreOutline
```

## [Assets/_Project/Runtime/Components/AimController](Assets/_Project/Runtime/Components/AimController)
## AimController {#aimcontroller}
[./AimController.cs](Assets/_Project/Runtime/Components/AimController/AimController.cs)

`AimController` — Unity-компонент для обработки системы прицеливания и управления жестами/тач-вводом. Отвечает за расчёт силы выстрела, угла поворота, состояний прицеливания (`AimStatus`) и генерацию событий (`AimEvents`) в процессе взаимодействия пользователя с экраном.

---

### 📦 Возможности

- Обработка тач-ввода и UI-raycast блокировок
- Расчёт силы выстрела (shot power) на основе смещения
- Расчёт угла поворота прицеливания
- Управление состояниями прицеливания через `AimStatus`
- Система событий (`onStart`, `onMove`, `onShot`, `onCancel`, `onMinDistanceBeginning`)
- Поддержка ограничений дистанции (`minDistance`, `maxDistance`)
- Поддержка Gizmos для визуализации зоны прицеливания
- Передача данных через `AimInfo` в `SendMessage`

---

### Класс

```csharp
public class AimController : MonoBehaviour
```

---

### Поля

#### aimEvents

Набор Unity-событий, вызываемых в разных состояниях прицеливания (старт, движение, выстрел, отмена, минимальная дистанция).

```csharp
public AimEvents aimEvents;
```

#### \_offsetTouch

Массив, хранящий начальную позицию касания (X, Y), используемую как базу для расчётов.

```csharp
public float[] _offsetTouch = new float[2];
```

#### controllers

Статический список всех активных `AimController` в сцене.

```csharp
public static List<AimController> controllers = new List<AimController>();
```

#### minDistance / maxDistance

Минимальная и максимальная дистанция прицеливания.

```csharp
public float minDistance = 0;
public float maxDistance = 1000;
```

#### layerIgnore

LayerMask для исключения объектов из взаимодействия (например UI или физика).

```csharp
public LayerMask layerIgnore;
```

#### offsetSencivity

Чувствительность смещения при расчёте силы выстрела.

```csharp
public float offsetSencivity = 0.009f;
```

#### status

Текущее состояние прицеливания (`AimStatus`).

```csharp
public AimStatus status;
```

#### blockedTouch

Флаг блокировки тач-ввода (например, если уже есть активный touch).

```csharp
public bool blockedTouch = false;
```

#### shotPower

Текущая рассчитанная сила выстрела.

```csharp
public float shotPower;
```

#### rotation

Текущий угол прицеливания в градусах.

```csharp
public float rotation;
```

#### touchPoint

Текущая позиция касания.

```csharp
public Vector2 touchPoint;
```

---

### Методы

#### Aim(Vector2, float, float, AimStatus)

Основной метод обновления состояния прицеливания. Отправляет `AimInfo` через `SendMessage` и вызывает соответствующие события в зависимости от состояния (`AimStatus`).

```csharp
public void Aim(Vector2 touchPoint, float shotPower, float rotation, AimStatus status)
```

---

#### HandleShot()

Обрабатывает завершение прицеливания и выполняет выстрел или отмену в зависимости от минимальной дистанции.

```csharp
public void HandleShot()
```

---

#### HandleAim(Vector2, Vector2)

Обрабатывает ввод прицеливания (позиция + чувствительность), рассчитывает силу и угол, управляет состояниями `Move`, `MinDistance`, `Started`, `Stay`.

```csharp
public void HandleAim(Vector2 _touchPoint, Vector2 sencivity)
```

---

#### HandleAim(Vector2)

Перегрузка `HandleAim` с дефолтной чувствительностью (`Vector2.one`).

```csharp
public void HandleAim(Vector2 _touchPoint)
```

---

#### HandleTouchAim()

Полная обработка тач-ввода через `Input.touchCount`, включая UI-блокировку через `EventSystem`, расчёт силы, угла и управление жизненным циклом прицеливания.

```csharp
public void HandleTouchAim()
```

---

#### CalculateRotation(Vector2, Vector2)

Возвращает угол поворота между текущей позицией и оффсетом.

```csharp
public float CalculateRotation(Vector2 position, Vector2 offset)
```

---

#### CalculateShotPover(Vector2, Vector2, Vector2)

Рассчитывает силу выстрела на основе расстояния между точками с учётом чувствительности.

```csharp
public float CalculateShotPover(Vector2 position, Vector2 offset, Vector2 sencivity)
```

---

#### MinDistance(float, float)

Проверяет, превышает ли сила выстрела минимальную дистанцию.

```csharp
public bool MinDistance(float minDistance, float shotPower)
```

---

#### OnDrawGizmos()

Отрисовывает визуальные Gizmos в редакторе Unity для отображения минимальной/максимальной дистанции и текущей силы выстрела.

```csharp
void OnDrawGizmos()
```
## [Assets/_Project/Runtime/Components/DynamicFace](Assets/_Project/Runtime/Components/DynamicFace)
## DynamicFace {#dynamicface}

[./DynamicFace.cs](Assets/_Project/Runtime/Components/DynamicFace/DynamicFace.cs)

`DynamicFace` — Unity-компонент, управляющий направлением взгляда персонажа (или объекта) на основе системы приоритетных “интересов” (`CodeOfInterest`). Используется для динамического управления глазами (`DynamicEye`) и автоматического переключения точки фокуса с таймерами и приоритетами.

---

### 📦 Возможности

* Управление направлением взгляда через систему приоритетов (`CodeOfInterest`)
* Поддержка нескольких источников интереса с таймером жизни
* Автоматическое переключение точки взгляда по приоритету
* Интеграция с системой `DynamicEye`
* Поддержка глобальных и локальных координат взгляда
* Автоматическое удаление устаревших интересов по таймеру
* Визуализация направления взгляда через Gizmos
* Поддержка анимации моргания (`EyesBlink`)

---

### Класс

```csharp
[ExecuteAlways]
public class DynamicFace : MonoBehaviour
```

---

### Enum

#### CodeOfInterest

Тип источника внимания (приоритета взгляда).

```csharp
public enum CodeOfInterest
```

* `Default` — базовое состояние
* `Touch` — касание пользователя
* `Target` — цель
* `Explosion` — взрыв
* `ExplosionGunshoot` — выстрел
* `ExplosionObject1` — объектный эффект 1
* `ExplosionObject2` — объектный эффект 2

---

### Вложенные классы

#### PointOfViewWithCodeOfInterest

Хранит точку интереса, её тип и таймер жизни.

```csharp
public class PointOfViewWithCodeOfInterest
```

##### Поля

#### pointOfView

Локальная точка интереса относительно объекта.

```csharp
public Vector2 pointOfView;
```

#### GPointOfView

Глобальная точка интереса (в мировых координатах).

```csharp
public Vector2 GPointOfView { get; set; }
```

#### codeOfInterest

Тип источника интереса (`CodeOfInterest`).

```csharp
public CodeOfInterest codeOfInterest;
```

#### timer

Время жизни точки интереса.

```csharp
public float timer = 0;
```

---

### Поля

#### pointOfView

Базовое направление взгляда, если нет активных интересов.

```csharp
public Vector2 pointOfView = Vector2.right;
```

#### linkedEyes

Список всех `DynamicEye`, привязанных к объекту (дочерние объекты).

```csharp
public List<DynamicEye> linkedEyes => GetComponentsInChildren<DynamicEye>().ToList();
```

#### codesOfInterest

Список приоритетов для определения важности точек интереса.

```csharp
public List<CodeOfInterest> codesOfInterest = new List<CodeOfInterest>();
```

#### pointsOfViewWithCodeOfInterest

Словарь активных точек интереса с их типами.

```csharp
public Dictionary<CodeOfInterest, PointOfViewWithCodeOfInterest> pointsOfViewWithCodeOfInterest
```

---

### Свойства

#### PointOfView

Возвращает текущую активную точку взгляда с учётом приоритетов.
Если есть активные интересы — выбирается самый приоритетный.

```csharp
public Vector2 PointOfView { get; set; }
```

---

#### GPointOfView

Глобальная версия точки взгляда (в мировых координатах).
Автоматически обновляет направление глаз.

```csharp
public Vector2 GPointOfView { get; set; }
```

---

### Методы

#### Update()

Обновляет:

* направление взгляда для каждого `DynamicEye`
* удаляет истёкшие интересы по таймеру
* пересчитывает текущую точку фокуса

```csharp
void Update()
```

---

#### UpdateEyes()

Принудительно обновляет все привязанные `DynamicEye`.

```csharp
public void UpdateEyes()
```

---

#### GetOrderOfCode(CodeOfInterest)

Возвращает индекс приоритета для указанного типа интереса.

```csharp
public int GetOrderOfCode(CodeOfInterest codeOfInterestToFound)
```

---

#### CreateInterestPosition(Vector2, CodeOfInterest, float)

Создаёт локальную точку интереса с таймером жизни.

```csharp
public PointOfViewWithCodeOfInterest CreateInterestPosition(Vector2 pointOfView, CodeOfInterest codeOfInterest, float timer)
```

---

#### CreateInterestGlobalPosition(Vector2, CodeOfInterest, float)

Создаёт глобальную точку интереса с таймером жизни.

```csharp
public PointOfViewWithCodeOfInterest CreateInterestGlobalPosition(Vector2 GPointOfView, CodeOfInterest codeOfInterest, float timer)
```

---

#### EyesBlink()

Запускает анимацию моргания через `Animator`.

```csharp
public void EyesBlink()
```

---

#### OnDrawGizmosSelected()

Отрисовывает Gizmos линиями от глаз до текущей точки взгляда.

```csharp
void OnDrawGizmosSelected()
```

## DynamicEye {#dynamiceye}

[./DynamicEye.cs](Assets/_Project/Runtime/Components/DynamicFace/DynamicEyes/DynamicEye.cs)

`DynamicEye` — Unity-компонент, отвечающий за процедурное управление “глазом” и “зрачком” через SpriteRenderer. Используется совместно с `DynamicFace` для динамического отслеживания точки интереса и визуального поворота взгляда персонажа.

---

### 📦 Возможности

* Процедурное создание и управление объектами глаза и зрачка
* Автоматическая генерация `SpriteRenderer` в рантайме
* Поддержка позиционирования зрачка в локальных и глобальных координатах
* Управление масштабом глаза и зрачка через `EyeFrame` и `PupilFrame`
* Поддержка сортировки слоёв рендера (`sortingOrder`)
* Интеграция с системой `DynamicFace`
* Визуализация границ глаза и зрачка через Gizmos
* Работа в режиме `ExecuteAlways` (в редакторе и рантайме)

---

### Класс

```csharp
[ExecuteAlways]
public class DynamicEye : MonoBehaviour
```

---

### Вложенные классы

#### EyeFrame

Параметры визуального состояния глаза.

```csharp
public class EyeFrame
```

##### Поля

#### scale

Масштаб глаза.

```csharp
public float scale;
```

#### offset

Смещение глаза.

```csharp
public Vector2 offset;
```

---

#### PupilFrame

Параметры визуального состояния зрачка.

```csharp
public class PupilFrame
```

##### Поля

#### scale

Масштаб зрачка.

```csharp
public float scale;
```

#### offset

Смещение зрачка.

```csharp
public Vector2 offset;
```

---

### Поля

#### pupil / eye

Спрайты зрачка и глаза.

```csharp
public Sprite pupil;
public Sprite eye;
```

---

#### pupilPosOne

Нормализованная позиция зрачка (вектор направления).

```csharp
public Vector2 pupilPosOne = new Vector2(1,1);
```

---

#### LocalPupilPos

Локальная позиция зрачка внутри глаза с учётом масштабов.

```csharp
public Vector2 LocalPupilPos { get; set; }
```

---

#### GPupilsPos

Глобальная позиция зрачка в мировых координатах.

```csharp
public Vector2 GPupilsPos { get; set; }
```

---

#### pupilScale / eyeScale

Масштаб зрачка и глаза.

```csharp
public Vector2 pupilScale = new Vector2(0,0);
public Vector2 eyeScale = new Vector2(0,0);
```

---

#### sortingOrder

Порядок отрисовки спрайтов.

```csharp
public int pupilsSortingOrder = 0;
public int eyeSortingOrder = 0;
```

---

#### pupilTransform / eyeTransform

Ссылки на созданные игровые объекты зрачка и глаза.

```csharp
public Transform pupilTransform;
public Transform eyeTransform;
```

---

#### eyeFrame / pupilFrame

Конфигурация состояния глаза и зрачка.

```csharp
public EyeFrame eyeFrame;
public PupilFrame pupilFrame;
```

---

### Методы

#### Update()

Основной метод обновления:

* создаёт объекты глаза и зрачка при необходимости
* обновляет позиции и масштабы
* применяет спрайты и sortingOrder
* рассчитывает позицию зрачка

```csharp
public void Update()
```

---

#### CreatePupil()

Создаёт объект зрачка и добавляет `SpriteRenderer`, если он отсутствует.

```csharp
void CreatePupil()
```

---

#### CreateEye()

Создаёт объект глаза и добавляет `SpriteRenderer`, если он отсутствует.

```csharp
void CreateEye()
```

---

#### GetAngle(Vector2, Vector2)

Возвращает угол между двумя точками в градусах.

```csharp
float GetAngle(Vector2 pointA, Vector2 pointB)
```

---

#### OnDrawGizmosSelected()

Отрисовывает радиусы глаза и зрачка в редакторе Unity.

```csharp
void OnDrawGizmosSelected()
```

***

## [Assets/_Project/Runtime/Player/Tools](Assets/_Project/Runtime/Player/Tools)
## PlayerToolBase

[./PlayerToolBase.cs](Assets/_Project/Runtime/Player/Tools/Components/PlayerToolBase.cs)

`PlayerToolBase` — базовый Unity-компонент инструмента игрока, который объединяет систему прицеливания (`AimController`), управление стрелкой направления, анимациями, звуком и стандартным поведением взаимодействия с `AimInfo`. Используется как основа для всех игровых инструментов (оружие, способности, взаимодействия).

---

### 📦 Возможности

* Управление стрелкой направления (ArrowController)
* Поддержка системы прицеливания через `AimController` и `AimInfo`
* Централизованная система анимаций с переходами и таймингами
* Поддержка UnityEvent для событий анимаций
* Воспроизведение звуков через AudioSource
* Базовая схема обработки Aim-состояний (`DefaultAimSheme`)
* Управление замедлением времени и blackout через `GameController`
* Автоматическое обновление анимаций и стрелки в `Update`
* Поддержка очередей анимационных переходов с таймаутами

---

### Класс

```csharp
public class PlayerToolBase : MonoBehaviour
```

---

### Поля

#### arrowController

Контроллер стрелки направления, управляющий визуализацией направления и длины выстрела/действия.

```csharp
public ArrowController arrowController;
```

#### BlackoutScaleProgress

Кривая анимации для управления интенсивностью blackout-эффекта.

```csharp
public AnimationCurve BlackoutScaleProgress;
```

#### audioSource

Источник звука, используемый для воспроизведения аудиоэффектов инструмента.

```csharp
public AudioSource audioSource;
```

#### toolContainer

Контейнер, связанный с текущим инструментом игрока.

```csharp
public ToolContainer toolContainer;
```

---

### Свойства

#### playerRb2D

Возвращает `Rigidbody2D` базового игрока.

```csharp
public Rigidbody2D playerRb2D { get; }
```

#### player

Возвращает компонент `Player` из родительского объекта.

```csharp
public Player player { get; }
```

#### basePlayer

Возвращает базовый игровой объект игрока (`BasePlayer`).

```csharp
public BasePlayer basePlayer { get; }
```

#### aimController

Возвращает компонент системы прицеливания (`AimController`).

```csharp
public AimController aimController { get; }
```

#### gameController

Возвращает глобальный `GameController.Instance`.

```csharp
public GameController gameController { get; }
```

#### isAnyPlayingAnimations

Проверяет, проигрывается ли хотя бы одна анимация в списке `animations`.

```csharp
public bool isAnyPlayingAnimations { get; }
```

---

### Методы

#### PlayAnimation(string animationName)

Запускает анимацию по её идентификатору (`id`) из списка `animations`.
Если анимация не найдена или игра не запущена — возвращает `null`.

```csharp
public AnimationTransition PlayAnimation(string animationName)
```

---

#### PlayAnimationEmpty(string animationName)

Обёртка над `PlayAnimation`, используется для UnityEvent/инспектора.

```csharp
public void PlayAnimationEmpty(string animationName)
```

---

#### PlaySound(AudioClip audioClip)

Воспроизводит указанный аудиоклип через `AudioSource`.

```csharp
public void PlaySound(AudioClip audioClip)
```

---

#### DefaultAimSheme(AimInfo aimInfo)

Базовая логика обработки состояний прицеливания:

* управление поворотом объекта
* управление стрелкой направления
* управление метатаймом и blackout эффектом

```csharp
protected void DefaultAimSheme(AimInfo aimInfo)
```

---

#### OnDestroy()

Сбрасывает состояния метатайма и blackout при уничтожении объекта.

```csharp
void OnDestroy()
```

---

#### Update()

Обновляет:

* активные анимации (`AnimationTransition.Update`)
* стрелку направления (`arrowController.UpdateArrow`)

```csharp
void Update()
```

***

## [Assets/_Project/Runtime/Player](Assets/_Project/Runtime/Player)
## BasePlayer {#baseplayer}

[./BasePlayer.cs](Assets/_Project/Runtime/Player/BasePlayer.cs)

`BasePlayer` — базовый игровой компонент игрока, объединяющий управление скином, физикой, направлением движения, визуальной синхронизацией, инструментами и системами анимации. Наследуется от `DamageBehaviour` и используется как основа всех игровых сущностей игрока.

---

### 📦 Возможности

* Управление и замена скинов (`Skin system`)
* Синхронизация поворота игрока с `Rigidbody2D` скоростью
* Автоматическое отражение спрайта и инструментов по направлению движения
* Поддержка динамической анимации через `Animator`
* Доступ к `ToolContainer` и системе инструментов игрока
* Полная замена объекта игрока через `ReplaceFull`
* Поддержка `DynamicFace` (система взгляда)
* Работа в режиме `ExecuteAlways` (Editor + PlayMode)
* Поддержка контекстного обновления скина

---

### Класс

```csharp
[ExecuteAlways]
public class BasePlayer : DamageBehaviour, IBasePlayer
```

---

### Поля и свойства

#### toolContainer

Возвращает контейнер инструментов игрока (из дочерних объектов).

```csharp
public ToolContainer toolContainer { get; }
```

---

#### skin

Текущий скин игрока. При установке:

* удаляет старые скины
* создаёт новый экземпляр
* вызывает `OnSkinChange`

```csharp
public Skin skin { get; set; }
```

---

#### Face

Возвращает компонент `DynamicFace`, отвечающий за направление взгляда.

```csharp
public DynamicFace Face { get; }
```

---

#### animator

Возвращает `Animator` игрока.

```csharp
public Animator animator { get; }
```

---

### Методы

#### OnSkinChange(Skin newSkin)

Виртуальный метод, вызываемый при смене скина.

```csharp
public virtual void OnSkinChange(Skin newSkin)
```

---

#### AlignToVelocity()

Синхронизирует:

* позицию игрока с `Rigidbody2D`
* поворот по направлению скорости
* зеркалирование (flip) персонажа и инструментов

```csharp
public void AlignToVelocity()
```

---

#### ReplaceFull(GameObject prefab)

Полностью заменяет объект игрока:

* создаёт новый prefab
* переносит позицию/вращение/scale
* переносит скин
* сбрасывает физику
* уничтожает старый объект

```csharp
public GameObject ReplaceFull(GameObject prefab)
```

---

#### RefreshSkin()

Контекстная функция (Inspector), принудительно пересоздаёт текущий скин.

```csharp
[ContextMenu("Refresh Skin")]
private void RefreshSkin()
```

---

### Мини-описание системы

`BasePlayer` является ядром игрока, связывающим:

* физику (`Rigidbody2D`)
* визуал (`Skin`, `Animator`)
* поведение (`DamageBehaviour`)
* управление инструментами (`ToolContainer`)
* ориентацию персонажа в мире (через скорость движения)

Он используется как базовый слой для всех расширений игрока (оружие, способности, визуальные эффекты и т.д.).

## PlayerBot {#playerbot}

[./Bot/PlayerBot.cs](Assets/_Project/Runtime/Player/Bot/PlayerBot.cs)

`PlayerBot` — расширение базового игрока (`BasePlayer`), реализующее поведение управляемого или AI-бота. Добавляет логику разрушения, задержанного удаления, реакции на урон и ограничение поворота/выравнивания при столкновениях.

---

### 📦 Возможности

* Наследование всей логики `BasePlayer`
* Обработка урона с визуальным эффектом `DamageFlash`
* Автоматическое уничтожение объекта после смерти с задержкой
* Очистка инструментов при уничтожении
* Ограничение выравнивания по скорости при столкновениях
* Контроль физики движения после разрушения
* Отключение `Animator Controller` при инициализации
* Поддержка временной блокировки вращения (`vectorOfFlyEnabled`)

---

### Класс

```csharp
public class PlayerBot : BasePlayer
```

---

### Поля

#### vectorOfFlyEnabled

Флаг, определяющий можно ли выравнивать бота по скорости движения.
Отключается при столкновении с объектами.

```csharp
private bool vectorOfFlyEnabled = true;
```

---

#### destroyTimerStarted

Флаг, предотвращающий повторный запуск таймера уничтожения после смерти.

```csharp
private bool destroyTimerStarted = false;
```

---

#### destroyDelay

Задержка перед уничтожением объекта после смерти.

```csharp
public float destroyDelay = 3f;
```

---

#### defaultToolDefinition

Дефолтное определение инструмента (используется как базовая настройка бота).

```csharp
public ToolDefinition defaultToolDefinition;
```

---

### Методы

#### ApplyDamageUpdate(DamageInfo damageInfo)

Обрабатывает получение урона:

* если бот жив — применяет базовый урон и запускает `DamageFlash`
* если бот уничтожен:

  * замедляет физику
  * ограничивает скорость
  * очищает инструменты
  * запускает таймер уничтожения

```csharp
public override void ApplyDamageUpdate(DamageInfo damageInfo)
```

---

#### DestroyAfterDelay()

Корутина, уничтожающая объект через `destroyDelay` секунд после смерти.

```csharp
private IEnumerator DestroyAfterDelay()
```

---

#### Awake()

Сброс `Animator Controller` при создании объекта (фиксирует состояние анимации).

```csharp
void Awake()
```

---

#### OnCollisionEnter2D(Collision2D collisionInfo2D)

Отключает выравнивание по скорости при столкновении.

```csharp
void OnCollisionEnter2D(Collision2D collisionInfo2D)
```

---

#### OnCollisionExit2D(Collision2D collisionInfo2D)

Восстанавливает выравнивание после выхода из столкновения.

```csharp
void OnCollisionExit2D(Collision2D collisionInfo2D)
```

---

#### LateUpdate()

Если нет активного столкновения — синхронизирует поворот с направлением скорости через `AlignToVelocity()`.

```csharp
private void LateUpdate()
```

---

### Краткое поведение

`PlayerBot` — это физически активный игрок-бот, который:

* реагирует на урон и умирает с задержкой
* теряет инструменты при смерти
* управляется физикой (Rigidbody2D)
* временно отключает авто-ориентацию при столкновениях
* наследует всю базовую систему игрока (`BasePlayer`)

## BaseBotBehavior {#basebotbehavior}

[./Bot/Behaviors/BaseBotBehavior.cs](Assets/_Project/Runtime/Player/Bot/Behaviors/BaseBotBehavior.cs)

`BaseBotBehavior` — базовый компонент поведения бота, отвечающий за логику AI-обновлений и отладочного режима в редакторе. Предоставляет точку расширения для реализации поведения ботов, а также вспомогательные утилиты для перемещения по точкам.

---

### 📦 Возможности

* Разделение логики поведения:

  * runtime (`OnBotBehaviorUpdate`)
  * editor debug (`OnBotDebug`)
* Автоматическое получение ссылки на `PlayerBot`
* Проверка состояния уничтожения бота
* Доступ ко всем `AimController` внутри объекта
* Утилита перемещения по списку точек (`MoveTowardsAxis`)
* Поддержка пошаговой навигации по waypoint-ам
* Работает в режиме `ExecuteInEditMode` для отладки в редакторе

---

### Класс

```csharp
[ExecuteInEditMode]
public class BaseBotBehavior : MonoBehaviour
```

---

### Свойства

#### bot

Возвращает компонент `PlayerBot`, прикреплённый к текущему объекту.

```csharp
public PlayerBot bot => GetComponent<PlayerBot>();
```

---

#### botIsDestroyed

Возвращает состояние уничтожения бота (`IsDestroyed` у `PlayerBot`).

```csharp
public bool botIsDestroyed => bot.IsDestroyed;
```

---

#### aimControllers

Возвращает все `AimController`, находящиеся в дочерних объектах бота.

```csharp
public AimController[] aimControllers => GetComponentsInChildren<AimController>();
```

---

### Методы

#### Update()

Основной цикл обновления:

* В редакторе вызывает `OnBotDebug()`
* В игре вызывает `OnBotBehaviorUpdate()`

```csharp
void Update()
```

---

#### MoveTowardsAxis(Vector2, List<Vector2>, ref int, Vector2, float)

Утилита перемещения объекта по списку точек с учётом скорости по осям.

Позволяет:

* двигаться к текущей точке пути
* автоматически переключаться на следующую точку
* учитывать скорость по X и Y отдельно
* работать с нормализованным временем шага

```csharp
public static Vector2 MoveTowardsAxis(
    Vector2 current,
    List<Vector2> waypoints,
    ref int index,
    Vector2 speed,
    float dt)
```

---

#### OnBotBehaviorUpdate()

Виртуальный метод, вызываемый в режиме игры. Используется для реализации логики AI.

```csharp
public virtual void OnBotBehaviorUpdate() { }
```

---

#### OnBotDebug()

Виртуальный метод, вызываемый только в редакторе (`Edit Mode`). Используется для визуальной отладки поведения бота.

```csharp
public virtual void OnBotDebug() { }
```

---

### Краткое поведение

`BaseBotBehavior` — это каркас AI-системы бота, который:

* разделяет runtime и debug логику
* предоставляет доступ к компонентам бота
* даёт базовую систему перемещения по waypoint-ам
* предназначен для наследования и расширения поведения

## [Assets/_Project/Runtime/Database](Assets/_Project/Runtime/Database)
## LocalDB {#localdb}

[./LocalDB.cs](Assets/_Project/Runtime/Database/LocalDB.cs)

`LocalDB` — центральная система управления локальной базой данных игры и синхронизацией с Supabase. Отвечает за SQLite-хранилище, кэширование пользовательских данных, работу с файловой системой, сериализацию, синхронизацию магазина и интеграцию с облачной БД.

---

### 📦 Возможности

* Управление несколькими SQLite подключениями (`Connections`)
* Автоматическая инициализация локальных баз из StreamingAssets
* Кроссплатформенная работа с файлами (Android + Desktop)
* Кэширование пользовательских данных (`UserMeta`)
* Система синхронизации магазина (`ShopExitSync`)
* Интеграция с Supabase (auth, RPC, Postgrest)
* Выполнение SQL команд с логированием (`DBMeta.RunCmd`)
* Фильтрация логов через ignore-паттерны
* XML сериализация/десериализация объектов
* Unity Editor утилиты (очистка, просмотр БД, выбор файлов)
* Асинхронная авторизация и загрузка метаданных пользователя
* Лидерборд через Supabase RPC
* Безопасное обновление кэша при изменениях данных

---

### Основной класс

```csharp
public class LocalDB
```

---

### 📌 Singleton

#### Instance

Глобальный доступ к LocalDB.

```csharp
public static LocalDB Instance;
```

---

### 📦 Подсистемы

#### Supabase

Обёртка над API Supabase (авторизация, RPC, Postgrest).

```csharp
public SupabaseAPI Supabase = new SupabaseAPI();
```

---

#### Connections

Словарь открытых SQLite подключений.

```csharp
public Dictionary<string, DBMeta> Connections;
```

---

### ⚙️ Settings

#### Settings

Глобальные настройки БД (ScriptableObject).

```csharp
public static ElysiumDBSettings Settings => ElysiumDBSettings.instance;
```

---

### 🌐 Platform

#### IsOffline

Проверка отсутствия интернета.

```csharp
public static bool IsOffline => Application.internetReachability == NetworkReachability.NotReachable;
```

---

#### PlatformDataPath

Путь хранения локальных баз.

```csharp
public static string PlatformDataPath
```

---

### 👤 User Data

#### UserMeta

Кэшированная информация о текущем пользователе.

* ленивое обновление
* SQL запрос при устаревании кэша
* хранит значения из `players_meta`

```csharp
public Dictionary<string, object> UserMeta
```

---

#### InvalidateUserMetaCache()

Сброс кэша пользователя.

```csharp
public void InvalidateUserMetaCache()
```

---

### 🚀 Инициализация

#### New()

Основной bootstrap системы:

* закрывает старые подключения
* очищает Connections
* читает список БД из `streamingassetssql`
* копирует файлы в persistent storage
* открывает SQLite подключения
* создаёт `DBMeta`
* сбрасывает кэш пользователя

```csharp
public void New()
```

---

#### Init()

Editor метод инициализации системы.

```csharp
public static void Init()
```

---

### 💾 Shop System

#### ShopExitSync(int, List<string>, List<string>)

Синхронизация данных магазина:

* обновление денег
* сохранённые предметы
* выбранные предметы
* сериализация через XML
* запись в SQLite
* сброс кэша

```csharp
public void ShopExitSync(int newMoney, List<string> choosedItemsIds, List<string> purchasedItems)
```

---

#### SupabaseSync()

(закомментированная) синхронизация SQLite → Supabase.

```csharp
public void SupabaseSync()
```

---

### 📁 File Utils

#### LoadFileBytes(string path)

Загрузка файла:

* Android → UnityWebRequest
* Desktop → File.ReadAllBytes

```csharp
private static byte[] LoadFileBytes(string path)
```

---

#### EnsureFileExists(string, byte[])

Создание файла при отсутствии.

```csharp
private static void EnsureFileExists(string path, byte[] bytes)
```

---

### 🧾 XML Utils

#### Serialize(object)

Сериализация объекта в XML (UTF-8).

```csharp
public static string Serialize(object obj)
```

---

#### Deserialize<T>(string)

Десериализация XML в объект.

```csharp
public static T Deserialize<T>(string xml)
```

---

#### Utf8StringWriter

Переопределение Encoding для XML.

```csharp
public class Utf8StringWriter : StringWriter
```

---

#### DbStringArray(object)

Парсинг строки в массив через `,`.

```csharp
public static string[] DbStringArray(object obj)
```

---

### 🧠 Supabase API

## SupabaseAPI {#supabaseapi}

```csharp
public class SupabaseAPI
```

### 📦 Возможности

* JWT авторизация
* RPC вызовы Supabase
* загрузка playerMeta
* обновление username
* обновление полей таблицы
* Postgrest CRUD операции

---

### Поля

#### playerMeta

JSON метаданные пользователя.

```csharp
public JObject playerMeta;
```

---

#### isAuthenticated

Флаг авторизации.

```csharp
public bool isAuthenticated;
```

---

### Методы

#### Init(string)

Инициализация с JWT.

```csharp
public async Task<bool> Init(string savedJWT)
```

---

#### UpdateAuth(string)

Создаёт Postgrest клиент + получает метаданные пользователя через RPC.

```csharp
public async Task<bool> UpdateAuth(string JWT)
```

---

#### AuthWithUsername(string, string)

Авторизация через username/password RPC.

```csharp
public async Task<bool> AuthWithUsername(string username, string password)
```

---

#### UpdateMetaInfo(Expression, object)

Обновление конкретного поля таблицы.

```csharp
public async Task UpdateMetaInfo(Expression<Func<PlayerMetaTableRow, object>> keySelector, object value)
```

---

#### UpdateUsername(string)

RPC смена username.

```csharp
public async Task UpdateUsername(string username)
```

---

### 📊 DBMeta {#dbmeta}

## DBMeta

```csharp
public class DBMeta
```

### 📦 Возможности

* выполнение SQL запросов
* логирование запросов
* фильтрация логов
* чтение данных через IDataReader
* поддержка Caller info attributes

---

### Поля

#### connection

SQLite соединение.

```csharp
public IDbConnection connection;
```

---

### Методы

#### RunCmd(string, int)

Выполняет SQL запрос:

* логирует запрос
* применяет ignore-фильтры
* выполняет ExecuteReader
* поддерживает skip строк

```csharp
public IDataReader RunCmd(string cmd, int linesToRead = 0)
```

---

### 🧑 UserScore {#userscore}

## UserScore

```csharp
public class UserScore
```

Модель лидерборда Supabase.

### Поля

```csharp
public string id;
public string user_name;
public int score;
```

---

### 🧩 Editor Tools

## DBSelectorWindow

```csharp
public class DBSelectorWindow : EditorWindow
```

### 📦 Возможности

* просмотр всех локальных БД
* открытие файлов через Explorer/Finder
* проверка существования файлов
* Unity Editor окно

---

### Методы

#### ShowWindow()

Открывает окно выбора БД.

```csharp
[MenuItem("LocalDB/Open/Select DB...")]
public static void ShowWindow()
```

---

#### OnGUI()

UI списка баз:

* кнопки для каждой БД
* открытие файла
* логирование отсутствующих файлов

```csharp
void OnGUI()
```

---

### 🧠 Мини-описание системы

`LocalDB` — это гибридная система:

* локальная SQLite база данных
* облачная синхронизация Supabase
* кэширование игровых данных
* файловая система Unity
* редакторские инструменты
* система магазинов и профиля игрока

Она выступает как единый слой данных между:

* игровым клиентом
* локальным хранилищем
* серверной БД (Supabase)




```text
📁 Assets
├── 📁 Adaptive Performance
│   ├── 📄 AdaptivePerformanceGeneralSettings.asset
│   ├── 📁 Provider
│   │   └── 📄 Samsung Android Provider Loader.asset
│   └── 📁 Settings
│       ├── 📄 Samsung Android Provider Settings.asset
│       └── 📄 Simulator Provider Settings.asset
├── 📁 Editor
│   ├── 📁 com.unity.mobile.notifications
│   │   └── 📄 NotificationSettings.asset
│   └── 📁 PngPrefabPreviewer
│       ├── 📄 PreviewMaker.cs
│       └── 📁 Window
│           └── 📄 MakePreviewSettings.cs
├── 📁 LiteSQLCustom
│   ├── 📄 SqliteCommandNative.cs
│   ├── 📄 SqliteConnectionNative.cs
│   ├── 📄 SqliteDataReaderNative.cs
│   └── 📄 SQLiteNative.cs
├── 📄 NuGet.config
├── 📁 Packages
│   ├── 📁 Microsoft.Bcl.AsyncInterfaces.1.1.0
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.1
│   │   │       ├── 📄 Microsoft.Bcl.AsyncInterfaces.dll
│   │   │       └── 📄 Microsoft.Bcl.AsyncInterfaces.xml
│   │   ├── 📄 LICENSE.TXT
│   │   ├── 📄 Microsoft.Bcl.AsyncInterfaces.nuspec
│   │   ├── 📄 THIRD-PARTY-NOTICES.TXT
│   │   ├── 📄 useSharedDesignerContext.txt
│   │   └── 📄 version.txt
│   ├── 📁 Microsoft.Extensions.DependencyInjection.Abstractions.8.0.0
│   │   ├── 📁 buildTransitive
│   │   │   ├── 📁 net461
│   │   │   │   └── 📄 Microsoft.Extensions.DependencyInjection.Abstractions.targets
│   │   │   ├── 📁 net462
│   │   │   │   └── 📄 _._
│   │   │   ├── 📁 net6.0
│   │   │   │   └── 📄 _._
│   │   │   └── 📁 netcoreapp2.0
│   │   │       └── 📄 Microsoft.Extensions.DependencyInjection.Abstractions.targets
│   │   ├── 📄 Icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.1
│   │   │       ├── 📄 Microsoft.Extensions.DependencyInjection.Abstractions.dll
│   │   │       └── 📄 Microsoft.Extensions.DependencyInjection.Abstractions.xml
│   │   ├── 📄 LICENSE.TXT
│   │   ├── 📄 Microsoft.Extensions.DependencyInjection.Abstractions.nuspec
│   │   ├── 📄 PACKAGE.md
│   │   ├── 📄 THIRD-PARTY-NOTICES.TXT
│   │   └── 📄 useSharedDesignerContext.txt
│   ├── 📁 Microsoft.Extensions.Logging.Abstractions.8.0.0
│   │   ├── 📁 analyzers
│   │   ├── 📁 buildTransitive
│   │   │   ├── 📁 net461
│   │   │   │   └── 📄 Microsoft.Extensions.Logging.Abstractions.targets
│   │   │   ├── 📁 net462
│   │   │   │   └── 📄 Microsoft.Extensions.Logging.Abstractions.targets
│   │   │   ├── 📁 net6.0
│   │   │   │   └── 📄 Microsoft.Extensions.Logging.Abstractions.targets
│   │   │   ├── 📁 netcoreapp2.0
│   │   │   │   └── 📄 Microsoft.Extensions.Logging.Abstractions.targets
│   │   │   └── 📁 netstandard2.0
│   │   │       └── 📄 Microsoft.Extensions.Logging.Abstractions.targets
│   │   ├── 📄 Icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Microsoft.Extensions.Logging.Abstractions.dll
│   │   │       └── 📄 Microsoft.Extensions.Logging.Abstractions.xml
│   │   ├── 📄 LICENSE.TXT
│   │   ├── 📄 Microsoft.Extensions.Logging.Abstractions.nuspec
│   │   ├── 📄 PACKAGE.md
│   │   ├── 📄 THIRD-PARTY-NOTICES.TXT
│   │   └── 📄 useSharedDesignerContext.txt
│   ├── 📁 Microsoft.IdentityModel.Abstractions.7.5.1
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Microsoft.IdentityModel.Abstractions.dll
│   │   │       └── 📄 Microsoft.IdentityModel.Abstractions.xml
│   │   └── 📄 Microsoft.IdentityModel.Abstractions.nuspec
│   ├── 📁 Microsoft.IdentityModel.JsonWebTokens.7.5.1
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Microsoft.IdentityModel.JsonWebTokens.dll
│   │   │       └── 📄 Microsoft.IdentityModel.JsonWebTokens.xml
│   │   └── 📄 Microsoft.IdentityModel.JsonWebTokens.nuspec
│   ├── 📁 Microsoft.IdentityModel.Logging.7.5.1
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Microsoft.IdentityModel.Logging.dll
│   │   │       └── 📄 Microsoft.IdentityModel.Logging.xml
│   │   └── 📄 Microsoft.IdentityModel.Logging.nuspec
│   ├── 📁 Microsoft.IdentityModel.Tokens.7.5.1
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Microsoft.IdentityModel.Tokens.dll
│   │   │       └── 📄 Microsoft.IdentityModel.Tokens.xml
│   │   └── 📄 Microsoft.IdentityModel.Tokens.nuspec
│   ├── 📁 Microsoft.IO.RecyclableMemoryStream.3.0.0
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.1
│   │   │       ├── 📄 Microsoft.IO.RecyclableMemoryStream.dll
│   │   │       └── 📄 Microsoft.IO.RecyclableMemoryStream.xml
│   │   ├── 📄 Microsoft.IO.RecyclableMemoryStream.nuspec
│   │   └── 📄 README.md
│   ├── 📁 MimeMapping.3.0.1
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 MimeMapping.dll
│   │   │       └── 📄 MimeMapping.xml
│   │   ├── 📄 MimeMapping.nuspec
│   │   └── 📄 README.md
│   ├── 📁 Newtonsoft.Json.13.0.3
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Newtonsoft.Json.dll
│   │   │       └── 📄 Newtonsoft.Json.xml
│   │   ├── 📄 LICENSE.md
│   │   ├── 📄 Newtonsoft.Json.nuspec
│   │   ├── 📄 packageIcon.png
│   │   └── 📄 README.md
│   ├── 📁 sqlite-net.1.6.292
│   │   ├── 📁 content
│   │   │   ├── 📄 SQLiteAsync.cs
│   │   │   └── 📄 SQLite.cs
│   │   └── 📄 sqlite-net.nuspec
│   ├── 📁 sqlite-net-pcl.1.9.172
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 SQLite-net.dll
│   │   │       └── 📄 SQLite-net.xml
│   │   ├── 📄 LICENSE.txt
│   │   ├── 📄 Logo-low.png
│   │   └── 📄 sqlite-net-pcl.nuspec
│   ├── 📁 SQLitePCLRaw.bundle_green.2.1.2
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       └── 📄 SQLitePCLRaw.batteries_v2.dll
│   │   └── 📄 SQLitePCLRaw.bundle_green.nuspec
│   ├── 📁 SQLitePCLRaw.core.2.1.2
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       └── 📄 SQLitePCLRaw.core.dll
│   │   └── 📄 SQLitePCLRaw.core.nuspec
│   ├── 📁 SQLitePCLRaw.lib.e_sqlite3.2.1.2
│   │   ├── 📁 buildTransitive
│   │   │   ├── 📁 net461
│   │   │   │   └── 📄 SQLitePCLRaw.lib.e_sqlite3.targets
│   │   │   ├── 📁 net6.0
│   │   │   │   └── 📄 SQLitePCLRaw.lib.e_sqlite3.targets
│   │   │   └── 📁 net7.0
│   │   │       └── 📄 SQLitePCLRaw.lib.e_sqlite3.targets
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       └── 📄 _._
│   │   ├── 📁 runtimes
│   │   │   ├── 📁 linux-x64
│   │   │   │   └── 📁 native
│   │   │   │       └── 📄 libe_sqlite3.so
│   │   │   ├── 📁 osx-arm64
│   │   │   │   └── 📁 native
│   │   │   │       └── 📄 libe_sqlite3.dylib
│   │   │   ├── 📁 osx-x64
│   │   │   │   └── 📁 native
│   │   │   │       └── 📄 libe_sqlite3.dylib
│   │   │   ├── 📁 win-x64
│   │   │   │   └── 📁 native
│   │   │   │       └── 📄 e_sqlite3.dll
│   │   │   └── 📁 win-x86
│   │   │       └── 📁 native
│   │   │           └── 📄 e_sqlite3.dll
│   │   └── 📄 SQLitePCLRaw.lib.e_sqlite3.nuspec
│   ├── 📁 SQLitePCLRaw.provider.e_sqlite3.2.1.2
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       └── 📄 SQLitePCLRaw.provider.e_sqlite3.dll
│   │   └── 📄 SQLitePCLRaw.provider.e_sqlite3.nuspec
│   ├── 📁 Supabase.1.1.1
│   │   ├── 📄 icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.1
│   │   │       ├── 📄 Supabase.dll
│   │   │       └── 📄 Supabase.xml
│   │   ├── 📄 README.md
│   │   └── 📄 Supabase.nuspec
│   ├── 📁 Supabase.Core.1.0.0
│   │   ├── 📄 icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Supabase.Core.dll
│   │   │       └── 📄 Supabase.Core.xml
│   │   ├── 📄 README.md
│   │   └── 📄 Supabase.Core.nuspec
│   ├── 📁 Supabase.Functions.2.0.0
│   │   ├── 📄 icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Supabase.Functions.dll
│   │   │       └── 📄 Supabase.Functions.xml
│   │   ├── 📄 README.md
│   │   └── 📄 Supabase.Functions.nuspec
│   ├── 📁 Supabase.Gotrue.6.0.3
│   │   ├── 📄 icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.1
│   │   │       ├── 📄 Supabase.Gotrue.dll
│   │   │       └── 📄 Supabase.Gotrue.xml
│   │   ├── 📄 README.md
│   │   └── 📄 Supabase.Gotrue.nuspec
│   ├── 📁 Supabase.Postgrest.4.1.0
│   │   ├── 📄 icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Supabase.Postgrest.dll
│   │   │       └── 📄 Supabase.Postgrest.xml
│   │   ├── 📄 README.md
│   │   └── 📄 Supabase.Postgrest.nuspec
│   ├── 📁 Supabase.Realtime.7.0.2
│   │   ├── 📄 icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.1
│   │   │       ├── 📄 Supabase.Realtime.dll
│   │   │       └── 📄 Supabase.Realtime.xml
│   │   ├── 📄 README.md
│   │   └── 📄 Supabase.Realtime.nuspec
│   ├── 📁 Supabase.Storage.2.0.2
│   │   ├── 📄 icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 Supabase.Storage.dll
│   │   │       └── 📄 Supabase.Storage.xml
│   │   ├── 📄 README.md
│   │   └── 📄 Supabase.Storage.nuspec
│   ├── 📁 System.IdentityModel.Tokens.Jwt.7.5.1
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 System.IdentityModel.Tokens.Jwt.dll
│   │   │       └── 📄 System.IdentityModel.Tokens.Jwt.xml
│   │   └── 📄 System.IdentityModel.Tokens.Jwt.nuspec
│   ├── 📁 System.Reactive.6.0.0
│   │   ├── 📁 buildTransitive
│   │   │   ├── 📁 net6.0
│   │   │   │   └── 📄 _._
│   │   │   └── 📁 net6.0-windows10.0.19041
│   │   │       └── 📄 _._
│   │   ├── 📄 icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 System.Reactive.dll
│   │   │       └── 📄 System.Reactive.xml
│   │   ├── 📄 readme.md
│   │   └── 📄 System.Reactive.nuspec
│   ├── 📁 System.Runtime.CompilerServices.Unsafe.4.7.1
│   │   ├── 📄 Icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 System.Runtime.CompilerServices.Unsafe.dll
│   │   │       └── 📄 System.Runtime.CompilerServices.Unsafe.xml
│   │   ├── 📄 LICENSE.TXT
│   │   ├── 📄 System.Runtime.CompilerServices.Unsafe.nuspec
│   │   ├── 📄 THIRD-PARTY-NOTICES.TXT
│   │   ├── 📄 useSharedDesignerContext.txt
│   │   └── 📄 version.txt
│   ├── 📁 System.Security.Cryptography.Cng.4.5.0
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       └── 📄 System.Security.Cryptography.Cng.dll
│   │   ├── 📄 LICENSE.TXT
│   │   ├── 📄 System.Security.Cryptography.Cng.nuspec
│   │   ├── 📄 THIRD-PARTY-NOTICES.TXT
│   │   ├── 📄 useSharedDesignerContext.txt
│   │   └── 📄 version.txt
│   ├── 📁 System.Text.Encodings.Web.4.7.2
│   │   ├── 📄 Icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.1
│   │   │       ├── 📄 System.Text.Encodings.Web.dll
│   │   │       └── 📄 System.Text.Encodings.Web.xml
│   │   ├── 📄 LICENSE.TXT
│   │   ├── 📄 System.Text.Encodings.Web.nuspec
│   │   ├── 📄 THIRD-PARTY-NOTICES.TXT
│   │   ├── 📄 useSharedDesignerContext.txt
│   │   └── 📄 version.txt
│   ├── 📁 System.Text.Json.4.7.2
│   │   ├── 📄 Icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.0
│   │   │       ├── 📄 System.Text.Json.dll
│   │   │       └── 📄 System.Text.Json.xml
│   │   ├── 📄 LICENSE.TXT
│   │   ├── 📄 System.Text.Json.nuspec
│   │   ├── 📄 THIRD-PARTY-NOTICES.TXT
│   │   ├── 📄 useSharedDesignerContext.txt
│   │   └── 📄 version.txt
│   ├── 📁 System.Threading.Channels.8.0.0
│   │   ├── 📁 buildTransitive
│   │   │   ├── 📁 net461
│   │   │   │   └── 📄 System.Threading.Channels.targets
│   │   │   ├── 📁 net462
│   │   │   │   └── 📄 _._
│   │   │   ├── 📁 net6.0
│   │   │   │   └── 📄 _._
│   │   │   └── 📁 netcoreapp2.0
│   │   │       └── 📄 System.Threading.Channels.targets
│   │   ├── 📄 Icon.png
│   │   ├── 📁 lib
│   │   │   └── 📁 netstandard2.1
│   │   │       ├── 📄 System.Threading.Channels.dll
│   │   │       └── 📄 System.Threading.Channels.xml
│   │   ├── 📄 LICENSE.TXT
│   │   ├── 📄 PACKAGE.md
│   │   ├── 📄 System.Threading.Channels.nuspec
│   │   ├── 📄 THIRD-PARTY-NOTICES.TXT
│   │   └── 📄 useSharedDesignerContext.txt
│   └── 📁 Websocket.Client.5.1.1
│       ├── 📄 icon-modern.png
│       ├── 📄 icon.png
│       ├── 📁 lib
│       │   └── 📁 netstandard2.1
│       │       ├── 📄 Websocket.Client.dll
│       │       └── 📄 Websocket.Client.xml
│       ├── 📄 README.md
│       └── 📄 Websocket.Client.nuspec
├── 📄 packages.config
├── 📁 Plugins
│   ├── 📁 Android
│   │   ├── 📄 AndroidManifest.xml
│   │   ├── 📄 launcherTemplate.gradle.DISABLED
│   │   ├── 📁 libs
│   │   │   ├── 📁 arm64-v8a
│   │   │   │   ├── 📄 libsqlite3.so
│   │   │   │   └── 📄 sqlite3.o
│   │   │   ├── 📁 armeabi-v7a
│   │   │   │   ├── 📄 libsqlite3.so
│   │   │   │   └── 📄 sqlite3.o
│   │   │   └── 📁 x86
│   │   └── 📄 mainTemplate.gradle
│   ├── 📁 WSA
│   │   ├── 📁 ARM
│   │   │   └── 📄 sqlite3.dll
│   │   ├── 📁 x64
│   │   │   └── 📄 sqlite3.dll
│   │   └── 📁 x86
│   │       └── 📄 sqlite3.dll
│   ├── 📁 x64
│   │   └── 📄 sqlite3.dll
│   └── 📁 x86
│       └── 📄 sqlite3.dll
├── 📁 _Project
│   ├── 📁 Animations
│   │   ├── 📁 Camera
│   │   │   ├── 📄 PC2DSmooth.anim
│   │   │   └── 📄 PlayerCamera.controller
│   │   ├── 📁 Loader_HotDogFly_brend
│   │   │   ├── 📄 Loader_HotDogFly_brend_0 1.controller
│   │   │   ├── 📄 Loader_HotDogFly_brend.anim
│   │   │   └── 📄 Loader_HotDogFly_brend.png
│   │   └── 📁 Spinner
│   │       ├── 📄 spinner_0.controller
│   │       ├── 📄 spinner.anim
│   │       └── 📄 spinner.png
│   ├── 📁 Art
│   │   ├── 📁 Accessories
│   │   │   └── 📄 hat_accessory.png
│   │   ├── 📁 Background
│   │   │   ├── 📄 100.png
│   │   │   ├── 📄 background_loading_page_style_1.png
│   │   │   ├── 📄 baner.png
│   │   │   ├── 📄 BgHotdogs.png
│   │   │   ├── 📄 location_preview.png
│   │   │   ├── 📄 город.jpeg
│   │   │   ├── 📄 Город.jpg
│   │   │   ├── 📄 Кухня.png
│   │   │   ├── 📄 Ресторан_1.png
│   │   │   └── 📄 Ресторан_2.png
│   │   ├── 📁 Decorations
│   │   │   ├── 📁 CIty
│   │   │   │   ├── 📄 hole_in_the_floor_style_1.png
│   │   │   │   ├── 📄 House (1).png
│   │   │   │   ├── 📄 House (2).png
│   │   │   │   ├── 📄 House (3).png
│   │   │   │   ├── 📄 House (4).png
│   │   │   │   ├── 📄 House (5).png
│   │   │   │   ├── 📄 House (6).png
│   │   │   │   ├── 📄 House (7).png
│   │   │   │   ├── 📄 House (8).png
│   │   │   │   ├── 📄 people_on_a_date_style_1.png
│   │   │   │   ├── 📄 waiter_style_1.png
│   │   │   │   └── 📄 waiter_style_2.png
│   │   │   ├── 📄 door.png
│   │   │   └── 📁 Roof
│   │   │       ├── 📄 cannopy_lights_between_soobs_style_1.png
│   │   │       ├── 📄 stone_partition.png
│   │   │       └── 📄 wooden_floor.png
│   │   ├── 📁 DynamicObjects
│   │   │   ├── 📄 arrow_decorations_boom_1.controller
│   │   │   ├── 📄 arrow_decorations_boom_2.controller
│   │   │   ├── 📄 arrow_decorations_boom.png
│   │   │   ├── 📄 boom_arrow.anim
│   │   │   ├── 📄 boom_sign.anim
│   │   │   ├── 📄 Горка.png
│   │   │   └── 📄 Прямоугольник, скругл. углы 2.png
│   │   ├── 📁 GameImprovements
│   │   │   └── 📄 air_jump_improve.png
│   │   ├── 📁 Icons
│   │   │   ├── 📁 GameUI
│   │   │   │   ├── 📄 icon_battle.png
│   │   │   │   ├── 📄 lock-cross-chains.png
│   │   │   │   ├── 📄 menu-icon.png
│   │   │   │   ├── 📄 money.png
│   │   │   │   ├── 📄 player_icon_ability.png
│   │   │   │   ├── 📄 progress_bar_background.png
│   │   │   │   ├── 📄 progress_bar_mask.png
│   │   │   │   └── 📄 shop_hotdogs.png
│   │   │   ├── 📁 Leaderboard
│   │   │   │   ├── 📄 1rd-place.png
│   │   │   │   ├── 📄 2rd-place.png
│   │   │   │   ├── 📄 3rd-place.png
│   │   │   │   ├── 📄 one.png
│   │   │   │   └── 📄 podium.png
│   │   │   ├── 📁 Platforms
│   │   │   │   ├── 📄 753-7536803_logo-with-wordmark.png
│   │   │   │   ├── 📄 google-play-games.png
│   │   │   │   ├── 📄 GooglePlayGames.png
│   │   │   │   └── 📄 Google_Play.png
│   │   │   ├── 📁 UI
│   │   │   │   ├── 📄 game-controller.png
│   │   │   │   ├── 📄 icons8-exit-100.png
│   │   │   │   ├── 📄 information.png
│   │   │   │   ├── 📄 menu_icon.png
│   │   │   │   ├── 📄 pause.png
│   │   │   │   ├── 📄 settings-icon.png
│   │   │   │   ├── 📄 shop.png
│   │   │   │   └── 📄 sound.png
│   │   │   └── 📁 UserProfile
│   │   │       ├── 📄 alpha_player_icon.png
│   │   │       ├── 📄 hotdog_bluster_icon.png
│   │   │       ├── 📄 hotdogfly_sign_icon.png
│   │   │       ├── 📄 player_bob_icon.png
│   │   │       └── 📄 player_robert_icon.png
│   │   ├── 📁 Interactions
│   │   │   ├── 📄 arrow.png
│   │   │   ├── 📄 barrel.png
│   │   │   ├── 📄 bubble_shell_for_improved_style_1.png
│   │   │   ├── 📄 mustard.png
│   │   │   ├── 📄 player_gun.png
│   │   │   ├── 📄 portal_game_object.png
│   │   │   ├── 📄 teleport_arrow.png
│   │   │   ├── 📄 tomato_big.png
│   │   │   └── 📄 tomato.png
│   │   ├── 📄 rope.png
│   │   ├── 📁 UIControlls
│   │   │   ├── 📄 blank-wooden-sign-board-vector-illustrations.png
│   │   │   ├── 📄 button_legacy.png
│   │   │   ├── 📄 button_style_1.png
│   │   │   ├── 📄 cutting-board.png
│   │   │   ├── 📄 frame_style_1.png
│   │   │   ├── 📄 frame_style_2.png
│   │   │   ├── 📄 input_style_1.png
│   │   │   └── 📄 input_style_2.png
│   │   ├── 📁 UIDecorations
│   │   │   ├── 📄 hotdog2.png
│   │   │   ├── 📄 hotdog.png
│   │   │   ├── 📄 plume_of_air.png
│   │   │   └── 📄 Sign.png
│   │   └── 📁 Weapons
│   │       ├── 📄 boxing_glove.png
│   │       ├── 📄 flying_down_icon.png
│   │       ├── 📁 Harpoon
│   │       │   ├── 📄 harpoon_arrow.png
│   │       │   └── 📄 harpoon.png
│   │       ├── 📄 hotdog_blaster_shop_item.png
│   │       ├── 📄 impulse_icon.png
│   │       ├── 📄 jump_curves.png
│   │       ├── 📄 Katana.png
│   │       ├── 📄 replacement_shop_item.png
│   │       ├── 📄 shield_icon.png
│   │       └── 📄 teleport_shop_item.png
│   ├── 📁 Data
│   │   ├── 📄 ElysiumDBSettings.asset
│   │   ├── 📄 GameURP.asset
│   │   ├── 📄 GameURP_Renderer.asset
│   │   └── 📄 UniversalRenderPipelineGlobalSettings.asset
│   ├── 📁 OLD
│   │   ├── 📁 Components
│   │   │   ├── 📁 AudioSystem
│   │   │   │   ├── 📄 AudioChannelCatcher.cs
│   │   │   │   ├── 📄 AudioChannel.cs
│   │   │   │   └── 📄 AudioMixer.cs
│   │   │   ├── 📄 DisplayWithoutEditDrawer.cs
│   │   │   └── 📄 Paralax.cs
│   │   ├── 📁 Locations
│   │   │   ├── 📁 Components
│   │   │   │   ├── 📄 LocationChunk.cs
│   │   │   │   ├── 📄 Location.cs
│   │   │   │   ├── 📄 LocationStreamer.cs
│   │   │   │   ├── 📄 RandomUtils.cs
│   │   │   │   └── 📄 SwitchLocationTriggers.cs
│   │   │   ├── 📁 Lobby
│   │   │   │   └── 📄 Location.prefab
│   │   │   ├── 📁 Patterns
│   │   │   │   └── 📁 Components
│   │   │   │       ├── 📄 Spawner.cs
│   │   │   │       ├── 📄 SpawnerRepeater.cs
│   │   │   │       └── 📄 SpawnGroup.cs
│   │   │   ├── 📄 roof.prefab
│   │   │   ├── 📁 Город
│   │   │   │   ├── 📄 LocationMirror.prefab
│   │   │   │   ├── 📄 Location.prefab
│   │   │   │   └── 📄 LocationsContainer.prefab
│   │   │   ├── 📄 Город_0.prefab
│   │   │   ├── 📁 Кухня
│   │   │   │   ├── 📄 Chunk.prefab
│   │   │   │   ├── 📄 Floor Physics Material 2D.physicsMaterial2D
│   │   │   │   └── 📄 Location.prefab
│   │   │   └── 📄 Ресторан.prefab
│   │   ├── 📁 OffsetTextureController
│   │   │   ├── 📄 OffsetTextureController.cs
│   │   │   ├── 📄 SpriteOffset.mat
│   │   │   └── 📄 TextureOffset.shader
│   │   └── 📁 Screens ( CanvasUI )
│   │       ├── 📁 PreLoading
│   │       │   └── 📁 Animations
│   │       │       ├── 📄 Canvas.controller
│   │       │       ├── 📄 PreloadingAnimation.anim
│   │       │       └── 📄 Start.anim
│   │       ├── 📁 Settings
│   │       │   ├── 📁 Components
│   │       │   │   └── 📄 Settings.cs
│   │       │   ├── 📁 Screens
│   │       │   │   └── 📁 Controlls
│   │       │   │       ├── 📁 Components
│   │       │   │       │   └── 📄 Controlls.cs
│   │       │   │       └── 📄 Controlls.prefab
│   │       │   └── 📄 Settings.prefab
│   │       ├── 📁 Shop
│   │       │   ├── 📁 Animations
│   │       │   │   ├── 📄 Link Toggle.controller
│   │       │   │   ├── 📄 Open.anim
│   │       │   │   ├── 📄 Preview.anim
│   │       │   │   └── 📄 Shop.controller
│   │       │   ├── 📁 Components
│   │       │   │   ├── 📄 BuyPanelShop.cs
│   │       │   │   ├── 📄 ShopContentLoader.cs
│   │       │   │   ├── 📄 Shop.cs
│   │       │   │   ├── 📄 Tab.cs
│   │       │   │   └── 📄 TabsController.cs
│   │       │   ├── 📁 Link Toggle
│   │       │   │   ├── 📄 LinkToggle.cs
│   │       │   │   ├── 📄 Link Toggle.prefab
│   │       │   │   └── 📄 ScrollToController.cs
│   │       │   ├── 📄 Shop.prefab
│   │       │   └── 📁 Stats
│   │       │       ├── 📄 Stat.cs
│   │       │       ├── 📁 StatPrefab
│   │       │       │   └── 📄 stat (  ).prefab
│   │       │       └── 📄 StatsController.cs
│   │       ├── 📁 StartedGame
│   │       │   ├── 📁 Animations
│   │       │   │   ├── 📄 Open.anim
│   │       │   │   └── 📄 StartedGame.controller
│   │       │   ├── 📁 Components
│   │       │   │   └── 📄 StartedGame.cs
│   │       │   ├── 📄 StartedGame.prefab
│   │       │   └── 📁 UI
│   │       │       ├── 📁 Icons
│   │       │       │   └── 📄 kz.png
│   │       │       ├── 📄 index.uxml
│   │       │       └── 📁 USS
│   │       │           └── 📄 style.uss
│   │       └── 📁 StopGame
│   │           └── 📄 StopGame.prefab
│   ├── 📁 Runtime
│   │   ├── 📁 Auth
│   │   │   └── 📄 AuthUI.cs
│   │   ├── 📁 Components
│   │   │   ├── 📁 AimController
│   │   │   │   ├── 📄 AimController.cs
│   │   │   │   └── 📁 Ui
│   │   │   │       └── 📄 DirectArrow.prefab
│   │   │   ├── 📁 Camera
│   │   │   │   └── 📁 CameraChanger
│   │   │   │       ├── 📄 CameraChanger.cs
│   │   │   │       └── 📁 Editor
│   │   │   │           └── 📄 CameraChangerEditor.cs
│   │   │   ├── 📄 ColliderImpactEffect.cs
│   │   │   ├── 📄 CollisionDamage.cs
│   │   │   ├── 📄 DamageFlash.cs
│   │   │   ├── 📁 DynamicFace
│   │   │   │   ├── 📁 DynamicEyes
│   │   │   │   │   ├── 📄 DynamicEye.cs
│   │   │   │   │   └── 📁 Editor
│   │   │   │   │       └── 📄 DynamicEyeEditor.cs
│   │   │   │   ├── 📄 DynamicFace.cs
│   │   │   │   ├── 📁 Editor
│   │   │   │   │   └── 📄 DynamicFaceEditor.cs
│   │   │   │   ├── 📄 EyesBlink.anim
│   │   │   │   ├── 📄 EyesMove.anim
│   │   │   │   └── 📄 Face.controller
│   │   │   ├── 📄 RandomSkinSetter.cs
│   │   │   ├── 📄 RedOverlayZone2D.cs
│   │   │   ├── 📄 ResourceLoader.cs
│   │   │   ├── 📁 SceneContentTimeout
│   │   │   │   └── 📄 ContentTimeout.cs
│   │   │   ├── 📄 SimpleCannon.cs
│   │   │   └── 📄 Singletons.cs
│   │   ├── 📁 Database
│   │   │   ├── 📁 DBSettings
│   │   │   │   ├── 📁 Editor
│   │   │   │   │   ├── 📄 ElysiumDBSettingsEditor.cs
│   │   │   │   │   └── 📄 ElysiumDBSettingsProvider.cs
│   │   │   │   └── 📄 ElysiumDBSettings.cs
│   │   │   ├── 📄 LocalDB.cs
│   │   │   ├── 📄 SupabaseConst.cs
│   │   │   └── 📄 SupabaseUser.cs
│   │   ├── 📁 Effects
│   │   │   └── 📁 smoke-expossion
│   │   │       ├── 📄 smoke-explosion-animation_0.controller
│   │   │       ├── 📄 smoke-explosion-animation_0.prefab
│   │   │       ├── 📄 smoke-explosion-animation.png
│   │   │       └── 📄 smoke-exposion.anim
│   │   ├── 📁 Game
│   │   │   ├── 📄 GameController.cs
│   │   │   ├── 📄 GameInfo.cs
│   │   │   └── 📄 LoadingScreen.cs
│   │   ├── 📁 Interface
│   │   │   ├── 📄 IBasePlayer.cs
│   │   │   ├── 📄 IHealth.cs
│   │   │   ├── 📄 IPreview.cs
│   │   │   └── 📄 ISingleton.cs
│   │   └── 📁 Player
│   │       ├── 📄 BasePlayer.cs
│   │       ├── 📁 Bot
│   │       │   ├── 📁 Behaviors
│   │       │   │   ├── 📄 BaseBotBehavior.cs
│   │       │   │   ├── 📁 Editor
│   │       │   │   │   ├── 📄 BaseBotBehaviorEditor.cs
│   │       │   │   │   └── 📄 LinearMoveBotBehaviourEditor.cs
│   │       │   │   └── 📄 LinearMoveBotBehaviour.cs
│   │       │   ├── 📁 Brain
│   │       │   │   ├── 📄 BotBrain.cs
│   │       │   │   └── 📁 Objects
│   │       │   │       └── 📄 LobbyBots.asset
│   │       │   ├── 📁 Components
│   │       │   │   ├── 📄 BotBehaviourFactory.cs
│   │       │   │   └── 📄 BotBehaviourType.cs
│   │       │   └── 📄 PlayerBot.cs
│   │       ├── 📄 ControllTestPlayer.cs
│   │       ├── 📄 LobbyPlayer.cs
│   │       ├── 📄 Player.cs
│   │       └── 📁 Prefabs
│   │           ├── 📄 LobbyBotFly.prefab
│   │           ├── 📄 LobbyPlayer.prefab
│   │           └── 📄 Player.prefab
│   ├── 📁 System
│   │   ├── 📁 ModalSystem
│   │   │   ├── 📁 ModalPresets
│   │   │   │   ├── 📁 Alert
│   │   │   │   ├── 📁 Error
│   │   │   │   │   ├── 📄 Button.prefab
│   │   │   │   │   ├── 📄 ErrorModal.cs
│   │   │   │   │   └── 📄 ModalError.prefab
│   │   │   │   └── 📁 Loader
│   │   │   ├── 📄 ModalSystem.cs
│   │   │   ├── 📄 ModalSystem.prefab
│   │   │   └── 📁 SRC
│   │   │       ├── 📄 Sign ( Bob - BG - Cap ).png
│   │   │       ├── 📄 Sign ( body ).png
│   │   │       └── 📄 Sign ( Cap ).png
│   │   ├── 📁 TMPFormaterSystem
│   │   │   ├── 📁 Attributes
│   │   │   │   └── 📄 TMPFLLabelAttribute.cs
│   │   │   ├── 📄 DoCreateTMPFL.cs
│   │   │   ├── 📁 Editor
│   │   │   ├── 📄 ITMPFormaterBaseLibrary.cs
│   │   │   ├── 📁 Package
│   │   │   │   └── 📄 TMPFormaterSystem.unitypackage
│   │   │   ├── 📄 Test.cs
│   │   │   ├── 📁 Textures
│   │   │   │   └── 📄 TMP - Text Component Icon.psd
│   │   │   └── 📄 TMPFormater.cs
│   │   ├── 📄 ToolContainer.cs
│   │   └── 📁 ToolInventory
│   │       ├── 📁 Editor
│   │       │   └── 📄 ToolInventoryEditor.cs
│   │       ├── 📄 ToolInventory.cs
│   │       └── 📄 ToolInventoryUI.cs
│   └── 📁 UI
│       ├── 📁 Localization
│       │   └── 📁 TMPFL`S
│       │       ├── 📄 CurrentUserTMPFL.cs
│       │       ├── 📄 ItemInfoTMPFL.cs
│       │       ├── 📄 LablesAuthTMPFL.cs
│       │       └── 📄 LablesGameTMPFL.cs
│       ├── 📁 Screens
│       │   ├── 📁 Animations
│       │   │   └── 📁 DefaultSwitch
│       │   │       ├── 📄 DefaulUI.controller
│       │   │       ├── 📄 ToLeftCloseUiAnimation.anim
│       │   │       ├── 📄 ToLeftOpenUiAnimation.anim
│       │   │       ├── 📄 ToRightCloseUiAnimation.anim
│       │   │       └── 📄 ToRightOpenUiAnimation.anim
│       │   ├── 📄 BrendLoader.prefab
│       │   ├── 📁 Components
│       │   │   ├── 📁 Chapter
│       │   │   │   ├── 📄 Chapter ( ChapterName ).prefab
│       │   │   │   ├── 📄 Chapter.cs
│       │   │   │   ├── 📁 ChapterElement
│       │   │   │   │   ├── 📄 ChapterElement.cs
│       │   │   │   │   └── 📄 ChapterElement.prefab
│       │   │   │   └── 📁 ChaptersGroup
│       │   │   │       ├── 📄 ChaptersGroup.cs
│       │   │   │       └── 📄 Chapters.prefab
│       │   │   ├── 📄 ScrollParalax.cs
│       │   │   ├── 📁 ShopItem
│       │   │   │   ├── 📁 Animations
│       │   │   │   │   ├── 📄 ChapterElement.controller
│       │   │   │   │   └── 📄 InitBounce.anim
│       │   │   │   ├── 📄 Chapter ( ChapterName ).prefab
│       │   │   │   ├── 📄 ChapterElement.prefab
│       │   │   │   ├── 📁 ItemActions
│       │   │   │   │   └── 📄 Button.prefab
│       │   │   │   ├── 📄 ShopItem.cs
│       │   │   │   └── 📁 Tabs
│       │   │   │       └── 📄 Button.prefab
│       │   │   └── 📁 ShopScrreen
│       │   │       ├── 📄 ChapterChoosedItemsFillder.cs
│       │   │       ├── 📄 ChapterVirtualElementsExtension.cs
│       │   │       ├── 📄 ShopItemsFillder.cs
│       │   │       ├── 📄 ShopPlayerPreview.cs
│       │   │       ├── 📄 ShopScreen.cs
│       │   │       └── 📄 TMPFItemDescriptionLibrary.cs
│       │   ├── 📄 Menu.prefab
│       │   ├── 📁 Patterns
│       │   │   └── 📄 LeaderBoard.prefab
│       │   ├── 📄 Shop.prefab
│       │   ├── 📄 StartedGame.prefab
│       │   └── 📄 StartGameScreen.prefab
│       ├── 📁 Text
│       │   └── 📄 AutoVerticalTMPScroll.cs
│       ├── 📁 UIinteractive
│       │   ├── 📁 Buttons
│       │   │   └── 📄 ButtonOnTap.cs
│       │   ├── 📄 ContentSizeFitterEx.cs
│       │   ├── 📁 ToolsBar
│       │   │   ├── 📁 ReloadIndicator
│       │   │   │   └── 📄 ReloadIndicator.cs
│       │   │   └── 📁 Tools
│       │   │       └── 📁 Editor
│       │   │           └── 📄 ToolContainerEditor.cs
│       │   └── 📄 UITabNavigation.cs
│       └── 📁 UISystem
│           ├── 📁 Components
│           │   ├── 📄 UISysEvents.cs
│           │   └── 📄 UISystemChanger.cs
│           ├── 📄 icon.png
│           ├── 📁 Modal
│           ├── 📁 Screens
│           │   └── 📁 Animations
│           │       └── 📁 Screens
│           ├── 📄 UISystem.cs
│           └── 📄 UISystem.prefab
├── 📁 Rendering
│   └── 📁 RendererFeatures
│       └── 📁 Outline
│           ├── 📁 Auxiliary
│           │   ├── 📄 IgnoreTargetOutline.cs
│           │   └── 📄 OutlineTarget.cs
│           ├── 📁 Feature
│           │   └── 📄 OutlineFeature.cs
│           ├── 📁 Material
│           │   ├── 📄 FullscreenMaterial.mat
│           │   └── 📄 OutlineMaterial.mat
│           └── 📁 Shader (HLSL)
│               ├── 📄 OutlineBlur.shader
│               ├── 📄 OutlineComposite.shader
│               ├── 📄 OutlineMask.shader
│               ├── 📄 OutlineTest.shader
│               └── 📄 UnlitTextureAlpha.shader
├── 📁 Resources
│   ├── 📁 Skins
│   │   ├── 📁 Animations
│   │   │   └── 📁 Base
│   │   │       ├── 📄 BaseSkin.controller
│   │   │       └── 📁 Shop
│   │   │           └── 📄 BaseShopPlayerSkinChange.anim
│   │   ├── 📄 BaseSkin Variant_Bob.prefab
│   │   ├── 📁 Components
│   │   │   └── 📄 Skin.cs
│   │   └── 📁 Src
│   │       ├── 📁 Alpha
│   │       │   ├── 📄 Blink.anim
│   │       │   ├── 📄 preview.png
│   │       │   ├── 📄 Skin.prefab
│   │       │   └── 📁 Textures
│   │       │       └── 📄 SpriteSheet_Alpha_Skin.png
│   │       ├── 📁 Bob
│   │       │   ├── 📄 Blink.anim
│   │       │   ├── 📄 preview.png
│   │       │   ├── 📄 Skin.prefab
│   │       │   └── 📁 Textures
│   │       │       └── 📄 SpriteSheet_Bob_Skin.png
│   │       └── 📁 Robert
│   │           ├── 📄 Blink.anim
│   │           ├── 📄 preview.png
│   │           ├── 📄 Skin.prefab
│   │           └── 📁 Textures
│   │               └── 📄 SpriteSheet_Bob_Skin.png
│   ├── 📄 streamingassetssql.txt
│   └── 📁 Tools
│       ├── 📁 Components
│       │   ├── 📁 Arrows
│       │   │   ├── 📄 BaseArrow.cs
│       │   │   └── 📄 TransformArrow.cs
│       │   ├── 📁 Indicators
│       │   │   ├── 📄 BaseShotIndicator.cs
│       │   │   └── 📁 Circle
│       │   │       ├── 📄 CircleShotIndicator.cs
│       │   │       └── 📄 CircleShotIndicator.prefab
│       │   ├── 📄 PlayerToolBase.cs
│       │   └── 📄 ShotDetector.cs
│       ├── 📁 ScriptableObject
│       │   └── 📄 ToolDefinition.cs
│       ├── 📁 Tool
│       │   ├── 📁 boxing_glove
│       │   │   ├── 📁 Animations
│       │   │   │   ├── 📄 boxing_glove.controller
│       │   │   │   └── 📄 Punch.anim
│       │   │   ├── 📄 boxing_glove.prefab
│       │   │   ├── 📁 Components
│       │   │   │   └── 📄 BoxingGlove.cs
│       │   │   ├── 📄 DescriptionInfo.json
│       │   │   ├── 📄 ItemDescription.asset
│       │   │   ├── 📄 ToolDefinition.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   ├── 📁 Components
│       │   │   └── 📄 ToolUI.cs
│       │   ├── 📁 DirectionChange
│       │   │   ├── 📁 Components
│       │   │   │   └── 📄 DirectionChange.cs
│       │   │   ├── 📄 DirectionChangeItem.prefab
│       │   │   └── 📄 ToolDefinition.asset
│       │   ├── 📁 flying_down
│       │   │   ├── 📄 DescriptionInfo.json
│       │   │   ├── 📄 ItemDescription.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   ├── 📁 Harpoon
│       │   │   ├── 📄 arrow.png
│       │   │   ├── 📄 DescriptionInfo.json
│       │   │   ├── 📄 harpoon_aftershoot.png
│       │   │   ├── 📄 harpoon_beforeshoot.png
│       │   │   ├── 📄 Harpoon.cs
│       │   │   ├── 📄 harpoon.prefab
│       │   │   ├── 📄 ItemDescription.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   ├── 📁 Jump_curves
│       │   │   ├── 📄 DescriptionInfo.json
│       │   │   ├── 📄 ItemDescription.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   ├── 📁 Katana
│       │   │   ├── 📄 DescriptionInfo.json
│       │   │   ├── 📄 ItemDescription.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   ├── 📁 replacement_shop_item
│       │   │   ├── 📄 DescriptionInfo.json
│       │   │   ├── 📄 ItemDescription.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   ├── 📁 Shield
│       │   │   ├── 📄 DescriptionInfo.json
│       │   │   ├── 📄 ItemDescription.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   ├── 📁 Teleporter
│       │   │   ├── 📁 Components
│       │   │   │   └── 📄 Teleporter.cs
│       │   │   ├── 📄 Teleporter.prefab
│       │   │   ├── 📄 ToolDefinition.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   ├── 📁 Tool_HotGun
│       │   │   ├── 📁 Animations
│       │   │   │   ├── 📄 hotdog_blaster_item.controller
│       │   │   │   └── 📄 Shot.anim
│       │   │   ├── 📁 Components
│       │   │   │   └── 📄 HotDogBlusterController.cs
│       │   │   ├── 📄 hotdog_blaster_item.prefab
│       │   │   ├── 📄 ToolDefinition.asset
│       │   │   └── 📄 Tool Variant.prefab
│       │   └── 📄 Tool.prefab
│       └── 📄 Tools.prefab
├── 📁 Scenes
│   ├── 📄 Authentication.unity
│   ├── 📄 Game.unity
│   ├── 📄 PreLoadingGame.unity
│   └── 📄 Test.unity
├── 📁 ScriptBoy
│   ├── 📁 EButton%20Attributes%20v2
│   │   ├── 📁 Documentation
│   │   ├── 📁 Scripts
│   │   │   ├── 📁 Attributes
│   │   │   └── 📁 Editor
│   │   └── 📁 Tests
│   └── 📁 EButton Attributes v2
│       ├── 📁 Documentation
│       │   ├── 📄 Changelog.txt
│       │   └── 📄 EButton Attributes v2.pdf
│       ├── 📁 Scripts
│       │   ├── 📁 Attributes
│       │   │   ├── 📄 EButtonAttribute.cs
│       │   │   ├── 📄 EButtonBaseAttribute.cs
│       │   │   ├── 📄 EButton.BeginHorizontalAttribute.cs
│       │   │   ├── 📄 EButton.BeginVerticalAttribute.cs
│       │   │   ├── 📄 EButton.EndHorizontalAttribute.cs
│       │   │   ├── 📄 EButton.EndVerticalAttribute.cs
│       │   │   └── 📄 ScriptBoy.EButtonAttributes.asmdef
│       │   └── 📁 Editor
│       │       ├── 📄 EButtonDrawer.cs
│       │       ├── 📄 EButtonDrawerExtension.cs
│       │       ├── 📄 MonoBehaviourInspector.cs
│       │       └── 📄 ScriptBoy.EButtonEditor.asmdef
│       └── 📁 Tests
│           ├── 📄 EButton Tests.unity
│           ├── 📄 ScriptBoy.EButtonTests.asmdef
│           └── 📄 TestEButton.cs
├── 📁 StreamingAssets
│   ├── 📄 Objects.db
│   └── 📄 Session.db
├── 📁 TestSRC
│   ├── 📄 CamBounds.anim
│   ├── 📁 Component
│   │   ├── 📁 DamageRaycast
│   │   │   ├── 📄 DamageBehaviour.cs
│   │   │   ├── 📄 DamageRaycaster.cs
│   │   │   ├── 📄 DamageRCG.cs
│   │   │   ├── 📁 Editor
│   │   │   │   ├── 📄 AnimationSettingsPD.cs
│   │   │   │   ├── 📄 DamageRaycasterEditor.cs
│   │   │   │   ├── 📄 DamageRCGEditor.cs
│   │   │   │   └── 📄 RaycastControllerPD.cs
│   │   │   ├── 📁 Example
│   │   │   │   └── 📄 DamageRaycastTargetTest.cs
│   │   │   └── 📁 Imgs
│   │   └── 📄 TestBox2D.cs
│   ├── 📄 Doors_1.controller
│   ├── 📄 DoorsOpen.anim
│   ├── 📄 Face.controller
│   ├── 📄 FallingCam.anim
│   ├── 📄 FallingSpawnAnimation.anim
│   ├── 📄 HotDog.controller
│   ├── 📄 HotDogShowing.anim
│   ├── 📄 Image.controller
│   ├── 📄 LaserPivot.controller
│   ├── 📄 LobbyPlayer.controller
│   ├── 📄 LobbyPlayerStart.anim
│   ├── 📄 Main Camera 1.controller
│   ├── 📄 Main Camera.controller
│   ├── 📁 Materyals
│   ├── 📄 New Animation.anim
│   ├── 📄 PreLoadingCameraShake.anim
│   ├── 📄 PreloadingContinueBlackout.anim
│   ├── 📄 PreloadingContinueBlackout.controller
│   ├── 📄 PreloadingShake.anim
│   ├── 📄 PressStartBounce.anim
│   ├── 📄 RaycastDamage.controller
│   ├── 📄 Smoke.anim
│   ├── 📄 smoke-explosion-animation_0.controller
│   ├── 📄 StartGameFocusMove.anim
│   ├── 📄 StartGameLoopAnimation.anim
│   ├── 📄 StartGameScreenClose.anim
│   ├── 📄 StartGameScreen.controller
│   ├── 📄 StartGameScreenShowing.anim
│   ├── 📄 StaticFly.anim
│   ├── 📄 StaticPlayerBounds.anim
│   ├── 📄 test.anim
│   ├── 📄 test.controller
│   ├── 📄 testraycast.anim
│   ├── 📁 Textures
│   │   ├── 📁 arc
│   │   │   ├── 📄 arc_120_128.png
│   │   │   ├── 📄 arc_120_64.png
│   │   │   ├── 📄 arc_180_128.png
│   │   │   ├── 📄 arc_180_64.png
│   │   │   ├── 📄 arc_360_128.png
│   │   │   ├── 📄 arc_360_64.png
│   │   │   ├── 📄 arc_90_128.png
│   │   │   ├── 📄 arc_90_64.png
│   │   │   ├── 📄 arc_twist_120_128.png
│   │   │   ├── 📄 arc_twist_180_128.png
│   │   │   ├── 📄 arc_twist_360_128.png
│   │   │   ├── 📄 arc_twist_90_128.png
│   │   │   ├── 📄 arc_twist_new_120_128.png
│   │   │   ├── 📄 arc_twist_new_180_128.png
│   │   │   ├── 📄 arc_twist_new_360_128.png
│   │   │   └── 📄 arc_twist_new_90_128.png
│   │   ├── 📄 arc_360_128.png
│   │   ├── 📁 circle
│   │   │   ├── 📄 circle_128.png
│   │   │   ├── 📄 circle_256.png
│   │   │   ├── 📄 circle_twist_128.png
│   │   │   ├── 📄 circle_twist_256.png
│   │   │   ├── 📄 circle_wave_256_2.png
│   │   │   └── 📄 circle_wave_256.png
│   │   ├── 📄 circle.png
│   │   ├── 📄 Grid.png
│   │   ├── 📄 Switch.png
│   │   └── 📄 white.png
│   └── 📄 сhest.png
├── 📁 TextMesh%20Pro
│   ├── 📁 Documentation
│   ├── 📁 Examples%20%26%20Extras
│   │   ├── 📁 Fonts
│   │   ├── 📁 Materials
│   │   ├── 📁 Prefabs
│   │   ├── 📁 Resources
│   │   │   ├── 📁 Color%20Gradient%20Presets
│   │   │   ├── 📁 Fonts%20%26%20Materials
│   │   │   └── 📁 Sprite%20Assets
│   │   ├── 📁 Scripts
│   │   ├── 📁 Sprites
│   │   └── 📁 Textures
│   ├── 📁 Fonts
│   ├── 📁 Resources
│   │   ├── 📁 Fonts%20%26%20Materials
│   │   ├── 📁 Sprite%20Assets
│   │   └── 📁 Style%20Sheets
│   ├── 📁 Shaders
│   └── 📁 Sprites
├── 📁 TextMesh Pro
│   ├── 📁 Documentation
│   │   └── 📄 TextMesh Pro User Guide 2016.pdf
│   ├── 📁 Examples & Extras
│   │   ├── 📁 Fonts
│   │   │   ├── 📄 Anton OFL.txt
│   │   │   ├── 📄 Anton.ttf
│   │   │   ├── 📄 Bangers - OFL.txt
│   │   │   ├── 📄 Bangers.ttf
│   │   │   ├── 📄 Electronic Highway Sign.TTF
│   │   │   ├── 📄 Oswald-Bold - OFL.txt
│   │   │   ├── 📄 Oswald-Bold.ttf
│   │   │   └── 📄 Roboto-Bold.ttf
│   │   ├── 📁 Materials
│   │   │   ├── 📄 Crate - Surface Shader Scene.mat
│   │   │   ├── 📄 Ground - Logo Scene.mat
│   │   │   ├── 📄 Ground - Surface Shader Scene.mat
│   │   │   └── 📄 Small Crate_diffuse.mat
│   │   ├── 📁 Prefabs
│   │   │   ├── 📄 TextMeshPro - Prefab 1.prefab
│   │   │   ├── 📄 TextMeshPro - Prefab 2.prefab
│   │   │   └── 📄 Text Popup.prefab
│   │   ├── 📁 Resources
│   │   │   ├── 📁 Color Gradient Presets
│   │   │   │   ├── 📄 Blue to Purple - Vertical.asset
│   │   │   │   ├── 📄 Dark to Light Green - Vertical.asset
│   │   │   │   ├── 📄 Light to Dark Green - Vertical.asset
│   │   │   │   └── 📄 Yellow to Orange - Vertical.asset
│   │   │   ├── 📁 Fonts & Materials
│   │   │   │   ├── 📄 Anton SDF.asset
│   │   │   │   ├── 📄 Anton SDF - Drop Shadow.mat
│   │   │   │   ├── 📄 Anton SDF - Outline.mat
│   │   │   │   ├── 📄 Anton SDF - Sunny Days.mat
│   │   │   │   ├── 📄 Bangers SDF.asset
│   │   │   │   ├── 📄 Bangers SDF - Drop Shadow.mat
│   │   │   │   ├── 📄 Bangers SDF Glow.mat
│   │   │   │   ├── 📄 Bangers SDF Logo.mat
│   │   │   │   ├── 📄 Bangers SDF - Outline.mat
│   │   │   │   ├── 📄 Electronic Highway Sign SDF.asset
│   │   │   │   ├── 📄 LiberationSans SDF - Overlay.mat
│   │   │   │   ├── 📄 LiberationSans SDF - Soft Mask.mat
│   │   │   │   ├── 📄 Oswald Bold SDF.asset
│   │   │   │   ├── 📄 Roboto-Bold SDF.asset
│   │   │   │   ├── 📄 Roboto-Bold SDF - Drop Shadow.mat
│   │   │   │   └── 📄 Roboto-Bold SDF - Surface.mat
│   │   │   └── 📁 Sprite Assets
│   │   │       ├── 📄 Default Sprite Asset.asset
│   │   │       └── 📄 DropCap Numbers.asset
│   │   ├── 📁 Scenes
│   │   │   ├── 📄 01-  Single Line TextMesh Pro.unity
│   │   │   ├── 📄 02 - Multi-line TextMesh Pro.unity
│   │   │   ├── 📄 03 - Line Justification.unity
│   │   │   ├── 📄 04 - Word Wrapping.unity
│   │   │   ├── 📄 05 - Style Tags.unity
│   │   │   ├── 📄 06 - Extra Rich Text Examples.unity
│   │   │   ├── 📄 07 - Superscript & Subscript Example.unity
│   │   │   ├── 📄 08 - Improved Text Alignment.unity
│   │   │   ├── 📄 09 - Margin Tag Example.unity
│   │   │   ├── 📄 10 - Bullets & Numbered List Example.unity
│   │   │   ├── 📄 11 - The Style Tag.unity
│   │   │   ├── 📄 12a - Text Interactions.unity
│   │   │   ├── 📄 12 - Link Example.unity
│   │   │   ├── 📄 13 - Soft Hyphenation.unity
│   │   │   ├── 📄 14 - Multi Font & Sprites.unity
│   │   │   ├── 📄 15 - Inline Graphics & Sprites.unity
│   │   │   ├── 📄 16 - Linked text overflow mode example.unity
│   │   │   ├── 📄 17 - Old Computer Terminal.unity
│   │   │   ├── 📄 18 - ScrollRect & Masking & Layout.unity
│   │   │   ├── 📄 19 - Masking Texture & Soft Mask.unity
│   │   │   ├── 📄 20 - Input Field with Scrollbar.unity
│   │   │   ├── 📄 21 - Script Example.unity
│   │   │   ├── 📄 22 - Basic Scripting Example.unity
│   │   │   ├── 📄 23 - Animating Vertex Attributes.unity
│   │   │   ├── 📄 24 - Surface Shader Example.unity
│   │   │   ├── 📄 25 - Sunny Days Example.unity
│   │   │   ├── 📄 26 - Dropdown Placeholder Example.unity
│   │   │   └── 📄 Benchmark (Floating Text).unity
│   │   ├── 📁 Scripts
│   │   │   ├── 📄 Benchmark01.cs
│   │   │   ├── 📄 Benchmark01_UGUI.cs
│   │   │   ├── 📄 Benchmark02.cs
│   │   │   ├── 📄 Benchmark03.cs
│   │   │   ├── 📄 Benchmark04.cs
│   │   │   ├── 📄 CameraController.cs
│   │   │   ├── 📄 ChatController.cs
│   │   │   ├── 📄 DropdownSample.cs
│   │   │   ├── 📄 EnvMapAnimator.cs
│   │   │   ├── 📄 ObjectSpin.cs
│   │   │   ├── 📄 ShaderPropAnimator.cs
│   │   │   ├── 📄 SimpleScript.cs
│   │   │   ├── 📄 SkewTextExample.cs
│   │   │   ├── 📄 TeleType.cs
│   │   │   ├── 📄 TextConsoleSimulator.cs
│   │   │   ├── 📄 TextMeshProFloatingText.cs
│   │   │   ├── 📄 TextMeshSpawner.cs
│   │   │   ├── 📄 TMP_DigitValidator.cs
│   │   │   ├── 📄 TMP_ExampleScript_01.cs
│   │   │   ├── 📄 TMP_FrameRateCounter.cs
│   │   │   ├── 📄 TMP_PhoneNumberValidator.cs
│   │   │   ├── 📄 TMPro_InstructionOverlay.cs
│   │   │   ├── 📄 TMP_TextEventCheck.cs
│   │   │   ├── 📄 TMP_TextEventHandler.cs
│   │   │   ├── 📄 TMP_TextInfoDebugTool.cs
│   │   │   ├── 📄 TMP_TextSelector_A.cs
│   │   │   ├── 📄 TMP_TextSelector_B.cs
│   │   │   ├── 📄 TMP_UiFrameRateCounter.cs
│   │   │   ├── 📄 VertexColorCycler.cs
│   │   │   ├── 📄 VertexJitter.cs
│   │   │   ├── 📄 VertexShakeA.cs
│   │   │   ├── 📄 VertexShakeB.cs
│   │   │   ├── 📄 VertexZoom.cs
│   │   │   └── 📄 WarpTextExample.cs
│   │   ├── 📁 Sprites
│   │   │   ├── 📄 Default Sprites.png
│   │   │   └── 📄 DropCap Numbers.psd
│   │   └── 📁 Textures
│   │       ├── 📄 Floor Cement.jpg
│   │       ├── 📄 Floor Tiles 1 - diffuse.jpg
│   │       ├── 📄 Fruit Jelly (B&W).jpg
│   │       ├── 📄 Gradient Diagonal (Color).jpg
│   │       ├── 📄 Gradient Horizontal (Color).jpg
│   │       ├── 📄 Gradient Vertical (Color).jpg
│   │       ├── 📄 Mask Zig-n-Zag.psd
│   │       ├── 📄 Small Crate_diffuse.jpg
│   │       ├── 📄 Small Crate_normal.jpg
│   │       ├── 📄 Sunny Days - Seamless.jpg
│   │       ├── 📄 Text Overflow - Linked Text Image 1.png
│   │       ├── 📄 Text Overflow - Linked Text UI Screenshot.png
│   │       ├── 📄 Wipe Pattern - Circle.psd
│   │       ├── 📄 Wipe Pattern - Diagonal.psd
│   │       ├── 📄 Wipe Pattern - Radial Double.psd
│   │       └── 📄 Wipe Pattern - Radial Quad.psd
│   ├── 📁 Fonts
│   │   ├── 📄 Bubble Sans ( KIR ) SDF.asset
│   │   ├── 📄 Bubble Sans ( KIR ).ttf
│   │   ├── 📄 COPYRIGHT.txt
│   │   ├── 📄 HOUSE_OF_TERROR SDF.asset
│   │   ├── 📄 HOUSE_OF_TERROR.ttf
│   │   ├── 📄 LiberationSans - OFL.txt
│   │   ├── 📄 LiberationSans SDF (KIR).asset
│   │   ├── 📄 LiberationSans.ttf
│   │   ├── 📄 VAGGummyBites SDF.asset
│   │   └── 📄 VAGGummyBites.ttf
│   ├── 📁 Resources
│   │   ├── 📁 Fonts & Materials
│   │   │   ├── 📄 LiberationSans SDF.asset
│   │   │   ├── 📄 LiberationSans SDF - Drop Shadow.mat
│   │   │   ├── 📄 LiberationSans SDF - Fallback.asset
│   │   │   └── 📄 LiberationSans SDF - Outline.mat
│   │   ├── 📄 LineBreaking Following Characters.txt
│   │   ├── 📄 LineBreaking Leading Characters.txt
│   │   ├── 📁 Sprite Assets
│   │   │   └── 📄 EmojiOne.asset
│   │   ├── 📁 Style Sheets
│   │   │   └── 📄 Default Style Sheet.asset
│   │   └── 📄 TMP Settings.asset
│   ├── 📁 Shaders
│   │   ├── 📄 TMP_Bitmap-Custom-Atlas.shader
│   │   ├── 📄 TMP_Bitmap-Mobile.shader
│   │   ├── 📄 TMP_Bitmap.shader
│   │   ├── 📄 TMPro.cginc
│   │   ├── 📄 TMPro_Mobile.cginc
│   │   ├── 📄 TMPro_Properties.cginc
│   │   ├── 📄 TMPro_Surface.cginc
│   │   ├── 📄 TMP_SDF-Mobile Masking.shader
│   │   ├── 📄 TMP_SDF-Mobile Overlay.shader
│   │   ├── 📄 TMP_SDF-Mobile.shader
│   │   ├── 📄 TMP_SDF-Mobile SSD.shader
│   │   ├── 📄 TMP_SDF Overlay.shader
│   │   ├── 📄 TMP_SDF.shader
│   │   ├── 📄 TMP_SDF SSD.shader
│   │   ├── 📄 TMP_SDF-Surface-Mobile.shader
│   │   ├── 📄 TMP_SDF-Surface.shader
│   │   └── 📄 TMP_Sprite.shader
│   └── 📁 Sprites
│       ├── 📄 EmojiOne Attribution.txt
│       ├── 📄 EmojiOne.json
│       └── 📄 EmojiOne.png
├── 📄 tree.txt
├── 📁 TutorialInfo
│   ├── 📁 Icons
│   │   ├── 📄 Help_Icon.png
│   │   └── 📄 Mobile 2D.png
│   ├── 📄 Layout.wlt
│   └── 📁 Scripts
│       ├── 📁 Editor
│       │   └── 📄 ReadmeEditor.cs
│       └── 📄 Readme.cs
└── 📁 Unity.VisualScripting.Generated
    ├── 📁 VisualScripting.Core
    └── 📁 VisualScripting.Flow
        └── 📄 UnitOptions.db

```
