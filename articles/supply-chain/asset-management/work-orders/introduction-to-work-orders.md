---
title: Töökäskude tutvustus
description: Selles teemas käsitletakse varahalduse töökäske.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e9890057ab852a7fb0d60056bb102ce15ac124e2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263730"
---
# <a name="introduction-to-work-orders"></a>Töökäskude tutvustus

[!include [banner](../../includes/banner.md)]



Töökäske kasutatakse hooldustööde haldamiseks, nende jaoks nõutava teabe esitamiseks ja nende tarbimise registreerimiseks. Iga töökäsk võib sisaldada vähemalt üht tööd ja iga töökäsuga saab ühendada vähemalt üht vara. Iga töökäsu töö määratleb varas ajastatud hooldustöö.

Töökäske saab luua järgmistel viisidel.

- Kalendripõhistele hoolduskavadele, mille säte „Automaatne loomine“ on sisse lülitatud automaatselt valikuga [Hoolduskavade ajastamine](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md).

- Hoolduskordadele, mille säte „Automaatne loomine“ on sisse lülitatud automaatselt valikuga [Hoolduskordade ajastamine](../preventive-and-reactive-maintenance/maintenance-rounds.md).

- Ennetavate hooldustööde või hooldusnõuete jaoks jaotisest [Hooldusgraafik](../preventive-and-reactive-maintenance/maintenance-schedule.md).

- Käsitsi

- Lehelt **Kõik hooldusnõuded**, **Aktiivsed hooldusnõuded** või **Minu töö asukoha hooldusnõuded**.

>[!NOTE]
>Sama varaga seotud töökäsu tööd seostuvad sama projekti ID-ga.

## <a name="all-work-orders"></a>Kõik töökäsud

Loendilehe **Kõik töökäsud** avamiseks valige **Varahaldus** > **Ühine** > **Töökäsud** > **Kõik töökäsud**. Sellel lehel kuvatakse kõik töökäsud ja osa iga töökäsuga seotud teabest.

Alloleval joonisel kuvatakse loendilehe **Kõik töökäsud** näide.

![Joonis 1](media/01-work-orders.png)

Ainult aktiivsete töökäskude loendi nägemiseks valige **Varahaldus** > **Ühine** > **Töökäsud** > **Aktiivsed töökäsud**. 

Teie, kui töötjaga seotud töö asukohtadesse paigaldatud varasid sisaldava töökäsu tööde loendi vaatamiseks valige **Varahaldus** > **Ühine** > **Töökäsud** > **Minu töö asukoha töökäsu hooldustööd**. (Töötajate ja töö asukoha vaheline seos on seadistatud lehel **Töötajad**. Lisateavet lugege teemast [Hooldustöötajad ja töötajate grupid](../setup-for-objects/workers-and-worker-groups.md).)

Siin on mõned viisid, kuidas kasutada lehte **Kõik töökäsud**.

- Valige tabelivaates link veerus **Work order**, et vaadata valitud kirje üksikasjade vaadet. Seejärel saate kirje redigeerimiseks avada valiku **Redigeeri**.

- Üksikasjade vaates näete töökäsuga seotud üksikasjalikku teavet.  

- Töökäsu töö üksikasjade vaatamiseks valige üksikasjade vaates vahekaart **Read** või töökäsu üksikasjade vaatamiseks valige vahekaart **Päis**.  

- Laiendage lehe paremal pool paani **Seostuv teave**, et vaadata valitud töökäsuga seotud lisateavet.

Alloleval joonisel kuvatakse üksikasjade vaate **Kõik töökäsud** näide.

![Joonis 2](media/02-work-orders.png)


Tegumiriba nupud on korraldatud vahekaartidel. Järgmises tabelis kirjeldatakse lühidalt mooduli Asse Management nuppe.



