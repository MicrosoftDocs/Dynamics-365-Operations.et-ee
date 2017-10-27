---
title: "Ostutellimuse ülevaade"
description: "Selles artiklis antakse üldist teavet ostutellimuste (PO-de) kohta ja lingid täiendavate artiklite juurde, mis on seotud mitmesuguste etappidega, mille PO läbib."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: c36795a071cc72721558bfa8984ecf1f47501c91
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-order-overview"></a>Ostutellimuse ülevaade

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Selles artiklis antakse üldist teavet ostutellimuste (PO-de) kohta ja lingid täiendavate artiklite juurde, mis on seotud mitmesuguste etappidega, mille PO läbib.

Ostutellimus (PO) on dokument, mis kujutab endast kokkulepet hankijaga kaupade või teenuste ostmiseks. See dokument aitab jälgida ka toote sissetulekuid, mis on tellimuse suhtes tehtud, ja hiljem tellimuse suhtes väljastatud hankija arvete arvestust.  

Lehel **Ostutellimused** on ülevaade olemasolevatest tellimustest ja seal saate neid tellimusi muuta. Kui PO avate, saate valida vaate **Päis**, mis sisaldab teavet, mis määratakse iga PO puhul ainult üks kord (nt hankija andmed). Teise võimalusena saate valida vaate **Read**, kus saab tellimuse ridu muuta. Tavaliselt liigute ostutellimuste muutmisel nende kahe vaate vahel. Tasusid pole lehel **Ostutellimused** otseselt loetletud, kuid nende juurde pääseb tellimuse päises ja ridadel olevate menüüde kaudu.  

On palju aruandeid, kus saate vaadata andmeid ostutellimuste, toote sissetulekute ja hankija arvete kohta. Need aruanded leiate ka moodulitest **Hanked** ja **Ostureskontro**.  

Tööruumides **Ostutellimuse ettevalmistamine** ja **Ostutellimuse vastuvõtt ja järeltegevus** saate vaadata ostutellimuste loendeid nende mitmesugustes olekutes, millesse need on jõudnud. Samuti pakuvad nad vajalike tegevuste kokkuvõtet. Tööruum **Ostutellimuse ettevalmistamine** keskendub ostutellimuse loomisele ja ülevaatamisele, tellimuse töötlemisele heakskiidu kaudu ja hankija kinnitusele. Tööruum **Ostutellimuse vastuvõtt ja järeltegevus** keskendub kaupade või teenuste vastuvõtmisele ostutellimuste suhtes. See sisaldab loendeid, mis annavad ülevaate sissetulekutest, mis on tähtaja ületanud või mille tarnija peaks varsti kohale toimetama. Neid tööruume ei kasutata laos toimuvate seotud sissetulekutegevuste läbiviimiseks. Neid tegevusi tehakse moodulite **Varude haldus** ja **Laohaldus** lehtede abil. Hankija arveid tuleks töödelda tööruumi **Hankija arve sisestamine** abil ja makseid tuleks teha tööruumi **Hankija maksed** abil.  

Järgmistes artiklites antakse ülevaade mitmesuguste etappide kohta, mille ostutellimus läbib.

-   [Ostutellimuse loomine](purchase-order-creation.md)
-   [Ostutellimuse heakskiitmine ja kinnitamine](purchase-order-approval-confirmation.md)
-   [Toote sissetulek ostutellimuste suhtes](product-receipt-against-purchase-orders.md)
-   [Hankija arvete ülevaade](../../financials/accounts-payable/vendor-invoices-overview.md)

## <a name="types-of-purchase-orders"></a>Ostutellimuste tüübid
Ostutellimusi on kolme tüüpi. Ostutellimuse loomisel tuleb määrata tüüp. Uute tellimuste kohta saab seadistada tellimuse vaiketüübi lehel **Hankeparameetrid**.

