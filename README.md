<p align="center">
  <h3 align="center">BCSVReader</h3>

  <p align="center">
    BCSVReader - библиотека для чтения csv файлов.
    <br/>
    <br/>
  </p>
</p>

![Downloads](https://img.shields.io/github/downloads/bol-it/BCSVReader/total) ![Contributors](https://img.shields.io/github/contributors/bol-it/BCSVReader?color=dark-green) ![Issues](https://img.shields.io/github/issues/bol-it/BCSVReader) ![License](https://img.shields.io/github/license/bol-it/BCSVReader) 

### Подключение

1. Скопировать файл BCSVReader.php в каталог App\Libraries
2. Прописать в контроллере:
```php
use App\Libraries\BCSVReader;
```
## Использование

Создаем новый объект
```php
$csv = new BCSVReader();
```
Указываем путь к файлу. Например:
```php
$file = storage_path('app/public/test/test.csv');
```
Установка разделителя поля
```php
$csv->setDelimiter(";");
```
Установка смещения заголовков
```php
$csv->setHeaderOffset(1);
```
Установка кодировки
```php
$csv->set_inputEncoding('Windows-1251');
```
Чтение по строчкам
```php
while (!$csv->eof()) {
    $row = $csv->readRowCSV();
}
```
Прочитать файл в массив
```php
$records = $csv->readCSVToArray();
```
Прочитать файл в массив объектов stdClass
```php
$records1 = $csv->readCSVToArrayObject();
```
