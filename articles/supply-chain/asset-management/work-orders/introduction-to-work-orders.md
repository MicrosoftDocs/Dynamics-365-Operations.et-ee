---
title: Töökäskude tutvustus
description: Selles teemas käsitletakse varahalduse töökäske.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875617"
---
# <a name="introduction-to-work-orders"></a>Töökäskude tutvustus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Töökäskudega hallatakse hooldustööde mahtu, esitatakse selle jaoks nõutavat teavet ja registreeritakse see. Töökäsk võib sisaldada vähemalt üht tööd ja sellega saab ühendada vähemalt üht vara. Iga töökäsu rida määratleb varas ajastatud hooldustööd.

Töökäske saab luua käsitsi või automaatselt:

- Määrake kalendripõhised hoolduskavad automaatselt ankeediga **Ajasta hoolduskava** valikule „Automaatne loomine“.  

- Määrake hoolduskorrad automaatselt ankeediga **Ajasta hoolduskord** valikule „Automaatne loomine“.  

- Loo hooldusgraafiku alusel, milleks võivad olla ennetavad hooldustööd või hooldusnõuded.  

- Looge töökäsk käsitsi.  

- Looge töökäsk järgmiste valikute seast: **Kõik hooldusnõuded** või **Aktiivsed hooldusnõuded** või **Minu töö asukoha hooldusnõuded**.

>[!NOTE]
>Sama varaga seotud töökäsu tööd seostuvad sama projekti ID-ga.

## <a name="all-work-orders"></a>Kõik töökäsud

Loendi avamiseks klõpsake **Varahaldus** > **Ühine** > **Töökäsud** > **Kõik töökäsud**. **Kõik töökäsud** sisaldab loendit kõikidest töökäskudest ja näitab nende kohta veidi teavet.

![Joonis 1](media/01-work-orders.png)

- Aktiivsete töökäskude loendi nägemiseks klõpsake **Varahaldus** > **Ühine** > **Töökäsud** > **Aktiivsed töökäsud**.

- Töö asukohtadesse paigaldatud varasid sisaldava töökäsu tööde loendi nägemiseks klõpsake **Varahaldus** > **Ühine** > **Töökäsud** > **Minu töö asukoha töökäsu hooldustööd**. Teisse suhtutakse kui töölisesse (seadistatud jaotises [Hooldustöötajad ja töörühmad](../setup-for-objects/workers-and-worker-groups.md)).

- Valitud kande andmete nägemiseks klõpsake loendi **Kõik töökäsud** (andmeruudustiku vaates) veerus **Töökäsk** linki. Muutmiseks klõpsake nuppu **Redigeeri**.  

- Andmete vaates näete töökäsuga seotud üksikasjalikku teavet.  

- Töökäsu töö andmete nägemiseks valige andmete vaates linki **Read** või töökäsu andmete nägemiseks valige link **Päis**.  

- Ekraani paremal pool asuv vertikaalne paan **Seotud teave** sisaldab täiendavat töökäsu alast teavet. Valitud töökäsu asjakohase teabe nägemiseks laiendage paan.  


![Joonis 2](media/02-work-orders.png)


Toimingupaani nupud on paigutatud vahekaartidesse. Siin on Enterprise Asset Managementiga seotud nuppude lühikirjeldus:



