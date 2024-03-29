---
title: Vöötkoodi maskide seadistamine
description: See artikkel kirjeldab, kuidas seadistada vöötkoodi maski tähemärke, vöötkoodi maske ja vöötkoodi maske vöötkoodidele määrata.
author: BrianShook
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 97b490384cff27c60191a87dc623eb6a2ef868f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853708"
---
# <a name="set-up-bar-code-masks"></a>Vöötkoodi maskide seadistamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada vöötkoodi maski tähemärke, vöötkoodi maske ja vöötkoodi maske vöötkoodidele määrata.

## <a name="set-up-bar-code-mask-characters"></a>Vöötkoodi maski tähemärkide häälestamine

Vöötkoodimaske kasutatakse vöötkoodide loomiseks ja kassas skannitavate vöötkoodide kiiresti tuvastamiseks. Maskid koosnevad kohatäidetena toimivatest märkidest, mis näitavad loodavate vöötkoodide vormingut. Vöötkoodi maski konfigureerimiseks peate seadistama vöötkoodi maski tähemärgid. Valige **Jaemüük ja kaubandus** &gt; **Varude haldus** &gt; **Vöötkoodid ja sildid** &gt; **Maski märgid**. Klõpsake vöötkoodi maski märkide loomiseks nuppu **Uus**. Maski tähemärke saab luua järgmiste vöötkoodi andmete näitamiseks.

| Väli            | Kirjeldus |
|------------------|-------------|
| Toode          | Toote ID kohatäide. |
| Mis tahes number       | Kasutatakse, et määrata number, mis on vöötkoodidesse püsiprogrammeeritud. |
| Kontrollnumber      | Näitab, et vöötkoodi vorming vöötkoodi maskis kasutab vöötkoodi kehtivuse kinnitamiseks kontrollnumbrit. |
| Suuruse numbrikoht       | Näitab suurust vöötkoodis, mis luuakse suurust hõlmava tootevariandi jaoks. |
| Värvi numbrikoht      | Näitab vöötkoodis värvi, mis on loodud värvi sisaldava tootevariandi jaoks. |
| Laadi numbrikoht      | Näitab vöötkoodis laadi, mis on loodud laadi sisaldava tootevariandi jaoks. |
| EAN-i litsentsi kood | Kohatäide EAN-i litsentsikoodi jaoks väljastatud EAN-i litsentsile. |
| Hind            | Näitab hinda hinda sisaldavate vöötkoodide puhul. |
| Kogus         | Näitab kogust kogust / juhuslikku kaalu sisaldavates vöötkoodides. |
| Töötaja         | Näitab vöötkoodi segmenti vöötkoodi kassa sisselogimise puhul kasutatava töötaja ID-koodi puhul. |
| Klient         | Näitab kliendi ID segmenti. |
| Andmekirje       | *Pole veel rakendatud.* |
| Allahindluse kood    | *Aegunud* alates Dynamics 365 for Retaili 2017. aasta kevade väljalaskest. Varem: näitab allahindluse koodi vöötkoodile, mida kasutatakse kassa kandele allahindluse lisamiseks. |
| Kupongikood      | Näitab tellimusele allahindluse lisamiseks kasutatava vöötkoodi kupongikoodi. See asendas allahindluse koodi. |
| Kinkekaart        | Näitab kinkekaardi väljastamisel või sellega tasumisel kinkekaardi numbrit. |
| Kliendikaart     | Lisab kandele püsikliendi ja seda saab kasutada kliendikaardiga tasumisel. |

## <a name="define-bar-code-masks"></a>Vöötkoodi maskide määratlemine

Pärast vajalikele vöötkoodi maskidele vöötkoodi maski tähemärkide määramist, valige **Jaemüük ja kaubandus** &gt; **Varude haldus** &gt; **Vöötkoodid ja sildid** &gt; **Vöötkoodi maski seadistus**. Sellel lehel saate määratleda vöötkoodi maskid, mis kasutavad varasemalt määratud tähemärke. Neid vöötkoodi maske kasutatakse vöötkoodide loomisel ja need aitavad ka kassas skannitud vöötkoode tuvastada.

1. Klõpsake uue vöötkoodi maski loomiseks nuppu **Uus**.
2. Sisestage väärtused väljadele **Maski ID** ja **Kirjeldus** ja valige seejärel väljal **Tüüp** vöötkoodi maski tüüp.
3. Jaotises **Üldine** valige väärtus väljal **Vöötkoodi standard** ja määrake seejärel vöötkoodi prefiks, kui see on vajalik.
4. Jaotises **Vöötkoodi maski segment** lisage vöötkoodi segmendid, mida kasutatakse loodavas vöötkoodis.

Näiteks vöötkoodi maski loomiseks maski ID-ga „Toode” teete järgmist.

1. Looge uus vöötkoodi mask ja valige tüüp „Toode”.
2. Valige vöötkoodi standard, näiteks „Kood 39”.
3. Sisestage prefiks, mida kasutatakse vöötkoodi hõlpsaks tuvastamiseks. Näiteks „22”.
4. Lisage maski segment. Valitakse maski segment „Toode”.
5. Sisestage tootesegmendi pikkus, näiteks „10”. Pikkus peaks vastama kaupluses tavaliselt kasutatava toote ID pikkusele. Mask kuvatakse eelvaatena jaotise **Mask** jaotises **Üldine**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Vöötkoodidele vöötkoodi maskide määramine

Vöötkoodi maskid tuleb enne nende kasutamist vöötkoodidele määrata. Jätkates eelmise näitega, vöötkoodi maski määramiseks vöötkoodile tehke järgmist.

1. Valige **Organisatsiooni haldus** &gt; **Seadistus** &gt; **Vöötkoodid**. Uue vöötkoodi loomiseks klõpsake nuppu **Uus**.
2. Sisestage väärtused väljadele **Vöötkoodi** **seadistus** ja **Seeadistus**.
3. Jaotises **Üldine** väljal **Vöötkoodi tüüp** valige „Kood 39”. Väljal **Maski** **ID** valige varasemalt loodud mask „Toode”.
4. Jaotisesse **Suurus** sisestage „12”.
5. Klõpsake nuppu **Salvesta**.

Vöötkoodi maski saab nüüd kasutada toodete jaoks vöötkoodide loomiseks. Eespool toodud juhised on näited selle kohta, kuidas toodete jaoks vöötkoodi maske luua, kuid need näitlikustavad ka seda, kuidas luua vöötkoodi maske mis tahes muude toetatud vöötkoodi tüüpide jaoks. Vöötkoodi maske, tüüpe ja pikkuseid tuleb korrigeerida teie konkreetses keskkonnas kasutamiseks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]