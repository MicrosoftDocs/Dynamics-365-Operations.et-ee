---
title: Hankija kannete loendi leht
description: See teema sisaldab teavet rakenduse Microsoft Dynamics 365 for Finance and Operations hankija kannete loendi lehe kohta.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: et-ee
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a>Hankija kannete loendi leht

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Kuva tasakaalustused

Vahekaart **Kuva tasakaalustused** toimingupaanil annab kiire juurdepääsu tasakaalustuste ajaloole ja lisateavet kogu tasakaalustuskande kohta. Saate ka kuvada lisakandeid, mis on seotud valitud kandega kas seetõttu, et need olid osa samast tasakaalustusest või kuna need on maksed, mis loodi samas makse töölehes.

1. Valige suvandid **Ostureskontro \> Kõik hankijad**.
2. Valige hankija, kellel on kanded, ja seejärel valige suvandid **Hankija \> Kanded**.
3. Valige uurimiseks kanne.
4. Valige toimingupaanilt vahekaart **Kuva tasakaalustused**.

    Avaneb dialoogiboks **Kuva tasakaalustused** ja kuvab valitud kande ning kõik dokumendid, mis on selle suhtes tasakaalustatud. See dialoogiboks meenutab tasakaalustuste ajaloo vaadet, aga sisaldab kõiki seotud dokumente.

5. Sellest dialoogiboksist saate teha mitmesuguseid toiminguid. Valige üks või mitu kannet ja seejärel valige üks järgmistest menüüdest:

   - **Kuva raamatupidamine** – kuvatakse kõik valitud dokumentidega seotud kanded. Valige dialoogiboksi sulgemiseks suvand **Sule**.
   - **Ekspordi** – ekspordi valitud kanded Microsoft Excelisse.
   - **Kuva seotud maksed** – kuvatakse kõik valitud dokumendiga seotud makse töölehes loodud töölehekanded. Peale selle kuvatakse kõik nende maksetega seotud tasakaalustused. Selle menüü silt muutub sildiks **Kuva tasakaalustused**. Valige suvand **Kuva tasakaalustused**, et kuvada ainult need kanded, mis kuvati dialoogiboksi **Kuva tasakaalustused** esimesel avamisel.
    - **Kannete tasakaalustamine** – see menüü ilmub, kui valitud algdokument ei olnud täielikult tasakaalustatud. Kui selle valite, ilmub dialoogiboks **Kannete tasakaalustamine**, kus saate valida tasakaalustamiseks kanded.
    - **Tasakaalustamise tühistamine** – see menüü ilmub, kui valitud algdokument oli täielikult tasakaalustatud. Kui selle valite, ilmub dialoogiboks **Tasakaalustamise tühistamine**, kus saate tühistada selle dokumendi tasakaalustamised.

