---
title: "Tootmise käivitamise registreerimine"
description: "Teema käsitleb põhimõisted ja mida tuleb mõista konfigureerida ja kasutada tootmise täitmise tingimused."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: aee0a4eda2a2ac2f272f590781b9e751a8797095
ms.lasthandoff: 03/31/2017


---

# <a name="registration-for-manufacturing-execution"></a>Tootmise käivitamise registreerimine

Teema käsitleb põhimõisted ja mida tuleb mõista konfigureerida ja kasutada tootmise täitmise tingimused. 

Tootmise käivitamist peaksid peamiselt kasutama tootmisettevõtted. Töötajad saavad tootmistööde käigus kulunud aega ja kaubakulu registreerida leheküljel **Töö registreerimine**. Registreerumine on kinnitatud ja on hiljem üle asjakohaste moodulite. Registreerimiste pideva kinnitamise ja ülekandmisega saavad juhid hõlpsalt jälgida tootmistellimuste tegelikke kulusid.

## <a name="manufacturing-execution-and-registration-terminology"></a>Tootmise käivitamine ja registreerimisterminoloogia
Järgmises tabelis on mõisted, mis on seotud tootmise käivitamise ja sellega seotud registreerimistoimingutega.

| Mõiste                          | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tootmise käivitamine       | Funktsioon, mida kasutatakse, et registreerida aega, materjali tarbimise, tootmise tööd, projektide ja kaudsete tegevuste kulude. Registreerimine toimub tootmise käivitamise registreerimiskliendis.                                                                                                                                                                                                                                                                                                                                                                                                   |
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
-   **Projekti tasu ja üksused** (saadaval koos siiani) – registreerida töötajate tasud (kulud), mis on seotud projekti projekti tasu žurnaali, nt läbisõidu ja silla teemaks. Töötajate ka saate registreerida kaubatarbimist projektide kohta. Seda tehakse projekti kauba töölehel.
-   **Teisele töötajale abilise registreerimine** – kui kaks või rohkem töötajat tootmistöös või projektis koos töötavad, saab töötaja registreeruda masina või teise töötaja abiliseks, kes sellisel juhul on juhtressurss või ‑töötaja. Vajaduse korral saab juhttöötaja valida teise töötaja juhttöötajaks.
-   **Puudumise registreerimine** (saadaval tööajaarvestuse puhul) – töötajad saavad puudumise aega registreerida mitmesuguste puudumiskoodidega. Puudumist saab näidata, kui töötaja hilineb, peab tööpäeva vältel töölt lahkuma või lahkub tavapärase tööaja profiili suhtes oodatust varem.
-   **Puhkepauside registreerimine** (saadaval tööajaarvestuse puhul) – töötajad saavad tööpäeva jooksul registreerida puhkepausiks tööjaamast lahkumisi. Seadistada saab mitut tüüpi puhkepause. Kui töötaja naaseb ja uuesti sisse logib, registreerib süsteem töötaja tagasijõudmise ja puhkepausi registreerimine lõpeb.
-   **Kaudsete tegevuste registreerimine** (saadaval tööajaarvestuse puhul) – kaudsed tegevused on mittetootlikud tegevused, milles töötajad võivad tööpäeva jooksul osaleda (nt osakonna koosolek, töörühma koosolek või töökojas tehtud hooldustööd). Töötajad saavad registreerida määratud kaudseid tegevusi.
-   **Ületundide registreerimine** (saadaval tööajaarvestuse puhul) – töötajad, kellel on palutud pikemaid töötunde teha, saavad valida, kas registreerida lisaaeg paindliku tööaja või ületunnitööna.



