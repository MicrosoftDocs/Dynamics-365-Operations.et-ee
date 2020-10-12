---
title: Varade teisaldamine, asendamine ja installimine
description: Selles teemas kirjeldatakse, kuidas varasid moodulis Asset Management teisaldada, asendada ja installida.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec150adb35eb0600844245b14cbec9e9632ab337
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889549"
---
# <a name="move-replace-and-install-assets"></a>Varade teisaldamine, asendamine ja installimine

[!include [banner](../../includes/banner.md)]

 

Selles teemas kirjeldatakse, kuidas varasid moodulis Asset Management teisaldada, asendada ja installida. Saate luua üksikuid varasid, millel pole seoseid muude varadega või luua vara struktuuri, mis sisaldab emavara (ülataseme vara) ja seotud tütarvarasid (alamvarasid). Moodulis Asset management on kolm võimalust vara asukoha teisaldamiseks ja muutmiseks.

- **Teisalda** – saate teisaldada vara kas muusse vara struktuuri või muusse asukohta samas varastruktuuris.
- **Asenda** – saate vara struktuurist ajutiselt eemaldada, et seda saaks parandada või remontida ja seejärel lisada remonditud vara hiljem tagasi vara struktuuri. Teise võimalusena asendada kasutatud vara püsivalt uue varaga.
- **Installi** – saate emavara ja kõik seotud tütarvarad töö asukohta installida.

> [!NOTE]
> Teisaldamisel, asendamisel või installimisel olev vara võib olla seotud mõne muu töö asukohaga. Sel juhul võib vara kasutada töö asukoha finantsdimensioone. Lehel **Töö asukoha tüübid** seadistage finantsdimensioonide käsitsemine töö asukohtadele.

## <a name="move-asset"></a>Vara teisaldamine

Funktsiooni **Vara teisaldamine** saate kasutada vara teisaldamiseks kas muusse vara struktuuri või muusse asukohta samas varastruktuuris. Vara saab teisaldada ka väljapoole vara struktuuris, nii et sellest saab eraldiseisev vara, millel pole seoseid struktuuriga.

> [!NOTE]
> Ärge kasutage seda funktsiooni, kui varasid parandatakse või asendatakse ajutiselt. Selle asemel kasutage funktsiooni **Vara asendamine**, mida kirjeldatakse hiljem selles teemas.

1. Valige **Varahaldus** \> **Ühine** \> **Varad** \> **Kõik varad** või **Aktiivsed varad**.
2. Valige loendist teisaldatav vara. Kui varal on alamarad, teisaldate ka need varad.
3. Valige **Teisalda vara**.
4. Vara teisaldamiseks nii, et see muutuks varade struktuuri osaks, valige uus emavara väljal **Emavara**. Kui teisaldate tütarvara ja soovite muuta selle eraldiseisvad põhivarad, millel pole struktuurisuhteid, jätke **emasvara** väli tühjaks.
5. Vaikimisi määratakse väljale **Kehtiv** praegune kuupäev ja kellaaeg. Siiski saate valida mõne muu kuupäeva ja kellaaja, millest alates vara teisaldamine kehtib.
6. Valige nupp **OK**.

## <a name="replace-asset"></a>Vara asendamine

Kasutage funktsiooni **Vara asendamine** seoses remontimise, renoveerimise või kulunud vara püsiva asendamisega uue varaga. Seda funktsiooni kasutatakse alamvarade asendamiseks vara struktuuris. Emavara jaoks (st varad, millel pole praegu emavara), tehakse see asendamine töö asukohas. Lisateabe saamiseks emavara asendamiseks töö asukohas lugege teemat [Varade installimine töö asukohtadesse](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Kui tootmisosakonnaga on seotud remonditöökoda, saate luua töö asukohti **(nt Remont**, **Praak**ja **Ladustamine**), et käsitseda vara parandamist ja asendamist.

1. Valige **Varahaldus** \> **Ühine** \> **Varad** \> **Kõik varad** või **Aktiivsed varad**.
2. Valige loendist asendatav alamvara. Kui varal on alamvarad, asendate ka need varad.
3. Valige **Asenda vara**.

    Väljal **Struktuuri muutus** kuvatakse viimane kuupäev ja kellaaeg, millal valitud vara ja seotud alamvarad vara struktuuris teisaldati.

4. Valige jaotise **Valitud vara** väljal **Töö sihtasukoht** töö asukoht, kuhu vara teisaldada. Näiteks saate valida asukoha **Remont** või **Praak**.

    Jaotises **Emavara** kuvatakse väljal **Kehtiv** viimane kuupäev ja kellaaeg, mil emavara ja sellega seotud tütarvarad on praegusesse töö asukohta installitud või teisaldatud.

5. Valige jaotise **Uus vara** väljal **Vara** valitud vara ajutiseks või püsivaks asendamiseks lisatav vara. See vara võib praegu asuda mõnes muus töö asukohas (nt **Ladustamine**).
7. Jaotises **Kehtiv alates** on väli **Kehtiv** seadistatud vaikimisi praegusele kuupäevale ja kellaajale. Siiski saate valida mõne muu kuupäeva ja kellaaja, millest alates vara asendamine kehtib.
8. Valige nupp **OK**.

## <a name="install-asset"></a>Vara installimine

Vara struktuuri installimiseks töö asukohta kasutage funktsiooni **Vara installimine**.

> [!NOTE]
> Valige alati emavara. Emavara ja sellega seotud tütarvarad teisaldatakse valitud töö asukohta.

1. Valige **Varahaldus** \> **Ühine** \> **Varad** \> **Kõik varad** või **Aktiivsed varad**.
2. Valige loendist ema vara, mida soovite installida muusse töö asukohta.
3. Valige **Installi vara**.

    Jaotises **Atribuudid** kuvatakse emavaras seadistatud vara atribuudid.

4. Valige väljal **Töö asukoht** uus asukoht.
5. Vaikimisi määratakse väljale **Kehtiv** praegune kuupäev ja kellaaeg. Siiski saate valida mõne muu kuupäeva ja kellaaja, millest alates vara installimine vara struktuuri kehtib.
6. Valige nupp **OK**.
