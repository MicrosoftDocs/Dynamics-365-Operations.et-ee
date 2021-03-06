---
title: Toodetud kaupade standardkulude säilitamise ettevalmistus
description: Selles teemas kirjeldatakse toodetud kaupade kulude haldamiseks ette valmistamise etappe.
author: AndersGirke
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
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a82b0a205ac6b7a86b9aca0771303469c6666c1
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187742"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Toodetud kaupade standardkulude säilitamise ettevalmistus

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse toodetud kaupade kulude haldamiseks ette valmistamise etappe. Toodetud kaupade etapid erinevad veidi ostetud kaupade etappidest.

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

## <a name="related-topics"></a>Seotud dokumendid

[Toodetud kauba püsikulude amortiseerimine](amortize-constant-costs-manufactured-item.md)

[Toodetavate või hangitavate toodete seadistamine](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]