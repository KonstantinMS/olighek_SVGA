≡ Библиотека для настройки по I2C следующих дисплеев фирмы Olightek:  
* **SVGA050**  
* **SVGA060**  
* **SVGA097**  

Для применения необходимо:
* добавить файлы в проект;
* собрать проект, после сборки обратить внимания на строчки **infos**, нужно подключить ваши вспомогательные файлы и вставить вашу функцию работы с I2C
* создать экземпляр класса (с указанием используемого адреса)
```cpp
olightek display(0x0F);
```
* Произвести миниммальную инициализацию дисплея
```cpp
display.olightek_init();
```
* Установить желаюмую яркость с помощью функций  
```cpp
bool olightek_brightness    (uint8_t value);			// Установка яркости дисплея
bool olightek_contrast      (uint8_t value);			// Установка контрастности дисплея
bool olightek_vCom          (uint8_t value);			// Установка напряжения катода дисплея
```