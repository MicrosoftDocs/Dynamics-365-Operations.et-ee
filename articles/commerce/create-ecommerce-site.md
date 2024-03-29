---
title: E-kaubanduse saidi loomine
description: See artikkel kirjeldab samme ja teavet, mida on vaja uue e-kaubanduse saidi loomiseks saidikonstruktoris Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: ea9afd89ce9ff79edbe5bff609b9843026005493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270233"
---
# <a name="create-an-e-commerce-site"></a>E-kaubanduse saidi loomine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab samme ja teavet, mida on vaja uue e-kaubanduse saidi loomiseks saidikonstruktoris Dynamics 365 Commerce.

Kui litsentsite Dynamics 365 Commerce'i võimalusi, valmistatakse saidiehitaja ette koos alustussaidiga, mida saate kasutada oma saidi alusena. Kui aga soovite alustada nullist või luua teise saidi, tuleb teil luua uus sait saidi autorluse keskkonnas. 

## <a name="site-creation-prerequisites"></a>Saidi loomise eeltingimused

Saidikonstruktori kasutajal peab olema Microsofti Azure Active Directory (Azure AD) Azure AD kasutajakonto, mis kuulub e-commerce’i süsteemi administraatoritele turvagruppi. Lisateavet vt teemast Uue e-äri [rentniku juurutamine](deploy-ecommerce-site.md).

> [!NOTE]
> Azure AD Külaliskasutajatel võivad olla teie rentnikus erinevad juurdepääsuõigused Azure AD. Isegi kui see Azure AD on kaasatud e-äri süsteemi administraatoritele määratud turvagruppi, Azure AD **võib** külaliskasutaja äris e-äri saidi loomiseks vajada väliste kasutajate õiguste sätete korrigeerimist. 

Väliste Azure AD **kasutajate sätete korrigeerimiseks** järgige neid samme.

1. Azure’i portaalis navigeerige oma rentnikuni Azure AD.
1. Minge kasutajasätete **\> väliste kasutajate ja** valige link **Välise koostöö sätete** haldamine. See avab välise **koostöö sätete lehe**, kus saab seada külaliskasutaja juurdepääsu, külalise kutse sätteid ja koostööpiiranguid. 
1. Korrigeerige välis koostöösätteid vastavalt teie ettevõtte turvapoliitikale. 

## <a name="set-up-your-site"></a>Saidi seadistamine

Oma saidi seadistamiseks tehke järgmist.

1. Avage saidiehitaja keskkond. Saidiehitaja lingi leiate Commerce'i keskkonna funktsioonide lehel Microsoft Lifecycle Services (LCS) alt.
1. Valige saidi autorluse keskkonna avalehel suvand **Uus sait**.
1. Sisestage dialoogiboksi **Uus sait** järgmine teave.

| Väli                               | Kirjeldus |
|-------------------------------------|-------------|
| Saidi nimi                           | Sisestage kuvatav nimi, mida tuleks saidi autorluse keskkonnas teie saidi jaoks kasutada. See nimi on nähtav ainult autorluse keskkonnas ja seda ei kuvata klientidele. |
| Saidi administraatori turberühm | Määrake Microsoft Azure Active Directory (Azure AD) turberühm, mis haldab kasutajaid, kellel on sellel saidil saidi administraatori roll. |
| Vaikekanal (tootmisüksuse number) | Valige veebipood, mille jaoks see sait toimib fassaadina. Kui soovite, et teie e-kaubanduse sait toetaks mitut veebipoodi, peate pärast saidi seadistamist seostama poed oma saidiga jaotises **Saidi sätted** . |
| Vaikekeel                            | Määrake selle veebipoe ja turu vaikekeel. Veebipood võib toetada mitut keelt. Kui soovite selle veebipoe või mõne muu veebipoe jaoks toetada mitut keelt, saate konfigureerida selle toe pärast saidi seadistamist suvandis **Saidi sätted**.  |
| Domeen                              | Valige domeeni nimi, mis toimib selle veebipoe jaoks domeenina. Kui te pole LCS-is ühtegi domeeni konfigureerinud, võite selle välja tühjaks jätta. Pärast domeeni LCS-is konfigureerimist peate lisama selle oma veebipoele suvandis **Saidi sätted**.  |
| Tee                              | Kui teie sait toetab antud domeeninime puhul rohkem kui ühte keelt, kasutage tee välja, et luua selle domeeni ja keele kombinatsiooni jaoks kordumatu saidi URL. Kui keel, mille väljal **Vaikekeel** määrasite, on ainus selle domeeni jaoks toetatav keel või see on pärast saidi täiendavate keelte jaoks lokaliseerimist jätkuvalt vaikekeel, soovitame jätta selle välja tühjaks. |

Pärast saidi loomist saate kontrollida, kas see on teie võrgupoega seotud, valides vahekaardi **Tooted**. Peaksite nägema veebipoele eraldatud toodete valikut. Saate kasutada ka lehe üleval vasakul ripploendit, et pääseda kategooriate põhjal eraldatud toodete juurde.

## <a name="rename-your-site"></a>Nimetage sait ümber

Saidi ümbernimetamiseks saidikonstruktoris järgige neid samme.

1. Saidiloendi vaate avamiseks valige ülemisel **parempoolsel nurgal** saidilüliti ja seejärel valige suvand Halda **saite**. 
1. Valige märkeruut saidi kõrval, mida soovite ümber nimetada ja seejärel valige käsuribal **ümbernimetamine**.
1. Dialoogiaknas **Uus saidi** nimi sisestage uus saidi nimi ja seejärel valige **OK**. Saidi loend uuendab saidi uue nime näitamiseks.

## <a name="delete-a-site"></a>Saidi kustutamine

Saidi kustutamiseks saidikonstruktorist järgige neid samme.

1. Saidiloendi vaate avamiseks valige ülemises **parempoolses nurgas** saidilüliti ja seejärel valige suvand Halda **saite**.
1. Valige sait, mida soovite kustutada ja seejärel valige **käsuribal** Kustuta.
1. **Dialoogiboksis Kustutamine \<site name\>** sisestage saidi nimi ja seejärel valige **kustutamisnimi**.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
