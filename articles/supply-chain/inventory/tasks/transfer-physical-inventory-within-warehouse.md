---
title: "Füüsiliste laovarude ülekandmine laos"
description: "See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedb209ab111ed1fb6281fda2f4dea345e0905ef
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Füüsiliste laovarude ülekandmine laos

[!include[task guide banner](../../includes/task-guide-banner.md)]

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