| Nupu nimi                     | Kirjeldus                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redigeerimine                            | Muuda valitud töökäsku.                                                                                                                                                                                                                                           |
| Uus                             | Loo uus töökäsk.                                                                                                                                                                                                                                                  |
| Kustutusklahv DELETE                          | Kustuta valitud töökäsk.                                                                                                                                                                                                                                         |
| Töökäsu kaust                 | Lisa valitud töökäsk kausta või eemalda see sealt.                                                                                                                                                                                           |
| Korrigeeri                          | Muuda valitud töökäskude järgmist teavet: eeldatav algus ja lõpp, teenuse tase, vastutav hooldustöötaja või vastutava hooldustöötaja rühm.                                                                                                                                     |
| Seotud töökäsk              | Loo valitud töökäsu tööga seotud uus töökäsk. See on kasulik esmaste ja teisejärguliste töökäskude registreerimise puhul.                                                                                                                              |
| Töökäsu kopeerimine                 | Loo uus töökäsk vastavalt olemasolevale töökäsule.                                                                                                                                                                                                                |
| Sündmuse ajalugu                   | Vt töökäsu registreerimisajalugu.                                                                                                                                                                                                                |
| Töökäsu hooldustöö märkmed                           | Kirjeldage töökäsku või sisestage sellele märkmeid või märkusi. Märkmele ajatempli ja kasutajanime lisamiseks klõpsake nuppu **Lisa ajatempel**. Märkmed asuvad ankeedi **Töökäsud** > FastTabi **Rea andmed** > vahekaardil **Kirjeldus**. |
| Tööriistad                           | Looge töökäsu jaoks vajalike tööriistade loend. Tööriistad on seadistatud ressurssidena kohas **Organisatsiooni haldus** > **Ühine** > **Ressursid** > **Ressursid**.                                                                                                      |
| Hoolduse kontrollnimekiri           | Vaadake töökäsuga ühendatud vara kontroll-loendit.                                                                                                                                                                                                              |
| Vara tõrge                     | Vaadake või registreerige tõrke haldamisel kasutatav vara tõrke teave.                                                                                                                                                                                        |
| Hoolduskatkestus            | Täpsustage töökäsu hoolduskatkestus.                                                                                                                                                                                                                               |
| Tingimuse hindamine            | Registreerige töökäsu tingimuse hinnangu nõuded.                                                                                                                                                                                                             |
| Varaloendurid                 | Looge vara loenduri registreeringud või vaadake neid.                                                                                                                                                                                                                     |
| Eelarve                        | Vaadake või looge töökäsu ennustusi.                                                                                                                                                                                                                               |
| Töölehed                        | Vaadake või looge töökäsu päevikuid. Päeviku ridu saab kopeerida ennustustest.                                                                                                                                                                                         |
| Projekti kanded            | Vaadake kõiki vara jaoks loodud töökäskudega seotud postitatud tehinguid.                                                                                                                                                                                             |
| Töökäsu oleku värskendamine                | Töökäsu tsükli oleku värskendamine.                                                                                                                                                                                                                                                |
| Töötsükli oleku logi                       | Valitud töökäsu tsükli olekuid näitav logi.                                                                                                                                                                                                                   |
| Vara dokumendid                | Vaata töökäsuga seotud varadele manustatud dokumentide loendit. Need dokumendid asuvad kohas **Varahaldus** > **Seadistus** > **Vara dokumendid**.                                                                                                 |
| Planeeri                        | Ajasta valitud töökäsud.                                                                                                                                                                                                                                      |
| Lähetus            | Ajasta ühe töötaja valitud töökäsud.                                                                                                                                                                                                                        |
| Graafiku kustutamine                 | Kustuta valitud töökäsu graafik.                                                                                                                                                                                                                          |
| Ajastatud töökäsu hooldustööd             | Avage leht **Ajastatud töökäsu hooldustööde** nimekiri.                                                                                                                                                                                                                             |
| Töökäsu ostutaotlus | Avage lehel loend **Töökäsu ostu tingimus**.                                                                                                                                                                                                                 |
| Töökäsu ost             | Avage lehel loend **Töökäsu ost**.                                                                                                                                                                                                                             |
| Kulude jälitamine                    | Võrrelge töökäsu eelarve kulusid ja tegelikke kulusid.                                                                                                                                                                                                                |
| Tunnijuhtimine                    | Võrrelge töökäsu eeldatavaid tunde ja tegelikke tunde.                                                                                                                                                                                                                |
| Töökäsu aruanne               | Printige töökäsu aruanne.                                                                                                                                                                                                                                                |
| Töökäsu tarbimine          | Printige kasutuse aruanne.                                                                                                                                                                                                                                               |


Vahekaardi **Töökäsk** > rühma **Projekt** nupud viitavad ennustamise, päevikute ja arveldamise mooduli **Projekti haldus ja raamatupidamine** funktsioonidele.

>[!NOTE]
>Töökäsus loodud ennustusi saab kaasata, kui käivitatakse põhiajastamine. Selleks kasutage ankeedis **Varahalduse näitajad** valitud ennustusmudelit.

