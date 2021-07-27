---
title: Ostureskontro konfigureerimise ülevaade
description: Selles artiklis kirjeldatakse lehti, mida kasutatakse i mooduli Ostureskontro põhi- ja valikuliste funktsioonide seadistamiseks. Kirjeldatakse ka seadistamistoiminguid, mis tuleb teha enne mooduli Ostureskontro seadistamist.
author: abruer
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d42b3aa5b692a300a4a2cb3eb64c9a014aa52f9e
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339080"
---
# <a name="configure-accounts-payable-overview"></a>Ostureskontro konfigureerimise ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse lehti, mida kasutatakse i mooduli Ostureskontro põhi- ja valikuliste funktsioonide seadistamiseks. Kirjeldatakse ka seadistamistoiminguid, mis tuleb teha enne mooduli Ostureskontro seadistamist.

## <a name="prerequisites-for-accounts-payable-setup"></a>Ostureskontro seadistamise eeltingimused

Enne ostureskontro seadistamist tuleb teha järgmine seadistus.

-   Pearaamatus.
    -   Kui kavatsete kasutada maksetöölehti, seadistage maksetöölehed.
    -   Kui te kavatsete käivitada vahetuskursi korrektsioone, seadistage valuutakoodid lehel Valuutad, seadistage vahetuskursi tüübid lehel Vahetuskursi tüübid ja valuutavahetuskursid lehel Valuutavahetuskursid.
-   Seadistage moodulis Sularaha- ja pangahaldus makseviiside korral kasutatavad pangakontod.

## <a name="setup-pages-for-accounts-payable"></a>Ostureskontro seadistuslehed

Kasutage järgmisi lehti iga juriidilise isiku jaoks ostureskontro põhifunktsioonide seadistamiseks. Lehed on loetletud soovitatavas seadistamise järjekorras. Seadistamisprotsessi hõlbustamiseks saate luua malle esimeste loodud kirjete põhjal. Mallis sisestatakse tavaliselt paljudele väljadele väärtused, mis kajastavad funktsioone, mida organisatsioon soovib teatud tüüpi hankija korral kasutada.
1.  Lehel Maksetingimused saate määratleda müügitellimustele, ostutellimustele, klientidele ja hankijatele määratud maksetingimused, mis määravad kindlaks arve tähtajad. Lisateavet vt [Hankija käitluslõivude määratlemine](tasks/define-vendor-payment-fees.md).
2.  Lehel Makseviisid – hankijad saate luua ja hallata andmeid selle kohta, kuidas organisatsioon oma hankijatele maksab.
3.  Lehel Hankijagrupid saate luua ja hallata hankijagruppe, millel on olulised ühised parameetrid sisestamise, tasakaalustuse ja maksmise, aruandluse ja prognoosimise jaoks.
4.  Lehel Hankija sisestusreeglid saate määratleda, kuidas hankijakanded pearaamatusse sisestatakse.
5.  Lehel Ostureskontro parameetrid saate seadistada vaikesätted, mida rakendada, kui täpsemat sätet ei ole määratletud, erinevate funktsioonide parameetrid ja erinevad ostureskontro numbriseeriad.
6.  Lehel Vormi seadistus saate määratleda erinevate dokumentide vormingu, mis on seotud hankijaga ja mida organisatsioon kasutab, et jälgida hankijatelt saadud sissetulekuid ja sisestada hankijate maksevoo põhjusi.
7.  Lehel Hankijad saate luua ja hallata hankijakontosid ja samuti maksuasutusi, millele teie organisatsioon käibearuandeid esitab.

## <a name="optional-setup-pages-for-accounts-payable"></a>Ostureskontro valikulised seadistuslehed
Lisaks põhifunktsioonidele on moodulil Ostureskontro muid funktsioone, mida saab seadistada.

Täiendavad seadistuslehed on organiseeritud funktsioonide järgi.

**Poliitikad**
-   Lehel Hankija arvepoliitika saate seadistada hankija arvepoliitikaid.

**Arvete võrdlemine**

-   Lehel Arvesummade lubatud kõikumised saate seadistada arvesummade lubatud kõikumisi.
-   Lehel Vastavusse viimise poliitika saate seadistada kahesuunalisi ja kolmesuunalisi vastavusse viimise poliitikaid.
-   Lehel Hinnakõikumised saate seadistada ühikuhindade lubatud kõikumisi.
-   Lehel Kauba hinnakõikumisgrupid saate seadistada kauba hinnakõikumisgruppe.
-   Lehel Hankija hinnakõikumisgrupid saate seadistada hankija hinnakõikumisgruppe.
-   Lehel Tasude kõikumised saate seadistada tasude lubatud kõikumisi.

