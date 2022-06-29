---
title: BOPIS-i konfigureerimine Dynamics 365 Commerce sisendkausta keskkonnas
description: See artikkel selgitab, kuidas konfigureerida ost võrgust, peale võtta kauplust (BOPIS) Microsoft Dynamics 365 Commerce sisendkausta keskkonnas pärast selle eraldiks tegemist.
author: BrianShook
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16cea7beb6ca05b5e96a9713b1217b414e27d56e
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013158"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-sandbox-environment"></a>BOPIS-i konfigureerimine Dynamics 365 Commerce sisendkausta keskkonnas

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas konfigureerida ost võrgus, peale võtta kauplust (BOPIS) Microsoft Dynamics 365 Commerce sisendkausta keskkonnas pärast seda, kui keskkond on juba ette salvestatud.

## <a name="prerequisite"></a>Eeltingimus

Viige selle artikli protseduurid lõpule alles siis, kui teie Rakenduse Commercebox keskkond on ette antud ja konfigureeritud. Teavet selle kohta, kuidas oma keskkonda ette ettevalmistamine ja konfigureerimine, vt [Dynamics 365 Commerce väljaminev keskkond ja](provisioning-guide.md)[Kaustakeskkonna Dynamics 365 Commerce konfigureerimine](./cpe-post-provisioning.md).

Kui teie Ärikeskkond on end eraldi ja konfigureeritud, saate selle artikli abil BOPIS-i stsenaariumid lubada.

## <a name="configure-the-pos"></a>Kassa konfigureerimine

### <a name="configure-modern-pos"></a>Modern POS-i konfigureerimine

BOPIS-i stsenaariumide jaoks, mis hõlmavad krediitkaardimakseid, on vaja riistvarajaama. Riistvarajaam on integreeritud rakendusse Modern POS Windowsi ja Androidi klientidele. Kui kasutate Cloud POS-i või Modern POS-i iOS-i jaoks, peab kassa (POS) klient olema ühendatud ühiskasutatava riistvarajaamaga. See artikkel selgitab, kuidas konfigureerida BOPIS-i Windowsi ja klientide Android jaoks. Lisateavet ühiskasutatava riistvarajaama seadistamise kohta leiate jaotisest [Jaemüügi riistvarajaama konfigureerimine ja installimine](./retail-hardware-station-configuration-installation.md).

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Registrid**.
2. Valige register **SANFRAN-5** ja seejärel valige **Redigeeri**.
3. Muutke väli **Riistvaraprofiil** väärtuselt **HW002** väärtusele **HW001** ja seejärel valige **Salvesta**.
4. Muudatuste sünkroonimiseks minge **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
5. Valige jaotusgraafik **1090** ja seejärel valige toimingupaanil käsk **Käita kohe**.
6. Valige **Jah** ja seejärel **OK**, et algatada andmete sünkroonimine. 

### <a name="install-modern-pos"></a>Modern POS-i installimine

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Seadmed**.
2. Valige seade **SANFRANCIS-5**.
3. Valige tegumipaanilt **Laadi alla** ja valige siis **Konfiguratsioonifail**.
4. Valige käsk **Laadi alla** ja seejärel **Retail Modern POS**. 
5. Kui faili **ModernPOSSetup.exe** allalaadimine on lõpule viidud, valige **Ava fail**.

    ![Avage fail.](./dev-itpro/media/PAYMENTS/openfile.png)

6. Valige **Järgmine**, et installimisprotsess lõpule viia. Kui installimine on lõpule viidud, valige **Sule**.

### <a name="activate-modern-pos"></a>Modern POS-i aktiveerimine

