---
title: Ostureskontro konfigureerimise ülevaade
description: Selles artiklis kirjeldatakse lehti, mida kasutatakse i mooduli Ostureskontro põhi- ja valikuliste funktsioonide seadistamiseks. Kirjeldatakse ka seadistamistoiminguid, mis tuleb teha enne mooduli Ostureskontro seadistamist.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bce5da0c9593bcfcfb9589f8fe7e09b8acd63726
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906528"
---
# <a name="configure-accounts-payable-overview"></a>Ostureskontro konfigureerimise ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse lehti, mida kasutatakse i mooduli Ostureskontro põhi- ja valikuliste funktsioonide seadistamiseks. Kirjeldatakse ka seadistamistoiminguid, mis tuleb teha enne mooduli Ostureskontro seadistamist.

## <a name="prerequisites-for-accounts-payable-setup"></a>Ostureskontro seadistamise eeltingimused

Enne ostureskontro seadistamist tuleb teha järgmine seadistus.

-   Pearaamatus:
    -   Kui kavatsete kasutada maksetöölehti, seadistage maksetöölehed.
    -   Kui plaanite käitada vahetuskursi korrekt korrigeerimisi, **seadistage valuutakoodid lehel Valuutad,** seadistage vahetuskursi tüübid lehel Vahetuskursi tüübid **ja** seadistage valuuta vahetuskursid lehel Valuuta vahetuskursid **.**
-   Seadistage moodulis Sularaha- ja pangahaldus makseviiside korral kasutatavad pangakontod.

## <a name="setup-pages-for-accounts-payable"></a>Ostureskontro seadistuslehed

Kasutage järgmisi lehti iga juriidilise isiku jaoks ostureskontro põhifunktsioonide seadistamiseks. Lehed on loetletud soovitatavas seadistamise järjekorras. Seadistamisprotsessi hõlbustamiseks saate luua malle esimeste loodud kirjete põhjal. Mallis sisestatakse tavaliselt paljudele väljadele väärtused, mis kajastavad funktsioone, mida organisatsioon soovib teatud tüüpi hankija korral kasutada.
1.  **Määratlege maksetingimused** lehel müügitellimustele, ostutellimustele, klientidele ja hankijatele määratavad maksetingimused, millega määratletakse arve tähtajad. Lisateavet vt [Hankija käitluslõivude määratlemine](tasks/define-vendor-payment-fees.md).
2.  Looge ja **säilitage lehel Makseviisid –** hankijad teave selle kohta, kuidas organisatsioon hankijatele maksab.
3.  Looge ja **säilitage** hankijagruppide lehel hankijagrupid, kellel on jagada olulisi parameetreid sisestamiseks, tasakaalustamiseks ja maksmiseks, aruandluseks ja prognoosimiseks.
4.  Määratlege **lehel Hankija** sisestusreeglid, kuidas hankijakanded pearaamatusse sisestatakse.
5.  Seadistage **ostureskontro** parameetrite lehel vaikesätted, mis rakendatakse juhul, kui täpsemat sätet ei ole määratud, erinevate funktsioonide parameetrid ja erinevad ostureskontro numbriseeriad.
6.  Määratlege **vormi** seadistamise lehel hankijatega seotud mitmesuguste dokumentide vorming, mida organisatsioon kasutab hankijate laekumiste jälgimiseks ja hankijatele maksete põhjuste sisestamiseks.
7.  Looge ja **säilitage** lehel Hankijad ning maksuametid, mille kohta teie organisatsioon esitab käibemaksuaruandeid.

## <a name="optional-setup-pages-for-accounts-payable"></a>Ostureskontro valikulised seadistuslehed
Lisaks põhifunktsioonidele on moodulil Ostureskontro muid funktsioone, mida saab seadistada.

Täiendavad seadistuslehed on organiseeritud funktsioonide järgi.

**Poliitikad**
-   Häälestage **hankija arve** poliitika lehel hankija arve poliitikad.

**Arvete võrdlemine**

-   Lehel Arve **kogusummade kõikumised** seadistage arve kogusummade kõikumised.
-   Vastavusse viimise **poliitika** lehel seadistage kahe- ja kolmepoolese vastavusse viimise poliitikad.
-   Hinnakõikumiste **lehel** seadistage ühiku hindade kõikumised.
-   Kauba hinnakõikumisgruppide **lehel seadistage** kauba hindade kõikumise grupid.
-   Seadistage **hankija hinna kõikumise** gruppide lehel hankija hindade kõikumise grupid.
-   **Lehel Tasude kõikumised** seadistage kõikumised tasude jaoks.

