---
title: Tühistatud sisestustööleht
description: See teema kirjeldab võimeid, mis võimaldavad kandeid kannete loendist või finantslehtedelt tagasi võtta.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248581"
---
# <a name="reverse-journal-posting"></a>Tühistatud sisestustööleht

[!include [banner](../includes/banner.md)]

See teema kirjeldab võimeid Microsoft Dynamics 365 Finance, mis lubab teil kogu töölehe tagasi võtta või ühe või mitu kannet kannete loendist tagasi võtta, sõltumata nende päritolust. 

## <a name="reversing-journals"></a>Töölehtede tühistamine

Töölehe ridu saate ükshaaval muuta. Tühistatud töölehe sisestamisega saate ka kogu Finantstöölehe tagasi võtta. Töölehe tühistamine: 
- Finantstöölehe ja sisestatud töölehtede filtri avamine
- Klõpsake vormi ülaosas olevas menüüs nuppu Tühista.
- Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat
- Valige Jah, et kasutada olemasolevaid kande kuupäevi või Ei, et sisestada uus. Mõnel juhul võib algse kande perioodi sulgeda ja soovite sisestada uue kande kuupäeva tühistamisele.
- Kui valisite Ei, sisestage tühistamise kande kuupäev. 
- Sisestage kommentaar, mida soovite tühistamise kandele lisada.
- Klõpsake nuppu Tühista.

Kanded tühistatakse. 

Kui kanderidade arv ületab 100 rida, käivitatakse tühistamise protsess pakktöötluse abil. Tühistamise tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös, mis käivitati. Kõik tõrked märgitakse pakett-töö ajaloos.

Kui vutšeri ridade arv on 100 või vähem, käivitub tühistamise protsess kohe. Tulemused esitatakse dialoogis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, ja põhjus, miks seda ei saanud tühistada. Klõpsake OK, et dialoogiboksi sulgeda.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Kande tühistamine kannete loendist. 

Samuti saate kandeid **kannete loendist** tagasi võtta kõigis pearaamatutes. Lisaks saate ümber nimetada rohkem kui ühe kande korraga. 

Ühe või mitme kande tühistamine: 
- Klõpsake vormi ülaosas olevas menüüs nuppu Tühista.
- Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat
- Valige Jah, et kasutada olemasolevaid kande kuupäevi või Ei, et sisestada uus. Mõnel juhul võib algse kande perioodi sulgeda ja soovite sisestada uue kande kuupäeva tühistamisele.
- Kui valisite Ei, sisestage tühistamise kande kuupäev. 
- Sisestage kommentaar, mida soovite tühistamise kandele lisada.
- Klõpsake nuppu Tühista.

Kanded tühistatakse. 

Kui kanderidade arv ületab 100 rida, käivitatakse tühistamise protsess pakktöötluse abil. Tühistamise tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös, mis käivitati. Kõik tõrked märgitakse pakett-töö ajaloos.

Kui vutšeri ridade arv on 100 või vähem, käivitub tühistamise protsess kohe. Tulemused esitatakse dialoogis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, ja põhjus, miks seda ei saanud tühistada. Klõpsake OK, et dialoogiboksi sulgeda.

