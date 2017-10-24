---
title: "Vastavuse loomine ja töötlemine"
description: "Kasutage seda protseduuri mittevastavuse haldamiseks olemasoleva kvaliteettellimuse põhjal."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-process-a-conformance"></a>Vastavuse loomine ja töötlemine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kasutage seda protseduuri mittevastavuse haldamiseks olemasoleva kvaliteettellimuse põhjal. Saate käivitada selle salvestise demoettevõttes USMF ja kasutada soovitatud väärtusi. Tavaliselt teostab selle protseduuri kvaliteediametnik.  Eeltingimusena käivitage ülesandesalvestis „Kaupade kvaliteedi kontrollimine”. Mittevastavuse kinnitamise töötlemiseks peab ülesandesalvestist käitavale kasutajale olema lehel Kasutajad määratud väärtus Nimi. Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.


## <a name="select-a-quality-order"></a>Kvaliteettellimuse valimine
1. Minge jaotisse Kvaliteettellimused.
2. Märkige loendis valitud rida.
    * Valige kvaliteettellimus, mis loodi ülesandesalvestises „Kaupade kvaliteedi kontrollimine”.  

## <a name="create-a-nonconformance"></a>Mittevastavuse loomine
1. Klõpsake suvandit Päringud.
2. Klõpsake suvandit Mittevastavused.
3. Klõpsake valikut Uus.
4. Klõpsake väljal Probleemi tüüp otsingu avamiseks ripploendi nuppu.
    * Valige kontrolliprotsessi käigus leitud probleem.  
5. Klõpsake väljal Probleemi tüüp otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake nuppu OK.

## <a name="approvereject-a-nonconformance"></a>Mittevastavuse kinnitamine/tagasilükkamine
1. Klõpsake suvandit Funktsioonid.
2. Klõpsake suvandit Kinnita mittevastavus.
    * Selles näites kinnitage mittevastavus. Kinnitatud mittevastavused saab seostada töö salvestamisega seotud toimingutega, mida tehakse osana mittevastavuse töötlemisest, ja (nagu selles ülesandesalvestises) paranduse käsitlemise töötlemisega.  
3. Klõpsake nuppu Jah.

## <a name="create-a-correction-action"></a>Parandustegevuse loomine
1. Klõpsake suvandit Parandused.
2. Klõpsake valikut Uus.
3. Märkige loendis valitud rida.
4. Klõpsake väljal Personalinumber otsingu avamiseks ripploendi nuppu.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake Vali.
7. Klõpsake suvandit Manusta.
    * Looge paranduse kohta märkus. Selles näites on tegevuseks hankijaga ühenduse võtmine, et arutleda mittevastavuse juhtumit.  
8. Klõpsake valikut Uus.
9. Klõpsake suvandit Märkus.
    * Pange tähele, et olenevalt aruande seadistusest saab mittevastavuse haldusega seotud aruannetele printida erinevat tüüpi dokumente.  
10. Sisestage väljale Kirjeldus soovitud väärtus.
11. Sulgege leht.

## <a name="maintain-a-correction"></a>Paranduse haldamine
1. Klõpsake suvandit Märgi lõpuleviiduks.
2. Klõpsake nuppu OK.
3. Sulgege leht.

## <a name="close-a-nonconformance"></a>Mittevastavuse sulgemine
1. Klõpsake suvandit Funktsioonid.
2. Klõpsake suvandit Sule mittevastavus.
3. Klõpsake nuppu Jah.
4. Sulgege leht.
5. Sulgege leht.

