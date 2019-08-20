---
title: Ostutellimusel põhinevate varade loomine
description: Selles teemas selgitatakse, kuidas luua vara üksuste loendit, mida saab kasutada varade loomisel hooldustööde jaoks varahalduses.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 536795ac8ac164a6cc16e9ba22b0aa7bf30ddfd8
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783223"
---
# <a name="create-assets-based-on-purchase-orders"></a>Ostutellimusel põhinevate varade loomine

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Selles teemas selgitatakse, kuidas luua vara üksuste loendit, mida saab kasutada varade loomisel hooldustööde jaoks varahalduses. Vara üksuste põhjal saate vaadata nende kaupade kohta loodud ostutellimuse ridade loendit. Selle funktsiooni eesmärk on hõlpsalt luua ostutellimusel põhinev vara varahalduses.

Esmalt saate seadistada kaubad, mida kasutatakse varade loomisel ostutellimuse põhjal suvandis **Kaubagrupid**. Pärast ostutellimuse rea loomist saate luua varad suvandis **Ootel varad**. Teil on võimalik otsustada, millises ostutellimuse etapis vara luuakse.


## <a name="select-asset-items"></a>Kaubagrupi valimine

1. Klõpsake **Varahaldus** > **Häälestus** > **Varad** > **Kaubad**.
2. Klõpsake suvandit **Uus**, et luua uus vara üksus.
3. Valige kaup väljal **Kaubakood**. Kui lahkute sellelt väljalt, sisestatakse kauba nimi automaatselt väljale **Toote nimetus**.
4. Kiirkaardil **Üldine** valige kauba jaoks vara tüüp.
5. Valige kauba jaoks vara tootja ja mudel.
6. Salvestage kaup.


## <a name="create-assets-from-pending-assets"></a>Varade loomine ootel varadest

1. Klõpsake**Varahaldus** > **Ühised** > **Varad** > **Ootel varad**.
2. Näete ostutellimuste värskendatud loendit, mis põhineb üksuses **Kaubagrupid** valitud kaupadel.
3. Saate filtreerida ostutellimuste olekut, et valida, millises elutsükli olekus vara tuleks luua. Näiteks võite luua varasid ainult siis, kui toote sissetulek on ostutellimusel sisestatud.
4. Valige ostutellimuse real link **Viitenumber**, et nähe kauba kohta üksikasjalikku teavet.
5. Kui soovite redigeerida, milliseid dimensioone kuvatakse kiirkaardil **Laoseisu dimensioonid**, klõpsake nuppu **Kuva dimensioonid** ja tehke oma valikud.
6. Kui soovite luua ostutellimuse real põhineva vara, märkige loendilehe veeru märkeruut **Märge** ja klõpsake nuppu **Loo varad**. Kuvatakse sõnum, mis teavitab teid vara ID-st.
7. Valige vara varade loendist **Kõik varad** ja klõpsake nuppu **Redigeeri**, et lisada vara kohta rohkem teavet.
8. Kui soovite suvandis **Ootel varad** rea kustutada, kuna te ei soovi vara luua, märkige selle rea veerus märkeruut **Märge** ja klõpsake **Hülga ootel varad**. Kuvatakse sõnum, mis teavitab teid vara ID-st. Te ei kustuta ostutellimust ega müügitellimust, vaid kirje, mille põhjal te oleksite saanud luua vara **varahalduses**.

>[!NOTE]
>Kõik tootedimensioonid (suurus, värv, konfiguratsioon jne) edastatakse automaatselt vara atribuutides. Jälgimisdimensioonid (seerianumber) talletatakse vara loomisel otse vara juures.


## <a name="find-pending-assets"></a>Leia ootel varad

Ootel varade kontrollimiseks käivitage **Ootel varade loendus**. Näiteks saab seda funktsiooni kasutada teatise vastuvõtmiseks iga kord, kui ootel vara on vara loomiseks valmis.

1. Klõpsake **Varahaldus** > **Perioodiline** > **Varad** > **Ootel varade loendamine**.
2. Klõpsake nuppu **OK** töö käivitamiseks ja loendi uuendamiseks suvandis **Ootel varad**.
3. Selle töö saate seadistada pakett-tööna, nt üks kord päevas.

**Ettevaatust:** kui andmeid muudetakse ostutellimusel *pärast* seda, kui olete loonud seotud kauba põhjal vara, ei kajastu need muudatused varas.
