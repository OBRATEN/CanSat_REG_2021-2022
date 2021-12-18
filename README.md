# CanSat_REG_2021-2022
Регулярная лига КанСата в данный момент проходит на двух конструкторах: старый на ATmega128a и новый на  STM32.
Для данной миссии выбран старый из-за низких требований в ресурсоёмкости микроконтроллера.

Характеристики ATmega128a:
4Кб SRAM, 128Кб FLASH, 512Б EEPROM, тактовая частота 8MGz.

Язык программирования: C

По рассчётам, миссия будет потреблять не более 2Кб SRAM, 32Б EEPROM во время работы.

Проверены и работают интерфейсы I2C, OneWire, UART, а так же датчики DS18B20, ADXL345.
На моменте испытания BMP280.
Предстоит по основной миссии: nRF, SD-карта, интерфейс SPI.
В планах дополнительной миссии:
Увеличить объём пакета до 1Кб, добавить слот дополнительной SRAM (максимальное расширение до 64Кб)
Увеличить объём EEPROM- или FLASH- памяти для хранения пакетов.
Создать несколько типов пакетов отправки на разных высотах (от 128Б до 2Кб).
