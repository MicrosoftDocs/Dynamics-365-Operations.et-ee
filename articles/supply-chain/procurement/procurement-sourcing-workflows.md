---
title: "Hangete töövood"
description: "Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas. Kinnitamisprotsessi seadistamiseks saate luua töövoo."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: ce9bc42751cf0f537a0ddb5069aca7c9779a6bb1
ms.contentlocale: et-ee
ms.lasthandoff: 12/14/2017

---

# <a name="procurement-and-sourcing-workflows"></a>Hangete töövood

[!INCLUDE [banner](../includes/banner.md)]

Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas. Kinnitamisprotsessi seadistamiseks saate luua töövoo.

Töövoog esindab äriprotsessi. Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama. Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.
-   **Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded. Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.
-   **Protsessi nähtavus** — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu. See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.
-   **Tööde koondloend** – kasutajad saavad vaadata tööde koondloendit, et näha neile määratud töövoo ülesandeid ja kinnitusi kõigis töövoogudes, milles nad osalevad. See on saadaval lehel Tööüksused.

## <a name="the-types-of-workflows-that-you-can-create"></a> Loodavate töövoogude tüübid
Jaotises Hanked on saadaval järgmised töövootüübid.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Tüüp**                         | **Kasutage seda tüüpi järgmiseks**                                          |
| Ostutaotluse ülevaade      | Saate luua ostutaotluste jaoks ülevaatuse ja kinnitamise töövood.            |
| Ostutaotluse rea eelvaade | Saate luua ostutaotluse ridade jaoks ülevaatuse ja kinnitamise töövood.       |
| Ostutellimuse töövoog          | Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuste jaoks.     |
| Ostutellimuse rea töövoog     | Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuse ridade jaoks. |
| Hankija lisamise rakenduse töövoog  | Saate luua ülevaatuse ja kinnitamise töövood uute hankijate lisamiseks hankija nõuete kaudu. |

## <a name="creating-a-workflow"></a>Töövoo loomine
Töövoo loomiseks minge jaotisse Hanked &gt; Seadistus &gt; Hangete töövood ja looge uus töövoog, valides loodava töövoo tüübi.  

Töövoo lõuendil saate lohistada töövoo elemendid kujundajasse ja linkida need voogu. Töövoo elemendid peavad olema konfigureeritud. Kinnitus- ja ülesandetöövoo elementide puhul saate konfigureerida, milline osaleja peaks tegutsema.
Osalejate tüübid
----------------------

Saate määrata kinnitamisetapi järgmistele osalejate gruppidele.

| Kasutajagrupp    | Kirjeldus                                                               |
|---------------|---------------------------------------------------------------------------|
| Osaleja   | Määrake kinnitamisetapp grupi või rolli liikmetele.                   |
| Hierarhia     | Määrake kinnitamisetapp teatud organisatsioonihierarhia kasutajatele. |
| Töövoo kasutaja | Määrake kinnitamisetapp selle töövoo kasutajatele.                       |
| Järjekord         | Määrake kinnitusetapp tööüksuste järjekorda.                            |
| Kasutaja          | Määrake kinnitamisetapp konkreetsetele kasutajatele.                               |



<a name="see-also"></a>Vt ka
--------

[Äriprotsessi töövoogude määratlemine ostutaotluste jaoks](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Ostutaotluse töövoog](purchase-requisitions-workflow.md)

[Hankijate sotsialiseerimine](vendor-onboarding.md)


