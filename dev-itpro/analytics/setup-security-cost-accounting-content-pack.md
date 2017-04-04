---
title: "Turvameetmete kuluarvestuse analüüsimiseks Power BI sisu"
description: "See teema selgitab, kuidas te võite levitada juurdepääsu tasemel turvalisust kuluarvestuse rea tasandil julgeolekut Microsoft Power BI. See funktsioon aitab tagada, et kasutajad näevad ainult Power BI andmeid, et neid makstakse juurdepääsu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Turvameetmete kuluarvestuse analüüsimiseks Power BI sisu

See teema selgitab, kuidas te võite levitada juurdepääsu tasemel turvalisust kuluarvestuse rea tasandil julgeolekut Microsoft Power BI. See funktsioon aitab tagada, et kasutajad näevad ainult Power BI andmeid, et neid makstakse juurdepääsu.

<a name="overview"></a>Ülevaade
--------

Selle **kuluarvestuse analüüs** Microsoft Power BI sisu kasutab Power BI rea tasandil turvalisuse piirata kasutaja juurdepääsu. Turvalisus põhineb juurdepääsutase organisatsiooni hierarhiale, kuluarvestuse parameetrites seadistatud. Lisateavet selle **kuluarvestuse analüüs** Power BI sisu, vt [kuluarvestuse analüüsi Power BI sisu](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Häälestus
Power BI sisu omanik tuleb propageerida Power BI-juurdepääsutase tagatist, toimige järgmiselt. **Märkus:** kasutaja, kes avaldab selle **kuluarvestuse analüüs** Power BI sisu muutub automaatselt. Ainult omanik saab seadistada turvalisuse Power BI. Lisaks kuni omanik lisab teiste kasutajate PowerBI.com, keegi peale omaniku näha kõik andmed selle **kuluarvestuse analüüs** Power BI sisu.

1.  Definitsioonifaili avaldada Power BI.
2.  Logi sisse PowerBI.com.
3.  Leia aineandmestik on **kuluarvestuse analüüs** Power BI sisu.
4.  Avage leht security. 

    [![Turvalisus-Avaleht](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  Selle **kulu objekti kontroller** roll on juba loodud. Lisada uusi liikmeid, kes on kuluarvestuse juurdepääsutase organisatsiooni hierarhia osa. 

    [![Liikmete lisamine](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Kasutajad, kes lisatakse selle **kulu objekti kontroller** rolli näevad ainult andmeid, mis nad on lubatud näha kuluarvestuse juurdepääsutase organisatsiooni hierarhia määratluse kohaselt. **Märkus:** rea tasandil tagatis kehtib plaadid ja Microsoft Dynamics 365 toiminguteks, mis on paigaldatud Power BI aruanded.

## <a name="updating-security"></a>Täiendav turvalisus
Uuendused tehakse juurdepääsu tasemel turvalisust kuluarvestuse, kui soovite Power BI kajastada neid värskendusi, peate värskendama üksus poe ning **kuluarvestuse analüüs** Power BI sisu. Pärast üksuse hoidla uuendamine Dynamics 365 toimingute lõpetamiseks peate uuendama PowerBI.com esemeid. Üksuse poe värskenduse kohta lisateabe saamiseks vt [Update üksuse poe](power-bi-integration-entity-store.md#update-entity-store). Omanik on **kuluarvestuse analüüs** Power BI sisu võtma üksus poes update kui uued kasutajad omavad juurdepääsu organisatsiooni hierarhiale. Lisaks omanik tuleb lisada uusi kasutajaid ning **kulu objekti kontroller** rolli PowerBI.com, nii et rea tasandil kautsjoni kohaldati neid.

## <a name="disabling-security"></a>Keelamine turvalisus
Eeldame, et teie organisatsioon soovib piirata juurdepääsu andmetele. Kui mingil põhjusel on julgeoleku parameetrid keelatud kuluarvestuse käivitamisel, omanik lisama kasutajatel on **eelarvestaja** Power BI rolli asemel. Kui muudate turvalisus lubatud olekus keelatud olekus, on mõistlik eemaldada kasutajate ning **kulu objekti kontroller** rolli. Ja vastupidi, kui turvalisuse uuesti lubada. Mõlema poole vestlust saab kuuluvad kasutajad. Ühine juurdepääs on mõlemad rollid. Puhul on **kuluarvestuse analüüs** Power BI sisu, ühise juurdepääsuga on piiramatu juurdepääsu andmetele. Kui teie eesmärgiks on kohaldada piiratud juurdepääsu, kasutajate tuleb määrata üksnes selle **kulu objekti kontroller** rolli. Rea tasandil Turvauuendused jõustuma viivitamata. Kasutajatel tuleks värskendada brauseri.

## <a name="additional-resources"></a>Lisaressursid
Lisateavet Power BI rea tasemel turvalisust, vt [hallata turvalisuse teie mudelil Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


