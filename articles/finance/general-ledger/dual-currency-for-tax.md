---
title: Maksu topeltvaluuta tugi
description: Selles teemas selgitatakse, kuidas laiendada maksudomeenis topeltvaluuta arvestuse funktsiooni ja maksude arvutamise ja sisestamise mõju
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 2e3e7ff93ca3c6a2266ba0f33c8eac7ceade0d4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978592"
---
# <a name="dual-currency-support-for-sales-tax"></a>Käibemaksu topeltvaluuta tugi
[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas laiendada käibemaksude topeltvaluuta arvestust ja käibemaksu arvutamise, sisestamise ja tasakaalustuste mõju.

Rakenduse Dynamics 365 Finance topeltvaluuta funktsioon lisati versioonis 8.1 (oktoober 2018). See muudab raamatupidamise kirjete aruandevaluutas arvutamise viisi.

Varasemates versioonides teisendati kanded aruandlusvaluutasse järgmises järjestuses. 

- Kande kogusumma arvutati kande valuutas > kande summa teisendati arvestusvaluutaks > arvestusvaluuta summa teisendati aruandlusvaluutaks

Pärast topeltvaluuta funktsiooni lubamist teisendati kanded aruandlusvaluutasse järgmises järjestuses.

- Kandevaluuta summa > Aruandlusvaluuta summa

Lisateavet topeltvaluuta kohta vt teemast [Topeltvaluuta](dual-currency.md).

Topeltvaluuta toe tulemusena on funktsiooni halduses saadaval kaks uut funktsiooni. 

- Käibemaksu konverteerimine (uus versioonis 10.0.13)

Käibemaksu topeltvaluuta tugi tagab, et maksud arvutatakse maksu valuutas täpselt ja et käibemaksu tasakaalustuse saldo arvutatakse täpselt nii arvestusvaluutas kui ka aruandlusvaluutas. 

## <a name="sales-tax-conversion"></a>Käibemaksu teisendamine

Parameeter **Käibemaksu teisendamine** pakub maksusumma kandevaluutast maksuvaluutasse teisendamiseks kaks võimalust. 

- Arvestusvaluuta: teekond on „Summa kandevaluutas > Summa arvestusvaluutas > Summa maksuvaluutas”. Valuuta konverteerimiseks kasutatakse arvestusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).
- Aruandlusvaluuta: teekond on „Summa kandevaluutas > Summa aruandlusvaluutas > Summa maksuvaluutas”. Valuuta konverteerimiseks kasutatakse aruandlusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).

### <a name="example"></a>Näide

Lihtne näide selle funktsiooni demonstreerimiseks on järgmine.

Pearaamatu ja maksu valuuta seadistamine

| Kande valuuta | Arvestusvaluuta | Aruandlusvaluuta | Maksuvaluuta |
| -------------------- | ------------------- | ------------------ | ------------ |
|  eurot                  | USA dollar                 | GBP                | GBP          |

Valuutakurss

| Valuutast | Valuutaks | Tegur | Valuutakurss |
| ------------- | ----------- | ------ | ------------- |
|  eurot           | USA dollar         | 1      | 1.11          |
|  eurot           | GBP         | 1      | 0.83          |
| USA dollar           | GBP         | 1      | 0.75          |

Maksusumma arvutamine erinevate parameetrite valikutega

Maksusumma = 100 EUR

| Käibemaksu teisendamise parameetrid | Kande valuuta (EUR) | Arvestusvaluuta (USD) | Aruandlusvaluuta (GBP) | Maksuvaluuta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Arvestusvaluuta             | 100                        | 111                       | 83                       | **83.25**          |
| Aruandlusvaluuta              | 100                        | 111                       | 83                       | **83**             |

Selle parameetri saab konfigureerida maksuhalduri nõuetelevastavuse nõude alusel.


### <a name="upgrade-consideration"></a>Täienduse kaalutlus

