---
title: Dynamics 365 Commerce'i hindamisekeskkonna ettevalmistamine
description: Selles teemas selgitatakse, kuidas valmistada ette rakenduses Microsoft Dynamics 365 Commerce hindamiskeskkond.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b675d4af6fb9a080f3f3a13e64b2c5b6ad4b783
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022418"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce'i hindamisekeskkonna ettevalmistamine

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas valmistada ette rakenduses Microsoft Dynamics 365 Commerce hindamiskeskkond.

Enne alustamist soovitame teil see teema kiiresti läbi vaadata, et saada protsessi nõudmistest aimu.

> [!NOTE]
> Commerce'i hindamiskeskkonnad pole üldiselt kättesaadavad ja antakse partneritele ning klientidele taotluse alusel. Lisateabe saamiseks pöörduge oma Microsofti partneri kontakti poole.

Oma Commerce’i hindamiskeskkonna edukaks ettevalmistamiseks peate looma projekti, millel on kindel toote nimi ja tüüp. Keskkonnal ja Commerce Scale Unitil (CSU) on samuti mõned konkreetsed parameetrid, mida peate kasutama, kui loodate hiljem e-kaubandust ette valmistada. Selle teema juhised kirjeldavad kõiki vajalikke etappe, mida on vaja ettevalmistamise lõpuleviimiseks, ja milliseid parameetreid peate kasutama.

Pärast seda, kui olete oma Commerce’i hindamiskeskkonna edukalt ette valmistanud, peate viima lõpule mõned ettevalmistamisjärgsed etapid selle kasutamiseks valmistumiseks. Mõned etapid on valikulised, olenevalt sellest, milliseid süsteemi aspekte soovite hinnata. Võite valikulised etapid alati hiljem läbida.

Teavet selle kohta, kuidas Commerce’i hindamiskeskkonda pärast ettevalmistamist konfigureerida, vaadake teemast [Commerce’i hindamiskeskkonna konfigureerimine](cpe-post-provisioning.md). Teavet selle kohta, kuidas Commerce’i hindamiskeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i hindamiskeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).

## <a name="prerequisites"></a>Eeltingimused

Enne Commerce’i hindamiskeskkonna ettevalmistamist peavad olema kehtestatud järgmised eeltingimused.

- Teid on teavitatud hindamisprogrammist ja teile on antud hindamiskeskkonna suutlikkus.
- Teil on juurdepääs Microsoft Dynamicsi portaalile Lifecycle Services (LCS).
- Olete olemasolev Microsoft Dynamics 365 partner või klient ja olete võimeline looma Dynamics 365 Commerce’i projekti.
- Teil on administraatori juurdepääs Microsoft Azure'i kordustellimusele või teil on võimalik võtta ühendust kordustellimuse administraatoriga, kes saab vajadusel teid abistada.
- Teie Azure Active Directory (Azure AD) rentniku ID on saadaval.
- Olete loonud Azure AD turberühma, mida saab kasutada e-kaubanduse süsteemiadministraatorite grupina ja mille ID on saadaval.
- Olete loonud Azure AD turberühma, mida saab kasutada hinnangute ja arvustuste moderaatori grupina ja mille ID on saadaval. (See turberühm võib olla sama, mis e-kaubanduse süsteemiadministraatorite grupp.)

Pange tähele, et see loend pole ammendav. Kui teil ilmneb mõni probleem, peaksite abi saamiseks pöörduma oma Microsofti partneri kontakti poole.

## <a name="provision-your-commerce-evaluation-environment"></a>Oma Commerce’i hindamiskeskkonna ettevalmistamine

Need protseduurid selgitavad, kuidas valmistada ette Commerce’i hindamiskeskkonda. Pärast nende edukat lõpule viimist on Commerce’i hindamiskeskkond konfigureerimiseks valmis. Kõik siin kirjeldatud tegevused esinevad LCS portaalis.

### <a name="create-a-new-project"></a>Loo uus projekt

LCS-is uue projekti loomiseks toimige järgmiselt.

