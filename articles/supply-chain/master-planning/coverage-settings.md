---
title: Laovarude sätted
description: Selles teemas on teave laovarude sätete kohta, mida Koondplaneerimises kasutatakse kaubavajaduse arvutamiseks.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aaacf28701542d329afedd8206a12f7c11b7ac7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999977"
---
# <a name="coverage-settings"></a>Laovarude sätted

[!include [banner](../includes/banner.md)]

Koondplaneerimine kasutab laovarude sätteid, et arvutada kaubavajadusi.

saate määratleda laovarude sätteid mitmel viisil:

- Määrake laovarude grupi laovarude sätted.

    Saate luua laovarude grupi, mis sisaldab kõigi laovarude grupiga lingitud toodete sätteid. Klõpsake laovarude grupi loomiseks valikuid **Koondplaneerimine &gt; Seadistus &gt; Laovarud &gt; Laovarude grupid**. Saate linkida tootega laovarude grupi. Kui link on tegevuskoha-, lao- või tootedimensiooni kohane, kasutage lehel **Kauba laovarud** välja **Laovarude grupp**. Kui link on üldine olenemata tootedimensioonidest kasutage välja **Toote üksikasjad** kiirkaardi **Plaan** lehte **Laovarude grupp**. Kui te ei lingi laovarude gruppi tootega, kasutab koondplaneerimine vaikesättena suvandit Üldine laovarude grupp, mis on määratud lehel **Koondplaneerimise parameetrid**.

- Määrake toote laovarude sätted.

    Saate luua laovarude sätted kindlale tootele. Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige toode ja klõpsake toimingupaanil vahekaardi **Plaan** jaotises **Laovarude** grupp valikut **Kauba laovarud**, et avada leht **Kauba laovarud**. Kui toode on laovarude grupiga juba lingitud, saate laovarude grupi sätted tühistada, kasutades välja **Tühista**. Laovarude sätted lehel **Kauba laovarud** alistavad lehel **Laovarude grupp** olevad sätted.

- Määrake toote laovarude sätted viisardi abil.

    Viisard juhendab teid sammhaaval läbi esmase kauba laovarude seadistamise protsessi. Klõpsake lehel **Kauba laovarud**, Toimingupaanil valige suvand **Viisard**, et avada leht **Kauba laovarude viisard**.

- Määrake dimensioonigrupi kaubavarude sätted.

    Avage **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Klõpsake lehe **Väljastatud toote üksikasjad** kiirkaardil **Üldine**, jaotises **Administreerimine** valige link **Laoala dimensioonigrupp**. Valige lehel **Laoala dimensioonigrupid** märkeruut **Laovarude planeerimine dimensiooni järgi**, et luua laovarude sätted laoala dimensioonigrupi dimensiooni jaoks. Kõigi tootedimensioonide, nagu konfiguratsioon, värv, suurus, stiil, puhul peab olema väli **Laovarude planeerimine dimensiooni järgi** valitud.


## <a name="coverage-codes"></a>Planeerimise koodid

Koondplaneerimise konfigureerimise abil saab kasutada erinevaid täiendamise meetodeid. Täiendamise meetodid või saatepartii mõõtmise meetodid on need tehnikad, mille abil süsteem määratleb ostetud või toodetud kaupade partii suuruse. 

Igale täiendamise meetodile määratakse üks allolevatest laovarude koodidest.

- **Käsitsi** – saatepartii mõõtmise meetod, mille puhul süsteem ei soovita kaubale ostu-, edastamis- või tootmistellimusi. Kauba plaanija vastutab kauba täiendamiseks nõutavate tellimuste loomise eest.
- **Vastavalt nõudele** – saatepartii mõõtmise meetod, mille puhul süsteem loob kaubale vajaduse korral plaanitud ostu-, edastamis- või tootmistellimuse. Seda kasutatakse tavaliselt hootise nõudlusega kulukate kaupade puhul.  
- **Vastavalt perioodile** – saatepartii mõõtmise meetod, mis koondab kauba nõudluse teatud perioodi jooksul ühte tellimusse. Tellimus planeeritakse perioodi esimesele päevale ja selle kogus vastab netosummale määratud perioodi jooksul. Periood algab kauba esimese nõudega ja katab määratud pikkusega aja jooksul. Järgmine periood algab kauba järgmiste nõuetega.
- **Min/maks** – saatepartii mõõtmise meetod, mis hõlmab varude täiendamist teatud tasemeni, kui ennustatud laoseis on väiksem kui seatud lävi. Varude täiendamise kogus on maksimaalse taseme ja prognoositava vaba taseme vaheline erinevus.


## <a name="additional-resources"></a>Lisaressursid

[Koondplaanide ülevaade](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]