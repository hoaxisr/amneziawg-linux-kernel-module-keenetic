# AmneziaWG 2.0 — модули ядра для Keenetic (MIPS) / (MIPSEL)

Готовые модули ядра [AmneziaWG](https://docs.amnezia.org/ru/documentation/amnezia-wg/) 2.0 для роутеров Keenetic на ядре `4.9-ndm-5`.

> **5 сборок покрывают все MIPS-модели (61 роутер)**

## Файлы модулей

| Файл | Размер | ELF | Vermagic | Моделей |
|---|---|---|---|---|
| `amneziawg-MIPSEL-MT7621.ko` | 150 KB | 32-bit LSB | 4.9-ndm-5 SMP | 15 |
| `amneziawg-MIPSEL-MT7628.ko` | 148 KB | 32-bit LSB | 4.9-ndm-5 (без SMP) | 33 |
| `amneziawg-MIPS-EN7512.ko` | 151 KB | 32-bit MSB | 4.9-ndm-5 SMP | 5 |
| `amneziawg-MIPS-EN7516.ko` | 151 KB | 32-bit MSB | 4.9-ndm-5 SMP | 4 |
| `amneziawg-MIPSEL-EN7528.ko` | 150 KB | 32-bit LSB | 4.9-ndm-5 SMP | 4 |

## Совместимость

| Сборка | Архитектура | Модели |
|---|---|---|
| **MT7621** | mipsel | KN-1010, 1011, 1810, 1910, 1913, 2310, 2311, 2610, 2810, 2910, 2911, 3010, 3013, 3410, 3510 |
| **MT7628** | mipsel | KN-1110, 1111, 1112, 1121, 1210–1221, 1310–1311, 1410, 1510–1511, 1610–1621, 1710–1721, 2210–2212, 3210–3311, 4910 |
| **EN7512** | mips (BE) | KN-2010, 2011, 2012, 2110, 2111 |
| **EN7516** | mips (BE) | KN-2112, 2410, 2510, 3610 |
| **EN7528** | mipsel | KN-1912, 3012, 3710, 3810 |

## Установка

1. Скачайте `.ko`-файл, соответствующий вашей модели роутера.
2. Скопируйте модуль на роутер, например через SCP:
   ```bash
   scp amneziawg-MIPSEL-MT7621.ko root@192.168.1.1:/opt/tmp/
   ```
3. Загрузите модуль:
   ```bash
   insmod /opt/tmp/amneziawg-MIPSEL-MT7621.ko
   ```


