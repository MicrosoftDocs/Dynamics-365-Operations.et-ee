---
title: Teatiste ülevaade (sisaldab videot)
description: See artikkel annab teatiste kohta üldist teavet. Teatisi saate kasutada, et olla kursis sündmustega, mida soovite tööpäeva jooksul jälgida.
author: RichdiMSFT
ms.date: 09/04/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: b81eb8e0be4c7d7357a6b8b7b5f0ac025b9ab8ca
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124254"
---
# <a name="alerts-overview"></a>Teatiste ülevaade

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Teatiste kohta
Teatised moodustavad süsteemis kriitiliste sündmuste teadete süsteemi. Teatisi saate kasutada, et olla kursis sündmustega, mida soovite tööpäeva jooksul jälgida. Saate hõlpsalt luua omi teatisereegleid tähtaja ületanud tarnete, kustutatud tellimuste, muutuvate hindade või muude reageerimist nõudvate sündmuste kohta.

Ettevõtte ressursiplaanimises (ERP) on toodud mitmesuguseid tavapäraseid stsenaariumeid, mille puhul teatiste funktsiooni kasutada saab. Järgmisena on toodud mõned näited.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Stsenaarium 1: teatisereegli loomine uute müügitellimuste jaoks

1. Avage leht **Kõik müügitellimused**.
2. Valige toimingupaani vahekaardil **Suvandid** rühmas **Anna ühiskasutusse** valik **Loo kohandatud teatis**.
3. Valige dialoogiboksi **Loo teatisereegel** kiirkaardi **Teavita mind, kui** väljalt **Sündmus** suvand **On loodud uus kirje**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Stsenaarium 2: teatise loomine tarnekuupäeva edasilükkumise kohta

1. Avage leht **Kõik ostutellimused**.
2. Ostutellimus üksikasjade vaatamiseks valige ostutellimuse ID.
3. Laiendage kiirkaarti **Ostutellimuse päis**.
4. Valige toimingupaani vahekaardil **Suvandid** rühmas **Anna ühiskasutusse** valik **Loo kohandatud teatis**.
5. Valige dialoogiboksi **Loo teatisereegel** kiirkaardi **Teavita mind, kui** väljalt **Väli** suvand **Tarnekuupäev**.
6. Valige väljal **Sündmus** suvand **on edasi lükatud**.
    
Pärast dialoogiboksi **Loo teatisereegel** sulgemist kuvatakse teie reegel lehel **Halda teatisereegleid**. Lehte **Halda teatisereegleid** saab kasutada olemasolevate teatisereeglite värskendamiseks. Näiteks saab muuta sündmuse käivitajaid, värskendada sündmuse teatiseid ja aegumiskuupäevi. Lehe **Halda teatisereegleid** avamiseks kasutage toimingupaani vahekaardi **Suvandid** nuppu **Teavita mind**.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Mis toimub teatisereegli loomisel?

Teatisereeglite loomisel saate eelmääratletud sündmuse konkreetse väljaga seostada. Näiteks, kui väljal määratud kuupäev saabub või välja sisu muutub. Teise võimalusena saate sündmuse seostada kindlal leheküljel olevate kirjetega. Näiteks kirje loomisel või kustutamisel.

Kui valitud sündmus toimub välja puhul või lehel oleva kirje puhul, saadetakse teile teatis. Näiteks loote reegli, mille konkreetse ostutellimuse rea välja **Tarnekuupäev** seostate sündmusega **tähtajast on möödas**. Määrate ajavahemikuks viis päeva. Sel juhul saadetakse teatis viis päeva pärast ostutellimuse rea tarnekuupäeva.

Lisaks saate teatisereegleid tingimuste seadistamisega täpsustada. Näiteks võite saada teatiseid konkreetse hankija kontode jaoks loodud uute ostutellimuste kohta.

## <a name="preparing-for-an-alert"></a>Teatise ettevalmistamine

Enne teatisreegli loomist otsustage, millal või milliste olukordades te teatisi saada soovite. Teades, millise sündmuse kohta te teatist soovite, saate otsida lehe, millel kuvatakse teatist käivitava sündmuse andmed. Sündmuseks võib olla saabuv kuupäev või teatud toimuv muudatus. Seega peate leidma lehe, kus kuvatakse kas määratud kuupäev, muudetud väli või uus loodud kirje. Alles seda teades saate luua teatisereegli.

## <a name="components-of-an-alert-rule"></a>Teatisereegli osad

Teatisereegel koosneb viiest osast.

- **Sündmus** – teatisereeglit käivitav sündmus saab olla kas saabuv kuupäev või teatud toimuv muudatus. Sündmused saate määrata dialoogiboksi **Loo teatise reegel** kiirkaardil **Töö oleku muudatuste kohta meiliteatiste saatmine**.
- **Tingimus** – dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisel juhul** saate valida tingimuse ulatuse, kontrollimaks, millal teid sündmustest teavitatakse. Saate reeglit rakendada kas ainult praegusele kirjele või kõigile lehel nähtavatele kirjetele. Kui reegel on juriidiliste isikute ülene, määrake suvandi **Organisatsiooniülene** väärtuseks **Jah**.
- **Reegli aegumine** – dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind kuni** saate määrata, kui kaua teatisereegel aktiivne peaks olema.
- **Sisu** – dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisega** saate määrata teema ja sõnumi teksti, mida teatiste puhul peaks kasutatama.
- **Kasutaja** – dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavitatav** saate määrata, milline kasutaja peaks teatiseid saama. Vaikimisi on valitud teie kasutaja ID.

    > [!NOTE]
    > See valik on piiratud organisatsiooni administraatoritele.

## <a name="videos"></a>Videod

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>Kuidas kasutada teatisi filtreeritud andmete jälgimiseks

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

Teatiste [kasutamine filtreeritud andme video jälgimiseks](https://youtu.be/ZYKMcv6kl9s) (vt ülal kuvatud) [sisaldub finantsis ja toimingutes, mille](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) kohta on saadaval YouTube.

### <a name="alert-rule-options"></a>Teatise reegli valikud

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

Teatisereegli [valikute](https://youtu.be/cpzimwOjicM) video (vt ülalpool) on kaasatud saadaolevasse [finantside ja toimingute](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sse YouTube.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
