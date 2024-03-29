---
title: Säästlik sidumine müügitellimuste põhjal
description: Protseduur keskendub müügirea sidumispuu kinnitamisele, kui kaup on toodetud kanbanidega.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8eca21f8bd988ca352c07e839295b3edd9669929
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580620"
---
# <a name="lean-pegging-from-sales-orders"></a>Säästlik sidumine müügitellimuste põhjal

[!include [banner](../../includes/banner.md)]

Protseduur keskendub müügirea sidumispuu kinnitamisele, kui kaup on toodetud kanbanidega. Pärast sidumispuu kinnitamist on kõik kanban-tööd plaanitud. See on kasulik tellimuste puhul, kus tellimuse vastuvõtja peab tagama, et tootmine saaks kohe alata. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Protseduur on mõeldud spetsialiseerunud tellimuste vastuvõtjale, kes töötab säästlikus ettevõttes.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Kanbani juhitud kauba jaoks müügitellimuse loomine
1. Avage Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
    * Kasutage US-001.  
4. Klõpsake nuppu OK.
5. Sisestage väljale Kaubakood tüüp L0001.
6. Määrake koguse väärtuseks 30.
    * Sündmuse kanban-reegli käivitamiseks peab kogus kindlasti olema suurem kui 24.  

## <a name="open-a-pegging-tree"></a>Sidumispuu avamine 
1. Klõpsake valikut Toode ja tarnimine.
2. Klõpsake suvandit Kuva sidumispuu.
    * Pange tähele, et sidumispuus on kuvatud kõik müügitellimuse rea jaoks vajalikud sidumistasemed. Selles näites on kaks kanbanide taset ja kõik nõutavad komponendid.  

## <a name="plan-the-pegging-tree"></a>Sidumispuu plaanimine
1. Valige puus „Sales line 000832\Kanban 000558”.
2. Laiendage jaotist Kanban-tööd.
    * Pange tähele, et kanban-töö olek on Plaanimata.  
3. Klõpsake käsku Plaani kogu sidumispuu.
    * See plaanib kõik sidumispuus olevad kanban-tööd, asendades töö oleku Plaanimata olekuga Plaanitud.  
4. Värskendage lehte.
    * Pange tähele, et kanban-töö olek Plaanimata asendati olekuga Plaanitud.  
5. Valige puus suvand „Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559”.
    * Teise kanbani töö on samuti plaanitud, kuna kogu sidumispuu on plaanitud. Pange tähele, et kanban-töö olek Plaanimata asendatakse olekuga Plaanitud.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]