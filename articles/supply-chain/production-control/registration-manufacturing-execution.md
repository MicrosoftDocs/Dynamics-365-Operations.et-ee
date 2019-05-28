---
title: Tootmise käivitamise registreerimine
description: Selles teemas kirjeldatakse põhimõisteid ja tingimusi, mida on vaja tootmise käivitamise konfigureerimiseks ja kasutamiseks mõista.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bbcd7ebea869f921c2eadd05e64509ff9246aa4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567468"
---
# <a name="registration-for-manufacturing-execution"></a>Tootmise käivitamise registreerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse põhimõisteid ja tingimusi, mida on vaja tootmise käivitamise konfigureerimiseks ja kasutamiseks mõista. 

Tootmise käivitamist peaksid peamiselt kasutama tootmisettevõtted. Töötajad saavad tootmistööde käigus kulunud aega ja kaubakulu registreerida leheküljel **Töö registreerimine**. Kõik registreerimised kinnitatakse ja kantakse hiljem üle vastavatesse moodulitesse. Registreerimiste pideva kinnitamise ja ülekandmisega saavad juhid hõlpsalt jälgida tootmistellimuste tegelikke kulusid.

## <a name="manufacturing-execution-and-registration-terminology"></a>Tootmise käivitamine ja registreerimisterminoloogia
Järgmises tabelis on mõisted, mis on seotud tootmise käivitamise ja sellega seotud registreerimistoimingutega.

| Mõiste                          | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tootmise käivitamine       | Funktsioon, millega registreeritakse aega, materjalikulu, tootmistööde, projektide ja kaudsete tegevuste kulu. Registreerimine toimub tootmise käivitamise registreerimiskliendis.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Tööde loend                      | Töötajatele kuvatakse leheküljel **Töö registreerimine** tööde loend, mida nad peavad kindla ressursiga, nt masinaga, tegema. Töötaja saab registreerida aja ja kauba kulu iga tööde loendis oleva töö või ülesande kohta.                                                                                                                                                                                                                                                                                                                                                                           |
| Tööde kogumiks koondamine                  | Kui töötaja alustab leheküljel **Töö registreerimine** samal ajal mitut tööd, nimetatakse seda tööde kogumisse sidumiseks. Kogumisse seotud töödele kulutatud aega saab üksikutele töödele eraldada mitmel viisil, kasutades eraldusvõtmeid.                                                                                                                                                                                                                                                                                                                                                         |
| Juhtressursi ja abilise registreerimised | Töötaja saab registreeruda ressursi abilisena ja luua väikese meeskonna, milles mitu töötajat teeb sama tootmistööd. Ressursse, millega töötajad on abilisena seotud, nimetatakse juhtressurssideks. Registreerimisi peab tegema ainult juhtressurss. Kõik abilised saavad automaatselt samad registreerimised. Kui näiteks masin toimib juhtressursina, saavad abilisena selle masina juurde registreeritud töötajad teha leheküljel **Töö registreerimine** registreerimisi ja nii masin kui ka sellega abilistena seotud töötajad saavad samad registreerimised. |
| Kaudne tegevus             | Tegevus või ülesanne, mis pole otseselt tootmise või projektiga seotud, näiteks osakonna koosolek, puhastustöö või hooldustöö töökojas. Töötajad saavad teha kaudsete tegevuste registreerimisi sama moodi kui tootmistööde ja projektide puhul.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Registreerimised tootmise käivitamisel
Töötajad saavad teha tootmisel mitmesuguseid registreerimisi tootmistööde tegemiseks. Süsteemi seadistusest olenevalt võib olla võimalik teha registreerimisi ka projekti ja mittetootlikele tegevustele, nagu puhkepaus, puudumised või kaudsed tegevused. Registreerumise tüübid on järgmised.

-   **Sisse-ja väljaregistreerimine** (saadaval tööajaarvestuse puhul) – töötajad registreeruvad tööle saabudes sisse ja lahkudes välja.
-   **Tootmistöödele registreerimine** – töötajad saavad teha registreerimisi (nt töö alustamine ja tööga seoses tagasiside andmine) tootmistöödele, mis kuvatakse tema tööde loendis. Töötajad saavad alustada mitut tööd korraga. Seda nimetatakse tööde kogumisse sidumiseks.
-   **Varude registreerimine** – töötajad saavad teha registreerimisi töökojas kasutatavate materjalide kasutamiseks, mis pole otseselt tootmistöödega seotud. Näiteks määre, õlid või muud masinate hooldamiseks vajalikud materjalid. Registreerimine tehakse laotöölehel.
-   **Projektidele registreerumine** (saadaval tööajaarvestuse puhul) – töötajad saavad teha registreerimisi, nt töö alustamine ja lõpetamine, projektidele või projekti tegevustele, mis kuvatakse tema tööde loendis.
-   **Projekti kulude ja projekti kaupade registreerimine** (saadaval tööajaarvestuse puhul) – töötajad saavad registreerida projektiga seotud tasusid (kulusid), nagu läbisõit ja kiirteemaksud, projekti tasu töölehel. Töötajad saavad registreerida ka kauba tarbimist projektide kohta. Seda tehakse projekti kauba töölehel.
-   **Teisele töötajale abilise registreerimine** – kui kaks või rohkem töötajat tootmistöös või projektis koos töötavad, saab töötaja registreeruda masina või teise töötaja abiliseks, kes sellisel juhul on juhtressurss või ‑töötaja. Vajaduse korral saab juhttöötaja valida teise töötaja juhttöötajaks.
-   **Puudumise registreerimine** (saadaval tööajaarvestuse puhul) – töötajad saavad puudumise aega registreerida mitmesuguste puudumiskoodidega. Puudumist saab näidata, kui töötaja hilineb, peab tööpäeva vältel töölt lahkuma või lahkub tavapärase tööaja profiili suhtes oodatust varem.
-   **Puhkepauside registreerimine** (saadaval tööajaarvestuse puhul) – töötajad saavad tööpäeva jooksul registreerida puhkepausiks tööjaamast lahkumisi. Seadistada saab mitut tüüpi puhkepause. Kui töötaja naaseb ja uuesti sisse logib, registreerib süsteem töötaja tagasijõudmise ja puhkepausi registreerimine lõpeb.
-   **Kaudsete tegevuste registreerimine** (saadaval tööajaarvestuse puhul) – kaudsed tegevused on mittetootlikud tegevused, milles töötajad võivad tööpäeva jooksul osaleda (nt osakonna koosolek, töörühma koosolek või töökojas tehtud hooldustööd). Töötajad saavad registreerida määratud kaudseid tegevusi.
-   **Ületundide registreerimine** (saadaval tööajaarvestuse puhul) – töötajad, kellel on palutud pikemaid töötunde teha, saavad valida, kas registreerida lisaaeg paindliku tööaja või ületunnitööna.




