---
title: Hangete töövood
description: Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas. Kinnitamisprotsessi seadistamiseks saate luua töövoo.
author: GalynaFedorova
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebfd96690eea762d0797db1b485544d957d17ce0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671922"
---
# <a name="procurement-and-sourcing-workflows"></a>Hangete töövood

[!include [banner](../includes/banner.md)]

Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas. Kinnitamisprotsessi seadistamiseks saate luua töövoo.

Töövoog esindab äriprotsessi. Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama. Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.

- **Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded. Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.
- **Protsessi nähtavus** — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu. See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.
- **Tööde koondloend** – kasutajad saavad vaadata tööde koondloendit, et näha neile määratud töövoo ülesandeid ja kinnitusi kõigis töövoogudes, milles nad osalevad. See on saadaval lehel Tööüksused.

## <a name="the-types-of-workflows-that-you-can-create"></a> Loodavate töövoogude tüübid

Jaotises Hanked on saadaval järgmised töövootüübid.

| Tüüp | Kasutage seda tüüpi järgmiseks |
|---|---|
| Ostutaotluse ülevaade | Saate luua ostutaotluste jaoks ülevaatuse ja kinnitamise töövood. |
| Ostutaotluse rea eelvaade | Saate luua ostutaotluse ridade jaoks ülevaatuse ja kinnitamise töövood. |
| Ostutellimuse töövoog | Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuste jaoks. |
| Ostutellimuse rea töövoog | Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuse ridade jaoks. |
| Hankija lisamise rakenduse töövoog | Saate luua ülevaatuse ja kinnitamise töövood uute hankijate lisamiseks hankija nõuete kaudu. |

> [!IMPORTANT]
> Uue töövoo lisamisel võidakse kuvada ka järgmised iganenud töövood, mis on loetletud dialoogiboksis **Töövoo loomine**. Need on seotud *vastuvõtukinnituse* funktsiooniga, mis oli saadaval teenuses [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), aga mis on nüüd iganenud. Neid töövooge praegu ei toetata.
> 
> - Tarnetähtaja teate töövoog
> - Arve saamise teatise töövoog
> - Toote sissetuleku nurjunud teatise töövoog
> - Kinnitamata toote sissetuleku tagasilükkamise teatise töövoog

## <a name="creating-a-workflow"></a>Töövoo loomine

Töövoo loomiseks minge jaotisse Hanked &gt; Seadistus &gt; Hangete töövood ja looge uus töövoog, valides loodava töövoo tüübi. 

Töövoo lõuendil saate lohistada töövoo elemendid kujundajasse ja linkida need voogu. Töövoo elemendid peavad olema konfigureeritud. Kinnitus- ja ülesandetöövoo elementide puhul saate konfigureerida, milline osaleja peaks tegutsema.

## <a name="types-of-participants"></a>Osalejate tüübid

Saate määrata kinnitamisetapi järgmistele osalejate gruppidele.

| Kasutajagrupp | Kirjeldus |
|---|---|
| Osaleja | Määrake kinnitamisetapp grupi või rolli liikmetele. |
| Hierarhia | Määrake kinnitamisetapp teatud organisatsioonihierarhia kasutajatele. |
| Töövoo kasutaja | Määrake kinnitamisetapp selle töövoo kasutajatele. |
| Järjekord | Määrake kinnitusetapp tööüksuste järjekorda. |
| Kasutaja | Määrake kinnitamisetapp konkreetsetele kasutajatele. |

## <a name="additional-resources"></a>Lisaressursid

- [Äriprotsessi töövoogude määratlemine ostutaotluste jaoks](https://www.microsoft.com/download/details.aspx?id=101821)
- [Ostutaotluse töövoog](purchase-requisitions-workflow.md)
- [Hankijate vastuvõtmine](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]