# Завершить базовую RTL-реализацию

## Теоретическая вставка

RTL (Register Transfer Level) описывает аппаратную логику как набор регистров, комбинаторной логики и правил передачи данных между ними. На этом уровне важно определить:

- тактируемые элементы;
- сигналы сброса;
- границы модулей;
- интерфейсы входа и выхода;
- условия передачи данных по pipeline.

Базовая RTL-реализация должна быть достаточно простой, чтобы её можно было синтезировать и проверить в симуляции, но при этом уже отражать основную идею проекта. Для Vivado важно, чтобы код был совместим с синтезом и не содержал недопустимых конструкций для целевой FPGA.

## Что стоит описать в проекте

- состав top-level модуля;
- назначение каждого submodule;
- формат входных и выходных данных;
- схема reset/clock;
- правила обработки валидных и невалидных данных.

## Полезные источники

- Vivado Design Suite User Guide: Synthesis (UG901) — https://docs.amd.com/r/en-US/ug901-vivado-synthesis
- Vivado Design Suite User Guide: Logic Simulation (UG900) — https://docs.amd.com/r/en-US/ug900-vivado-logic-simulation
- Vivado Design Suite User Guide: Designing with IP (UG896) — https://docs.amd.com/r/en-US/ug896-vivado-ip/Vivado-Design-Suite-Documentation
- Vivado Design Suite User Guide: Creating and Packaging Custom IP (UG1118) — https://docs.amd.com/r/en-US/ug896-vivado-ip/Vivado-Design-Suite-Documentation

## Практический акцент

Для первого рабочего варианта полезно сделать минимальный, но полностью проходящий поток данных: input -> processing -> output. После этого уже можно добавлять оптимизации, DMA и интерфейсы управления.


[Вернуться на галвную](https://github.com/Galahad47/AI-SAR-on-fpga)