---
title: "Hangete töövood"
description: "Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas. Kinnitamisprotsessi seadistamiseks saate luua töövoo."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 27c211e6ded17e085559add916c28a48c40e5b8e
ms.lasthandoff: 03/31/2017


---

# <a name="procurement-and-sourcing-workflows"></a>Hangete töövood

Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas. Kinnitamisprotsessi seadistamiseks saate luua töövoo.

Töövoog esindab äriprotsessi. Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama. Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.
-   **Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded. Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.
-   **Protsessi nähtavus** — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu. See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.
-   **Tsentraliseeritud tööde nimekiri**— kasutajad saate vaadata, tsentraliseeritud töö töövooülesanded ja kinnituste osalevad kõik töövood kogu neile määratud. See on töö kaubad lehel saadaval.

## <a name="the-types-of-workflows-that-you-can-create"></a> Loodavate töövoogude tüübid
Jaotises Hanked on saadaval järgmised töövootüübid.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Tüüp**                         | **Kasutage seda tüüpi järgmiseks**                                          |
| Ostutaotluse ülevaade      | Saate luua ülevaatuse töövoogusid ostutaotluste jaoks.            |
| Ostutaotluse rea eelvaade | Saate luua ülevaatuse töövoogusid ostutaotluse ridade jaoks.       |
| Ostutellimuse töövoog          | Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuste jaoks.     |
| Ostutellimuse rea töövoog     | Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuse ridade jaoks. |

## <a name="creating-a-workflow"></a>Töövoo loomine
Töövoo loomiseks Mine hangete ja mis hangivad &gt;Setup &gt;hankimise ja töövoogude hankimisel ja luua uue töövoo valides töövoo loomiseks.  

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

[Purchase requisition workflow](purchase-requisitions-workflow.md)


