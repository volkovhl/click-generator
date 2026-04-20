<p align="center">
  <a href="https://volkovhl.github.io/click-generator/">
    <img src="https://github.com/volkovhl/click-generator/blob/main/click-generator.webp?raw=true" alt="Click Generator Preview" width="640" style="border-radius:12px; box-shadow: 0 8px 32px rgba(0,0,0,0.5);">
  </a>
</p>

<h1 align="center">
  ⚡ Click Generator
</h1>

<p align="center">
  <strong>Генератор щелчков от 0.1 Гц до 400 Гц (6–24 000 BPM) в браузере</strong><br>
  Идеальный метроном для медитации, экспериментов со звуком и настройки аппаратуры
</p>

<p align="center">
  <a href="https://volkovhl.github.io/click-generator/">
    <img src="https://img.shields.io/badge/ЗАПУСТИТЬ_ДЕМО-00D4FF?style=for-the-badge&logo=google-chrome&logoColor=white&labelColor=111" alt="Live Demo">
  </a>
  &nbsp;
  <a href="https://github.com/volkovhl/click-generator/stargazers">
    <img src="https://img.shields.io/github/stars/volkovhl/click-generator?style=for-the-badge&logo=github&logoColor=white&labelColor=111" alt="Stars">
  </a>
  &nbsp;
  <a href="https://github.com/volkovhl/click-generator/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/volkovhl/click-generator?style=for-the-badge&logo=opensourceinitiative&logoColor=white&labelColor=111" alt="License">
  </a>
</p>

---

## ✨ Возможности

<div align="center">
  <table>
    <tr>
      <td align="center" width="160">🎛️<br><b>0.1 Гц – 400 Гц</b></td>
      <td align="center" width="160">🔄<br><b>BPM / Гц синхронизация</b></td>
      <td align="center" width="160">👆<br><b>Drag & click</b></td>
      <td align="center" width="160">📱<br><b>Мобильный</b></td>
    </tr>
  </table>
</div>

- 🎚️ **Уникальный диапазон**: от инфранизких частот (0.1 Гц / 6 BPM) до звуковых импульсов (400 Гц / 24 000 BPM)  
- 🎛️ **Два режима управления**: задавайте темп в BPM или в герцах — поля синхронизированы  
- 🎨 **Визуальный индикатор**: яркая вспышка при каждом щелчке  
- 🔊 **Чистый звук**: короткий щелчок на Web Audio API с возможностью точной настройки  
- 📱 **Адаптивный дизайн**: удобно работает на смартфонах, планшетах и ПК  
- ⚡ **Высокая точность**: интеллектуальный планировщик с компенсацией джиттера

---

## 🛠 Технологии

- **Чистый стек**: HTML + CSS + JavaScript (без внешних библиотек)  
- **Звуковой движок**: Web Audio API + динамическая генерация клика  
- **Интерфейс**: Реактивные ползунки, кнопки степпера, визуальная обратная связь  
- **Планирование времени**: `setTimeout` с адаптивной коррекцией ожидаемого времени  
- **Адаптивность**: Responsive layout + безопасные зоны для касаний

---

## 📲 Как использовать

1. Откройте **[демо](https://volkovhl.github.io/click-generator/)**  
2. Нажмите **СТАРТ** и разрешите звук в браузере (если потребуется)  
3. Регулируйте темп:
   - Перетаскивайте ползунок **BPM** или **Гц**
   - Используйте кнопки **+ / –**
   - Вводите точные значения в числовые поля  
4. Следите за визуальным индикатором — он мигает синхронно со звуком  
5. Нажмите **СТОП**, чтобы завершить

> 💡 **Совет**: Для очень низких частот (0.1 Гц) используйте большие наушники — пауза между щелчками составляет 10 секунд.  
> ⚡ На 400 Гц интервал всего 2.5 мс — это уже звуковой тон, а не отдельные удары.

---

## 🧠 Что внутри

### Диапазон частот

| Режим | Нижняя граница | Верхняя граница | Применение |
|-------|----------------|----------------|-------------|
| BPM   | 6 уд/мин       | 24 000 уд/мин  | Музыкальный метроном |
| Гц    | 0.1 щелчков/с  | 400 щелчков/с  | Научные эксперименты, тесты |

### Звуковой движок
- Генерация короткого импульса (35 мс) с частотой 1850 Гц + шумовая огибающая  
- Регулировка громкости через `GainNode`  
- Независимое воспроизведение без блокировки UI  

### Планировщик
- Динамический расчёт задержки: `expectedTime = expectedTime + intervalMs`  
- Коррекция при дрейфе >30% от интервала  
- Визуальная вспышка с дебаунсом (80 мс)

---

<p align="center">
  <a href="https://volkovhl.github.io/click-generator/">▶️ Запустить генератор</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/volkovhl/click-generator">📂 Исходный код</a>
</p>

<p align="center">
  <sub>MIT License • Сделано с ❤️ в Russia</sub>
</p>
