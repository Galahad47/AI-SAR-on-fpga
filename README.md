# AI-SAR-on-fpga

Проект FPGA-ускорения алгоритмов **AI / SAR** с использованием **Xilinx Vivado**.

## Описание

`AI-SAR-on-fpga` — это аппаратный проект для реализации вычислительно интенсивной обработки на FPGA. Цель проекта — перенести часть вычислений на логику FPGA, чтобы уменьшить задержку, повысить производительность и улучшить энергоэффективность.

Проект ориентирован на потоковую обработку данных и может включать:

* RTL-модули на Verilog, VHDL или SystemVerilog;
* тестбенчи для функциональной проверки;
* constraints-файлы для Vivado;
* скрипты сборки и автоматизации;
* программную часть для управления и тестирования.

## Возможности

* реализация аппаратного ядра для AI / SAR;
* поддержка потоковой обработки данных;
* интеграция с интерфейсами AXI;
* синтез, implementation и генерация bitstream в Vivado;
* проверка результата через симуляцию;
* адаптация под конкретную FPGA-плату.

## Технологии

* **Vivado**
* Verilog / VHDL / SystemVerilog
* AXI / AXI-Stream / UART / DMA — при необходимости
* Tcl-скрипты для автоматизации
* Python — для вспомогательных утилит и анализа данных

## Требования

### Аппаратные

* FPGA-плата: `[укажите плату]`
* Тактовая частота: `[укажите частоту]`
* Интерфейсы: `[AXI / UART / Ethernet / другое]`

### Программные

* Xilinx Vivado: `[рекомендуемая версия]`
* Vivado Simulator или другой симулятор
* Python 3.x — если используются скрипты

## Структура репозитория

```text
AI-SAR-on-fpga/
├── rtl/            # HDL-модули
├── tb/             # testbench
├── sim/             # файлы симуляции
├── vivado/          # Vivado project (.xpr)
├── constraints/     # XDC-файлы
├── scripts/         # Tcl и вспомогательные скрипты
├── sw/              # программная часть, если есть
└── README.md
```

## Быстрый старт

### 1. Клонировать репозиторий

```bash
git clone https://github.com/<your-username>/AI-SAR-on-fpga.git
cd AI-SAR-on-fpga
```

### 2. Открыть проект в Vivado

```tcl
open_project vivado/project.xpr
```

Или через GUI:

* File → Open Project
* выбрать файл `.xpr`

### 3. Запустить синтез

```tcl
launch_runs synth_1
wait_on_run synth_1
```

### 4. Запустить implementation

```tcl
launch_runs impl_1
wait_on_run impl_1
```

### 5. Сгенерировать bitstream

```tcl
launch_runs impl_1 -to_step write_bitstream
wait_on_run impl_1
```

## Симуляция

Для запуска симуляции в Vivado:

```tcl
launch_simulation
```

Если используются отдельные скрипты:

```bash
./scripts/run_sim.sh
```

## Использование

После генерации bitstream:

1. Загрузите прошивку на FPGA.
2. Подайте входные данные через нужный интерфейс.
3. Получите результат через выходной интерфейс или логирование.
4. Сравните результат с эталонной моделью.

## Constraints

Ограничения проекта должны находиться в файле:

```text
constraints/top.xdc
```

Туда обычно входят:

* назначение пинов;
* ограничения по тактовой частоте;
* временные ограничения;
* параметры интерфейсов.

## Производительность

После запуска на целевой плате можно указать:

* частоту работы: `[MHz]`
* задержку: `[cycles]`
* пропускную способность: `[samples/sec]`
* использование ресурсов:

  * LUT: `[ ]`
  * FF: `[ ]`
  * BRAM: `[ ]`
  * DSP: `[ ]`

## Дорожная карта

* [ ] [Завершить базовую RTL-реализацию](https://github.com/Galahad47/AI-SAR-on-fpga/tree/main/docs/01_bazovaya_rtl_realizatsiya.md)
* [ ] [Добавить полное тестовое покрытие](https://github.com/Galahad47/AI-SAR-on-fpga/tree/main/docs/02_testovoe_pokrytie.md)
* [ ] [Оптимизировать pipeline](https://github.com/Galahad47/AI-SAR-on-fpga/tree/main/docs/03_optimizatsiya_pipeline.md)
* [ ] [Улучшить timing closure](https://github.com/Galahad47/AI-SAR-on-fpga/tree/main/docs/04_timing_closure.md)
* [ ] [Добавить обработку через AXI DMA](https://github.com/Galahad47/AI-SAR-on-fpga/tree/main/docs/05_axi_dma.md)
* [ ] [Подготовить демонстрационный пример](https://github.com/Galahad47/AI-SAR-on-fpga/tree/main/docs/06_demo_example.md)

## Вклад

Pull Request'ы приветствуются.

Перед отправкой изменений проверьте:

* успешный синтез в Vivado;
* отсутствие ошибок симуляции;
* корректность constraints;
* стабильность на целевой плате.

## Лицензия

Укажите лицензию проекта здесь, например:

* MIT
* Apache-2.0
* BSD-3-Clause

## Автор

* `a. s. kovalev`

## Контакты

* Email: `askovalev24@gmail.com`
