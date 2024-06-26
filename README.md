**Лабораториска вежба бр.2 Софтверско Инженерство.**

David Bogoevski 226091

**Control Flow Graph**

![CreditCart CFG](https://github.com/AzureVolcano/SI_2024_lab2_226091/assets/163325967/e2ac83d3-76a9-4afa-b5f3-352f6db07e64)

**Цикломатска комплексност** 

Цикломатска сложеност е софтверска метрика, што се користи за да се покаже сложеноста на една програма.
Цикломатската комплексност на овој код е **10**, резултатот е добиен според бројот на региони на самиот даден граф.
Т.Н P+1 -> 9 + 1 = **10** (9 предикатни јазли + 1)

**Тест случаи според критериумот Every Branch**

Every Branch ми беа доволни 7 тест случаи за да ги иcпитам можните случаеви според дадениот критериумот.

Payment type: any; AllItems=null -> (фрла исклучок)


AllItems=[]; payment=0 -> (враќа 0)

Allitems=[]; payment=-1 ->(негативна вредност)

AllItems[{name="",price"20",discount="0.5"},barcode=null]; payment=any -> (вредност 0 или празен некој стринг)

AllItems[{name="", price="2000", discount="0.5"},barcode="01234"]; payment=2 ->(вредноста на баркодот е 0 и цена од над 300 ден)

{name="abcde",barcode="4636vh",price"320",discount="0.5"} in AllItemspayment=any -> (баркодот содржи некои рандом букви)

{name="abcde",barcode="4636",price"20",discount="-1"} AllItems; payment=any -> (помала цена (од 300) со негативна вредност (т.н попуст))


**Тест случаи според критериумот Multiple Condition**

а)350 ; 0.2 ; 12345 -> враќа F, **TTF**

б)350 ;0 ; 12345 -> враќа F, **TFF**

в)350 ; 0.2 ; 01234 -> враќа T, **TTT**

г)100 ; 0.2 ; 01234 -> враќа F, **FTT**

Unit тестовите се опфатени во SILab2Test.java.
