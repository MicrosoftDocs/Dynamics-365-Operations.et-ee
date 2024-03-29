---
title: Toodetud kaupade standardkulude säilitamise ettevalmistus
description: See artikkel kirjeldab samme toodetud kaupade kulude säilitamiseks.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 423da8022faf8066c5aa524c49c5071d0871de04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886011"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Toodetud kaupade standardkulude säilitamise ettevalmistus

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab samme toodetud kaupade kulude säilitamiseks. Toodetud kaupade etapid erinevad veidi ostetud kaupade etappidest.

Toodetavatele kaupadele määratud tegevuspõhimõtted võivad mõjutada kulu kalkulatsioone toodetava põhikauba puhul. Toodetud kaupade kulude haldamise ettevalmistamiseks tehke läbi järgmised etapid.

1. Määrake toodetavale kaubale kauba mudeligrupp. 

   Kauba mudeligrupp määrab standardsete kulude kasutamise.

2. Määrake toodetavale kaubale kaubagrupp. 

   Kaubagrupp sisaldab toodetavale kaubale kehtivaid pearaamatukontosid. Standardse kulu laomudeliga toodetava kauba pearaamatukontod hõlmavad mitut tootmiskulude hälvet, kulu muutmise hälvet ja varude kulu ümberhindlust.

3. Määrake kaubale lao mõõtühik. 

   Kauba kulud esitatakse alati kauba lao mõõtühikutes.

4. Ärge määrake oodetavale kaubale kulugruppi, välja arvatud juhul, kui seda käsitletakse ostetud kaubana.

5. Määrake toodetavale kaubale koosluse kalkulatsioonigrupp. 

   Kauba koosluse kalkulatsioonigrupp määratleb kehtivad hoiatustingimused. Sel viisil saab pärast koosluse kalkulatsiooni luua hoiatussõnumeid arvutusvigade võimalike allikate kohta. Näiteks võib hoiatussõnum määrata, kui aktiivne kooslus või protsess puudub. Koosluse kalkulatsioonigrupp sisaldab koosnevuse peatamise poliitikat, mis määrab, millal tuleb toodetavat kaupa ostetud kaubana käsitleda.

6. Kui toodetud kaubal on püsikuld, määrake sellele standardne tellimiskogus. 

   Standardne tellimiskogus on raamatupidamise saatepartii suurus püsikulude amortiseerimiseks. Püsikulude näited hõlmavad seadistusaegu protsessi operatsioonides ja komponentide püsikogust koosluses.

7. Määrake toodetavale kaubale kooslus. 

   Toodetavale kaubale saab määrata ühe või mitu koosluse versiooni. Kontrollige, et soovitud versioonid oleksid märgitud kui kinnitatud ja aktiivsed ning et neil on soovitud kehtivuse kuupäevad. Koosluse versioon võib hõlmata kogu ettevõtet või olla laoala-põhine.

8. Määrake toodetavale kaubale protsess. 

   Toodetavale kaubale saab määrata ühe või mitu protsessiversiooni. Kontrollige, et soovitud versioonid oleksid märgitud kui kinnitatud ja aktiivsed ning et neil on soovitud kehtivuse kuupäevad. Protsessiversioon peab olema laoala-põhine.

Kui soovite protsesside teavet kasutada kulueesmärkidel, peate tegema ettevalmistavaid lisasamme. Näiteks peavad protsessi operatsioonidele määratud kulukategooriad olema õiged ja lõpule viidud.

## <a name="related-articles"></a>Seotud artiklid

[Toodetud kauba püsikulude amortiseerimine](amortize-constant-costs-manufactured-item.md)

[Toodetavate või hangitavate toodete seadistamine](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]