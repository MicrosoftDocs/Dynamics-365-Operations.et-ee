---
title: Maksekviitungi vormingu seadistamine projektiarvete jaoks
description: Ettevõtted kinnitavad sageli arvetele prinditud maksekviitungeid, et aidata kliente ja pakkuda sisestamise ja tasakaalustamise jaoks makseviidet.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b365585e884749bb73f8ba9054e446f210e10f37
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565063"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Maksekviitungi vormingu seadistamine projektiarvete jaoks

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ettevõtted kinnitavad sageli arvetele prinditud maksekviitungeid, et aidata kliente ja pakkuda sisestamise ja tasakaalustamise jaoks makseviidet. Maksekviitungit saab lisaks müügiarvetele ja vabas vormis arvetele kasutada projekti ja teenuse arvete, märgukirjade, viivisearvete, kontoväljavõtete jaoks. Maksekviitungite töötlemiseks seadistage esmalt oma kreeditori ID-number ja maksekviitungi manuste vormingud.

See protsess kasutab demoettevõtte DEMF-i andmeid. 

See funktsionaalsus on saadaval ainult juriidilistele isikutele, kelle esmane aadress on Taanis.


## <a name="set-up-a-creditor-id-number"></a>Kreeditori ID-numbri seadistamine
1. Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.
2. Laiendage või ahendage jaotist Pangakonto teave.
3. Klõpsake nuppu Redigeeri.
4. Sisestage väärtus väljale FI-kreeditor.
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Maksekviitungi vormingu seadistamine arvete, märkmete, kirjade ja väljavõtete jaoks.
1. Minge jaotisse Müügireskontro > Seadistus > Vormid > Vormi seadistus.
2. Klõpsake vahekaarti Arve.
3. Valige suvand väljal Seotud maksemanus kliendiarvel.
    * Puudub: maksekviitungit ei prindita. Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).   FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.   FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.  
4. Klõpsake nuppu Salvesta.
5. Klõpsake vahekaarti Vabas vormis arve.
6. Valige suvand väljal Seotud maksemanus vabas vormis arvel.
    * Puudub: maksekviitungit ei prindita. Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).   FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.   FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.  
7. Klõpsake nuppu Salvesta.
8. Klõpsake vahekaarti Viivisearve.
9. Valige suvand väljal Seotud maksemanus viivisearvel.
    * Puudub: maksekviitungit ei prindita. Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).   FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.   FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.  
10. Klõpsake nuppu Salvesta.
11. Klõpsake vahekaarti Märgukiri.
12. Valige suvand väljal Seotud maksemanus märgukirjal.
    * Puudub: maksekviitungit ei prindita. Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).   FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.   FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.  
13. Klõpsake nuppu Salvesta.
14. Klõpsake vahekaarti Kontoväljavõte.
15. Valige suvand väljal Seotud maksemanus kontoväljavõttel.
    * Puudub: maksekviitungit ei prindita. Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).   FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.   FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.  
16. Klõpsake nuppu Salvesta.
17. Sulgege leht.

