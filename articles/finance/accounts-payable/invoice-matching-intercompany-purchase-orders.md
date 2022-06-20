---
title: Arvete võrdlemine ja kontsernisisesed ostutellimused
description: Kontsernisisese kaubanduse kandega seotud juriidilise isiku ostu saab seadistada kasutama ostureskontro arvete võrdlemist. Sel juhul peavad nii kontsernisisese kaubanduse kui ka ostureskontro arvete võrdlemise sisestamisnõuded olema täidetud, enne kui saab sisestada kontsernisisesed hankijate arved.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4be32a7158561bdf00a996831dca7395ce6f331
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879736"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Arvete võrdlemine ja kontsernisisesed ostutellimused

[!include [banner](../includes/banner.md)]

Kontsernisisese kaubanduse kandega seotud juriidilise isiku ostu saab seadistada kasutama ostureskontro arvete võrdlemist. Kui ostureskontro **parameetrite lehel** on **seadistatud** **väli** Sisesta arve lahknevustega, tehakse arvete vastendamise kinnitamine. Sel juhul peavad nii kontsernisisese kaubanduse kui ka ostureskontro arvete võrdlemise sisestamisnõuded olema täidetud, enne kui saab sisestada kontsernisisesed hankijate arved.

Selle artikli näidetes kasutatakse kontserni kaubavahetuse jaoks järgmist seadistust:
-   Fabrikam Purchase on ostja juriidiline isik.
-   Fabrikam Sales on müüja juriidiline isik.
-   Klient 4020 eksisteerib valikus Fabrikam Müük.
-   Hankija 3024 eksisteerib valikus Fabrikam Ost.
-   Ettevõttes Fabrikam Purchase on kontsernisisene teave määratud müüja 3024 kohta. Fabrikam Sales on määratletud klientettevõttena ja klient 4020 on määratletud kliendikontona, mis vastab juriidilisele isikule Fabrikam Purchase.
-   Ettevõttes Fabrikam Sales on kontsernisisene teave määratud kliendi 4020 kohta. Fabrikam Purchase on määratletud hankijaettevõttena ja hankija 3024 on määratletud hankijakontona, mis vastab juriidilisele isikule Fabrikam Sales.

Nendes näidetes kasutatakse järgmist ostureskontrote arvete vastendamise seadistust valiku Fabrikam Purchase puhul.
-   Ostureskontro **parameetrite lehel** on valitud **suvand Luba arvete vastendamise** kontrollimine.
-   Ostureskontro **parameetrite lehel** on välja **Lahknevustega arvete sisestamine** väärtuseks seatud Nõua **kinnitust**.
-   Hinnakõikumise protsent on selle juriidilise isiku puhul 2 protsenti.

## <a name="example-price-matching-and-intercompany-trade"></a> Näide: hindade vastendamine ja kontsernisisene kaubandus
Kontsernisisese hankija arve ja kontsernisisese kliendiarve netosummad peavad olema võrdsed. See nõue alistab kõik kohaldatavad arvete vastendamise kinnitused või hinnakõikumisprotsendid. Näiteks võite teha järgmist.
1.  Looge üksusele Fabrikam Purchase müügitellimus SO888 kliendile 4020. Kontsernisisene ostutellimus ICPO222 luuakse automaatselt üksuses Fabrikam Purchase hankijale 3024 ja müügitellimus ICSO888 luuakse automaatselt üksuses Fabrikam Sales.
2.  Registreerige jaotises Fabrikam Sales kaupade kättesaamine ja sisestage saateleht. Olek ICSO888 muutub olekuks Tarnitud. Olek ICPO222 muutub olekuks Vastu võetud.
3.  Fabrikam Müügis uuendage ICSO888 arvet. Ühiku hind on 0,45 ja uuendatakse 100 üksust.
4.  Koostage jaotises Fabrikam Purchase arve üksusele ICPO222. Määrate netohinnaks kogemata 45.00 asemel 54.00. Kuvatakse ikoon, mis näitab lubatava hinnahälbe – kahe protsendi – ületamist.
5.  Arvete vastendamise **üksikasjade lehel** valige suvand, et kinnitada sisestamine sobivate lahknevustega. Klõpsake hankija **arve lehel** OK **·**. Sisestamine õnnestuks, kui hankija arve poleks kontsernisisene hankija arve. Kuid kuna töötate kontsernisisese hankija arvega, ei õnnestu sisestamine. Kontsernisisese kaubavahetuse puhul peavad kontsernisisese müügitellimuse kogusummad võrduma vastava kontsernisisese ostutellimuse arve kogusummadega. Selle probleemi lahendamiseks peate parandama arve netohinda, muutes netohinna uuesti vaikesummaks 45.00.

## <a name="example-quantity-matching-with-intercompany-trade"></a> Näide: koguste vastendamine kontsernisisese kaubanduse puhul
Kontsernisisene ostutellimuse ja kontsernisisene müügitellimuse kogused peavad olema võrdsed. See nõue alistab kõik kohaldatavad arvete vastendamise kinnitused. See näide kasutab järgmist täiendavat kontsernisisese kaubavahetuse seadistust.
-   Üksusel Fabrikam Purchase on hankija 3024 ostutellimuse tegevuspoliitika seadistatud sisestama automaatselt nii algset kliendiarvet kui ka kontsernisisest hankija arvet.

Selles näites kasutatakse järgmist ostureskontrote arvete vastendamise lisaseadistust valiku Fabrikam Purchase puhul.
-   **Kauba** B-R14 kasutatava mudeligrupi kauba mudeligruppide lehel on valitud **suvand Vastuvõtunõuded**.
-   Vaba kaubavaru kogus kauba B-R14 puhul on 0 (null).

Näiteks võite teha järgmist.
1.  Koostage üksusele Fabrikam Purchase müügitellimus SO999 kliendile 4020. Tellimus sisaldab ühte reaüksust: 100 patareid (kaup B-R14) ühiku hinnaga 1.00. Kontsernisisene ostutellimus ICPO333 luuakse automaatselt üksuses Fabrikam Purchase hankijale 3024 ja müügitellimus ICSO999 luuakse automaatselt üksuses Fabrikam Sales.
2.  Tehke jaotises Fabrikam Sales arveuuendus ICSO999. Sisestamine nurjub, sest kaup on laost otsas ning seda pole veel vastu võetud. Seetõttu ei saa finantsandmeid uuendada.
3.  Registreerige kaupade kättesaamine ja sisestage ICSO999 saateleht üksusele Fabrikam Sales. ICPO333 toote sissetulek sisestatakse automaatselt üksusele Fabrikam Purchase. Vastuvõetud kauba B-R14 kogus on üksusel Fabrikam Purchase nüüd 100.
4.  Tehke jaotises Fabrikam Sales arveuuendus ICSO999. Sisestamine on mõlema juriidilise isiku puhul edukas. Üksusel Fabrikam Purchase muutub kauba B-R14 ostetud kogus väärtuseks 100. 







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