| Ostutellimuse tüüp        | Kirjeldus                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tööleht        | Kasutage seda tüüpi tellimuse mustandi loomiseks. See tüüp ei mõjuta varude koguseid ega tekita laokandeid. Ostutellimuse töölehe ridu ei lisata koondplaneerimisse.                                                                                                       |
| Ostutellimus | Kasutage seda tüüpi ostutellimuste loomiseks, kui hankija on tellimused kinnitanud ja tellimuste töötlemisel sissetuleku ja arveldamise kaudu enne makse tegemist hankijale. Seda tüüpi PO on kõige levinum.                                                                          |
| Tagastatud tellimus | Kasutage seda tüüpi kaupade tagastamisel hankijale. Seda tüüpi tellimus nõuab, et määraksite tagastatava materjali autoriseerimise (RMA) numbri, mille hankija teile annab. RMA numbri saab määrata ostutellimuse vahekaardil **Üldine**. Tellimuse ridadel peavad olema negatiivsed kogused. |

## <a name="purchase-order-statuses"></a>Ostutellimuse olekud
Ostutellimused sisaldavad mitut olekuvälja, mis näitavad tellimuse edenemist. Kõik need väljad on näha tellimuse vaates **Päis** ja mõned neist on nähtavad ka kõigi tellimuste ruudustikuvaates. Väljal **Olek** on näha tellimusel olevate koguste olek. Saadaval on järgmised väärtused:

-   **Avatud tellimus** – tellimused on loodud ja tellimusel on kogused.
-   **Saadud** – mõned kogused on vastu võetud, kuid veel arveldamata.
-   **Arveldatud** – terve tellimusel olev kogus on arveldatud. **Märkus.** Kui tellimus on *osaliselt* arveldatud, pole ei olek **Saadud** ega **Arveldatud** sobilik. Seega on tellimuse olek endiselt **Avatud tellimus**.
-   **Tühistatud** – tellimus kinnitati, kuid tühistati hiljem. Seetõttu näitab see olek, et tellimusel pole enam avatud koguseid.

Väli **Dokumendi olek** aitab teil töödeldud dokumentide põhjal tellimuse edenemist kiiresti üle vaadata. See näitab tellimuse puhul kõige viimati täidetud dokumendi olekut. Saadaval on järgmised väärtused:

-   **Puudub** – tellimuse puhul pole veel ühtegi dokumenti töödeldud.
-   **Ostupäring** – koostatud on ostupäring ja tellimus ootab hankija tagasisidet.
-   **Ostutellimus** – tellimuse kinnitus on töödeldud.
-   **Toote sissetulek** – tellimusel on toote sissetulek töödeldud.
-   **Arve** – tellimusele on registreeritud arve.

Välja **Kinnitamise olek** kasutatakse, kui ostutellimus läbib töövoo ülevaatusprotsessi. Saadaval on järgmised väärtused:

-   **Mustand**, **Ülevaatamisel** ja **Tagasi lükatud** – neid olekuid kasutatakse ainult siis, kui ostutellimuse puhul kasutatakse kinnitamise töövoogu.
-   **Kinnitatud** – see olek määratakse tellimustele, mis on läbinud töövoo kinnitamise. Tellimused, mis on loodud kinnitamise töövoogu kasutamata, saavad kohe oleku **Kinnitatud**.
-   **Välisel ülevaatamisel** – seda olekut kasutatakse stsenaariumides, kus ostutellimus on hankijale saadetud, et hankija saaks ostutellimuse tingimused kinnitada. Seda olekut kasutatakse ka protsessis, mis algatatakse tegevusega **Kinnituse taotlus**. Selle protsessi puhul palutakse hankijal kinnitada ostutellimuse tingimused, luues ühenduse teie süsteemiga ja registreerides, kas ta kinnitab tellimuse või lükkab selle tagasi.
-   **Kinnitatud** – see olek määratakse pärast tellimuse kinnitamist. Tavaliselt on see olek viimane tellimusele määratud kinnitusolek.


<a name="see-also"></a>Vt ka
--------

[Ostutellimuse loomine](purchase-order-creation.md)

[Ostutellimuse heakskiitmine ja kinnitamine](purchase-order-approval-confirmation.md)

[Toote sissetulek ostutellimuste suhtes](product-receipt-against-purchase-orders.md)

[Hankija arvete ülevaade](../../financials/accounts-payable/vendor-invoices-overview.md)




