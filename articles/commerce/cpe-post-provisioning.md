---
title: Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 Commerce hindamiskeskkonda, kui see on ette valmistatud.
author: psimolin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9738700ca495d54c91ad91aa9c5a3d32c95a5a5
ms.sourcegitcommit: 4a973ac0e7af0176270a8070a96a52293567dfbf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/13/2022
ms.locfileid: "8747633"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 Commerce hindamiskeskkonda, kui see on ette valmistatud.

Viige lõpule selle teema protseduurid alles pärast seda, kui rakenduse Commerce hindamiskeskkond on ette valmistatud. Teavet selle kohta, kuidas Commerce’i hindamiskeskkonda ette valmistada, vaadake teemast [Commerce’i hindamiskeskkonna ettevalmistamine](provisioning-guide.md).

Pärast seda, kui teie Commerce'i hindamiskeskkond on täielikult ettevalmistatud, tuleb lõpule viia ettevalmistusjärgsed konfigureerimisetapid, enne kui saate hakata keskkonda hindama. Nende sammude lõpetamiseks peate kasutama teenust Microsoft Dynamics Lifecycle Services (LCS) ja rakendust Dynamics 365 Commerce.

## <a name="before-you-start"></a>Enne alustamist

1. Logige sisse [LCS portaali](https://lcs.dynamics.com).
1. Avage oma projekt.
1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Valige loendist oma keskkond.
1. Valige paremal olevast keskkonna teabest **Keskkonda sisselogimine**. Teid suunatakse Commerce'i peakontorisse.
1. Veenduge, et **USRT** juriidiline isik on valitud ülemises parempoolses nurgas.
1. Minge Commerce'i **parameetrite \> konfiguratsiooniparameetritele** **ja veenduge, et productSearch.UseAzureSearch** oleks kirje ja et väärtuseks on seatud **Tõene**. Kui see kirje puudub, saate selle lisada, **·** **seada väärtuseks Tõene ja seejärel valida kanali \>** andmebaasi andmete täielik sünkroonimine commerce Scale Uniti jaoks, mis on seotud teie e-äri veebisaidiga.
1. Minge rakenduse **Retail ja Commerce \> Headquarters häälestamise rakenduse \> Commerce andmeedastaja \> lähtestamiseks**. Menüüs Lähtesta **äriedastaja** väljaminek seadke suvandi **Kustuta olemasolev konfiguratsioon väärtuseks** Jah **ja** seejärel valige **OK**.
1. Kanalite lisamiseks Commerce Scale Unitile minge **Rakenduse Retail ja Commerce \> Headquarters \> häälestamise rakenduse Commerce andmeedastaja \> kanali** andmebaasi ja valige vasakul paanil Commerce Scale Unit. Jaemüügikanali **kiirkaardil** lisage **AW-e-pood**, **AW Businesse e-pood** ja **Fabrikami laiendatud võrgupoe kanalid**. Valikuna saate lisada ka jaekauplusi, kui kasutate kassat (nt Seattle, **San Maria** ja **SanTagem**). **·**

Commerce'i peakontori ettevalmistusjärgsete tegevuste käigus veenduge, et juriidiline isik **USRT** oleks alati valitud.

## <a name="configure-the-point-of-sale"></a>Kassa konfigureerimine

### <a name="associate-a-worker-with-your-identity"></a>Seosta töötaja oma identiteediga

Töötaja seostamiseks Commerce'i peakontoris oma identiteediga toimige järgmiselt.

1. Kasutage vasakul asuvat menüüd, et avada **Moodulid \> Jaemüük ja kaubandus \> Töövõtjad \> Töötajad**.
1. Otsige loendist ja valige kirje **000713 – Andrew Collette**.
1. Valige toimingupaanil **Kaubandus**.
1. Valige **Seosta olemasolev identiteet**.
1. Väljale **Meil**, mis on paremal pool väljast **Otsi meili abil**, sisestage oma meiliaadress.
1. Valige **Otsi**.
1. Valige oma nimega kirje.
1. Valige nupp **OK**.
1. Valige käsk **Salvesta**.

### <a name="activate-cloud-pos"></a>Pilve kassa aktiveerimist

Pilve kassa aktiveerimiseks järgige LCS-is neid etappe.

1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Valige loendist oma keskkond.
1. Valige paremal olevast keskkonna teabest **Pilve kassasse sisselogimine**.
1. Valige **Edasi** dialoogiboksi **Enne alustamist** avamiseks.
1. Ärge muutke välja **Serveri URL**. Valige **Edasi**.
1. Logige sisse oma Microsoft Azure Active Directory (Azure AD) konto abil.
1. Valige jaotises **Kaupluse nimi** suvand **San Francisco** ja seejärel valige **Edasi**.
1. Jaotise **Register ja seade** väärtuseks valige **SANFRAN-1**.
1. Valige **Aktiveeri**. Olete välja logitud ja viidud Kassa sisselogimise lehele.
1. Nüüd saate pilve kassasse sisse logida, kasutades operaatori ID-d **000713** ja parooli **123**.

## <a name="set-up-your-site-in-commerce"></a>Saidi seadistamine Commerce'is

Et alustada oma hindamise saidi seadistamist Commerce'is, toimige järgmiselt.

1. Logige saidiehitajasse sisse, kasutades URL-i, mille märkisite üles, kui te e-kaubanduse lähtestamist ette valmistasite (vt [e-kaubanduse lähtestamine](provisioning-guide.md#initialize-e-commerce)).
1. Klõpsake saidil **Fabrikam**, et avada saidi häälestuse kast.
1. Valige domeen, mille sisestasite e-kaubanduse lähtestamisel.
1. Vaikimisi kanali jaoks valige **Fabrikami laiendatud e-pood**. (Veenduge, et valite **laiendatud** e-poe.)
1. Vaikekeeleks valige **en-us**.
1. Jätke välja **tee** väärtus nii, nagu see on.
1. Valige nupp **OK**. Kuvatakse saidi lehtede loend.
1. Korrake samme 2–7 **AdventureWorks** saidi puhul (**mis vastendab AW** võrgupoe kanaliga) **AdventureWorks ja Ettevõtte** saidiga (mis **vastendab AW Businessi võrgupoe kanalile**). **Kui** Fabrikami saidi tee väli on tühi, AdventureWorks peate lisama teed kahele saidile (nt awbusiness").

## <a name="enable-jobs"></a>Tööde lubamine

Commerce’is tööde lubamiseks tehke järgmist.

1. Logige sisse keskkonda (HQ).
1. Kasutades menüüd vasakul, avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Pakett-tööd**.

    Selle protseduuri ülejäänud sammud peavad olema täidetud iga järgmise töö puhul:

    * Jaemüügitellimuse meiliteavituse töötlemine
    * Toote saadavus
    * P-0001
    * Tellimuste tööde sünkroonimine

1. Kasutage kiirfiltrit, et otsida tööd, kasutades selle nime.
1. Kui töö olek on **Teostamine**, tehke järgmist:

    1. Vali kirje.
    1. Tegumiribal valikus **Pakett-töö**, klõpsake **Muuda olekut**.
    1. Valige **Tühistamine** ja seejärel valige **OK**.

1. Kui töö olek on Kinnipeetud **, järgige** neid samme.

    1. Vali kirje.
    1. Tegumiribal valikus **Pakett-töö**, klõpsake **Muuda olekut**.
    1. Valige suvand **Ootel** ja seejärel nupp **OK**.

Saate seadistada ka kordumise intervalli iga ühe (1) minuti järel järgmiste tööde puhul.

* Jaemüügitellimuse meiliteavituse töötlemise töö
* P-0001 töö
* Tellimuste tööde sünkroonimine

### <a name="run-full-data-synchronization"></a>Kõikide andmete sünkroonimise käitamine

Commerce’is kõikide andmete sünkroonimise käitamiseks tehke Commerce'i peakontoris järgmist.

1. Kasutage vasakul asuvat menüüd, et avada **Moodulid \> Jaemüük ja kaubandus \> Peakontori häälestus \> Kaubanduse planeerija \> Kanali andmebaas**.
1. Valige muu kanal nimega **scXXXXXXXXX**.
1. Valige tegumiribal suvand **Andmete täielik sünkroonimine**.
1. Sisestage jaotugraafikuna väärtus **9999**.
1. Valige nupp **OK**.
1. Valige nupp **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Testige krediitkaardi teavet, et sooritada testoste.

Selleks, et sooritada testi kandeid saidil, saate kasutada järgmist testi krediitkaardi teavet.

- **Kaardi number:** 4111-1111-1111-1111
- **Aegumiskuupäev:** 10/30
- **Kaardi tõendamise väärtus (CVV) kood:** 737

> [!IMPORTANT]
> Te ei tohiks proovida kasutada tegeliku krediitkaardi teavet testi tegevuskohas mitte ühelgi juhul.

## <a name="next-steps"></a>Järgmised etapid

Pärast ettevalmistamise ja konfigureerimise etappide lõpule viimist, olete valmis oma hindamiskeskkonda kasutama. Kasutage Commerce'i saidiehitaja URL-i, et minna autorluskogemuse juurde. Kasutage Commerce'i saidi URL-i, et minna jaemüügi klientide saidikogemuse juurde.

Teavet selle kohta, kuidas Commerce’i hindamiskeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i hindamiskeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).

> [!NOTE]
> Commerce'i hindamiskeskkonnad on eellaaditud Azure Active Directory (Azure AD) ettvõttelt tarbijale (B2C) rentnikule demo eesmärgil. Oma Azure AD B2C rentniku konfigureerimine ei ole hindamiskeskkondade jaoks vajalik. Kui aga konfigureerite hindamiskeskkonda oma Azure AD B2C rentniku kasutamiseks, lisage ``https://login.commerce.dynamics.com/_msdyn365/authresp`` see Azure AD Azure Portaali kaudu B2C-rakendusele vastuse URL-ina.

## <a name="troubleshooting"></a>Tõrkeotsing

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Saidikonstruktori kanaliloend on saidi konfigureerimisel tühi.

Kui saidikonstruktoril ei ole ühtegi võrgupoe kanalit, veenduge peakontoris, et kanalid on Commerce Scale Uniti [lisatud, nagu on kirjeldatud jaotises Enne kui alustate](#before-you-start). Samuti käivitage **Lähtesta äriajasti**, nii et Kustuta **olemasolev konfiguratsiooni** väärtus on seatud väärtusele **Jah**.  Kui need sammud on läbitud, **käivitage** Kanali andmebaasi lehel (**Retail ja Commerce \> Headquartersi \> häälestus Commerce Scheduler \> Channeli** andmebaas) **9999-töö** Commerce Scale Unitis.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Värvitoonid ei renderda kategoorialehel, vaid renderdavad toote üksikasjade lehel (PDP).

Järgige neid samme, et veenduda, et värvi- ja suuruseatriisid on võimalik täpsustada.

1. Minge peakontoris jaemüügi ja **ärikanali häälestuse \> kanali kategooriatesse \> ja toote atribuutidesse**.
1. Valige vasakul paanil võrgupoe kanal ja seejärel valige atribuudi metaandmete **komplekt**.
1. Seadke kanali **suvandi Näita atribuuti** valikule **Jah**, seadke **valiku Saab täiustada valikuks** **Jah** ja seejärel valige suvand **Salvesta**. 
1. Minge tagasi võrgupoe kanali lehele ja valige suvand Avalda **kanali värskendused**.
1. Minge Rakenduse **Retail ja Commerce \> Headquarters häälestamise rakenduse \> Commerce andmeedastaja \> kanali** **andmebaasi ja käitage 9999-töö** Commerce Scale Unitis.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Ärifunktsioonid ei ole ettevõtte saidi puhul sisse lülitatud AdventureWorks.

Kontrollige peakontoris, et võrgupoe kanal on konfigureeritud **B2B-le** häälestatud **klienditüübiga**. Kui kliendi **tüübiks** on seatud **B2C**, tuleb luua uus kanal, kuna olemasolevat kanalit ei saa redigeerida. 

Commerce versioonis 10.0.26 tarnitud demoandmetel oli varem viga **, kus AW Businessi võrgupoe** kanal konfigureeriti valesti. Lahenduseks on luua uus kanal, **millel** on samad sätted ja konfiguratsioonid, v.a kliendi tüüp, mis tuleks seadistada **B2B-le**.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce'i hindamiskeskkonna ülevaade](cpe-overview.md)

[Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine](provisioning-guide.md)

[Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md)

[BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas](cpe-bopis.md)

[Dynamics 365 Commerce'i hindamiskeskkonna KKK](cpe-faq.md)

[Microsofti elutsükli teenused (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure'i portaal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)

[Jaekaubandusrentniku häälestamine Commerce'is](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