See funktsioon rakendub ainult uutele kannetele. Tabelis TAXTRANS juba salvestatud, kuid veel mitte tasakaalustatud maksukannete puhul ei arvuta süsteem maksu summat maksu valuutas ümber, kuna maksu sisestamise hetke vahetuskurss on juba puudu.

Eelneva stsenaariumi vältimiseks soovitame muuta selle parameetri väärtust uues (puhtas) maksu tasakaalustusperioodil, mis ei sisalda ühtegi tasakaalustamata maksukannet. Selle väärtuse muutmiseks maksu tasakaalustusperioodi keskel käivitage enne selle parameetri väärtuse muutmist programm „Käibemaksu tasakaalustamine ja sisestamine” praeguse maksu tasakaalustusperioodi jaoks.


## <a name="track-reporting-currency-tax-amount"></a>Aruandlusvaluuta maksu summa jälgimine

Aruandlusvaluuta summade jälgimiseks lisati maksudega seotud tabelitesse kolm uut välja. Need väljad asuvad tabelites TAXUNCOMMITTED ja TAXTRANS.

- TaxAmountRep: maksusumma aruandlusvaluutas
- TaxBaseAmountRep: aruandlusvaluuta baassumma
- TaxInCostPriceRep: mahaarvamatu summa aruandlusvaluutas

Ainult tabelis TAXUNCOMMITTED salvestatud maks, mis pole veel postitatud, arvutab süsteem maksu summa postitmise ajal aruandlusvaluutas ümber ja salvestab tabelis TAXTRANS.

See väljaanne ei sisalda muudatusi aruannetes ega vormides, mis näitavad maksu summat aruandlusvaluutas. Aruannete ja vormide muudatused edastatakse tulevases väljaannetes.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Maksu tasakaalustuse automaatne saldo aruandlusvaluutas

Kui maksu tasakaalustamine ei ole aruandlusvaluuta jaoks mingil põhjusel tasakaalus, näiteks müügimaksu teisendustee on „Arvestusvaluuta” või vahetuskurss muutub samal maksu tasakaalustamise perioodil, siis süsteem loob automaatselt raamatupidamise kirjed, et reguleerida maksu summa erinevust ja tasakaalustada seda realiseeritud vahetusega saadud tulu/kulu kontoga, mis on pearaamatu seadistuses konfigureeritud.

Kasutades selle funktsiooni demonstreerimiseks eelmist näidet, oletagem, et tabeli TAXTRANS andmed on sisestamise ajal järgmised.

| Käibemaksu teisendamise parameetrid | Kande valuuta (EUR) | Arvestusvaluuta (USD) | Aruandlusvaluuta (GBP) | Maksuvaluuta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Arvestusvaluuta             | 100                        | 111                       | 83                       | **83.25**          |
| Aruandlusvaluuta              | 100                        | 111                       | 83                       | **83**             |

Kui käivitate käibemaksu tasakaalustuse programmi kuu lõpus, on raamatupidamise kirje järgmine.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Stsenaarium: müügimaksu teisendamine = „arvestusvaluuta”

| Põhikonto           | Kande valuuta (GBP) | Arvestusvaluuta (USD) | Aruandlusvaluuta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Makstav/saadav maks | –83,25                     | –111                      | –83,25                   |
| Maksu tasakaalustus         | 83.25                      | 111                       | 83.25                    |
| Realiseeritud kasum/kahjum     | 0                          | 0                         | –0,25                    |
| Makstav/saadav maks | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Stsenaarium: müügimaksu teisendamine = „aruandlusvaluuta”


| Põhikonto           | Kande valuuta (GBP) | Arvestusvaluuta (USD) | Aruandlusvaluuta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Makstav/saadav maks | –83                        | –110,67                   | –83                      |
| Maksu tasakaalustus         | 83                         | 110.67                    | 83                       |
| Realiseeritud kasum/kahjum     | 0                          | 0.33                      | 0                        |
| Makstav/saadav maks | 0                          | –0,33                     | 0                        |



Lisateavet vt järgmistest teemadest:

- [Topeltvaluuta](dual-currency.md)
- [Käibemaksu ülevaade](indirect-taxes-overview.md)

