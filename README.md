# Компонент вкладок

## Обзор

Этот проект реализует компонент навигации с вкладками с использованием HTML, CSS и JavaScript. Компонент поддерживает как простые, так и вложенные вкладки, предоставляя пользователям доступный интерфейс.

## Возможности

- **Множественные группы вкладок**: Создавайте несколько групп вкладок на одной странице, включая вложенные вкладки внутри других вкладок.
- **Доступность с клавиатуры**: Переключайтесь между вкладками с помощью клавиатуры, поддерживаются клавиши со стрелками, Home и End.
- **Поддержка ARIA**: Включает роли и атрибуты ARIA для улучшения доступности.
- **Настраиваемый дизайн**: Легко изменяйте стили вкладок с помощью предоставленного CSS.

## Структура файлов

- **HTML**: Разметка для вкладок, кнопок и контейнеров с содержимым.
- **CSS**: Стили для вкладок и управления активными состояниями.
- **JavaScript**: Обрабатывает логику переключения вкладок, управление активными состояниями и обеспечивает доступность.

### Структура HTML

```html
<div class="tabs" data-tabs>
    <div class="tabs__list" data-list>
        <button class="tabs__button" data-target="tab1">Вкладка 1</button>
        <button class="tabs__button" data-target="tab2">Вкладка 2</button>
        <button class="tabs__button" data-target="tab3">Вкладка 3</button>
    </div>
    <div class="tabs__container" data-tab="tab1">Содержимое для Вкладки 1.</div>
    <div class="tabs__container" data-tab="tab2">Содержимое для Вкладки 2.</div>
    <div class="tabs__container" data-tab="tab3">
        <!-- Пример вложенных вкладок -->
        <div class="tabs" data-tabs>
            <div class="tabs__list" data-list>
                <button class="tabs__button" data-target="nested-tab1">Вложенная вкладка 1</button>
                <button class="tabs__button" data-target="nested-tab2">Вложенная вкладка 2</button>
            </div>
            <div class="tabs__container" data-tab="nested-tab1">Содержимое для Вложенной Вкладки 1.</div>
            <div class="tabs__container" data-tab="nested-tab2">Содержимое для Вложенной Вкладки 2.</div>
        </div>
    </div>
</div>


