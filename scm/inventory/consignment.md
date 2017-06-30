---
title: Saadetis
description: Selles teemas selgitatakse, kuidas kasutada sissetuleva veose laoprotsesse.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a6e3f0e58e14cc4d68d2249a4e3b69515f23e838
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="consignment"></a>Saadetis

[!include[banner](../includes/banner.md)]


Selles teemas selgitatakse, kuidas kasutada sissetuleva veose laoprotsesse.

Veose varud on varud, mis kuuluvad hankijale, kuid mida hoitakse teie tegevuskohas. Kui olete valmis tarbima või kasutama varusid, võtate varude omandiõiguse üle. See hõlmab teavet selle kohta, kuidas füüsiliselt vastu võtta hankijale kuuluvaid varusid laos ilma pearaamatu kannete loomiseta, kuidas käivitada tootmisprotsessi, kus hankijale kuuluvaid varusid saab füüsiliselt reserveerida, ning kuidas muuta toormaterjali omandiõigust, et töödelda tarbimist osana tootmistellimuse töötlemisest. On ka teavet selle kohta, kuidas hankijad saavad jälgida nende varude tarbimist, kasutades hankija koostöö liidest. Sissetuleva veose protsesside lubamise ja konfigureerimise kohta lisateabe saamiseks vaadake [Saadetise seadistamine](set-up-consignment.md).

## <a name="overview-of-the-consignment-process"></a>Veose töötlemise ülevaade
Selles näidisstsenaariumis on ettevõtte USMF-l veose leping hankijaga US-104 toormaterjali M9211CI jaoks.

1.  Veose täiendamise tellimuse loob käsitsi keegi USMF-s oodatava nõudluse põhjal. Tellimus luuakse hankijale US-104 ja rida lisatakse kaubale MS9211CI.
2.  Hankijat teavitatakse eeldatava tarnekuupäeva kohta. See võib juhtuda ühel kolmest viisist.
    -   Keegi, kes töötab USMF-s, saadab hankijale tellimuse teabe.
    -   Hankija saab jälgida eeldatavaid vabu varusid, kasutades hankija koostööliidest.
    -   Keegi, kes töötab USMF-s, filtreerib andmeid lehel **Vaba kaubavaru**, et näidata ainult hankija US-104 kirjeid, kus sissetuleku olek on **Tellitud**, ja saadab selle teabe seejärel hankijale.

3.  Varud tarnitakse US-104-st USMF-sse.
4.  Kui materjal saabub USMF-sse, värskendatakse veose täiendamistellimust toote sissetulekuga. Kirjendatakse ainult hankijale kuuluvate varude füüsilised kogused. Puuduvad loodud pearaamatu kanded, kuna varude omanik on ikka hankija.
5.  Hankija jälgib värskendusi füüsilistele vabadele varudele, kasutades lehte **Veose vaba kaubavaru**.
6.  Nüüd, kui füüsilised varud on laos, reserveerib tootmisprotsess hankijale kuuluvad varud ja käivitab tootmistellimuse lõpetatud kaupadele, mis tarbivad toormaterjali M9211CI.
7.  Tänases tootmises tarbitavate reserveeritud toormaterjalide omanik muudetakse US-104-lt USMF-le. Selleks kasutatakse varude omandiõiguse muutmise töölehte. See protsess loob ostutellimused, kus väli **Päritolu** on määratud valikule **Saadetis**.
8.  Hankija jälgib tarbimist (omandiõiguse muutmine) lehel **Veose varudest saadud tooted** ja väljastab arve kahe ettevõtte vaheliste lepingute põhjal.
9.  Tootmisprotsess tarbib toormaterjali tootmise komplekteerimislehe kaudu. Füüsilist reserveerimist värskendatakse automaatselt näitamaks, et vabade varude omanik on USMF.
10. US-104 arvet töödeldakse ostutellimuste suhtes, mis loodi automaatselt varude omandiõiguse töölehe töötlemisel. Makse tehakse hankijale US-104 tarbitud varude eest.

