# InHive — Android

[![Latest release](https://img.shields.io/github/v/release/TwilgateLabs/inhive-android?sort=semver&label=latest)](https://github.com/TwilgateLabs/inhive-android/releases/latest)
[![Min SDK](https://img.shields.io/badge/min%20SDK-21%20(Android%205.0%20Lollipop)-green)](#)
[![ABI](https://img.shields.io/badge/ABI-arm64--v8a%20%2B%20armeabi--v7a%20%2B%20x86__64-blue)](#)

InHive — кроссплатформенный VPN-клиент. Этот репозиторий — публичная точка для **Android-сборок** (универсальный APK с тремя ABI).

## 📥 Скачать

→ [**Latest release**](https://github.com/TwilgateLabs/inhive-android/releases/latest) — универсальный `.apk`, SHA-256 публикуется рядом с бинарём.

Google Play публикация в очереди — следим в [новостях](https://inhive.ru/news).

## 🚀 Установка

1. Скачай `inhive-android-x.y.z-universal.apk` со страницы релиза.
2. Открой файл из менеджера файлов → нажми **Установить**.
3. Если Android ругается на «неизвестный источник», разреши установку: **Настройки → Приложения → Спец. доступ → Установка из неизвестных источников → разреши для своего браузера/менеджера**.

**Требования:** Android 5.0 (API 21) или новее. Универсальный APK содержит `arm64-v8a` + `armeabi-v7a` + `x86_64` ABIs — поддерживает все актуальные устройства, включая Android-эмуляторы.

## 🔐 Безопасность

Проверь SHA-256 скачанного APK — он публикуется в release notes рядом с бинарём. На Linux/macOS:

```bash
shasum -a 256 inhive-android-x.y.z-universal.apk
```

Подпись APK: V2 + V3 (`apksigner verify --verbose --print-certs inhive-android-x.y.z-universal.apk`). Issuer fingerprint совпадает между всеми релизами — если вдруг поменялся, **не устанавливай** и пиши в [@InHive_support_bot](https://t.me/InHive_support_bot).

Нашёл security issue? **Не открывай публичный issue.** Пиши в [@InHive_support_bot](https://t.me/InHive_support_bot) с темой `SECURITY` — coordinated disclosure, стандартный 90-дневный embargo.

## 🔗 Связанные репозитории

- [TwilgateLabs/inhive-core](https://github.com/TwilgateLabs/inhive-core) — Go-ядро (sing-box 1.13 fork; Android AAR сборка через `make android`)
- [twilgate/inhive-web](https://github.com/twilgate/inhive-web) — Web (private; `inhive.ru`)

## 📜 Лицензия

Этот mirror-repo не содержит исходного кода — только release notes и подписанные бинарные артефакты. Исходники Android в [twilgate/inhive-app](https://github.com/twilgate/inhive-app) (private). Go-ядро — Apache 2.0 (upstream sing-box + наши патчи), см. [TwilgateLabs/inhive-core](https://github.com/TwilgateLabs/inhive-core/blob/main/LICENSE).
