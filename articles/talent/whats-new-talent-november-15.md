---
title: "Mis on Dynamics 365 for Talent Core HR-is uut või mida on muudetud (15. november 2018)"
description: "Teema kirjeldab funktsioone, mis on Microsoft Dynamics 365 for Talent Core HR-is kas uued või muudetud."
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>Mis on Dynamics 365 for Talent Core HR-is uut või mida on muudetud (15. november 2018)

[!include [banner](includes/banner.md)]

**Järk 8.1.2045**

Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.

## <a name="other-changesfixes"></a>Muud muudatused/parandused

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Töövõtja praegust ametikohta ei saa muuta tulevaseks vabaks ametikohaks

Tehti muudatus ametikoha üleviimise võimaldamiseks juhul, kui ametikoht on ainult tulevikus saadaval. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Töökohta ei kuvata uue töövõtja loomisel

Tehti muudatus kõigi vabade ametikohtade kuvamiseks, mis on Talentis uut töövõtjat värvates määramiseks saadaval. See hõlmab ajaloolisi positsioone või kui positsioonidel on tulevane kuupäev. Positsioonid ilmuvad nüüd õigesti töösuhte alguskuupäeva alusel. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Lõpetamise kuupäeva kuvatakse kasutajasätete alusel

Tehti muudatus varasemate töövõtjate loendis töövõtja eelistatud ajavööndi korral ajavööndi nihete arvestamiseks töösuhte lõpetamise kuupäeva kuvamisel.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Mulle määratud tööüksused ei kuva õiget teavet

Selle muudatusega saab kuvada valitud kauba jaoks õige teabe, kui navigeerida loendis üksikute tööüksuste üksikasjadele. Probleem ilmnes ainult täpsemate turvasuvanditega.


## <a name="known-issue"></a>Teadaolev probleem

- **Probleemi**: uuele töötajale seotuse lisamisel on nupud **Uus** ja **Redigeeri** hallid. 
- **Lahendus:** veenduge enne manuse lehe avamist, et **Töötaja** lehe kiirinfod oleksid suletud. Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manuste nupud lubatud. (See probleem lahendatakse järgmisel platvormivärskendusel.)