**Töövoog**

-   Seadistage **ostureskontro** töövoogude lehel töölehe kinnituste ja ostutaotluste töövoo konfiguratsioonid.

**Põhjused**

-   Seadistage **põhjusekoodid** lehel Hankija põhjused.

**Tasud**

-   Seadistage **tasukoodi** lehel ostutellimustel kasutatavate kulude koodid.
-   Looge ja **säilitage hankijate** tasugrupid hankija kulude grupi lehel.
-   Looge ja **säilitage kaupade** kulugrupid lehel Kaubakulugrupid.
-   Määratlege **automaatsete** kulude lehel kulud, mis määratakse tellimustele automaatselt.

**Lisakaubad**

-   Looge ja **säilitage lisakaubagrupid** hankijate jaoks leheküljel Lisakaubagrupid - Hankija.
-   Looge ja **säilitage lisakaubagrupid** leheküljel Lisakaubagrupid - Varud.

**Jaotus**

-   **Looge ja säilitage** tarnetingimuste lehel tingimused kauba üleandmiseks müüjalt ostjale.
-   **Looge ja säilitage** lehel Tarneviisid transpordiviise, mida kasutatakse tellimuse tarnimisel müüjalt ostjale.
-   Sihtkoodide **lehel** looge ja säilitage tarnesihtkohtade ID-d ja kirjeldused.

**Vormid**

-   Looge vormi **märkuste** lehel standardtekst, mis kuvatakse erinevatel lehekülgedel.
-   Seadistage **vormil sortimisparameetrite** lehel ostutellimuste, saabunud kaupade loendite, saatelehtede ja arvete sortimisjärjestus.
-   Seadistage **prindihalduse seadistuslehel** prindihalduse teave lehtede originaalide ja koopiate kohta.

**Maksed**

-   Lehel Skontod **seadistage** ja hallake skonto saamise tingimusi. Skonto koodid on seotud hankijatega ja neid rakendatakse ostutellimuste korral.
-   Seadistage **maksegraafikute** lehel maksegraafikud, mida kasutatakse hankijatele tehtavate osamaksete haldamiseks.
-   Määratlege **maksepäevade** lehel maksepäevad, mida kasutatakse tähtaja arvutamiseks ja määrake maksepäevad kindlale nädala- või kuupäevale.
-   Looge ja **säilitage** maksetasu lehel hankijatega seotud maksetasud.
-   Looge ja **säilitage** maksejuhiste lehel Maksejuhis.

**Statistika**

-   Aegumisperioodi **definitsioonide lehel seadistage** kasutaja määratletud intervallid, mida kasutatakse hankijakontode tähtajaliste distributsioonide analüüsimiseks.
-   **Looge ettevõtterea lehel** hankijatele määratud äriüksuse (LOB) koodid.

**Maks 1099**

-   Lehel **1099 väljad** saate kontrollida ja muuta miinimumsummasid, millest tuleb USA Maksuametile (IRS-ile) viimaste IRS-i nõuete alusel aru anda.

## <a name="optional-setup-for-other-modules"></a>**Valikuline seadistus teiste moodulite puhul**
**Organisatsiooni haldus**

-   Seadistage **numbriseeria grupid** arvenumbrite jaoks lehel Numbriseeriad.
-   Saate seadistada järgmistel lehtedel aadressiteabe.
    -   **Aadressi häälestamine**
    -   **NAF-koodid**
    -   **Impordi sihtnumbrid**

**Pearaamat**

-   Seadistage **finantsdimensioonid** lehel Finantsdimensioonid.
-   Järgmistel lehtedel saate seadistada maksuteavet.
    -   **Käibemaksukoodid**
    -   **Käibemaksugrupid**
    -   **Kauba käibemaksugrupid**
    -   **Kontogrupp**
    -   **Käibemaksuvabastuse koodid**
    -   **Käibemaksu jurisdiktsioonid**
    -   **Käibemaksuhaldurid**
    -   **Käibemaksu tasakaalustusperioodid**

**Sularaha- ja pangahaldus**

-   Seadistage **makse eesmärgi** koodide lehel keskpanga **eesmärgikood**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
