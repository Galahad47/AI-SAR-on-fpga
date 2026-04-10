# Подготовить демонстрационный пример

## Теоретическая вставка

Демонстрационный пример нужен для того, чтобы показать проект как воспроизводимую систему: от сборки до результата на железе. Такой пример должен быть коротким, понятным и стабильным.

Обычно demo включает:

- подготовленный набор входных данных;
- инструкцию по сборке в Vivado;
- шаги по загрузке bitstream;
- запуск обмена данными;
- ожидаемый результат и способ его проверки.

## Что стоит описать в проекте

- минимальный сценарий запуска;
- формат тестового входа;
- способ получения результата;
- краткую схему всех шагов;
- ожидаемый output для сравнения.

## Полезные источники

- Vivado Design Suite User Guide: Programming and Debugging (UG908) — https://docs.amd.com/r/en-US/ug908-vivado-programming-debugging
- Vivado Design Suite User Guide: Logic Simulation (UG900) — https://docs.amd.com/r/en-US/ug900-vivado-logic-simulation
- Vivado Design Suite User Guide: Using Constraints (UG903) — https://docs.amd.com/r/en-US/ug903-vivado-using-constraints

## Практический акцент

Хороший demo-сценарий позволяет показать, что проект не только синтезируется, но и реально работает на FPGA с понятным повторяемым результатом.


[Вернуться на галвную](https://github.com/Galahad47/AI-SAR-on-fpga)