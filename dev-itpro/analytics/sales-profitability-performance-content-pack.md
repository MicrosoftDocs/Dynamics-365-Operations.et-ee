---
title: "Müügi ja tulususe tulemuste Power BI sisu"
description: "See teema kirjeldab Microsoft Power BI-le mõeldud Microsoft Dynamics 365 for Operationsi müügi ja tulususe alaste tulemuste sisupaketis sisalduvat. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida sisupaketi loomiseks kasutatakse."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Müügi ja tulususe tulemuste Power BI sisu

See teema kirjeldab Microsoft Power BI-le mõeldud Microsoft Dynamics 365 for Operationsi müügi ja tulususe alaste tulemuste sisupaketis sisalduvat. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida sisupaketi loomiseks kasutatakse.

<a name="overview"></a>Ülevaade
--------

See sisupakett loodi müügijuhtidele juhtimismõõdikute (tulu, brutokasum ja kasumimarginaalid) jälgimiseks. See kasutab Microsoft Dynamics 365 for Operationsi müügikannete andmeid ning annab koondvaate kogu ettevõtte müüginumbritest ja müügitulemuste jaotusest klientide ning toodete kohta. Tulude ja kasumi kasvu muudatuste esiletõstmisega saab aruandeid kasutada juhtide teavitamiseks eraldi klientide ja toodete positiivsetest ning negatiivsetest trendidest. Kategooria- ja piirkonnajuhtidele on abiks diagrammid, mis võrdlevad üksteisega erinevate kategooriate ja kliendigruppide tulusid ja kasumlikkust, tuues välja mahajääjad ja liidrid. Põhjalik aruanne, mis näitab eraldi kliendi tulu võrreldes kasumimarginaaliga, annab kliendihalduritele andmepõhja müügi- ja turunduspanuse kohandamiseks iga kliendi vastava profiiliga. Müügi ja tulususe tulemuste sisupakett võimaldab müügijuhtidel analüüsida müügitulemusi järgmisel alusel.

-   Aasta senine tulu (kliendigruppide ja eraldi klientide, müügikategooriate ja eraldi toodete ning geograafiliste asukohtade järgi)
-   Tulu muutus aastate lõikes (kliendipiirkondade ja müügikategooriate alusel)

Tulusust saab analüüsida järgmistel alustel.

-   Brutokasum ja kasumimarginaal (kliendigruppide ja toote müügikategooriate alusel)
-   Brutokasumi muutus aastate lõikes
-   Kliendi kasumlikkus (tulu järgi võrreldes kogutuluga)

## <a name="accessing-the-content-pack"></a>Juurdepääs sisupaketile
Müügi ja tulususe tulemuste Power BI sisupakett on avaldatud juurutusvahendina teenuses Lifecycle Services (LCS) ja sellele pääseb juurde rakendusest Microsoft Dynamics 365 for Operations. Lisateavet Power BI aruannete juurde pääsemise ja nende käivitamise kohta vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Sisupaketti kuuluvad mõõdikud
Sisupakett sisaldab diagrammide, paanide ja tabelitena visualiseeritud mõõdikute kogumist koosnevat aruannet. Järgmine tabel annab ülevaate sisupaketi visualiseerimistest.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Aruandeleht**        | **Diagrammid**                                 | **Paanid**                                               |
| Tulu kliendi alusel    | 10 parimat klienti tulu alusel                | Kogutulem                                           |
|                        | Kogutulu kliendigrupi alusel            | YOY tulu kasv                                      |
|                        | Keskmine kliendi tulu kliendigrupi alusel | Kogutulu                                            |
|                        | Tulu ja brutokasum kliendigrupi alusel   |                                                         |
| Tulu toote alusel     | Tulu ja brutokasum müügikategooria alusel   | Toodete \# kokku                                    |
|                        | 10 parimat toodet tulu alusel                 | Aktiivsete toodete arv ja osakaal koguarvust |
|                        | Kogutulu müügikategooria alusel            | Toodete arv, mis annavad 80% tulust           |
| Tulu perioodi alusel\*    | Tulu kuu alusel                           | YOY tulu kasv                                      |
|                        | Varasema tulu hälve, YOY             | YOY tulu kasvu %                                    |
|                        | Müügihälve kokku kliendipiirkonna alusel    |                                                         |
| Tulu asukoha järgi    | Müügitulu linna alusel                      |                                                         |
|                        | YOY tulu kasvu %                       |                                                         |
|                        | Müügitulu piirkonna alusel                    |                                                         |
| Kliendi kasumlikkus | Kogutulu võrreldes kliendipõhise tuluga   | Brutokasum, kogutulu, YOY tulu kasv          |
| Tulususe analüüs | Tulu ja kogutulu kuu alusel          |                                                         |
|                        | 15 parimat klienti kogutulu alusel           |                                                         |
|                        | Kogutulu kuu alusel, YOY                 |                                                         |

\* Selle ja eelmise aasta tulu ja kasv müügikategooriate alusel.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Müügi ja tulususe tulemuste sisupaketi aruande täitmiseks kasutatakse Dynamics 365 for Operationsi andmeid. Need esitatakse koondmõõtmistena, mis on koondatud üksuse kauplusse, mis on analüüsimiseks optimeeritud Microsoft SQL-i andmebaas. Lugege selle kohta lisa ajaveebist [Power BI integratsioon üksuse kauplusega Dynamicsis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Selle sisupaketi koondmõõtmised on rakenduste Dynamics AX 2012 ja AX 2012 R3 müügikuubis olnud koondmõõtmiste alamkogum. Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks. Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebis [Power BI integratsioon üksuse kauplusega Dynamicsis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Järgmisi arve ridade üksuse peamisi koondmõõtmisi kasutatakse sisupaketi alusena.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Üksus**    | **Peamised koondmõõtmised**               | **Dynamics 365 for Operationsi andmeallikas** | **Väli**                                    | **Kirjeldus**                          |
| Arve read | Tulu                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Summa arvestusvaluutas            |
|               | Müüdud kaupade omahind                           | InventTrans                                     | SUM(CostAmountPosted + CostAmountAdjustment) | Kulusumma + korrigeerimine                 |
|               | Komisjoni rea summa – arvestusvaluuta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisjoni rea summa arvestusvaluutas |

Järgmine tabel näitab arve ridade üksuse peamisi koondmõõtmisi, mida kasutatakse mitme arvutatud meetme loomiseks sisupaketi andmekogumis.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Mõõt**       | **Arvutatakse kui**                                                                                |
| Kogukasum      | SUM(Tulu – COGS – Komisjon – Käibemaks (sisaldub kliendiarve rea summas))          |
| Kogutulu      | SUM(Kogutulu / (Tulu – Käibemaks (sisaldub kliendiarve rea summas)))             |
| Eelmise aasta tulu | Eelmise aasta tulu = CALCULATE(SUM('Arve read'\[Tulu\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\])) |

Järgmisi **müügikuubi** põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate andmiseks.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Üksus**       | **Atribuutide näited**                           |
| Kliendid        | Kliendigrupid, Kliendipiirkonnad, Aadress, Valdkond |
| Tooted         | Tootenumber, Toote nimi, Kaubagruppide nimi       |
| Müügikategooriad | Müügi kategooria nimed                                 |
| Juriidilised isikud   | Juriidilise isiku nimed                                   |
| Kuupäevad            | Kuupäevad                                                |

Vaikimisi kuvab sisupakett jooksva kalendriaasta andmed, kuid saate avada aruandefiltrite jaotise ja kuupäevafiltrit muuta. Saate muuta ka ettevõtte filtrit.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)



