# Улучшить timing closure

## Теоретическая вставка

Timing closure — это достижение таких временных ограничений, при которых проект стабильно работает на целевой частоте. Для FPGA это означает, что все критические пути укладываются в заданный clock period.

Основные задачи timing closure:

- корректно задать clock constraints;
- определить пути, которые действительно должны быть синхронизированы;
- уменьшить длинные комбинаторные цепочки;
- улучшить placement и routing;
- устранить нарушения setup/hold timing.

## Что стоит описать в проекте

- частота целевого clock;
- основные timing constraints;
- список критических путей;
- результаты после оптимизаций;
- что изменилось в RTL или constraints.

## Полезные источники

- Vivado Design Suite User Guide: Using Constraints (UG903) — https://docs.amd.com/r/en-US/ug903-vivado-using-constraints
- Defining Timing Constraints in Four Steps (UG949) — https://docs.amd.com/r/en-US/ug949-vivado-design-methodology/Defining-Timing-Constraints-in-Four-Steps
- Vivado Design Suite User Guide: Implementation (UG904) — https://docs.amd.com/r/en-US/ug904-vivado-implementation
- Vivado Design Suite User Guide: Synthesis (UG901) — https://docs.amd.com/r/en-US/ug901-vivado-synthesis

## Практический акцент

Для документации полезно хранить отчёты Vivado до и после оптимизаций: это помогает показать, что timing closure был улучшен не «на словах», а по измеримым метрикам.