| Nupu nimi                     | Kirjeldus                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redigeerimine                            | Muuda valitud töökäsku.                                                                                                                                                                                                                                           |
| Uus                             | Loo uus töökäsk.                                                                                                                                                                                                                                                  |
| Kustutusklahv Delete                          | Kustuta valitud töökäsk.                                                                                                                                                                                                                                         |
| Töökäsu kaust                 | Lisage valitud töökäsk töökäskude kausta või eemaldage see sealt.                                                                                                                                                                                           |
| Korrigeeri                          | Muuda valitud töökäskude järgmist teavet: eeldatav algus ja lõpp, teenuse tase, vastutav hooldustöötaja või vastutava hooldustöötaja rühm.                                                                                                                                     |
| Seotud töökäsk              | Loo valitud töökäsu tööga seotud uus töökäsk. See on kasulik esmaste ja teisejärguliste töökäskude registreerimise puhul.                                                                                                                              |
| Töökäsu kopeerimine                 | Looge olemasoleva töökäsu põhjal uus töökäsk.                                                                                                                                                                                                               |
| Sündmuse ajalugu                   | Vaadake töökäsu registreerimisajalugu.                                                                                                                                                                                                                |
| Töökäsu hooldustöö märkmed                           | Looge töökäsu kirjeldus või sisestage selle kohta märkmeid või märkusi. Märkmele kasutajanime ja ajatempli lisamiseks valige esmalt **Lisa ajatempel**. Märkused kuvatakse vahekaardi **Kirjeldus** lehe **Töökäsk** kiirkaardil **Rea üksikasjad**.         |
| Tööriistad                           | Looge töökäsu jaoks vajalike tööriistade loend. Tööriistad on seadistatud ressurssidena kohas **Organisatsiooni haldus** > **Ressursid** > **Ressursid**.                                                                                                      |
| Hoolduse kontrollnimekiri           | Vaadake töökäsuga ühendatud vara kontroll-loendit.                                                                                                                                                                                                              |
| Vara tõrge                     | Vaadake või registreerige vara tõrke teave. Teavet kasutatakse tõrgete halduseks.                                                                                                                                                                                      |
| Hoolduskatkestus            | Täpsustage töökäsu hoolduskatkestus.                                                                                                                                                                                                                               |
| Tingimuse hindamine            | Registreerige töökäsu tingimuse hinnangu nõuded.                                                                                                                                                                                                             |
| Varaloendurid                 | Looge vara loenduri registreeringud või vaadake neid.                                                                                                                                                                                                                     |
| Eelarve                        | Vaadake või looge töökäsu ennustusi.                                                                                                                                                                                                                               |
| Töölehed                        | Vaadake või looge töökäsu päevikuid. Päeviku ridu saab kopeerida ennustustest.                                                                                                                                                                                         |
| Projekti kanded            | Vaadake kõiki vara jaoks loodud töökäskudega seotud postitatud tehinguid.                                                                                                                                                                                             |
| Töökäsu oleku värskendamine           | Töökäsu tsükli oleku värskendamine.                                                                                                                                                                                                                                                |
| Töötsükli oleku logi                      | Vaadake logi, mis näitab valitud töökäsu töötsüklite olekuid.                                                                                                                                                                                                                   |
| Vara dokumendid                | Vaadake töökäsuga seotud varadele manustatud dokumentide loendit. Need dokumendid asuvad kohas **Varahaldus** > **Seadistus** > **Vara dokumendid**.                                                                                                 |
| Planeeri                        | Ajasta valitud töökäsud.                                                                                                                                                                                                                                      |
| Lähetus            | Ajasta ühe töötaja valitud töökäsud.                                                                                                                                                                                                                        |
| Graafiku kustutamine                 | Kustutage valitud töökäsu graafik.                                                                                                                                                                                                                          |
| Planeeritud töökäsu hooldustööd             | Avage leht **Ajastatud töökäsu hooldustööde** nimekiri.                                                                                                                                                                                                                             |
| Töökäsu ostutaotlus | Avage lehel loend **Töökäsu ostu tingimus**.                                                                                                                                                                                                                 |
| Töökäsu ost             | Avage lehel loend **Töökäsu ost**.                                                                                                                                                                                                                             |
| Kulude jälitamine                    | Võrrelge töökäsu eelarve kulusid ja tegelikke kulusid.                                                                                                                                                                                                                |
| Tunnijuhtimine                    | Võrrelge töökäsu eeldatavaid tunde ja tegelikke tunde.                                                                                                                                                                                                                |
| Töökäsu aruanne               | Printige töökäsu aruanne.                                                                                                                                                                                                                                                |
| Töökäsu tarbimine          | Printige kasutuse aruanne.                                                                                                                                                                                                                                               |


Jaotise **Projekt** nupud tegumiriba vahekaardil **Töökäsk** tab on seotud prognooside, päevikute ja arveldamise funktsioonidega moodulis **Projektihaldus- ja arvestus**.

>[!NOTE]
>Töökäsus loodud ennustuste kaasamiseks, kui käivitatakse põhiajastamine kasutage ankeedis **Varahalduse näitajad** valitud ennustusmudelit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]