# MicroserviceCurrencyConversion

 Cоздаем второй микросервис - сервис конвертации валют (CCS), он конвертирует заданное количество валюты
 в другую валюту, по обменному курсу, полученному с Forex сервиса (исходные данные Forex сервиса смотри в репо ForexService). 
 
 запуск (CCS) MicroserviceCurrencyConversion, аналогичен Forex сервису (смотри описание ForexService). Для тестерирования  вводим в браузере 
 http://localhost:8100/currency-converter/from/EUR/to/INR/quantity/10000
 получаем ответ в Json файле
 {
  id: 10002,
  from: "EUR",
  to: "INR",
  conversionMultiple: 75,
  quantity: 10000,
  totalCalculatedAmount: 750000,
  port: 8000,
}
Запрос выше позволяет определить стоимость 10000 евро в индийских рупиях.
TotalCalculatedAmount составляет 750000 INR, тестирование показывает, что связь между CCS и FS сервисами установлена.
