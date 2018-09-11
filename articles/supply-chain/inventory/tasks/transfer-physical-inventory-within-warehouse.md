--- 
title: "Füüsiliste laovarude ülekandmine laos"
description: "See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise."
author: MarkusFogelberg
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bfba69731a4897906d08ff9fb9ce69e79121efeb
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Füüsiliste laovarude ülekandmine laos

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise. Enne selle käivitamist peate seadistama varude üleviimiste jaoks varude töölehe nime. Saate läbida selle protseduuri demoettevõtte USMF andmete põhjal, kasutades kuvatavaid näidisväärtusi, või võite kasutada oma andmeid, kui teil on tooted ja asukohad seadistatud. Neid ülesandeid täidab üldjuhul laotöötaja.


## <a name="create-an-inventory-transfer-journal"></a>Lao üleviimistöölehe loomine
1. Minge jaotisse Ülekanne.
2. Klõpsake valikut Uus.
3. Sisestage või valige väärtus väljal Nimi.
4. Klõpsake nuppu OK.
    * Määrata saab iga töölehe dimensioonid Alates ja Kuni. Need on selle töölehe tüübi puhul olulised. Saate viia kaupu asukohtadesse üle, kasutades mitmesuguseid reegleid. Selles näites viime kauba üle samas laos, litsentsiplaadiga kontrollitavast asukohast asukohta, mida litsentsiplaadiga ei kontrollita.   

## <a name="create-journal-lines"></a>Tööleheridade loomine
1. Klõpsake valikut Uus.
2. Sisestage või valige väärtus väljal Kaubakood.
    * Kui kasutate USMF-i, võite valida väärtuse A0001.  
3. Sisestage või valige väärtus väljal Lähtekoht.
    * Kui kasutate USMF-i, võite valida väärtuse 2.  
4. Sisestage või valige väärtus väljal Sihtkoht.
    * Kui kasutate USMF-i, võite valida väärtuse 2.  
5. Sisestage või valige väärtus väljal Laost.
    * Kui kasutate USMF-i, võite valida väärtuse 24.  
6. Sisestage või valige väärtus väljal Lattu.
    * Kui kasutate USMF-i, võite valida väärtuse 24.  
7. Sisestage või valige väärtus väljal Lähteasukoht.
    * Kui kasutate USMF-i, võite valida väärtuse FL-001.  
8. Sisestage või valige väärtus väljal Sihtasukoht.
    * Kui kasutate USMF-i, võite valida väärtuse BULK-001.  
9. Sisestage arv väljale Kogus.
10. Klõpsake vahekaarti Varude dimensioonid.
11. Valige või sisestage väärtus väljal Litsentsiplaat.
    * Kui kasutate USMF-i, võite valida väärtuse 24.  
12. Klõpsake nuppu Salvesta.

## <a name="post-the-inventory-transfer-journal"></a>Lao üleviimistöölehe sisestamine
1. Klõpsake valikut Sisesta.
2. Klõpsake nuppu OK.

## <a name="view-inventory-transactions"></a>Varude kannete kuvamine
1. Klõpsake Ladu.
2. Klõpsake suvandit Kanded.
    * Siin näete kandeid, mis loodi, kui oma töölehe sisestasite.  