USMF teeb täiendavad perioodilised protsessid.

-   Hankijale kuuluvate varude füüsilist liikumist töödeldakse erinevate ladude vahel üleviimistöölehte kasutades.
-   Füüsiliste varude laoseisu värskendatakse, kasutades töölehte**Kauba inventuur**. Inventuuri saab kasutada ka hankija, et värskendada vabu varusid, kui neil on luba seda teha.

Hankija, US-104, saab jälgida värskendusi, kasutades lehte **Veose vaba kaubavaru**.

## <a name="consignment-replenishment-orders"></a>Veose täiendustellimused
Veose täiendustellimus on dokument, mida kasutatakse, et nõuda ja jälgida toodete varude koguseid, mida hankija soovib tarnida teatud kuupäevaintervalli siseselt, luues tellitud varude kanded. Tavaliselt põhineb see konkreetsete toodete prognoosil ja tegelikul nõudlusel. Varud, mis võetakse vastu veose täiendustellimuse suhtes, jääb hankija omandusse. Ainult füüsilise sissetuleku värskendusega seotud toodete omandus kirjendatakse ja seetõttu ei esine pearaamatu kande värskendusi. Dimensiooni **Omanik** kasutatakse, et eraldada teavet selle kohta, millised varud kuuluvad hankijale ja millised vastuvõtvale juriidilisele isikule. Veose täiendamistellimuse ridadel on olek **Avatud tellimus** seni, kuni ridade täielikku kogust pole vastu võetud või tühistatud. Kui täielik kogus on vastu võetud või tühistatud, muudetakse olekuks **Tühistatud**. Veose täiendamistellimusega seotud füüsilisi vabu varusid saab kirjendada, kasutades registreerimisprotsessi, aga ka toote sissetuleku värskendamisprotsessi. Registreerimist saab teha osana kauba saabumisprotsessist või tellimusridu käsitsi värskendades. Toote sissetuleku värskendamisprotsessi kasutamisel tehakse kirje toote sissetuleku töölehele, mida saab kasutada kaupade hankijale sissetuleku kinnitamiseks. 

[![veose-täiendustellimus](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Varude omandiõiguse muutmise tööleht
Varude omaniku muutmise protsess hankijalt vastuvõtvale juriidilisele isikule tehakse varude omandiõiguse muutmise töölehe kasutamisega. Ühtegi eeldatavat laokannet ei looda töölehele. Ainsad loodavad laokanded on need, mis on seotud sisestatud töölehega. Millal tööleht sisestatakse?

-   Hankijale kuuluvad varud väljastatakse, kasutades viidet **Omandiõiguse muutmine** olekuga **Müüdud**.
-   Vabad kaubavarud võtab vastu juriidiline isik, kes tarbib neid, kasutades toote sissetulekut, mida värskendatakse ostutellimuse varude kandega. See määrab tellimuse olekuks **Vastu võetud**. Veose jaoks kasutatavatel ostutellimustel on väli **Päritolu** määratud valikule **Saadetis**.

Pärast seda, kui tellimus on loodud, ei ole võimalik värsendada kogust veose ostutellimuse ridadel. 

[![varude-omandiõiguse-muutmise-tööleht](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Hankija koostöö veose protsessides
Hankija koostööliidesel on kolm sissetuleva veose protsessiga seotud lehte.

-   **Ostutellimused,** **mis tarbivad veose varusid** – näitab üksikasjalikku ostutellimuse teavet, mis on seotud omandiõiguse vahetusega veose protsessist.
-   **Veose varudest saadud tooted** – näitab teavet kaupade ja kogemuste kohta, mille toote sissetulekuid värskendatakse omandiõiguse muutmisprotsessi käigus.
-   **Veose vaba kaubavaru** – näitab teavet selliste veose kaupade kohta, mille tarnimist nad ootavad ja selliste, mis on juba kliendi tegevuskohas füüsiliselt saadaval.





