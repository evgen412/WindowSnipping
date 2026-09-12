
# WindowSnipping — mixed-DPI fix

Fork of [RaptorX/WindowSnipping](https://github.com/RaptorX/WindowSnipping), by Joe Glines / The Automator. This variant preserves the tested version 1.57.12 and adds support for pinned screenshots on monitors with different Windows scaling settings.

## Changes

- Capture in physical pixels without applying scaling twice.
- Retain the original bitmap and source monitor DPI.
- Redraw the complete screenshot at destination DPI / source DPI when dragging between monitors.
- Use custom dragging to prevent clipped or incorrectly sized screenshot windows.

The intended result is the same interface and text size as the original DPI-aware application moved to the destination display. Enlarging a raster screenshot cannot reproduce the sharpness of freshly rendered text.

## Installation

1. Install AutoHotkey v1.1.36+ in the v1 series, including the 32-bit Unicode interpreter. AutoHotkey v2 is not compatible.
2. Download this branch as a ZIP and extract it. Keep `lib` and `res` beside `WindowSnipping.ahk`.
3. Run the script on Windows 10/11; if necessary, explicitly open it with `AutoHotkeyU32.exe`.
4. Configure shortcuts in the tray menu, capture a region and drag it to another monitor.

Built-in updating is disabled: the update menu item and upstream download handler have been removed to protect this fork's modifications. Get updates manually from this repository.

## Validation

Compiled and launched with AutoHotkey v1.1.37.02. The user manually tested capture and cross-monitor dragging and confirmed the desired behavior. Other upstream features and all possible display layouts have not been comprehensively tested.

Monitor selection uses the center of the screenshot. Selections spanning monitors use the DPI at the center of the selected area. DPI changes while the screenshot is stationary have not been validated.

## Русский

Исправление для мониторов с разным масштабом Windows. Снимок захватывается без уменьшения, а при переносе полностью перерисовывается под DPI другого экрана. Размер букв должен соответствовать оригинальному окну; при увеличении снимка резкость может быть ниже.

Нужен AutoHotkey **v1**, 32-битный Unicode-интерпретатор. Скачайте ZIP этой ветки, сохраните папки `lib` и `res` и запустите `WindowSnipping.ahk`. Встроенное обновление отключено: пункт меню и загрузчик оригинальной версии удалены. Новые версии этого форка устанавливаются вручную из данного репозитория.

## License

Original copyright and MIT permission notice are preserved in [LICENSE](LICENSE). This is an unofficial fork.
