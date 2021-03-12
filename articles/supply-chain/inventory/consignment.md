---
title: Saadetise seadistamine
description: Selles teemas selgitatakse, kuidas kasutada sissetuleva veose laoprotsesse.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchTablePart, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 01767385130bef6c252d78c8a328e30b7af4306f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963506"
---
# <a name="set-up-consignment"></a>Saadetise seadistamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas kasutada sissetuleva veose laoprotsesse.

Veose varud on varud, mis kuuluvad hankijale, kuid mida hoitakse teie tegevuskohas. Kui olete valmis tarbima või kasutama varusid, võtate varude omandiõiguse üle. See hõlmab teavet selle kohta, kuidas füüsiliselt vastu võtta hankijale kuuluvaid varusid laos ilma pearaamatu kannete loomiseta, kuidas käivitada tootmisprotsessi, kus hankijale kuuluvaid varusid saab füüsiliselt reserveerida, ning kuidas muuta toormaterjali omandiõigust, et töödelda tarbimist osana tootmistellimuse töötlemisest. On ka teavet selle kohta, kuidas hankijad saavad jälgida nende varude tarbimist, kasutades hankija koostöö liidest. 

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
-   Füüsiliste varude laoseisu värskendatakse, kasutades töölehte **Kauba inventuur**. Inventuuri saab kasutada ka hankija, et värskendada vabu varusid, kui neil on luba seda teha.

Hankija, US-104, saab jälgida värskendusi, kasutades lehte **Veose vaba kaubavaru**.

## <a name="consignment-replenishment-orders"></a>Veose täiendustellimused
Veose täiendustellimus on dokument, mida kasutatakse, et nõuda ja jälgida toodete varude koguseid, mida hankija soovib tarnida teatud kuupäevaintervalli siseselt, luues tellitud varude kanded. Tavaliselt põhineb see konkreetsete toodete prognoosil ja tegelikul nõudlusel. Varud, mis võetakse vastu veose täiendustellimuse suhtes, jääb hankija omandusse. Ainult füüsilise sissetuleku värskendusega seotud toodete omandus kirjendatakse ja seetõttu ei esine pearaamatu kande värskendusi. 

Dimensiooni **Omanik** kasutatakse, et eraldada teavet selle kohta, millised varud kuuluvad hankijale ja millised vastuvõtvale juriidilisele isikule. Veose täiendamistellimuse ridadel on olek **Avatud tellimus** seni, kuni ridade täielikku kogust pole vastu võetud või tühistatud. Kui täielik kogus on vastu võetud või tühistatud, muudetakse olekuks **Tühistatud**. Veose täiendamistellimusega seotud füüsilisi vabu varusid saab kirjendada, kasutades registreerimisprotsessi, aga ka toote sissetuleku värskendamisprotsessi. Registreerimist saab teha osana kauba saabumisprotsessist või tellimusridu käsitsi värskendades. Toote sissetuleku värskendamisprotsessi kasutamisel tehakse kirje toote sissetuleku töölehele, mida saab kasutada kaupade hankijale sissetuleku kinnitamiseks.

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

## <a name="inventory-owners"></a>Varude omanikud
Füüsiliste sissetulevate veose varude kirjendamiseks peate määratlema hankijast omaniku. Seda tehakse lehel **Varude omanik**. Kui teete valiku **Hankija konto**, loob see väljade **Nimi** ja **Omanik** jaoks vaikeväärtused. Väärtus väljal **Omanik** on hankijale nähtav, seega võite soovi korral seda muuta, kui hankijakonto nimesid pole välistel inimestel lihtne tuvastada. On võimalik redigeerida välja **Omanik**, kuid ainult kirje **Varude omanik** salvestamiseni. Väli **Nimi** täidetakse selle osapoole nimega, millega hankija konto on seostatud ja seda ei saa muuta.

[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Jälgimisdimensioonigrupp
Veose protsessides kasutatavad kaubad tuleb seostada valikuga **Jälgimisdimensioonigrupp**, kus dimensioon **Omanik** on määratud sättele **Aktiivne**. Dimensioonil Omanik on suvandid **Füüsiline ladu** ja **Finantsiline laovaru** valitud. Suvand **Laovarude planeerimine dimensioonide kaupa** pole kunagi valitud.

[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Varude omandiõiguse muutmise tööleht
Töölehte **Varude omandiõiguse muutmine** kasutatakse, et kirjendada veose varude omandiõiguse ülekannet hankijalt juriidilisele isikule, kes seda tarbib. Nagu iga varude töölehega, tuleb see tuvastada lao töölehe nimega. Need nimed luuakse lehel **Lao töölehe nimed** ja valik **Töölehe tüüp** tuleb määrata sättele **Omandiõiguse muutmine**.

[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Hankija koostöö veoseprotsessides
Kui hankijad kasutavad hankija koostööliidest, saavad nad seda kasutada varude tarbimise jälgimiseks teie tegevuskohas. Lisateavet hankijate koostööks tarnijate seadistamise kohta leiate jaotisest [Hankijaportaali kasutaja turvalisus](../procurement/configure-security-vendor-portal-users.md).