1. Valige Windowsi töölaual nupp **Start** ja sisestage **Retail Modern POS**.
2. Valige aktiveerimise käivitamiseks rakendus **Retail Modern POS**.
3. Valige **Edasi**. Väljad **Serveri URL**, **Seadme ID** ja **Registri number** peaksid olema eelhäälestatud, kasutades eelmises protsessis allalaaditud konfiguratsioonifaili teavet.
4. Valige **Aktiveeri**.
5. Kuvatakse dialoogiboks autentimiseks. Valige konto, mis kasutab e-posti aadressi, mis oli varem seotud töötajaga **000713 – Andrew Collette**.

    > [!NOTE]
    > Kui te pole veel töötajat oma identiteediga seostanud, siis aktiveerimine nurjub. Sel juhul järgige jaotise "Töötaja seostamine oma identiteediga" [jaotises "Töötaja Dynamics 365 Commerce seostamine oma identinfo konfigureerimise keskkonna artikliga](cpe-post-provisioning.md#associate-a-worker-with-your-identity) ".
    
6. Kui teil palutakse lasta oma organisatsioonil seadet hallata, valige **Ainult see rakendus**.
7. Kui aktiveerimine on lõpule viidud, valige **Alustamine**.

### <a name="enable-bopis-in-modern-pos"></a>BOPIS-i lubamine rakenduses Modern POS

1. Logige rakendusse Modern POS sisse, kasutades operaatori ID-d **000713** ja parooli **123**.
2. Sissejuhatava video esitamise ajal märkige dialoogiboksi alumises vasakus nurgas kaks ruutu ja sulgege seejärel dialoogiboks.
3. Kui teil ei paluta vahetust sulgeda, kerige **Tervituslehel** paremale, valige käsk **Sule vahetus** ja seejärel logige kassasse tagasi sisse.
4. Pärast sisselogimist, valige **Kassavälise toimingu tegemine**, kui teilt seda küsitakse.
5. Kerige **Tervituslehel** paremale ja valige toiming **Riistvarajaama valimine**.
6. Valige **Halda**, seadke suvandi **Riistvarajaama kasutamine** väärtuseks **Sees** ja seejärel valige **OK**.
7. Logige kassast välja ja siis uuesti sisse.
8. Kui olete sisse loginud, valige **Ava uus vahetus** ja seejärel valige **Sahtel**.

## <a name="complete-a-bopis-scenario"></a>BOPISi stsenaariumi lõpuleviimine

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Poetellimuse loomine kauplusest kättesaamise jaoks

1. Minge URL-i juurde, mille määrasite keskkonna konfigureerimise ajal sammu [E-kaubanduse lähtestamine](./provisioning-guide.md#initialize-e-commerce) käigus.
2. Valige kaup ja valige **Lisa ostukorvi**.
3. Ostukorvi lehel valige äsja loodud tellimuse rea jaoks **Tulen järele**.
4. Dialoogiboksis **Kaupluse valimine** sisestage **San Francisco** ja seejärel klõpsake nuppu **Otsi**.
5. Leidke otsingutulemustest San Francisco kauplus ja valige **Tulen siia järele**.
6. Valige ostukorvi lehel valik **Külalisena maksmine**. 

    > [!NOTE]
    > Maksmise jätkamiseks peate küpsiseteatisega nõustuma. See teade kuvatakse maksmislehe üleval ribana.

7. Krediitkaardiga maksmise puhul sisestage järgmised üksikasjad.

    - **Kaardiomaniku nimi:** sisestage mis tahes nimi.
    - **Kaardi number:** sisestage **4111-1111-1111-1111**.
    - **Aegumiskuupäev:** sisestage **10/20**.
    - **Kaardi tõendamise väärtuse (CVV) kood:** sisestage **737**.

    > [!IMPORTANT]
    > Te ei tohiks proovida kasutada tegeliku krediitkaardi teavet testi tegevuskohas mitte ühelgi juhul.

8. Jätkake maksmist, sisestades arve aadressi üksikasjad ja seejärel valige **Salvesta ja jätka**.
9. Kui tellimus on valmis, valige **Maksmine**.

### <a name="synchronize-online-orders-to-the-back-office"></a>Võrgutellimuste sünkroonimine kontoriga

Lisateavet võrgutellimuste sünkroonimise kohta vaadake teemast [Veebimüügi ja -maksete sisestamine](./tasks/posting-online-sales-payments.md).

### <a name="pick-up-an-order-in-the-store"></a>Tellimuse kättesaamine kauplusest

1. Logige kassasse sisse.
2. Valige **Tervitusekraanil** suvand **Tellimuse täitmine**
3. Valige kättesaamiseks mõeldud kaupade loendist võrgus tehtud tellimuse rida.
4. Kui tellimuse rida on valitud, valige **Kättesaamine**.

    Rea kaup lisatakse tehingu ekraanile ja makstav summa on **0,00 $**.

5. Valige makstav summa **0,00 $** või valige tehingu tegemiseks mis tahes makseviis.

## <a name="troubleshooting"></a>Tõrkeotsing

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>Kassasse toodud võrgutellimustel on nullist erinev summa

Kui tellimusele tullakse kauplusesse järele, veenduge juhul, kui summa pole 0 (null), et Modern POS oleks kasutusel ja et riistvarajaam oleks aktiivne. Kui kasutatakse Cloud POS-i või Modern POS-i iOS-i jaoks, veenduge, et ühiskasutatav riistvarajaam oleks aktiivne. Internetis tehtud maksete toomiseks on vaja mingit tüüpi aktiivset riistvarajaama.

### <a name="general-issues-with-payment-capture"></a>Üldised probleemid makse hõivamisega

Kõigi üldiste probleemide puhul peaksite alati esimesena uurima Modern POS-i või interneti teabeteenuste haldamise (IIS) riistvarajaama sündmustelogisid. Need logid leiate Windowsi sündmustelogi järgmistes sõlmedes.

- Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> Commerce – Modern POS
- Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> Commerce – riistvarajaam

## <a name="additional-resources"></a>Lisaressursid

[Info keskkonna Dynamics 365 Commerce ettevalmistamine](provisioning-guide.md)

[Valikuliste funktsioonide konfigureerimine kausta Dynamics 365 Commerce keskkonna jaoks](cpe-optional-features.md)

[Microsofti elutsükli teenused (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure'i portaal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)

[Adyeni makse ülekandmine](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[Veebimaksevahendite salvestamine Adyeni konnektori abil](./dev-itpro/adyen-connector-listpi.md)

[Omnikanali maksete ülevaade](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
