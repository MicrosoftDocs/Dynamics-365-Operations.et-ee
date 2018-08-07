---
title: "Käibemaksu korvamine kulude halduses"
description: "Teema selgitab, kuidas saada tagasimakseid sobilike käibemaksukannete korral."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: et-ee
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>Käibemaksu korvamine kulude halduses

Tagasimaksete saamiseks sobilike käibemaksukannete korral peab ettevõte või organisatsioon tuvastada, koguma, kinnitama ja esitama täpset teavet. Protsess hõlmab erinevaid ülesandeid ja olenevalt teie ettevõtte suurusest võib kaasata erinevaid töötajaid või rolle.

Käibemaksu korvamiseks kulude halduse abil peavad olema täidetud järgmised eeltingimused.

- Kulukategooriatesse eraldatud riikide/regioonide jaoks tuleb luua maksukoodid.
- Iga maksukoodi jaoks tuleb luua käibemaksugrupp.
- Iga käibemaksugrupi jaoks tuleb luua kauba käibemaksukood.

Pärast eeltingimuste täitmist järgivad töövõtjad neid etappe, et taotleda käibemaksukannetega seotud tagasimakseid.

1. Kuluaruandes sisestage maksuteave krediitkaardikannete kohta, et tuvastada sobilikud käibemaksutagastused.
2. Veenduge, et kogu maksuteave oleks lisatud ja seejärel sisestage kuluaruanne.
3. Töödelge kulusid, mis on sobilikud rahvusvaheliseks käibemaksu korvamiseks.
4. Saatke käibemaksu korvamise andmed muust osapoolest hankijale, et registreerida rahvusvahelised korvamised.
5. Töödelge kulusid kodumaiseks käibemaksu korvamiseks.

Järgmistes jaotistes on esitatud näiteid, mis näitavad, kuidas Contoso töövõtjad läbivad iga etapi.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Kuluaruandes maksuteabe sisestamine krediitkaardikannete kohta, et tuvastada sobilikud käibemaksutagastused

Contoso müügiesindaja Nancy, kes elab USAs, naasis hiljuti müügireisilt Ühendkuningriiki. Reisi ajal tekkisid tal mõned isikliku krediitkaardi kulutused toitlustuse eest. Nüüd peab Nancy kulude vastavusseviimiseks looma kuluaruande.

Kui Nancy sisestab oma kuluaruandes andmeid, valib ta lehel **Redigeeri kuluaruannet** väljal **Riik/regioon** riigi **Ühendkuningriik**. Seejärel filtreeritakse käibemaksugruppide loendit, et kuvada ainult Ühendkuningriigile kehtivad grupid. Nancy valib käibemaksugrupi **Ühendkuningriik 001** ja kauba käibemaksugrupi **Toitlustus**. Seejärel lisab ta uue kande majutuse jaoks. Kuna Ühendkuningriigis on majutuse jaoks ainult üks käibemaksugrupp ja kauba käibemaksugrupp, lisatakse see teave Nancy kuluaruandesse automaatselt.

Contoso poliitika kohaselt peab kõigi kulude kohta olema olemas vastav kviitung. Seetõttu, kui Nancy salvestab oma kuluaruannet, saab ta teate, mis ütleb, et ta peab kuluaruandes loetletud iga kande jaoks lisama kviitungi. Nancy veendub, et ta oma kuluaruandesse lisanud digitaalse pildi igast kande kviitungist ja seejärel esitab aruande kinnitamiseks. Seejärel saadab ta paberkviitungid arveldusosakonna töörühmale. See töörühm saadab käibemaksu tagastamise andmed muust osapoolest hankijale, kes esitab rahvusvahelised käibemaksukorvamised Contosole.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Veendumine, et kogu maksuteave oleks lisatud ja seejärel kuluaruande sisestamine

Contoso ostureskontro koordinaator April peab enne aruande sisestamist sisestama kogu võimaliku maksuteabe, mis on kuluaruandest puudu. Ta avab lehe **Kuluaruande üksikasjad** ja näeb Nancy kinnitatud kuluaruannet. Seejärel avab April kuluaruande, et vaadata kannete üksikasju. Ta näeb, et Nancy ei sisestanud ühe kande jaoks kauba käibemaksugruppi. Kuna see teave on esitamata, ei saa April kuluaruannet sisestada. Seetõttu vaatab April kulude halduses lehte **Maksukonfiguratsioonid** ja leiab üles riigi/regiooni vastava kauba käibemaksugrupi ja kande tüübi. Nüüd saab April kuluaruande pearaamatusse sisestada.

Kui April sisestab kuluaruande, luuakse käibemaksu tagastamise tööüksus. See tööüksus määratakse arveldusosakonna töörühma liikmele. April saab teate, mis kinnitab, et sisestamine õnnestus. Teates on loetletud ka korvamiseks sobilike käibemaksukannete arv.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Rahvusvaheliseks käibemaksu korvamiseks sobilike kulude töötlemine

Contoso arveldusosakonna töörühma liikme Arnie ülesanne on kinnitada, et kogu käibemaksu korvamiseks vajalik teave on kuluaruannetes olemas. Ta avab lehe **Kulumaksu korvamine** ja valib Nancy esitatud kuluaruande. Arnie kontrollib, kas kõik vajalikud kviitungid on olemas ning kas õige käibemaksugrupp ja kauba käibemaksukoodid on sisestatud.

Kui Arnie saab Nancylt paberkviitungid, võrdleb ta neid digitaalsete kviitungitega ja muudab kuluaruande olekuks **Korvamiseks valmis**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Käibemaksu korvamise andmete saatmine muust osapoolest hankijale, et registreerida rahvusvahelised korvamised

Kui Arnie on valmis kuluaruande andmete saatmiseks muust osapoolest hankijale, kes esitab käibemaksu korvamised, avab ta lehe **Kulumaksu korvamine**. Ta filtreerib lehte, et see kuvaks ainult kuluaruanded, millel on märge **Korvamiseks valmis**. Seejärel valib Arnie suvandid **Fail** &gt; **Ekspordi Excelisse**. Käibemaksu teave kuluaruannetest eksporditakse Microsoft Exceli töölehele. Arnie esitab selle töölehe muust osapoolest hankijale ja lisab sõnumi teatega, et paberkviitungid on saadetud kulleriga.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Kodumaise käibemaksu korvamise kulude töötlemine

Arnie peab veenduma, et kuluaruande kanded on käibemaksu korvamiseks sobilikud ja et aruannetele on lisatud digitaalsed kviitungid. Kodumaiseks korvamiseks sobilike kulude töötlemiseks avab Arnie lehe **Kulumaksu korvamine** ja valib kinnitamist vajava kuluaruande. Ta kontrollib, et kviitungid on ettevõtte nimel, mitte töövõtja nimel. Käibemaksu korvamiseks peavad kviitungid olema ettevõtte nimel. Seejärel kinnitab Arnie, et kasutati õiget käibemaksugruppi ja kauba käibemaksukoode.

Kui Arnie saab paberkviitungid, muudab ta kuluaruande olekuks **Korvamiseks valmis**. Seejärel saab ta kinnitada korvamise sobivale maksuasutusele. Praegusel juhul on vastutav maksuasutus USAs IRS.

