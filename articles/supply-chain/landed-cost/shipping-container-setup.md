---
title: Saatmiskonteinerid
description: See artikkel kirjeldab, kuidas seadistada saatmiskonteineriid väljaminev kulumoodulile.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 345f815a4f85db30db18aba3f8a4d41835c2e3f2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860838"
---
# <a name="shipping-container-setup"></a>Saatmiskonteineri seadistamine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada saatmiskonteineriid väljaminev **kulumoodulile**.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Saatmiskonteineritüüpide seadistamine

Saatmiskonteineritüübid määravad mis tüüpi konteinerid on saadaval tarnimisel ja teekondades kasutamiseks.

Saatmiskonteineritüüpidega töötamiseks avage **Väljalaadimiskulu \> Konteinerite seadistus \> Saatmiskonteineritüübid**. Seal saate konteineritüüpide kirjeid vaadata, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Saatmiskonteineri tüüp | Sisestage saatmiskonteineritüübi ainu-ID nimi/number. |
| Kirjeldus | Sisestage saatmiskonteineritüübi kirjeldus. |
| Maht | Sisestage seda tüüpi saatmiskonteinerite lubatud maksimummaht. |
| Kaal | Sisestage seda tüüpi saatmiskonteinerite lubatud maksimumkaal. |
| Tagastatav | Määrake, kas seda tüüpi saatmiskonteinerid saab pärast teekonnal kasutamist tagastada hankijale. Kui suvandi väärtuseks on seatud *Jah*, võivad seda tüüpi saatmiskonteinerite lähtesadamasse tagastamisele rakenduda lisakulud. |

## <a name="set-up-shipping-containers"></a>Saatmiskonteinerite seadistamine

Kõigi teekondades kasutatud konteinerite tuvastamiseks kasutate saatmiskonteinerikirjeid. Teekonna loomisel saate selle jaoks valida kindla konteineri kõigi siin määratud saatmiskonteinerikirjete loendist. See funktsioon on eriti kasulik juhul, kui ettevõttel on oma saatmiskonteinerid.

Saatmiskonteinerinumbreid ei pea sisestada selliste saatmiskonteinerite jaoks, mida kasutatakse ainult üks kord. Selle asemel saate saatmiskonteineri numbri lisada teekonna loomisel.

Saatmiskonteinerikirjeid kasutatakse ainult moodulis Väljalaadimiskulu. Need pole saadaval standardmoodulis **Transpordihaldus** (TMS).

Saatmiskonteineritega töötamiseks avage **Väljalaadimiskulu \> Konteinerite seadistus \> Saatmiskonteinerid**. Seal saate saatmiskonteinerite kirjeid vaadata, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Saatmiskonteiner | Sisestage saatmiskonteineri ainu-ID nimi/number. |
| Saatmiskonteineri tüüp | Valige saatmiskonteineri tüüp. Lisateabe saamiseks vt selle artikli [varasemat jaotist Konteineri](#shipping-container-types) tüüpide lähetuse häälestamine. |

> [!NOTE]
> - Saatmiskonteineri seadistamine on valikuline. Tavaliselt kasutatakse seda ainult juhul, kui ettevõttel on oma saatmiskonteinerid või kui see kasutab sageli samu saatmiskonteinereid.
> - Saatmiskonteinerinumbrite jaoks ei arvutata kontrollnumbreid.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Ühikutüüpide seadistamine

Ühikutüübid määravad saatmiskonteinerite jaoks täiendavad rühmitus- ja tuvastusmeetodid. Ühikutüüpi kasutatakse tavaliselt selleks, et tuvastada kaupu sisaldava konteineri tüüp, näiteks kaubaalused või vaadid. Ühikutüübi saate valida, kui seadistate konteineri lehel **Kõik saatmiskonteinerid**.

Ühikutüüpe kasutatakse ainult moodulis Väljalaadimiskulu. Need ei ole saadaval TMS-is.

Ühikutüüpidega töötamiseks avage **Väljalaadimiskulu \> Konteinerite seadistus \> Ühikutüübid**. Seal saate ühikutüüpide kirjeid vaadata, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Ühiku tüüp | Sisestage ühikutüübi ainu-ID nimi/number. |
| Kirjeldus | Sisestage ühikutüübi kirjeldus. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Külmutuse tüüpide seadistamine

Külmutuse tüübid määravad saatmiskonteinerite (tavaliselt külmkonteinerite) jaoks täiendavad rühmitus- ja tuvastusmeetodid. Külmutuse tüübi saate valida, kui seadistate konteineri lehel **Kõik saatmiskonteinerid**.

Külmutuse tüüpidega töötamiseks avage **Väljalaadimiskulu \> Konteinerite seadistus \> Külmutuse tüübid**. Seal saate külmutuse tüüpide kirjeid vaadata, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Külmutuse tüüp | Sisestage külmutuse tüübi ainu-ID nimi/number. |
| Kirjeldus | Sisestage külmutuse tüübi kirjeldus. |
