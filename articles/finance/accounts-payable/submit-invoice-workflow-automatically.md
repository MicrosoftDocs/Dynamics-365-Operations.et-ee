---
title: Arvete esitamine töövoosüsteemi ja toote sissetulekuridade vastendamine
description: Selles teemas kirjeldatakse, kuidas hankija arveid töövoosüsteemile edastada ja sisestatud toote sissetuleku ridasid automaatselt hankija arvetega vastavusse viia.
author: abruer
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 84699746349024854a4eeb9cee62960ec38bc338
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827814"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Arvete esitamine töövoosüsteemi ja toote sissetulekuridade vastendamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas hankija arveid töövoosüsteemile edastada ja sisestatud toote sissetuleku ridasid automaatselt hankija arvetega vastavusse viia.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Imporditud hankija arvete edastamine töövoosüsteemile ja sisestatud toote sissetuleku ridade vastavusse viimine ootel hankija arve ridadega

Täiesti automaatse ostureskontro arveldusprotsessi osana saate lasta süsteemil automaatselt edastada imporditud arveid töövoosüsteemi. Saate konfigureerida imporditud arvete edastamise töövoosüsteemile vahekaardil **Hankija arve automatiseerimine**, mis asub lehel **Ostureskontro parameetrid** (**Ostureskontro \> Seadistus \> Ostureskontro parameetrid**). Töövoole edastamise protsess käivitub taustal sagedusel, mille määrate teie (kas iga tund või iga päev).

Kui edastate arveid töövoosüsteemile automaatselt, peate alustama imporditud arvega. Tagamaks, et arvet saaks töödelda algusest lõpuni automaatselt, peate töövookonfiguratsiooni kaasama automatiseeritud sisestamisülesande. Töövoosüsteemile saab automaatselt edastada ostutellimustega seotud arveid ning arveid, mis sisaldavad ostutellimusega mitteseotud hankekategooriat ja mitteladustatavaid ridasid. Käsitsi sisestatud arved tuleb töövoosüsteemile käsitsi edastada.

Töövoos olev väärtus **Edastaja** on kasutaja ID, mis sisestati taustaülesande **Hankija arvete edastamine töövoole** jaoks lehel **Protsessi automatiseerimine**. Kasutaja, kellel on see kasutaja ID, saab vajaduse korral arve töövoosüsteemist tagasi kutsuda.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Toote sissetulekute vastavusseviimine arve ridadega, millel on kolmesuunaline vastavusse viimise poliitika

Täiesti automaatse ostureskontro arveldusprotsessi osana saab süsteem sisestatud toote sissetulekuid automaatselt arve ridadega vastavusse viia. Selle ülesande jaoks tuleb määratleda kolmesuunaline vastavusse viimise poliitika. See funktsioon on saadaval, kui funktsioon **Hankija arve automatiseerimine** on lehel **Funktsioonihaldus** lubatud.

Vastendusprotsess töötab seni, kuni vastavusse viidud toote sissetuleku kogus võrdub arve kogusega. Kui aga ühel arvereal on mitu toote sissetulekut, peate täieliku koguse vastenduse saavutamiseks protsessi mitu korda käitama. Saate määrata, mitu korda peaks süsteem maksimaalset üritama viia toote sissetulekuid vastavusse arve ridadega, enne kui jõuab järeldusele, et protsess nurjus. Protsess töötab taustal, kas iga tund või iga päev. 

Saate käivitada automatiseeritud vastavusseviimise protsessi osana arvete edastamise protsessist töövoosüsteemi. Teise võimalusena saate selle käivitada eraldiseisva protsessina. Sätted toote sissetulekute vastavusseviimiseks arve ridadega konfigureeritakse vahekaardil **Hankija arve automatiseerimine**, mis asub lehel **Ostureskontro parameetrid** (**Ostureskontro \> Seadistus \> Ostureskontro parameetrid**).

Arve read, millel on kolmesuunaline vastavusse viimise poliitika, kus vastavusse viidava sissetuleku kogus on väiksem arve kogusest, kaasatakse automaatsesse toote sissetulekuga vastavusse viimise protsessi.

Et näha olekut **Viimane vastavusseviimine** arvete puhul, mis ei ole automatiseeritud töövoosüsteemile edastamise protsessi osa, avage arve lehel **Hankija arved**. Arve vaatamisel värskendatakse vastavusseviimise kontrollimise teavet. Olekut **Viimane vastendus** saab värskendada automaatselt, kasutades taustaülesannet **Arvete võrdlemise kinnitamine**. Saate automaatset oleku **Viimane vastendus** värskendamise protsessi konfigureerida vahekaardil **Taustaprotsessid** lehel **Protsessi automatiseerimised** (**Süsteemihaldus\> Seadistamine\> Protsessi automatiseerimised**).

Arve rida eemaldatakse automatiseeritud töötlusest, kui kehtib mõni järgmistest tingimustest.

- Arve rea väärtus **Automatiseeritud sissetuleku vastavusseviimise olek** on **Nurjunud**.
- Arvet kasutatakse.
- Arve on töövoosüsteemis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
