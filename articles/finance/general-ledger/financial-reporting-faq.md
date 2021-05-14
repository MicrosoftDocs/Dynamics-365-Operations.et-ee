---
title: Finantsaruandluse KKK
description: Sellesse teemasse on kogutud teiste kasutajate esitatud finantsaruandlusega seotud küsimused.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923021"
---
# <a name="financial-reporting-faq"></a>Finantsaruandluse KKK 

Selles teemas antakse vastused korduma kippuvatele küsimustele finantsaruandluse kohta. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Kuidas piirata puuturbe abil juurdepääsu aruandele?

Järgmises näites kirjeldatakse aruandele juurdepääsu piiramist puuturbe abil.

Demoettevõttel USMF on bilansiaruanne, millele ei pea kõik finantsaruandluse kasutajad juurde pääsema. Juurdepääsu piiramiseks saate kasutada puuturvet, et keelata juurdepääs ühele aruandele, nii et sellele pääseksid juurde ainult teatud kasutajad. Juurdepääsu piiramiseks tehke järgmist. 

1. Logige sisse Financial Reporter Report Designerisse.
2. Looge uus puudefinitsioon. Avage **Fail > Uus > Puu definitsioon**.
3. Topeltklõpsake veerus **Üksuse turve** rida **Kokkuvõte**.
4. Valige **Kasutajad ja grupid**.  
5. Valige kasutajad või grupid, kellele soovite anda juurdepääsu sellele aruandele. 
6. Valige käsk **Salvesta**.
7. Lisage aruandedefinitsioonis uus puudefinitsioon.
8. Valige puudefinitsioonis **Säte**. Valige jaotises **Aruandlusüksuse valik** **Kaasa kõik üksused**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Kuidas tuvastada, millised kontod minu saldodele ei vasta?

Kui teil on aruanne, millel pole vastavaid saldosid, võivad järgmised tegevused aidata teil selliseid kontosid ja hälbeid tuvastada. 

**Financial Reporter Report Designer**
1. Looge Financial Reporter Report Designeris uus readefinitsioon. 
2. Valige **Redigeeri > Lisa read dimensioonidest**.
3. Valige **MainAccount**.  
4. Valige nupp **OK**.
5. Salvestage readefinitsioon.
6. Uue veerudefinitsiooni loomine
7. Looge uus aruandedefinitsioon.
8. Valige **Sätted** ja tühjendage selle suvandi ruut.  
9. Looge aruanne. 
10. Eksportige aruanne Microsoft Excelisse.

**Dynamics 365 Finance** 
1. Avage Dynamics 365 Finance'is **Pearaamat > Päringud ja aruanded > Proovibilanss**.
2. Saate määrata järgmised parameetrid.
   - **Alguskuupäev** – sisestage finantsaasta algus.
   - **Lõppkuupäev** – sisestage kuupäev, mille kohta aruande loote.
   - **Finantsdimensioon** – seadke selle välja väärtuseks **Põhikonto kogum**.
 3. Valige **Arvuta**.
 4. Eksportige aruanne Microsoft Excelisse.

Nüüd saate kopeerida andmeid Financial Reporteri Exceli aruandest proovibilansi aruandesse, et võrrelda veerge **Sulgemissaldo**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]