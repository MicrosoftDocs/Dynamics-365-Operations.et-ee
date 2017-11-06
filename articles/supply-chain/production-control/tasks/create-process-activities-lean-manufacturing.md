--- 
title: 'Protsessitegevuste loomine: lean manufacturing'
description: Protsessitegevuse loomine lean manufacturingi jaoks.
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dd77c20b622fd8a14e1cdf77883043699f9a6317
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-process-activities-for-lean-manufacturing"></a>Protsessitegevuste loomine: lean manufacturing

[!include[task guide banner](../../includes/task-guide-banner.md)]

Protsessitegevuse loomine lean manufacturingi jaoks. 

Eeltingimused: 

1. Tuleb luua tootmisvoog ja mitteaktiivne versioon.

2. Tuleb luua töörakk.


## <a name="find-the-production-flow-version"></a>Tootmisvoo versiooni leidmine
1. Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.

## <a name="create-a-new-activity"></a>Uue tegevuse loomine
1. Klõpsake suvandit Tegevused.
    * Veenduge, et valitud tootmisvool oleks mustandversioon, ja valige see versioon.  
2. Klõpsake suvandit Uue plaanitegevuse loomine.
3. Klõpsake käsku Edasi.
4. Sisestage väärtus väljale Nimi.
5. Sisestage väärtus väljale Nimi.
    * Pange tähele, et nimi peab kõnealuse tootmisvoo kõigi versioonide puhul olema kordumatu.  
6. Sisestage number väljale Protsessikogus.
    * Pange tähele, et olenemata töödeldavast töökogusest on see tööjõukulu arvutamiseks minimaalne kogus iga töö kohta. Kui töökogused sellest kogusest hälbivad, luuakse tööjõuhälve.  
7. Klõpsake käsku Edasi.

## <a name="select-the-work-cell"></a>Tööraku valimine
1. Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.
2. Klõpsake loendis valitud real olevat linki.

## <a name="define-the-inventory-updates"></a>Laovarude värskenduste määratlemine
1. Märkige või tühjendage ruut Värskenda laoseisu sissetulekut.
    * Kui suvandi Laoseisu värskendamine sätteks on valitud Ei, saate määratleda tegevuse vastu võtma pooltoodet (tegevus ei jõua järgmisele kooslusetasemele).    Saate valida ka pooltoodete tarbimise.  

## <a name="define-the-picking-activities"></a>Komplekteerimistegevuste määratlemine
1. Klõpsake käsku Edasi.
2. Märkige loendis valitud rida.
    * Valitud tööraku sisendasukoha kohta luuakse vaikekomplekteerimistegevus.  
3. Klõpsake vahekaarti Lisa.
    * Saate luua kindlate toodete puhul täiendavaid komplekteerimistegevusi, mis ei ole tööraku sisendtegevuses etapiviisilised.  
4. Otsige loendist ja valige soovitud kirje.
5. Sisestage väärtus väljale Kaubakood.
6. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
    * Selle määratlusega komplekteeritakse kõik tegevuses tarbitavad materjalid vaikesisendlaost ja -asukohast, v.a kaup, mis määratletakse teises komplekteerimistegevuses. See kaup komplekteeritakse teisest laost ja asukohast.  
7. Otsige loendist ja valige soovitud kirje.
8. Klõpsake loendis valitud real olevat linki.
9. Märkige või tühjendage ruut Registreeri praak.
10. Klõpsake käsku Edasi.

## <a name="define-the-activity-times"></a>Tegevusaegade määratlemine
1. Otsige loendist ja valige soovitud kirje.
    * Vajalik on Käitusaja määratlus. Käitusaega kasutatakse kanban-tööde maksumuse ja läbilaskeaegade arvutamiseks. Käitusaegu ei kasutata täiskoormuse ja tarbimise arvutamiseks; neid arvutatakse tsükliaja järgi, mis saadakse tootmisvoo versiooni ülesandest.  
2. Sisestage number väljale Kellaaeg.
3. Sisestage väärtus väljale Ühik.
4. Valige ajaühik.
5. Sisestage number väljale Koguse kohta.
6. Otsige loendist ja valige soovitud kirje.
    * Ooteajad on valikulised.  
7. Sisestage number väljale Kellaaeg.
8. Sisestage väärtus väljale Ühik.
9. Valige ajaühik.
10. Sisestage number väljale Koguse kohta.
11. Klõpsake käsku Edasi.
12. Klõpsake Lõpeta.
13. Sulgege leht.

