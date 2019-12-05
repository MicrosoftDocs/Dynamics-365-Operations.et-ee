---
title: Plaanitud tellimuste haldamine
description: See teema pakub teavet plaanitud tellimuste haldamise kohta. See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813772"
---
# <a name="maintain-planned-orders"></a>Plaanitud tellimuste haldamine

[!include [banner](../includes/banner.md)]

See teema pakub teavet plaanitud tellimuste haldamise kohta. See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel.

Saate planeeritud tellimusi hallata tööruumis **Koondplaneerimine**, loendis **Plaanitud tellimus** või loendites **Plaanitud tootmistellimused**, **Plaanitud ostutellimused** ja **Plaanitud üleviimised**. 

## <a name="planned-order-status"></a>Plaanitud tellimuse olek
Saate edenemist jälgida välja **Olek** abil. Kasutatakse järgmisi väärtusi.

-   Kui koondplaneerimine loob plaanitud tellimused, on nende olek **Töötlemata**.
-   Kui otsustate plaanitud tellimust mitte kinnitada, saate sellele määrata oleku **Lõpule viidud**.
-   Kui soovite kinnitada plaanitud tellimuse, saate määrata selle olekuks **Kinnitatud**. Olekuga **Kinnitatud** plaanitud tellimusi arvestatakse koondplaneerimisel, nii et neid ei muudeta ega kustutata hilisema koondplaneerimise käivitamise ajal. 

## <a name="firming-planned-orders"></a>Plaanitud tellimuste kinnitamine 
Plaanitud tellimuste kinnitamisega luuakse tegelikud tellimused. Neid nimetatakse ka *väljastatud* või *avatud tellimusteks*. Kui plaanitud tellimus on kinnitatud, teisaldatakse see asjakohase mooduli tellimuste jaotisse.

Lehel **Plaanitud tellimused** saate valida kaks kinnitamissuvandit.

-   **Kinnita** – sellega kinnitatakse üks või mitu valitud plaanitud tellimust.
-   **Kinnita kõik** – sellega kinnitatakse kõik filtris olevad plaanitud tellimused. Valides suvandi **Kinnita kõik** ei pea te valima plaanitud tellimust, kõiki filtris olevad plaanitud tellimused kinnitatakse. See suvand võib olla kasulik juhul, kui kinnitate suure hulga plaanitud tellimusi.

> [!NOTE]
> **Kinnitamise ajaloo** jaotises **Plaanitud tellimuste vorm > Vaade > Kinnitamise ajalugu** saate jälgida kinnitatud plaanitud tellimust.

## <a name="parallelize-firming"></a>Paralleelne kinnitamine
Kui plaanite kinnitada korraga mitu tellimust, võib käituse paralleelimine parandada käitusaega või jõudlust. See valik on saadaval mitme plaanitud tellimuse kinnitamisel kas suvandiga **Kinnita** või **Kinnita kõik**. Saadaval on järgmised parameetrid.

-   **Kinnitamise paralleelimine** – kui **Jah**, siis paralleelitakse kinnitamisprotsessi lõimede arvuga, mis on määratletud väärtusega **Lõimede arv**.
-   **Lõimede arv** – reguleerib kinnitamise paralleelimiseks kasutatavate lõimede arvu. Parameeter kuvatakse ainult siis, kui valiku **Kinnitamise paralleelimine** väärtuseks on seatud **Jah**.


<a name="additional-resources"></a>Lisaressursid
--------

[Koondplaanide ülevaade](master-plans.md)



