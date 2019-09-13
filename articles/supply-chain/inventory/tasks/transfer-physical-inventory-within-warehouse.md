---
title: Füüsiliste laovarude ülekandmine laos
description: See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7715c8e7a56703993e8512af03f2ab8d6802a987
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916572"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Füüsiliste laovarude ülekandmine laos

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise. Enne selle käivitamist peate seadistama varude üleviimiste jaoks varude töölehe nime. Saate läbida selle protseduuri demoettevõtte USMF andmete põhjal, kasutades kuvatavaid näidisväärtusi, või võite kasutada oma andmeid, kui teil on tooted ja asukohad seadistatud. Neid ülesandeid täidab üldjuhul laotöötaja.


## <a name="create-an-inventory-transfer-journal"></a>Lao üleviimistöölehe loomine
1. Avage **Navigeerimispaneelil** **Varuhaldus > Töölehe kanded > Kaubad > Edastus**.
2. Klõpsake valikut **Uus**.
3. Sisestage või valige väärtus väljal **Nimi**.
4. Klõpsake valikut **OK**. Määrata saab iga töölehe dimensioonid Alates ja Kuni. Need on selle töölehe tüübi puhul olulised. Saate viia kaupu asukohtadesse üle, kasutades mitmesuguseid reegleid. Selles näites viime kauba üle samas laos, litsentsiplaadiga kontrollitavast asukohast asukohta, mida litsentsiplaadiga ei kontrollita.   

## <a name="create-journal-lines"></a>Loo töölehe read
1. Klõpsake kaardil **Töölehe read fastTab** **Uus**.
2. Sisestage või valige väärtus väljale **Kauba kood**. Kui kasutate USMF-i, võite valida väärtuse A0001.  
3. Sisestage välja **Saidist** väärtus või valige see. Kui kasutate USMF-i, võite valida väärtuse 2.  
4. Sisestage välja **Saidile** väärtus või valige see. Kui kasutate USMF-i, võite valida väärtuse 2.  
5. Sisestage välja **Laost** väärtus või valige see. Kui kasutate USMF-i, võite valida väärtuse 24.  
6. Sisestage välja **Lattu** väärtus või valige see. Kui kasutate USMF-i, võite valida väärtuse 24.  
7. Sisestage välja **Asukohast** väärtus või valige see. Kui kasutate USMF-i, võite valida väärtuse FL-001.  
8. Sisestage välja **Asukohta** väärtus või valige see. Kui kasutate USMF-i, võite valida väärtuse BULK-001.  
9. Sisestage arv väljale **Kogus**.
10. Klõpsake kiirkaardil **Rea üksikasjad** vahekaarti **Varude dimensioonid**.
11. Sisestage **Varude dimensioonides** välja **Identifitseerimisnumber** väärtus või valige see. Kui kasutate USMF-i, võite valida väärtuse 24.  
12. Klõpsake valikut **Salvesta**.

## <a name="post-the-inventory-transfer-journal"></a>Lao üleviimistöölehe sisestamine
1. Paanil **Toimingupaan** klõpsake käsku **Sisesta**.
2. Klõpsake valikut **OK**.

## <a name="view-inventory-transactions"></a>Varude kannete kuvamine
1. Klõpsake **Varu**.
2. Klõpsake **Kanded**. Siin näete kandeid, mis loodi, kui oma töölehe sisestasite.  

