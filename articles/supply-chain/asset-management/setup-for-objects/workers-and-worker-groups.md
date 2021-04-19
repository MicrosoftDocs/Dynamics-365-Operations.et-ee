---
title: Hooldustöötajad ja töötajate rühmad
description: Selles teemas selgitatakse hooldustöötajaid ja töötajate rühmi varahalduses.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553dce8df5e91cce58b64e340d8ff72586d8d46d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838558"
---
# <a name="maintenance-workers-and-worker-groups"></a>Hooldustöötajad ja töötajate rühmad

[!include [banner](../../includes/banner.md)]

 

Selles teemas selgitatakse hooldustöötajaid ja töötajate rühmi varahalduses. Varahalduses saate ühendada hooldustöötajaid funktsionaalsete asukohtadega. (Lisateavet funktsionaalsete asukohtade kohta leiate jaotisest [Funktsionaalsete asukohtade loomine](../functional-locations/create-functional-locations.md).)See funktsioon võib olla kasulik, kui näiteks plaanite hooldustöid masinas, mis asub funktsionaalses asukohas 01 ja soovite selle töö jaoks eraldada samast asukohast hooldustöötajad.

Saate luua ka hooldustöötajate rühmi ja seostada nendega hooldustöötajaid. See funktsioon on kasulik siis, kui teete lihtsat töökäsu planeerimist ja soovite planeerida töökäsule hooldustöötajate rühma. Võite kasutada hooldustöötajaid ja hooldustöötajate rühmi eelistatud hooldustöötajate ja vastutavate hooldustöötajate seadistamiseks. 


## <a name="create-workers"></a>Töötajate loomine

1. Valige **Varahaldus**\>**Häälestus**\>**Töötajad**\>**Töötajad**.
2. Töötaja loendisse lisamiseks valige **Uus**.
3. Valige töötaja väljal **Töötaja**.
4. Seadistage suvand **Aktiivne** olekusse **Jah**, et planeerida töötaja töökäskudele.

    Kiirkaardil **Üldine** täidetakse väljad **Ressurss** ja **Kirjeldus** automaatselt, kui töötajale on ressurss valitud. Väli **Kalender** täidetakse samuti automaatselt, kui olete töötaja ressursina seadistanud ja sellele ressursile lehel **Ressursid** kalendri eraldanud (**Organisatsiooni haldamine**\>**Ressursid**\>**Ressursid**).

5. Valige kiirkaardil **Rühmad** suvand **Lisa** ja seejärel valige töötajale hooldustöötajate rühm. Töötaja võib olla seotud rohkem kui ühe rühmaga.
6. Tavapärase häälestuse korral hakkab töötaja seotus rühmaga kehtima kuupäevast, millal te rühma lisate, ja see ei aegu kunagi. See kuupäev on näidatud väljal **Tõhus**. Välja **Tõhus** nägemiseks valige **Kuva**\>**kõik**. Kui töötaja seotus rühmaga peaks piirduma konkreetse ajaperioodiga, kasutage perioodi määramiseks välju **Tõhus** ja **Aegumine**.
7. Valige kiirkaardil **Funktsionaalsed asukohad** suvand **Lisa** ja seejärel vali hooldustöötajale funktsionaalne asukoht. Määratlege ka see, milline asukoht on töötaja peamine funktsionaalne asukoht.

    > [!NOTE]
    > Kui lisate töötajale funktsionaalseid asukohti, kuvatakse kõiki nende funktsionaalsete asukohtadega seotud aktiivseid varasid mitmetes menüü-üksustes, nagu näiteks **Minu aktiivsed varad** ja **Minu aktiivsed funktsionaalsed asukohad**. Neid kuvatakse ka varade otsingutes, mida kuvatakse siis, kui loote uue vara, hooldustaotluse või töökäsu.

    Väljad kiirkaardil **Üksikasjad** näitavad mitmeid hooldustöötajate rühmi ja funktsionaalseid asukohti, millega valitud hooldustöötajad seotud on.

## <a name="create-worker-groups"></a>Töötajate rühmade loomine

1. Valige **Varahaldus**\>**Häälestus**\>**Töötajad**\>**Hooldustöötajate rühmad**.
2. Töötajate rühma loendisse lisamiseks valige **Uus**.
3. Sisestage väljale **Hooldustöötajate rühm** rühma ID.
4. Väljale **Nimi** sisestage nimi.
5. Valige kiirkaardil **Töötajad** suvand **Lisa** ja seejärel valige töötajate rühmale hooldustöötaja. Lisainfot väljade **Tõhus** ja **Aegumine** kohta leiate eelneva protseduuri 6. etapist.
6. Kui valitud hooldustöötajate rühmaga peaks olema seotud ressursirühm, valige **Kopeeri ressursirühmast**. Väljal **Rühjm** valige ressursirühm kalendri sätete kopeerimiseks. Seejärel valige väljal **Töötajate rühm** töötajate rühm ressursirühma kalendri sätete kopeerimiseks. See etapp on asjakohane ainult siis, kui soovite, et hooldustöötajad kasutaksid töökäsu plaanimisel ressursiga (töökeskus) seotud kalendrit.

    Kiirkaart **Üksikasjad** kuvab nende hooldustöötajate arvu, kes on määratud valitud hooldustöötajate rühma.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]