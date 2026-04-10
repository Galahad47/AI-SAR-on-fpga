# Оптимизировать pipeline

## Теоретическая вставка

Pipeline в FPGA — это способ разделить вычисление на несколько последовательных стадий с регистрами между ними. Это позволяет:

- уменьшить длину комбинаторных путей;
- повысить частоту работы;
- увеличить пропускную способность;
- лучше использовать параллелизм FPGA.

При проектировании pipeline важно балансировать задержки между стадиями. Если одна стадия существенно тяжелее остальных, именно она будет ограничивать частоту всей системы.

## Что стоит описать в проекте

- количество стадий pipeline;
- задержка каждой стадии;
- где стоят регистры;
- как синхронизируются данные и valid-сигналы;
- как меняется latency и throughput после оптимизации.

## Полезные источники

- UltraFast Design Methodology Guide for FPGAs and SoCs (UG949) — https://docs.amd.com/r/en-US/ug949-vivado-design-methodology/Vivado-Design-Suite-User-and-Reference-Guides
- Vivado Design Suite User Guide: Synthesis (UG901) — https://docs.amd.com/r/en-US/ug901-vivado-synthesis
- Vivado Design Suite User Guide: Implementation (UG904) — https://docs.amd.com/r/en-US/ug904-vivado-implementation
- Vivado Design Suite User Guide: Synthesis Constraints and Attributes (UG949) — https://docs.amd.com/r/en-US/ug949-vivado-design-methodology/Defining-Timing-Constraints-in-Four-Steps

## Практический акцент

Оптимизация pipeline обычно идёт вместе с анализом timing reports: сначала находят критический путь, потом решают, на какую стадию его лучше разрезать.


[Вернуться на галвную](https://github.com/Galahad47/AI-SAR-on-fpga)