1. LCS-i avalehel valige projekti loomiseks plussmärk (**+**).
1. Parempoolsel paanil järgige ühte järgmistest etappidest.

    - Kui olete partner, valige suvand **Migreerimine, lahenduste loomine ja teave**.
    - Kui olete klient, valige suvand **Potentsiaalsed eelmüügid**.

1. Sisestage nimi, kirjeldus ja valdkond.
1. Valige väljal **Toote nimi** suvand **Dynamics 365 Commerce**.
1. Valige väljal **Toote versioon** suvand **Dynamics 365 Commerce**.
1. Väljal **Metoodika** valige **Dynamics Retail juurutamise metoodika**.
1. Valikuline: võite portida rollid ja kasutajad olemasolevast projektist.
1. Valige **Loo**. Kuvatakse projekti vaade.

### <a name="add-the-azure-connector"></a>Azure’i konnektori lisamine

Azure'i konnektori lisamiseks oma LCS-i projekti, järgige etappe teemas [Azure Resource Manageri (ARM) sisseelamisprotsessi lõpule viimine](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).

### <a name="deploy-the-environment"></a>Keskkonna juurutamine

Keskkonna juurutamiseks tehke järgmist.

> [!NOTE]
> Võimalik, et te ei pea samme 6, 7 ja/või 8 läbima, kuna ühe suvandi ekraanid jäetakse vahele. Kui olete vaates **Keskkonna parameetrid**, kinnitage, et tekst **Dynamics 365 Commerce (eelvaade) – demo (10.0.* x* platvormi värskendus *xx*)** kuvatakse otse välja **Keskkonna nimi** kohal. Üksikasju vt jooniselt, mis kuvatakse pärast sammu 8.

1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Valige suvand **Lisa** keskkonna lisamiseks.
1. Väljal **Rakenduse versioon** valige uusim versioon. Kui teil on konkreetne vajadus valida rakenduse versioon, mis ei ole kõige uuem versioon, ärge valige varasemat versiooni kui **10.0.14**.
1. Kasutage väljal **Platvormi versioon** platvormi versiooni, mis valitakse automaatselt valitud rakenduse versiooni jaoks. 

    ![Rakenduse ja platvormi versioonide valimine](./media/project1.png)

1. Valige **Edasi**.
1. Valige keskkonna topoloogiaks **Demo**.

    ![Keskkonna topoloogia valimine 1](./media/project2.png)

1. Lehel **Keskkonna juurutamine** sisestage keskkonna nimi. Jätke täpsemad sätted nii nagu need on.

    ![Keskkonna juurutamise leht](./media/project4.png)

1. Kohandage VM-i suurust vastavalt vajadusele. (Soovitame VM-i varude arvestusühikut \[SKU\] **D13 v2**.)
1. Vaadake üle hinnakujunduse ja litsentsimise tingimused ning märkige ruut, et näidata, et olete nendega nõus.
1. Valige **Edasi**.
1. Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Juuruta**. Olete naasnud vaatesse **Pilve majutatud keskkonnad** ja teie keskkond peaks ilmuma loendis.

    Teie soovitud keskkond ilmub järjekorras ja seejärel juurutatakse. Keskkonna töövoogude lõpule viimine võtab aega. Seetõttu kontrollige umbes kuue kuni üheksa tunni pärast uuesti.

1. Enne jätkamist veenduge, et teie keskkonna olek oleks **Juurutatud**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Uniti (pilv) lähtestamine

CSU lähtestamiseks tehke järgmist.

1. Vaates **Pilve majutatud keskkonnad** valige loendist oma keskkond.
1. Valige paremal olevast keskkonna vaatest **Täielik teave**. Ilmub keskkonna üksikasjade vaade.
1. Jaotises **Keskkonna funktsioonid** valige käsk **Halda**.
1. Vahekaardil **Kaubandus** valige käsk **Lähtesta**. Ilmub CSU lähtestamise parameetrite vaade.
1. Valige väljal **Piirkond** see piirkond, mis on sama või asub selle piirkonna lähedal, kuhu te keskkonna juurutasite.
1. Ärge muutke välja **Versioon**.
1. Valige **Lähtesta**.
1. Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Jah**. Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **Kaubandus** on valitud. Teie CSU on ettevalmistamiseks ootele pandud.
1. Enne jätkamist veenduge, et teie CSU olek oleks **Õnnestus**. Lähtestamiseks kulub umbes kaks kuni viis tundi.

