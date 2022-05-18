---
title: Kontsernisiseste tellimuste muutmine
description: See teema selgitab kontsernisiseste tellimuste funktsioonide muutmist
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 10efc397c64833785f286983987fd05854a69c0f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672902"
---
# <a name="change-intercompany-orders"></a>Kontsernisiseste tellimuste muutmine

[!include [banner](../../includes/banner.md)]

Kui muudate kontsernisisest müügi- või ostutellimust, peegeldab seda muutust ka vastav müügi- või ostutellimus vastavas ettevõte.

## <a name="adding-new-lines"></a>Uute ridade lisamine

Kui algne müügitellimus on osa kontsernisisesest tellimusahelast, saate lisada uusi ridu kontsernisisesele müügitellimusele ja ostutellimusele. Kui algne müügitellimus ei ole otsetarne, saate lisada ka uusi ridu. Kui algne müügitellimus on otsetarne, saate lisada uusi tellimusridu kontsernisisesele müügitellimusele ja ostutellimusele ainult siis, kui algse müügitellimuse kiirkaardil on valitud väli **Luba kaudne loomine** suvand **Kontsernisisesed sätted**.

## <a name="changing-prices-and-discounts"></a>Hindade ja allahindluste muutmine

Saate muuta hindu ja allahindlusi, kui **Kontsernisisesel** lehel on märgitud ruudud **Luba hinna redigeerimine** ja **Luba allahindluse** redigeerimist.

Kui muudate kontsernisisese müügitellimuse rea ühe olemasoleva rea ühiku hinda, muutub ka ühiku hind kontsernisisesel ostutellimusel.

Kui muudate mis tahes allahindluse välja kontsernisisesel müügitellimuse real, värskendab rakendus vastavad allahindluse väljad kontsernisisesel ostutellimusel.

## <a name="changing-and-adding-new-charges"></a>Uute kulude muutmine ja lisamine

Saate muuta kulusid, kui **Kontsernisisesel** lehel on märgitud ruudud **Luba hinna redigeerimine** ja **Luba allahindluse redigeerimist**.

Kui lisate kontsernisisesele müügitellimuse päisele uue kulu ja lisate kontsernisisesele müügireale uue kulu, kopeeritakse mõlemad kulud kontsernisisesele ostutellimusele. Seega on kontsernisisesel müügitellimusel ja kontsernisisesel ostutellimusel sama kogusumma. Lisakulusid ei kopeerita kunagi algsele müügitellimusele.

## <a name="copying-a-fee"></a>Tasu kopeerimine

Tasu kopeerimiseks algsele müügitellimusele looge see uue müügireana millel on **Teenus** üksus.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Koguste muutmine ja kontsernisiseste ostu- ja müügitellimuse ridade kustutamine

Saate muuta ainult kogust või kustutada kontsernisisese müügi- või ostutellimuse rea, kui rida on loodud otse vormilt **Müügitellimus** või **Ostutellimus**. See muutus muudab kas kontsernisisese ostu- või müügi tellimuse read allikaks.

## <a name="origins-of-orders-and-order-lines"></a>Tellimuste päritolud ja tellimuse read

Kontsernisisestel tellimustel ja tellimuste ridadel võib olla üks kahest päritolust:

- **Tuletatud** – tellimus loodi automaatselt ettevõtetevahelisest tellimuste ahelast.
- **Allikas** – tellimus loodi kasutaja poolt käsitsi.

Päritolu näidatakse kontsernisiseste tellimuste ja müügitellimuste tellimuspäises väljal **Päritolu**. See väli asub müügitellimuse kiirkaardil **Kontsernisiseste sätete** ja ostutellimuse **Seadistamise** kiirkaardil.

Päritolu **Tuletatud** ja **Allikas** kehtib ainult kontsernisiseste tellimuste puhul. Seega on kõigi teiste müügitellimuste, ostutellimuste ja tellimuse ridade puhu väli **Allikas** tühi. See väli on tühi ka algsel müügitellimusel.

## <a name="example-derived-origin"></a>Näide: Tuletatud päritolu

Te loote algse müügitellimuse väliskliendile. See müügitellimus sisaldab ühte tellimuse rida. See algne müügitellimus loob kontsernisisese ostutellimuse, mis sisaldab ühte tellimuse rida, mis loob kontsernisisese müügitellimuse, mis sisaldab ühte tellimuse rida. Kontsernisisene ostutellimuse päis ja tellimuse rida luuakse automaatselt algsest müügitellimusest.

Kontsernisisese ostutellimuse **Seadistamise** kiirkaardi välja **Päritolu** väärtus ja kontsernisiseste müügitellimuste päiste **Kontsernisiseste sätete** kiirkaart on **Tuletatud**. Ostutellimuse ja müügitellimuse ridade vahekaardi **Rea üksikasjad** välja **Päritolu** väärtus on samuti **tuletatud**.

Kui tellimuserea päritoluks on **Tuletatud**, ei saa te tellimuse rida otse kustutada. Saate tellimuse rida kustutada ainult allikast, mis lõi tellimuse rea. Samuti saate muuta tellitud kogust ainult allikast, mis lõi tellimuse rea.

Kui algne müügitellimus ja algne müügitellimuse rida on osa kontsernisisesest tellimusahelast, saate muuta tellitud koguseid algselt müügitellimuselt, ja saate kustutada tellimuse read algsest müügitellimusest.

## <a name="example-source-origin"></a>Näide: Allika päritolu

Saate luua ostutellimuse kontsernisisesele hankijale. Kontsernisisesel ostutellimusel ja tellimuse real on mõlemail olek **Allikas**. Seega on see kontsernisisene ostutellimus kontrollija ja automaatselt loodud kontsernisisene müügitellimus hankija kontos on **Tuletatud**.

Lisaks ei saa kontsernisisesel ostutellimusel loodud tellimuserea tellitud koguseid kontsernisisesel müügitellimusel muuta. Tellimuse rea saab kustutada ainult kontsernisisesest ostutellimusest. Kui kontsernisisesele müügitellimusele lisatakse uus rida, on selle kontsernisisese müügitellimuse rea päritoluks **Allikas**.

Kui algne müügitellimus on osa kontsernisisesest tellimusahelast, saate te kontsernisiseseid tellimusi ja kontsernisiseseid tellimuse ridu kontrollida algsest müügitellimusest.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
