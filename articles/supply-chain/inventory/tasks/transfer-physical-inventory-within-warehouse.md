---
title: Füüsiliste laovarude ülekandmine laos
description: See protseduur juhatab teid läbi lao üleviimistöölehe loomise ja sisestamise protsessi, et registreerida kauba liikumine ühest lao asukohast teise.
author: yufeihuang
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf5a3711cfcd6e5a2ddce09af8569ea26c3502c8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580788"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Füüsiliste laovarude ülekandmine laos

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]