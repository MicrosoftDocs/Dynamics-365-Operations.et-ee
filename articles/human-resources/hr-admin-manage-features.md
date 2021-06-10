---
title: Lahenduse Human Resources funktsioonide haldamine
description: Saage teada, kuidas lülitada uusi funktsioone rakenduses Dynamics 365 Human Resources sisse või välja.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9454125428a0bb9b8d60d8e1733f7e56144d4a3e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058532"
---
# <a name="manage-features-in-human-resources"></a>Lahenduse Human Resources funktsioonide haldamine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduse Microsoft Dynamics 365 Human Resources pidevate uute võimaluste levitamise osana tahame, et kliendid saaksid proovida uusi funktsioone niipea kui võimalik. Pakume uusi eelvaatefunktsioone, mis on peaaegu valmis üldiseks kasutamiseks ja on läbinud põhjalikud kontrollid. Eelvaatefunktsioonide puhul soovime saada täiendavat kasutajate tagasidet ja kinnitust, enne kui funktsioonid üldiselt kättesaadavaks teeme.

Lisateavet Human Resourcesi uute funktsioonide kohta vt teemast [Mis on uut rakenduses Human Resources](hr-admin-whats-new.md) ja [Dynamics 365 ja Power Platformi väljalaskeplaan](/dynamics365/release-plans/?panel=products1#pivot=products).

Tööruumis **Funktsioonihaldus** on toodud loend igas väljaandes saadetud funktsioonidest. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks. Lisateavet funktsioonihalduse kohta vt [Funktsioonihalduse ülevaade](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Kõik uued funktsioonid jäävad vähemalt 30 päevaks eelvaatesse ja tavaliselt 30–60 päevaks. Peamised funktsioonid on tavaliselt saadaval eelvaate perioodile järgneva iga aasta oktoobris ja aprillis. Kohe kui näete tööruumis **Funktsioonihaldus** uusi võimalusi, saate need sisse lülitada. Mõned funktsioonid võivad olla vaikimisi sisse lülitatud.

Kui funktsioon on üldsusele saadaval, võib selle tootmiskeskkonnas sisse või välja lülitada. Tööruum **Funktsioonihaldus** näitab, millal muutub eelvaate funktsioon kohustuslikuks. See kuupäev on tavaliselt 1. oktoobril või 1. aprillil, et ühitada poolaasta väljalaskeplaanidega. Kohustuslikke funktsioone välja lülitada ei saa. Kuni see muutub kohustuslikuks, saate funktsiooni kõikides keskkondades sisse ja välja lülitada.

## <a name="enable-or-disable-preview-features"></a>Eelvaatefunktsioonide lubamine või keelamine

Eelvaatefunktsioonidele ligipääsemiseks peate kõigepealt need oma keskkonnas lubama. Eelvaatefunktsioonide lubamine või keelamine sõltub keskkonnast.

> [!IMPORTANT]
> Eelvaatefunktsioonid on saadaval ainult keskkondades **Liivakast**. Kui lülitate eelvaatefunktsiooni sisse, siis lubate selle kõikidele teie organisatsiooni kasutajatele, kes on selles keskkonnas. Kui lülitate eelvaatefunktsiooni välja, siis keelate selle ja teie kasutajatel pole sellele juurdepääsu. Eelvaatefunktsioonidel on rakenduses Human Resources piiratud tugi. Need võivad kasutada vähem privaatsus- ja turbemeetmeid ning pole hõlmatud teenuse Human Resources teenindustaseme lepingus (SLA). Eelvaatefunktsioone ei tohi kasutada isikuandmete (st igasugused andmed, mis võimaldavad isikut tuvastada) ega muude andmete töötlemiseks, millele kehtivad seaduste või regulatsioonide järgmise nõuded.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Valige paan **Funktsioonihaldus**.

3. Eelvaatefunktsiooni lubamiseks valige see loendist ja seejärel valige käsk **Luba**. Eelvaatefunktsiooni keelamiseks valige see loendist ja seejärel valige käsk **Keela**.

## <a name="enable-or-disable-benefits-management"></a>Soodustuste halduse lubamine või keelamine

Soodustuste halduse lubamiseks kasutage sama protseduuri jaotises [Eelvaatefunktsioonide lubamine või keelamine](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Keskkonnas **Tootmine** ei saa soodustuste haldust keelata, kui olete selle lubanud. Soodustuste halduse saate keelata **Liivakasti** keskkondades.

Lisateavet soodustuste halduse konfiguratsiooni ja kasutamise kohta vt teemast [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

Soodustuste haldus asendab funktsiooni tööruumis **Soodustused**. Kui lubate soodustuste halduse eelvaatefunktsiooni, ei saa te enam kasutada tööruumi **Soodustused** järgmisi vorme:

- **Soodustused**
- **Soodustuse elemendid**
- **Panuse arvutamise määrad**
- **Soodustuse registreerimise tulemused**
- **Soodustuse aegunuks märkimise ja pikendamise tulemused**
- **Soodustuskõlblikkuse poliitika reegli tüübid**
- **Soodustuse saamise õiguse eeskirjad**
- **Kõlblikkuse sündmused**

Saate kuvada nende vormi teabe ainult kirjutuskaitstud režiimis. Kui soovite teavet redigeerida, peake kõigepealt keelama soodustuste halduse (kohaldatav ainult **Liivakasti** keskkondades).

## <a name="enable-or-disable-leave-and-absence"></a>Puhkuste ja puudumiste lubamine või keelamine

Puhkuste ja puudumiste lubamiseks kasutage sama protseduuri jaotises [Eelvaatefunktsioonide lubamine või keelamine](hr-admin-manage-features.md?enable-or-disable-preview-features).

> [!IMPORTANT]
> Te ei saa keelata funktsiooni **Mitme puhkuse tüüp** Puhkuste ja puudumiste korral pärast selle lubamist. See kehtib nii **Liivakasti** kui ka **Tootmise** keskkondade korral.

Lisateavet Puhkuste ja puudumiste eelvaatefunktsioonide kohta vt [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

## <a name="send-us-feedback"></a>Tagasiside saatmine

Ootame teie tagasisidet teie kogemuse kohta nende eelvaatefunktsioonidega. Soovitame teil postitada tagasisidet nende või muude funktsioonide kasutamise kohta järgmistel saitidel.

- [Kogukonna foorum](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – sellel saidil on mitmeid ressursse ning kasutajad saavad arutada kasutusjuhtumeid, küsida küsimusi ja otsida kogukonnalt abi.
- Andke meile teada funktsioonidest, mida soovite tootes näha, või andke teada muudatustest, mida teie arvates oleks olemasolevates funktsioonides vaja. Pakkuge tooteideid asukohas [Rakenduse Human Resources ideed](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources).
    
Ärge kasutage tagasisides ega tootearvustustes isikuandmeid (igasugused andmed, mis võimaldavad isikut tuvastada). Kogutud teavet võidakse põhjalikumalt analüüsida ja seda ei kasutata kohalduvate isikuandmete kaitse seaduste järgi taotluste täitmiseks. Isikuandmetele, mida kogutakse eraldi nende programmidega, kehtib [Microsofti privaatsusavaldus](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Vt ka

- [Mis on rakenduses Human Resources uut?](hr-admin-whats-new.md)
- [Dynamics 365 ja Power Platformi väljalaskeplaan](/dynamics365/release-plans/?panel=products1#pivot=products)

[!INCLUDE[footer-include](../includes/footer-banner.md)]