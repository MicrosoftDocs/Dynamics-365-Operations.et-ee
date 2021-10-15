---
title: Tootemudeli protsessi haldamine
description: Selle protseduuri käitamine nõuab toote konfiguratsioonimudeli olemasolu.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88df8b867ac7f354417add0462e7999747333451
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577260"
---
# <a name="maintain-route-for-a-product-model"></a>Tootemudeli protsessi haldamine

[!include [banner](../../includes/banner.md)]

Selle protseduuri käitamine nõuab toote konfiguratsioonimudeli olemasolu. See protseduur kasutab tipptasemel kõlari mudelit demoettevõttes USMF, et juhatada teid läbi protsessi.

## <a name="add-a-route-operation"></a>Lisage protsessitoiming

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
1. Otsige loendist ja valige soovitud kirje.
    * Valige selle harjutuse jaoks tipptasemel kõlari mudel.  
1. Valige loendis link valitud reas.
1. Laiendage jaotist **Protsessitoimingud**.
1. Valige **Lisa**.
1. Sisestage väärtus väljale **Nimi**.
1. Sisestage väärtus väljale **Kirjeldus**.
1. Valige käsk **Salvesta**.

## <a name="enter-route-operation-details"></a>Sisestage protsessitoimingu üksikasjad

1. Valige **Protsessi operatsiooni üksikasjad**.
1. Sisestage või valige väärtus väljal **Toiming**.
1. Väljal **Toim. nr** number.
    * Toimingunumbrid määravad protsessi järjekorra.  
    * Iga protsessitoimingu atribuut võib saada statistilise väärtuse või olla vastendatud atribuudiga. Atribuudiga vastendamisel määratakse väärtus konfiguratsiooni osaks.  
1. Sisestage või valige väärtus väljal **Protsessigrupp**.
    * Protsessigrupp määrab kuluarvutuse, tarbimise ja seadistuse põhikäitumise.  
1. Valige vahekaart **Häälestus**.
1. Valige vahekaart **Ajad**.
1. Sisestage arv väljale **Protsessi kogus**.
    * Määrake, mitu ühe toimingu käigus töödeldakse.  
1. Sisestage number väljale **Tunnid/aeg**.
    * Sisestage aja suhe.  
1. Märkige ruut **Määra**.
1. Sisestage number väljale **Käitusaeg**.
    * Määrake määratud koguse töötlemisaeg.  
1. Valige vahekaart **Ressursinõuded**.
1. Valige **Lisa**.
1. Märkige loendis valitud rida.
1. Valige suvand väljal **Nõude tüüp**.
    * Otsustage, kas soovite määrata konkreetseid ressursse või võimalusi, mis neil peavad olema.  
1. Valige või sisestage väärtus väljal **Nõue**.
1. Valige nupp **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]