Kui te ei leia keskkonna üksikasjade vaates linki **Halda**, võtke abi saamiseks ühendust oma Microsofti kontaktiga.

Juurutamisprotsessi käigus võite saada järgmise tõrketeate.

> Hindamiskeskkonnad (demo/test) peavad peakontoris registreerima skaalaüksuse konnektori rakenduse \<application ID\>.

Kui CSU lähtestamine nurjub ja te saate selle tõrketeate, tehke märkus rakenduse ID kohta, mis on globaalne ainuidentifikaator (GUID) ja seejärel järgige järgmise jaotise etappe CSU juurutamise rakenduse registreerimiseks Commerce'i peakontoris.

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>CSU juurutuse rakenduse registreerimine Commerce peakontoris (vajadusel)

CSU juurutuse rakenduse registreerimiseks Commerce'i peakontoris toimige järgmiselt.

1. Avage Commerce'i peakontoris **Süsteemihaldus \> Seadistus \> Azure Active Directory rakendused**.
1. Sisestage veergu **Kliendi ID** rakenduse ID saadud CSU lähtestamise tõrketeatest.
1. Sisestage veergu **Nimi** mistahes kirjeldav tekst (nt **CSU hinnang**).
1. Sisestage veergu **Kasutaja ID** väärtus **RetailServiceAccount**.
1. Proovige CSU lähtestamist ja LCS-i juurutamist uuesti.

### <a name="initialize-e-commerce"></a>E-kaubanduse lähtestamine

E-kaubanduse lähtestamiseks tehke järgmist.

1. Vahekaardil **E-kaubandus** vaadake üle hindamise nõusolek ja seejärel valige suvand **Seadistus**.
1. Sisestage nimi väljale **E-kaubanduse keskkonna nimi**. Võtke arvesse, et see nimi on nähtav mõnes URL-is, mis viitavad teie e-kaubanduse eksemplarile.
1. Väljal **Commerce Scale Uniti nimi** valige loendist oma CSU. (Loendis peaks olema ainult üks valik.)

    Väli **E-kaubanduse geograafia** määratakse automaatselt.

1. Jätkamiseks valige nupp **Edasi**.
1. Väljale **Toetatud hostinimed** mis tahes kehtiv domeen, nt `www.fabrikam.com`.
1. Sisestage väljale **AAD turberühm süsteemiadministraatorile** turberühma nime paar esimest tähemärki, mida soovite kasutada, ja seejärel valige suurendusklaasi sümbol otsingutulemuste kuvamiseks. Valige loendist õige turberühm.
1.  Sisestage väljale **AAD turberühm hinnangute ja arvustuse moderaatorile** turberühma nime paar esimest tähemärki, mida soovite kasutada, ja seejärel valige suurendusklaasi sümbol otsingutulemuste kuvamiseks. Valige loendist õige turberühm.
1. Jätke suvandi **Hinnangute ja arvustuse teenuse lubamine** väärtuseks **Jah**.
1. Valige **Lähtesta**. Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **e-kaubandus** on valitud. E-kaubanduse lähtestamine on käivitatud.
1. Enne jätkamist oodake, kuni teie e-kaubanduse lähtestamise olek on **Lähtestamine edukas**.
1. All paremal jaotises **Lingid** märkige järgmiste linkide URL-id:

    * **E-kaubanduse sait** – link teie e-kaubanduse saidi juurele.
    * **E-kaubanduse saidiehitaja** – link saidi halduse tööriistale.

## <a name="next-steps"></a>Järgmised etapid

Oma Commerce’i hindamiskeskkonna ettevalmistamise ja konfigueerimise protsessi jätkamiseks vaadake teemat [Commerce’i hindamiskeskkonna konfigureerimine](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce'i hindamiskeskkonna ülevaade](cpe-overview.md)

[Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine](cpe-post-provisioning.md)

[BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas](cpe-bopis.md)

[Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md)

[Dynamics 365 Commerce'i hindamiskeskkonna KKK](cpe-faq.md)

[Microsofti elutsükli teenused (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (pilv)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure'i portaal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]