**Töövoog**

-   Lehel Ostureskontro töövood saate seadistada töövookonfiguratsioone töölehtede kinnituste ja ostutaotluste jaoks.

**Põhjused**

-   Lehel Hankija põhjused saate seadistada põhjusekoode.

**Tasud**

-   Lehel Tasukoodid saate seadistada ostutellimustel kasutatavaid tasukoode.
-   Lehel Hankija tasude grupp saate luua ja hallata hankijate tasugruppe.
-   Lehel Kauba tasugrupid saate luua ja hallata kaupade tasugruppe.
-   Lehel Automaatsed kulud saate määratleda tellimustele automaatselt määratavad tasud.

**Lisakaubad**

-   Lehel Lisakaubagrupid – hankija saate luua ja hallata hankijate lisakaubagruppe.
-   Lehel Lisakaubagrupid – varud saate luua ja hallata kaupade lisakaubagruppe.

**Jaotus**

-   Lehel Tarnetingimused saate luua ja hallata kauba müüjalt ostjale tarnimise tingimusi.
-   Lehel Tarneviisid saate luua ja hallata transpordiviise, mida kasutatakse tellimuse transportimisel müüjalt ostjale.
-   Lehel Sihtkoha koodid saate luua ja hallata sihtkohtade koode ja kirjeldusi.

**Vormid**

-   Lehel Vormi märkused saate luua mitmesugustel lehtedel kuvatavat standardteksti.
-   Lehel Vormi sortimisparameetrid saate seadistada ostutellimuste, saabunud kaupade loendi, saatelehtede ja arvete sortimisjärjestuse.
-   Lehel Prindihalduse seadistus saate seadistada prindihalduse teabe lehtede originaalidele ja koopiatele.

**Maksed**

-   Lehel Skontod saate seadistada ja hallata skontode saamise tingimusi. Skonto koodid on seotud hankijatega ja neid rakendatakse ostutellimuste korral.
-   Lehel Maksegraafikud saate seadistada maksegraafikuid, mida kasutatakse hankijatele osamaksete tegemiseks.
-   Lehel Maksepäevad saate määratleda tähtaegade arvutamiseks kasutatavad maksepäevad ja täpsustada maksepäevaks konkreetse nädalapäeva või kuu.
-   Lehel Maksetasu saate luua ja hallata hankijatega seotud maksetasusid.
-   Lehel Maksejuhis saate luua ja hallata maksejuhiseid.

**Statistika**

-   Lehel Aegumisperioodi määratlused saate seadistada kasutaja määratletud intervalle, mida kasutatakse hankijakontode tähtajalise jaotuse analüüsimiseks.
-   Lehel Tegevusala saate luua tegevusala koode, mis hankijatele määratakse.

**Maks 1099**

-   Lehel **1099 väljad** saate kontrollida ja muuta miinimumsummasid, millest tuleb USA Maksuametile (IRS-ile) viimaste IRS-i nõuete alusel aru anda.

## <a name="optional-setup-for-other-modules"></a>**Valikuline seadistus teiste moodulite puhul**
**Organisatsiooni haldus**

-   Lehel numbriseeriad saate seadistada arvenumbritele numbriseeriate grupid.
-   Saate seadistada järgmistel lehtedel aadressiteabe.
    -   Aadressi häälestamine
    -   NAF-koodid
    -   Impordi sihtnumbrid

**Pearaamat**

-   Lehel Finantsdimensioonid saate seadistada finantsdimensioone.
-   Järgmistel lehtedel saate seadistada maksuteavet.
    -   Käibemaksukoodid
    -   Käibemaksugrupid
    -   Kauba käibemaksugrupid
    -   Kontogrupp
    -   Käibemaksuvabastuse koodid
    -   Käibemaksu jurisdiktsioonid
    -   Käibemaksuhaldurid
    -   Käibemaksu tasakaalustusperioodid

**Sularaha- ja pangahaldus**

-   Lehel Makse eesmärgi koodid saate seadistada keskpangamakse eesmärgikoodi.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]