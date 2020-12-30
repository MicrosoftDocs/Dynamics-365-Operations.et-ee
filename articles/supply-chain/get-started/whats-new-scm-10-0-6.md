---
title: Mis onuut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.6 (november 2019)
description: Selles teemas kirjeldatakse Dynamics 365 Supply Chain Management 10.0.6 uusi või muutunud funktsioone.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9ee25036488d2f7f24c1691d36239f3f34caf0cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426307"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Mis onuut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.6 (november 2019)

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 Supply Chain Management 10.0.6 uusi või muutunud funktsioone. Selle versioonijärgu number on 10.0.234. Kuigi üldise kättesaadavuse kuupäev on plaanitud novembrisse, on uued funktsioonid saadaval ka varajases väljalaskes oktoobris. Lisateabe saamiseks versiooni 10.0.6 kohta vt [Lisaressurssid](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>Toote konfiguratsioonimudelite V2 andmeüksus

Antakse välja „Toote konfiguratsioonimudelite” andmeüksuse teine versioon (nn „toodete konfiguratsioonimudelid V2”). Vaikemall „418-toote konfiguratsioonimudelid” peab olema nii, et see kasutaks importimise/eksportimise raamistiku mallides uut andmeüksust „toote konfiguratsioonimudelid V2”. Malli ei uuendata automaatselt, see tuleb vaikemallist käsitsi laadida. V2-üksus ekspordib ühe rea tekstisisese asemel eraldi manustatud failina, mis lahendab V1-üksuse suurusepiirangud. 
 
Mida peate selle muudatuse hankimiseks tegema?
-    Kuna V1-üksus on aegunud, peaksite alustama V1 üleminekut V2-le. Kui kasutate malli „418-toote konfiguratsioonimudelid”, saate klõpsata nuppu „laadi vaikemallid” ja laadida malli „418‑toote konfiguratsioonimudelid” uuesti
-    Kui teil on vaja säilitada ühilduvus olemasolevate süsteemidega, saate nüüd jätkata olemasoleva malli ja (aegunud) V1-üksuse kasutamist, kuni te teisaldate oma integratsiooni uuele mallile. 

## <a name="feature-management-enhancements"></a>Funktsioonihalduse täiustused
Funktsioonide haldus võimaldab teil nüüd lubada kõik uued funktsioonid vaikimisi, nõuda funktsiooni lubamiseks kinnitust ja lubada kõik funktsioonid, mis pole veel lubatud. 


## <a name="purchase-agreement-responsible-party"></a>Ostulepingu vastutav isik
Nüüd on teil võimalus määratleda esmased ja teisesed vastutavad osapooled ostulepingu klassifikatsioonivormil ja tulenevatel ostulepingutel.  See annab lepingute järelevalvet teostavale kasutajale juurdepääsu.

## <a name="rfq-link-on-the-purchase-order-line"></a>Pakkumiskutse link ostutellimuse real
Saate lisada ostutellimuse reale viitava lingi vastavale pakkumiskutse reale, kust need pärit on, võimaldades kasutajal hõlpsasti vaadata täiendavat pakkumiskutse dokumenti.

## <a name="additional-resources"></a>Lisaressursid

### <a name="bug-fixes"></a>Veaparandused
Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.6 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Platvormivärskendus update 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 sisaldab Platform update'i 30. Lisateavet Platform Update 30 kohta leiate teemast [Mis on uut või muudetud rakenduses Platform Update'is 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365 2019. aasta väljalaske 2. voo plaan
Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake teemat [Dynamics 365: 2019. aasta väljalaske 2. voo plaan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md) kirjeldatakse funktsioone, mis on eemaldatud või aegunud või kavandatakse eemaldada Supply Chain Managementist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest, teavitatakse aegumisest 12 kuud ette teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md).

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.
