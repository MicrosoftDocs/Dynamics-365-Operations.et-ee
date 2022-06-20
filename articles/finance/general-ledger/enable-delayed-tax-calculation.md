---
title: Luba töölehtedel viivitusega maksuarvutus
description: See artikkel selgitab, kuidas lülitada sisse hilinenud maksu arvutamise funktsioon, et aidata parandada maksuarvutuste jõudlust, kui töölehe ridade arv on väga suur.
author: EricWang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 02a038318d4c0fb44b6fcc4bb159ea87c2e9368a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887915"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Luba töölehtedel viivitusega maksuarvutus
[!include [banner](../includes/banner.md)]


See artikkel selgitab, kuidas saate käibemaksu arvutamisega töölehtedel viivitada. See võimalus aitab parandada maksuarvutuste jõudlust, kui töölehe ridu on palju.

Vaikimisi arvutatakse töölehe ridadel käibemaksu summad iga kord, kui maksudega seotud välju uuendatakse. Need väljad hõlmavad käibemaksugruppide ja kauba käibemaksugruppide välju. Iga tööleherea uuendamine põhjustab maksusummade ümberarvutamist kõigi tööleheridade puhul. Kuigi selline käitumine aitab kasutajal näha reaalajas arvutatud maksusummasid, võib see mõjutada ka jõudlust, kui tööleheridade arv on väga suur.

Viivitusega maksuarvutuse funktsioon võimaldab teil viivitada maksude arvutamisega töölehtedel ja aitab seega parandada jõudlusprobleeme. Kui see funktsioon on sisse lülitatud, arvutatakse maksusummad ainult siis, kui kasutaja valib käsu **Käibemaks** või sisestab töölehe.

Käibemaksu arvutamisega saate viivitada kolmel tasandil:

- Juriidiline isik
- Töölehe nimi
- Töölehe päis

Süsteem annab prioriteedi töölehe päise sättele. Vaikimisi võetakse see säte töölehe nimest. Töölehe nime säte võetakse vaikimisi töölehe nime loomisel lehe **Pearaamatu parameetrid** sättest. Järgmistes jaotistes selgitatakse, kuidas lülitada sisse viivitusega maksuarvutust juriidiliste isikute, töölehe nimede ja töölehe päiste jaoks.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Viivitusega maksuarvutuse sisselülitamine juriidilise isiku tasandil

1. Avage **Pearaamat \> Pearaamatu seadistamine \> Pearaamatu parameetrid**.
2. Määrake vahekaardi **Käibemaks** kiirkaardi **Üldine** valiku **Viivitusega maksuarvutus** väärtuseks **Jah**.

![Pearaamatu parameetrite kujutis.](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Viivitusega maksuarvutuse sisselülitamine töölehe nime tasandil

1. Avage **Pearaamat \> Töölehe seadistamine \> Töölehtede nimed**.
2. Määrake kiirkaardi **Üldine** jaotises **Käibemaks** valiku **Viivitusega maksuarvutus** väärtuseks **Jah**.

![Töölehe nimede kujutis.](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Viivitusega maksuarvutuse sisselülitamine töölehe päise tasandil

1. Avage **Pearaamat \> Töölehekirjed \> Päevaraamatud**.
2. Valige suvand **Uus**.
3. Valige töölehe nimi.
4. Seadke vahekaardil **Seadistus** valiku **Viivitusega maksuarvutus** väärtuseks **Jah**.

![Päevaraamatu lehe kujutis.](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
