# Добавить обработку через AXI DMA

## Теоретическая вставка

AXI DMA — это IP-ядро, которое обеспечивает высокоскоростную передачу данных между памятью и AXI4-Stream-переферией. Оно снимает часть нагрузки с CPU, потому что передача массивов данных может выполняться аппаратно.

В контексте FPGA-проекта AXI DMA обычно используют для:

- загрузки входных данных в потоковую логику;
- передачи результатов обратно в память;
- уменьшения участия процессора в копировании данных;
- построения эффективного dataflow-пайплайна.

## Что стоит описать в проекте

- структура канала передачи данных;
- формат AXI4-Stream;
- сигналы TVALID, TREADY, TLAST;
- схема взаимодействия DMA и core-модуля;
- особенности scatter/gather или direct register mode.

## Полезные источники

- AXI DMA LogiCORE IP Product Guide (PG021) — https://docs.amd.com/r/en-US/pg021_axi_dma
- AXI DMA Introduction (PG021) — https://docs.amd.com/r/en-US/pg021_axi_dma/Introduction
- AXI DMA Feature Summary (PG021) — https://docs.amd.com/r/en-US/pg021_axi_dma/Feature-Summary
- Vivado Design Suite: AXI Reference Guide (UG1037) — https://docs.amd.com/r/en-US/ug1037-vivado-axi-reference-guide
- How AXI4-Stream Works — https://docs.amd.com/r/en-US/ug1399-vitis-hls/How-AXI4-Stream-Works

## Практический акцент

Для реального запуска лучше сразу зафиксировать, кто управляет DMA, какой буфер используется и как определяется конец пакета через TLAST.


[Вернуться на галвную](https://github.com/Galahad47/AI-SAR-on-fpga)