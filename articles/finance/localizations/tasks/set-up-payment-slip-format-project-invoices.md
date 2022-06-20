---
title: Maksekviitungi vormingu häälestus projektiarvete jaoks
description: See artikkel selgitab, kuidas lisada projekti arvetele prinditud maksekviitungeid ja pakkuda sisestamiseks ja tasakaalustamiseks makseviiteid.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f9e956f6c6a5d7a783bfc3a475ff4ca60473f17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879434"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Maksekviitungi vormingu seadistamine projektiarvete jaoks

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
