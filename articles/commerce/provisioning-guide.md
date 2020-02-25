---
title: Dynamics 365 Commerce’i eelvaatekeskkonna ettevalmistamine
description: Selles teemas selgitatakse, kuidas valmistada ette Microsoft Dynamics 365 Commerce’i eelvaatekeskkond.
author: psimolin
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cbd4c118de2e91c8849461b20a01403049a07e66
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024632"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Dynamics 365 Commerce’i eelvaatekeskkonna ettevalmistamine


[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas valmistada ette Dynamics 365 Commerce’i eelvaatekeskkond.

Enne alustamist soovitame teil see teema kiiresti läbi vaadata, et saada protsessi nõudmistest aimu.

> [!NOTE]
> Kui te pole veel andnud juurdepääsu rakenduse Dynamics 365 Commerce eelvaatele, saate taotleda eelvaate juurdepääsu [Dynamics 365 Commerce’i veebisaidilt](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Ülevaade

Oma Commerce’i eelvaatekeskkonna edukaks ettevalmistamiseks peate looma projekti, millel on kindel toote nimi ja tüüp. Keskkonnal ja kaubanduse skaala üksusel (CSU) on samuti mõned konkreetsed parameetrid, mida peate kasutama, kui hiljem e-kaubandust ette valmistate. Selle teema juhised kirjeldavad kõiki vajalikke etappe, mida peate ettevalmistamiseks täitma, ja milliseid parameetreid peate kasutada.

Pärast seda, kui olete oma Commerce’i eelvaatekeskkonna edukat ette valmistanud, peate läbima ettevalmistamiseks mõned hilisemad etapid. Mõned etapid on valikulised, olenevalt sellest, milliseid süsteemi aspekte soovite hinnata. Võite valikulised etapid alati hiljem läbida.

Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonda pärast ettevalmistamist konfigureerida, vaadake teemast [Commerce’i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md). Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).

Kui teil on küsimusi ettevalmistamise etappide kohta või esineb probleeme, andke Microsoftile sellest teada [rakenduse Microsoft Dynamics 365 Commerce eelvaate Yammeri grupis](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Eeltingimused

Enne Commerce’i eelvaatekeskkonna ettevalmistamist peavad olema kehtestatud järgmised eeltingimused.

- Teil on juurdepääs Microsoft Dynamicsi portaalile Lifecycle Services (LCS).
- Olete olemasolev Microsoft Dynamics 365 partner või klient ja olete võimeline looma Dynamics 365 Commerce’i projekti.
- Teid on rakenduse Dynamics 365 Commerce eelvaate programmi vastu võetud.
- Teil on vajalikud õigused, et luua projekt suvandile **Migreerimine, lahenduste loomine ja teave**.
- Olete rolli **Keskkonnahaldur** või **Projekti omanik** liige projektis, kus te keskkonna ette valmistate.
- Teil on administraatori juurdepääs oma Microsoft Azure’i tellimusele või olete ühenduses tellimise administraatoriga, kes saab teie nimel lõpetada kaks etappi, mis nõuavad administraatori õigusi.
- Teie Azure Active Directory (Azure AD) rentniku ID on saadaval.
- Olete loonud Azure AD turberühma, mida saab kasutada e-kaubanduse süsteemiadministraatorite grupina ja mille ID on saadaval.
- Olete loonud Azure AD turberühma, mida saab kasutada hinnangute ja arvustuste moderaatori grupina ja mille ID on saadaval. (See turberühm võib olla sama, mis e-kaubanduse süsteemiadministraatorite grupp.)

## <a name="provision-your-commerce-preview-environment"></a>Oma Commerce’i eelvaatekeskkonna ettevalmistamine

Need protseduurid selgitavad, kuidas valmistada ette Commerce’i eelvaatekeskkonda. Pärast nende edukat lõpetamist on Commerce’i eelvaatekeskkond konfigureerimiseks valmis. Kõik siin kirjeldatud tegevused esinevad LCS portaalis.

> [!IMPORTANT]
> Eelvaate juurdepääs on seotud LCS-i konto ja organisatsiooniga, mille määrasite oma Commerce’i eelvaate rakenduses. Peate kasutama Commerce’i eelvaatekeskkonna ettevalmistamiseks sama kontot. Kui peate kasutama Commerce’i eelvaatekeskkonna jaoks erinevat LCS-i kontot või rentnikku, peate teavitama Microsofti nendest üksikasjadest. Kontaktandmete jaoks vaadake selles teema jaotist [Commerce’i eelvaatekeskkonna tugi](#commerce-preview-environment-support).

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Kinnitamine, et eelvaate funktsioonid on saadaval ja LCS-is sisse lülitatud

Kinnitamaks, et eelvaate funktsioonid on saadaval ja LCS-is sisse lülitatud, tehke järgmist

1. Logige [LCS-i portaali](https://lcs.dynamics.com)sisse, kasutades sama LCS-i kontot, mida kasutasite eelvaatele juurdepääsu taotlemiseks.
1. Kerige LCS-i avalehel täielikult paremale ja valige paan **Eelvaate funktsiooni haldamine**.

    ![Eelvaate funktsiooni paan](./media/preview1.png)

1. Kerige alla jaotisesse **Privaatsed eelvaate funktsioonid** ja kinnitage, et järgmised funktsioonid oleksid saadaval ja sisse lülitatud.

    - E-kaubanduse hindamine
    - Kaubanduse eelvaate programmi keskkonnad

    ![Privaatse eelvaate funktsioonid](./media/preview2.png)

1. Kui need funktsioonid loendis ei ilmu, võtke Microsoftiga ühendust ja andke oma töö meiliaadress, LCS-i konto ja rentniku üksikasjad. Kontaktandmete jaoks vaadake jaotist [Commerce’i eelvaatekeskkonna tugi](#commerce-preview-environment-support).

### <a name="create-a-new-project"></a>Loo uus projekt

LCS-is uue projekti loomiseks toimige järgmiselt.

1. LCS-i avalehel valige projekti loomiseks plussmärk (**+**).
1. Parempoolsel paanil järgige ühte järgmistest etappidest.

    - Kui olete partner, valige suvand **Migreerimine, lahenduste loomine ja teave**.
    - Kui olete klient, valige suvand **Potentsiaalsed eelmüügid**.

1. Sisestage nimi, kirjeldus ja valdkond.
1. Valige väljal **Toote nimi** suvand **Dynamics 365 Retail**.
1. Valige väljal **Toote versioon** suvand **Dynamics 365 Retail**.
1. Väljal **Metoodika** valige **Dynamics Retail juurutamise metoodika**.
1. Valikuline: võite portida rollid ja kasutajad olemasolevast projektist.
1. Valige **Loo**. Kuvatakse projekti vaade.

### <a name="add-the-azure-connector"></a>Azure’i konnektori lisamine

Oma LCS-i projektile Azure’i konnektori lisamiseks toimige järgmiselt.

1. Järgige üht neist sammudest.

    - Kui olete partner, valige paan **Projekti sätted** kõige parempoolsemal küljel.
    - Kui olete klient, valige suvand **Projekti sätted** ülemisest menüüst.

1. Valige suvand **Azure’i konnektorid**.
1. Azure’i konnektori lisamiseks valige suvand **Lisa**.
1. Sisestage nimi.
1. Sisestage oma Azure’i tellimuse ID.
1. Lülitage suvand **Azureʼi ressursihalduri (ARM) kasutamise konfigureerimine** sisse
1. Veenduge, et väärtus **Azure’i kordustellimuse AAD rentniku domeen (või ID)** oleks õige. Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.
1. Valige **Edasi**.
1. Järgige lehel kuvatavaid juhiseid, et anda nõutud rakendustele juurdepääs teie tellimusele. Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.

    1. Logige sisse [Azure’i portaali](https://portal.azure.com/).
    1. Veenduge, et valitud oleks õige kaust, ja seejärel valige vasakpoolsel menüül suvand **Tellimused**
    1. Leidke loendist õige tellimus ja valige see. Vastavalt vajadusele kasutage otsingufunktsiooni.
    1. Valige menüüs suvand **Juurdepääsu juhtelement (IAM)**.
    1. Valige paremal küljel jaotises **Lisa rollimäärang** käsk **Lisa**. Kuvatakse paan **Lisa rollimäärang**.
    1. Valige väljalt **Roll** väärtus **Kaasautor**.
    1. Jätke väljale **Määra juurdepääs** vaikeväärtus **Azure AD kasutaja, grupp või teenusesubjekt**.
    1. Jaotisesse **Vali** sisestage **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Valige loendist **Dynamicsi juurutamise teenused \[wsfed-enabled\]**.
    1. Valige käsk **Salvesta**.

1. Valige **Edasi**.
1. Järgige lehel kuvatavaid juhiseid, et anda nõutud rakendustele juurdepääs teie tellimusele. Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.
1. Valige **Edasi**.
1. Väljal **Azure’i regioon** valige **Ida-USA**, **Ida-USA 2**, **Lääne-USA** või **Lääne-USA 2**.
1. Valige käsk **Ühenda**. Teie Azure'i konnektor peaks loendis ilmuma.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Commerce’i eelvaate demobaasi laiendi importimine

Commerce’i eelvaate demobaasi laiendi oma projekti importimiseks toimige järgmiselt.

1. Avage oma projekti avaleht, valides ülaosas projekti nime.
1. Järgige üht neist sammudest.

    - Kui olete partner, valige paan **Varateek** kõige parempoolsemal küljel.
    - Kui olete klient, valige suvand **Varateek** ülemisest menüüst.

1. Valige vasakpoolses loendis suvand **Tarkvara juurutatav pakett**.
1. Valige **Impordi**.
1. Jaotises **Jagatud varateek** valige varade loendist suvand **Commerce’i eelvaate demobaasi laiend**.
1. Valige käsk **Võta**. Naasete varateeki ja peaksite nägema laiendit loendis.

Järgmisel joonisel on näha tegevused, mis tuleb teha LCS-i lehel **Varateek**.

![Commerce’i eelvaate demobaasi laiendi importimine](./media/import.png)

### <a name="deploy-the-environment"></a>Keskkonna juurutamine

Keskkonna juurutamiseks tehke järgmist.

> [!NOTE]
> Võimalik, et te ei pea samme 6, 7 ja/või 8 läbima, kuna ühe suvandi ekraanid jäetakse vahele. Kui olete vaates **Keskkonna parameetrid**, kinnitage, et tekst **Dynamics 365 Commerce (eelvaade) – demo (10.0.* x* platvormi värskendus *xx*)** kuvatakse otse välja **Keskkonna nimi** kohal. Üksikasju vt jooniselt, mis kuvatakse pärast sammu 8.

1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Valige suvand **Lisa** keskkonna lisamiseks.
1. Väljal **Rakenduse versioon** valige uusim versioon. Kui teil on konkreetne vajadus valida rakenduse versioon, mis ei ole kõige uuem versioon, ärge valige varasemat versiooni kui **10.0.8**.
1. Kasutage väljal **Platvormi versioon** platvormi versiooni, mis valitakse automaatselt valitud rakenduse versiooni jaoks. 

    ![Rakenduse ja platvormi versioonide valimine](./media/project1.png)

1. Valige **Edasi**.
1. Valige keskkonna topoloogiaks **Demo**.

    ![Keskkonna topoloogia valimine 1](./media/project2.png)

1. Valige keskkonna topoloogiaks **Dynamics 365 Commerce – Demo**. Kui olete varem konfigureerinud ühe Azure’i konnektori, kasutatakse seda selles keskkonnas. Mitme Azure’i konnektori konfigureerimisel saate valida, millist konnektorit kasutada: **Ida-USA**, **Ida-USA**2 **, Lääne-USA** või **Lääne-USA 2**. (Parima lõppeesmärgini jõudluse saavutamiseks soovitame valida **Lääne-USA 2**.)

    ![Keskkonna topoloogia valimine 2](./media/project3.png)

1. Lehel **Keskkonna juurutamine** sisestage keskkonna nimi. Jätke täpsemad sätted nii nagu need on.

    ![Keskkonna juurutamise leht](./media/project4.png)

1. Kohandage VM-i suurust vastavalt vajadusele. (Soovitame VM-i varude arvestusühikut \[SKU\] **D13 v2**.)
1. Vaadake üle hinnakujunduse ja litsentsimise tingimused ning märkige ruut, et näidata, et olete nendega nõus.
1. Valige **Edasi**.
1. Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Juuruta**. Olete naasnud vaatesse **Pilve majutatud keskkonnad** ja teie keskkond peaks ilmuma loendis.

    Teie soovitud keskkond ilmub järjekorras ja seejärel juurutatakse. Keskkonna töövoogude lõpule viimine võtab aega. Seetõttu kontrollige umbes kuue kuni üheksa tunni pärast uuesti.

1. Enne jätkamist veenduge, et teie keskkonna olek oleks **Juurutatud**.

### <a name="initialize-the-commerce-scale-unit-csu"></a>Kaubanduse skaala üksuse (Commerce Scale Unit, CSU) lähtestamine

CSU-i lähtestamiseks tehke järgmist.

1. Vaates **Pilve majutatud keskkonnad** valige loendist oma keskkond.
1. Valige paremal olevast keskkonna vaatest **Täielik teave**. Ilmub keskkonna üksikasjade vaade.
1. Jaotises **Keskkonna funktsioonid** valige käsk **Halda**.
1. Vahekaardil **Kaubandus** valige käsk **Lähtesta**. Ilmub CSU lähtestamise parameetrite vaade.
1. Väljal **Regioon** valige **Ida-USA**, **Ida-USA 2**, **Lääne-USA** või **Lääne-USA 2**.
1. Väljal **Versioon** valige loendist suvand **Määra versioon** ja määrake seejärel kuvataval väljal **9.18.20014.4**. Määrake kindlasti siin näidatud täpne versioon. Vastasel juhul peate uuendama RCSU hiljem õigele versioonile.
1. Lülitage suvand **Rakenda laiend** sisse.
1. Laiendite loendist valige suvand **Kaubanduse eelvaate demobaasi laiend**.
1. Valige **Lähtesta**.
1. Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Jah**. Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **Kaubandus** on valitud. Teie CSU on ettevalmistamiseks ootele pandud.
1. Enne jätkamist veenduge, et teie CSU olek oleks **Õnnestus**. Lähtestamiseks kulub umbes kaks kuni viis tundi.

### <a name="initialize-e-commerce"></a>E-kaubanduse lähtestamine

E-kaubanduse lähtestamiseks tehke järgmist.

1. Vahekaardil **E-kaubandus** vaadake üle eelvaate nõusolek ja seejärel valige suvand **Seadistus**.
1. Väljale **E-kaubanduse rentniku nimi** sisestage nimi. Võtke siiski arvesse, et see nimi on nähtav mõnes URL-is, mis viitavad teie e-kaubanduse eksemplarile.
1. Väljal **Kaubanduse skaala üksuse nimi** valige loendist oma CSU. (Loendis peaks olema ainult üks valik.)

    Väli **E-kaubanduse geograafia** väli määratakse automaatselt ja väärtust ei saa muuta.

1. Jätkamiseks valige nupp **Edasi**.
1. Väljale **Toetatud hostinimed** mis tahes kehtiv domeen, nt `www.fabrikam.com`.
1.  Väljale **AAD süsteemi administraatori turberühm** sisestage selle turberühma nime esimesed tähed, mida soovite kasutada. Otsingutulemuste kuvamiseks valige suurendusklaasi ikoon. Valige loendist õige turberühm.
2.  Väljale **AAD hinnangute ja arvustuse moderaatori turberühm** sisestage selle turberühma nime esimesed tähed, mida soovite kasutada. Otsingutulemuste kuvamiseks valige suurendusklaasi ikoon. Valige loendist õige turberühm.
1. Jätke suvand **Hinnangute ja arvustuste teenuse häälestuse lubamine** sisselülitatuks.
1. Valige **Lähtesta**. Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **e-kaubandus** on valitud. E-kaubanduse lähtestamine on käivitatud.
1. Enne jätkamist oodake, kuni teie e-kaubanduse lähtestamise olek on **Lähtestamine edukas**.
1. All paremal jaotises **Lingid** märkige järgmiste linkide URL-id:

    * **E-kaubanduse sait** – link teie e-kaubanduse saidi juurele.
    * **E-kaubanduse saidi haldustööriist** – link saidi halduse tööriistale.

## <a name="commerce-preview-environment-support"></a>Commerce’i eelvaatekeskkonna tugi

Kui teil tekib ettevalmistuse etappide lõpetamisel probleeme, külastage abi saamiseks [Rakenduse Microsoft Dynamics 365 Commerce eelvaate Yammeri gruppi](https://aka.ms/Dynamics365CommercePreviewYammer).

Kui teil tekib probleeme Yammer-grupile juurdepääsu loomisel, saate Microsoftiga ühendust võtta e-postiaadressil <Dynamics365Commerce@microsoft.com>. Seda meiliaadressi ei jälgita aktiivselt. Seetõttu oodata viivitust vastuses.

## <a name="next-steps"></a>Järgmised etapid

Oma Commerce’i eelvaatekeskkonna ettevalmistamise ja konfigueerimise protsessi jätkamiseks vaadake teemat [Commerce’i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce’i eelvaatekeskkonna ülevaade](cpe-overview.md)

[Dynamics 365 Commerce’i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md)

[Dynamics 365 Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md)

[Dynamics 365 Commerce’i eelvaatekeskkonna KKK](cpe-faq.md)

[Microsofti elutsükli teenused (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure'i portaal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)

