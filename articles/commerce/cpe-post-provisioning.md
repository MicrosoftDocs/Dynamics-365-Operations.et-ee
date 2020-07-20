---
title: Dynamics 365 Commerce eelvaatekeskkonna konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i eelvaatekeskkond, kui see on ette valmistatud.
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ad05996eaabd3965308370649a27b8bc3080c7ce
ms.sourcegitcommit: f72e90dccc80718e99cab2752eaf8931dcbb915e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2020
ms.locfileid: "3534063"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a>Dynamics 365 Commerce eelvaatekeskkonna konfigureerimine


[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i eelvaatekeskkond, kui see on ette valmistatud.

## <a name="overview"></a>Ülevaade

Lõpetage selle teema protseduurid alles pärast seda, kui rakenduse Commerce eelvaatekeskkond on ette valmistatud. Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonda ette valmistada, vaadake teemast [Commerce’i eelvaatekeskkonna ettevalmistamine](provisioning-guide.md).

Pärast seda, kui teie Commerce eelvaatekeskkond on eelnevalt lõpetatud, tuleb lõpule viia täiendavad konteeringu konfigureerimise etapid, enne kui saate hakata keskkonda hindama. Nende sammude lõpetamiseks peate kasutama teenust Microsoft Dynamics Lifecycle Services (LCS) ja rakendust Dynamics 365 Commerce.

## <a name="before-you-start"></a>Enne alustamist

1. Logige sisse [LCS portaali](https://lcs.dynamics.com).
1. Avage oma projekt.
1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Valige loendist oma keskkond.
1. Valige paremal olevast keskkonna informatsioonist **Täielik teave**.
1. Valige **Logi sisse**, et avada menüü ja valige suvand **Logi keskkonda**.
1. Veenduge, et **USRT** juriidiline isik on valitud ülemises parempoolses nurgas.

## <a name="configure-the-point-of-sale-in-lcs"></a>Müügikoha konfigureerimine LCS-is

### <a name="associate-a-worker-with-your-identity"></a>Seosta töötaja oma identiteediga

Töötaja seostamiseks LCS-is oma identiteediga toimige järgmiselt.

1. Kasutage vasakul asuvat menüüd, et avada **Moodulid \> Jaemüük ja kaubandus \> Töövõtjad \> Töötajad**.
1. Otsige loendist ja valige kirje **000713 – Andrew Collette**.
1. Toimingupaanil valige käsk **Jaemüük**.
1. Valige **Seosta olemasolev identiteet**.
1. Väljale **Meil**, mis on paremal pool väljast **Otsi meili abil**, sisestage oma meiliaadress.
1. Valige **Otsi**.
1. Valige oma nimega kirje.
1. Valige nupp **OK**.
1. Valige käsk **Salvesta**.

### <a name="activate-cloud-pos"></a>Pilve kassa aktiveerimist

Pilve POS aktiveerimiseks LCS-s toimige järgmiselt.

1. Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.
1. Valige loendist oma keskkond.
1. Valige paremal olevast keskkonna informatsioonist **Täielik teave**.
1. Menüü avalmiseks valige **Logi sisse** ja seejärel valige **Logi sisse pilve kassasse** et avada kassa (POS).
1. Valige **Edasi**.
1. Logige sisse oma Microsoft Azure Active Directory (Azure AD) konto abil.
1. Välja **Kaupluse nimi** väärtuseks valige **San Francisco**.
1. Valige **Edasi**.
1. Jaotise **Register ja seade** väärtuseks valige **SANFRAN-1**.
1. Valige **Aktiveeri**. Olete välja logitud ja viidud Kassa sisselogimise lehele.
1. Nüüd saate pilve kassasse sisse logida, kasutades operaatori ID-d **000713** ja parooli **123**.

## <a name="set-up-your-site-in-commerce"></a>Saidi seadistamine Commerce'is

Et alustada oma eelvaate saidi seadistamist Commerce'is, toimige järgmiselt.

1. Logige saidi halduse tööriista sisse, kasutades URL-i, mis te tegite, kui te tegite e-kaubanduse lähtestamisel ettevalmistuse (vt [e-kaubanduse lähtestamine](provisioning-guide.md#initialize-e-commerce)).
1. Klõpsake saidil **Fabrikam**, et avada saidi häälestuse kast.
1. Valige domeen, mille sisestasite e-kaubanduse lähtestamisel.
1. Vaikimisi kanali jaoks valige **Fabrikami laiendatud e-pood**. (Veenduge, et valite **laiendatud** e-poe.)
1. Vaikekeeleks valige **en-us**.
1. Jätke välja **tee** väärtus nii, nagu see on.
1. Valige nupp **OK**. Kuvatakse saidi lehtede loend.

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
1. Kui töö olek on **Kinnipeetud**, tehke järgmist:

    1. Vali kirje.
    1. Tegumiribal valikus **Pakett-töö**, klõpsake **Muuda olekut**.
    1. Valige suvand **Ootel** ja seejärel nupp **OK**.

### <a name="run-full-data-synchronization"></a>Kõikide andmete sünkroonimise käitamine

Commerce’is kõikide andmete sünkroonimise käitamiseks tehke järgmist.

1. Kasutage vasakul asuvat menüüd, et avada **Moodulid \> Jaemüük ja kaubandus \> Peakontori häälestus \> Kaubanduse planeerija \> Kanali andmebaas**.
1. Kanal **Vaikimisi** valitakse vasakul olevast loendist. Valige muu saadaolev kanal. Selle kanali nimi on **scXXXXXXXXX**.
1. Valige tegumiribal suvand **Andmete täielik sünkroonimine**.
1. Sisestage jaotugraafikuna väärtus **9999**.
1. Valige nupp **OK**.
1. Valige nupp **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Testige krediitkaardi teavet, et sooritada testoste.

Selleks, et sooritada testi kandeid saidil, saate kasutada järgmist testi krediitkaardi teavet.

- **Kaardi number:** 4111-1111-1111-1111
- **Aegumiskuupäev:** 10/20
- **Kaardi tõendamise väärtus (CVV) kood:** 737

> [!IMPORTANT]
> Te ei tohiks proovida kasutada tegeliku krediitkaardi teavet testi tegevuskohas mitte ühelgi juhul.

## <a name="next-steps"></a>Järgmised etapid

Pärast ettevalmistamise ja konfigureerimise sammude lõpetamist olete valmis oma eelvaate keskkonda hindama. Kasutage rakenduse Commerce Site Management tööriista URL-i, et minna autorluse kogemuse juurde. Kasutage rakenduse Commerce jaemüügi klientide saidi URL-i, et minna autorluse kogemuse juurde.

Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce eelvaatekeskkonna ülevaade](cpe-overview.md)

[Dynamics 365 Commerce'i eelvaatekeskkonna ettevalmistamine](provisioning-guide.md)

[Dynamics 365 Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md)

[Dynamics 365 Commerce eelvaatekeskkonna KKK](cpe-faq.md)

[Microsofti elutsükli teenused (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure'i portaal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)
