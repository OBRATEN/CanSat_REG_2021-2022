# CanSat_REG_2021-2022
Регулярная лига CanSat в данный момент проходит на двух конструкторах: старый на ATmega128a и новый на STM32.
Для данной миссии выбран старый из-за низких требований в ресурсоёмкости микроконтроллера.

Характеристики ATmega128a:
4Кб SRAM, 128Кб FLASH, 512Б EEPROM, тактовая частота 8MGz.

Языки программирования: C/C++

По рассчётам, миссия будет потреблять не более 2Кб SRAM, 32Б EEPROM, 10Кб FLASH.

Проверены интерфейсы I2C, OneWire, UART, SPI;
Проверены датчики:
1. Датчик температуры DS18B2, считывание в тип данных float,
2. Трёхосевой акселирометр ADXL345, считывание в тип данных float,
3. Датчик температуры и давления BMP280, считывание температуры в int32, давления в float. Высчитывается высота в float;

Написана передача данных по радиосвязи на частоте 2.4ГГц. Выбран 78 канал (2.478ГГц);
Написано "сырое" взаимодействие с SD (R/W);

В планах дополнительной миссии:
Создать внешнюю систему "Watchdog" для защиты от зависаний на основе микроконтроллера ATtiny;
Создать несколько типов пакетов отправки на разных высотах (от 128Б до 2Кб).

![alt_text](https://github.com/OBRATEN/CanSat_REG_2021-2022/blob/main/2021-12-20-182703_1366x768_scrot.png)
