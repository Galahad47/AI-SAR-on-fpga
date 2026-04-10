# Добавить полное тестовое покрытие

## Теоретическая вставка

Тестовое покрытие в FPGA-проектах обычно строится на нескольких уровнях:

- модульные тесты для отдельных блоков;
- интеграционные тесты для связки блоков;
- проверка граничных случаев;
- сравнение с эталонной моделью;
- регрессионные тесты после изменений.

Для RTL-проектов особенно важно проверить не только штатный режим, но и поведение при reset, отсутствии valid-сигнала, переполнениях, изменении длины пакета и ошибочных входных данных.

## Что стоит описать в проекте

- перечень тестбенчей;
- входные стимулы;
- ожидаемые результаты;
- метрики прохождения теста;
- способ автозапуска симуляции.

## Полезные источники

- Vivado Design Suite User Guide: Logic Simulation (UG900) — https://docs.amd.com/r/en-US/ug900-vivado-logic-simulation
- Vivado Design Suite User Guide: Logic Simulation Overview (UG900) — https://docs.amd.com/r/en-US/ug900-vivado-logic-simulation/Logic-Simulation-Overview
- Vivado Design Suite User Guide: Preparing for Simulation (UG900) — https://docs.amd.com/r/en-US/ug900-vivado-logic-simulation/Preparing-for-Simulation
- Vivado Design Suite User Guide: Supported Simulators (UG900) — https://docs.amd.com/r/en-US/ug900-vivado-logic-simulation/Supported-Simulators

## Практический акцент

Хорошее тестовое покрытие для этого проекта должно позволять быстро убедиться, что изменения в RTL не ломают корректность вычислений и интерфейсов.
