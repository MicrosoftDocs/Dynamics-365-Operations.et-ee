---
title: Dynamics 365 Commerce’i liivakastikeskkonna ettevalmistamine
description: See artikkel selgitab, kuidas valmis demo- Microsoft Dynamics 365 Commerce või kaustakasutust koos sisseehitatud demoandmetega ette kasutada.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 1fc50f98055f1df72d255a5be6e863570564b183
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283637"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commerce’i liivakastikeskkonna ettevalmistamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas kasutada mestiboksi Microsoft Dynamics 365 Commerce keskkonda demokasutuseks sisseehitatud demoandmetega. Tootmiskeskkonna seadistamise protsess on sarnane, kuid täpsustab seda, kuna demoandmetes on juba esitatud paljud eeltingimuseks olevad keskkonnad.

Enne alustamist soovitame teil selle artikli kaudu kiiresti skannida, et saada aimu, mida protsess nõuab.

Commerceboxi keskkonna edukaks ettevalmistamiseks peate täpsustama mõned keskkonna ja Commerce Scale Uniti (CSU) parameetrid, mida kasutatakse Äri hilisemal eraldise puhul. Selle artikli juhised kirjeldavad kõiki etappe, mis on vajalikud selleks, et ettevalmistamine lõpule viia, ja parameetreid, mida peate kasutama.

Pärast Ärikeskkonna edukat ettevalmistamist peate selle kasutamiseks sooritama mõned järelettevalmistamise sammud. Sõltuvalt kasutatava süsteemi aspektidest on mõned sammud valikulised. Võite valikulised etapid alati hiljem läbida.

Lisateavet Ärikeskkonna konfigureerimise kohta pärast selle ülesseadmist vt [Commerceboxi keskkonna konfigureerimine](cpe-post-provisioning.md). Lisateavet rakenduse Commerce keskkonna valikuliste funktsioonide konfigureerimise kohta vt [Commerceboxi keskkonna valikuliste funktsioonide konfigureerimisest](cpe-optional-features.md).

## <a name="prerequisites"></a>Eeltingimused

Enne Commerce’i keskkonna kasutamist peavad olema täidetud järgmised eeltingimused:

- Teil on juurdepääs Microsoft Dynamicsi portaalile Lifecycle Services (LCS).
- Te olete olemasolev Microsoft Dynamics 365 partner või klient ning teil on juba loodud rakendusprojekt, mis on LCS-s kasutamiseks juba loodud.  
- Olete loonud Azure Active Directory (Azure AD) turvagrupi, mida saab kasutada Commerce’i süsteemi administraatorigrupina ja teil on selle ID saadaval.
- Olete loonud turvagrupi Azure AD, mida saab kasutada hinnangute ja ülevaatete moderaatori grupina ja teil on selle ID saadaval. (See turvagrupp võib olla sama mis Commerce’i süsteemi administraatorigrupp.)
- Juurutanud peakontori eksemplari LCS-i sees. Lisateavet vt teemast Uue [keskkonna juurutamine](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Pange tähele, et see loend pole ammendav. Kui teil ilmneb mõni probleem, peaksite abi saamiseks pöörduma oma Microsofti partneri kontakti poole.

## <a name="provision-your-commerce-environment"></a>Ärikeskkonna ettevalmistamine

Järgmistes protseduurides selgitatakse, kuidas ärikeskkonda ette näha. Pärast sammude edukat lõpule viimist on ärikeskkond konfigureerimiseks valmis. Kõik allpool kirjeldatud sammud toimuvad LCS-i portaalis.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Uniti (pilv) lähtestamine

CSU lähtestamiseks tehke järgmist.

1. LCS-s valige loendist oma keskkond.
1. **Valige paremal vaates ENVIRONMENTS** täielikud **üksikasjad**. Ilmub keskkonna üksikasjade vaade.
1. Jaotises Keskkonna **haldamine jaotises** KESKKONNAFUNKTSIOONID **valige** Haldamine **·**.
1. Vahekaardil Commerce **Scale Units (** Äriskaala ühikud) tehke valik **Initialize (Lähtesta**). Kuvatakse **kaaluühiku** lisamise vaade.
1. **Väljal REGION** valige piirkond, mis on sama või lähedal regioonile, kus te juurutaste keskkonna.
1. **Ripploendist** Versioon valige uusim saadav versioon.
1. Valige **Lähtesta**.
1. Valige hoiatusdialoogiaknas, kus soovite kinnitada Commerce Scale Uniti lähtestamise, valik **Jah**. CSU on nüüd uuesti väljastatav.
1. Enne jätkamist veenduge, et teie CSU olek on **edukas**. Lähtestamiseks kulub umbes kaks kuni viis tundi.

Kui te ei leia keskkonna üksikasjade vaates linki **Halda**, võtke abi saamiseks ühendust oma Microsofti kontaktiga.

### <a name="initialize-e-commerce"></a>E-kaubanduse lähtestamine

Äri lähtestamiseks järgige neid samme.

1. Vahekaardil **E-kaubandus** valige **Seadistus**.
1. Sisestage nimi väljale **E-kaubanduse keskkonna nimi**. Võtke arvesse, et see nimi on nähtav mõnes URL-is, mis viitavad teie e-kaubanduse eksemplarile.
1. Väljal **Commerce Scale Uniti nimi** valige loendist oma CSU. (Loendis peaks olema ainult üks valik.)

    Väli **E-kaubanduse geograafia** määratakse automaatselt.

1. Jätkamiseks valige nupp **Edasi**.
1. Väljale **Toetatud hostinimed** mis tahes kehtiv domeen, nt `www.fabrikam.com`.
1. Sisestage väljale **AAD turberühm süsteemiadministraatorile** turberühma nime paar esimest tähemärki, mida soovite kasutada, ja seejärel valige suurendusklaasi sümbol otsingutulemuste kuvamiseks. Valige loendist õige turberühm.
1.  Sisestage väljale **AAD turberühm hinnangute ja arvustuse moderaatorile** turberühma nime paar esimest tähemärki, mida soovite kasutada, ja seejärel valige suurendusklaasi sümbol otsingutulemuste kuvamiseks. Valige loendist õige turberühm.
1. Jätke suvandi **Hinnangute ja arvustuse teenuse lubamine** väärtuseks **Jah**.
1. Valige **Lähtesta**. Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **e-kaubandus** on valitud. E-kaubanduse lähtestamine on käivitatud.
1. Enne jätkamist oodake, kuni Commerce’i lähtestamise olek on **EDUKAS**.
1. All paremal jaotises **Lingid** märkige järgmiste linkide URL-id:

    * **E-kaubanduse sait** – link teie e-kaubanduse saidi juurele.
    * **E-kaubanduse saidiehitaja** – link saidi halduse tööriistale.

## <a name="next-steps"></a>Järgmised etapid

Commerce’i keskkonna ettevalmistamise ja konfigureerimise jätkamiseks vaadake teemat [Rakenduse Commercebox keskkonna konfigureerimine](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Lisaressursid

[Einfo Dynamics 365 Commerce keskkonna konfigureerimine](cpe-post-provisioning.md)

[BOPIS-i konfigureerimine Dynamics 365 Commerce sisendkausta keskkonnas](cpe-bopis.md)

[Valikuliste funktsioonide konfigureerimine kausta Dynamics 365 Commerce keskkonna jaoks](cpe-optional-features.md)

[Microsofti elutsükli teenused (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (pilv)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure'i portaal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
