---
title: E-kaubanduse saidi ülevaade
description: Selles teemas antakse ülevaade Microsofti e-kaubanduse saitide toest Dynamics 365 Commerce'is.
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae220e98acbda99255beefea598d973dbaa22368
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997543"
---
# <a name="e-commerce-site-overview"></a>E-kaubanduse saidi ülevaade

[!include [banner](includes/banner.md)]

Selles teemas antakse ülevaade Microsofti e-kaubanduse saitide toest Dynamics 365 Commerce'is. See sisaldab teavet selle kohta, kuidas e-kaubanduse võrgupoode lähtestatakse ja hallatakse rakenduses Dynamics 365 Commerce. See sisaldab ka linke lisateabele võrgupoodide ja e-kaubanduse saidi häälestamise ja konfigureerimise kohta. Kuigi see teema hõlmab paljusid põhitõdesid, ei hõlma see kõike, mis on vajalik tootmise e-kaubanduse saidi loomiseks. Täpsemad teemad leiate Dynamics 365 Commerce'i dokumentatsioonist.

## <a name="online-store-channel"></a>Võrgupoe kanal

Enne oma saidi loomist teenuses Dynamics 365 Commerce, peab olema häälestatud vähemalt üks võrgupoe kanal. Lisateavet leiate teemast [Võrgukanali häälestamine](channel-setup-online.md). 

Teenuses Dynamics 365 Commerce kasutate võrgupoe kanalit toodete, hindade, keelte, makseviiside, tarneviiside, täitmise keskuste ja teiste võrgukogemuse aspektide loomiseks, mis peaksid olema klientidele kättesaadavad.

Enne teenuse Dynamics 365 Commerce kasutamise alustamist peab olema seadistatud ainult üks võrgupoe kanal. Samas võib üks e-kaubanduse sait pakkuda mitme võrgupoe võrgukogemust. Näiteks kui erinevate geograafiliste piirkondade toetamiseks on seadistatud mitu võrgupoodi, saab kasutada ühte e-kaubanduse lehtede komplekti, et pakkuda iga poe poolt määratletud ainulaadset kogemust. Lisateavet selle kohta, kuidas konfigureerida saiti mitme e-poe toetamiseks, leiate teemast [Veebisaidi seostamine kanaliga](associate-site-online-store.md).

Pärast e-poe seadistamist saab selle seostada teenuse Dynamics 365 Commerce saidiga, mis esitatakse teie e-poe fassaadina. Lisateavet e-poodide ja nende seadistamise kohta leiate teemast [E-poodide seadistamine](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Uue e-kaubanduse rentniku juurutamine

E-kaubanduse saidi lähtestamisel küsitakse teilt domeeninime. Lisateavet Domeenide kohta Commerce'is leiate teemast [Domeeninime](configure-your-domain-name.md) ja domeenide konfigureerimine [rakenduses Dynamics 365 Commerce](domains-commerce.md). Uue e-kaubanduse rentniku juurutamiseks [Microsoft Dynamics Lifecycle Servicesi (LCS-i) abil](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) järgige teemas [Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md) toodud juhiseid. Pärast seda, kui teie e-kaubanduse rentnik on LCS-is häälestatud, antakse Commerce'i saidiehitaja link. Seejärel saate kasutada Commerce'i saidiehitajat oma e-kaubanduse saitide lähtestamiseks ja konfigureerimiseks.

## <a name="initialize-your-e-commerce-site"></a>E-kaubanduse saidi lähtestamine

Kui käivitate Commerce'i saidiehitaja LCS-i kaudu, kuvatakse leht **Saidid**. Sellel lehel on kaks eelkonfigureeritud saiti, **Vaikimisi** ja **Fabrikam**, nagu on näidatud järgmisel joonisel toodud näites.

![Saitide leht Commerce'i saidiehitajas](media/e-commerce-site-01.png)

Kui valite ühe neist saitidest, palutakse teil valida domeeni nimi, võrgupoe vaikekanal, valitud kanali toetatud keel ja tee. Kui kasutatakse ainult ühte kanalit, võite tee tühjaks jätta. Rohkem võrgupoe kanaleid või keeli saab hiljem konfigureerida Commerce'i saidiehitajas. Iga täiendav kanal või keel nõuab kordumatut teed. Oletagem näiteks, et teil on kaks võrgukanalit, mis on seotud ühe saidiga ja saidi domeeninimi on `www.fabrikam.com`. Sel juhul võib ühe kanali tee olla vaikeväärtus, millel puudub tee (`https://www.fabrikam.com`) ja teise kanali saab määrata uuele teele, näiteks **Sait2**, mille URL on `https://www.fabrikam.com/site2`. Järgmisel joonisel on näide saidi lähtestamise dialoogiboksist Commerce'i saidikoosturis.

![Saidi lähtestamise dialoogiboks Commerce'i saidikoosturis](media/e-commerce-site-02.png)

Lehel **Saidid** on ka nupp **Uus sait**. Selle nupu valimisel kuvatav dialoogiboks sarnaneb saidi lähtestamise dialoogiboksiga, kuid seda kasutatakse uue saidi loomiseks. Uued saidid on tühjad. Need ei sisalda samu vaikemalle, fragmente, lehti ega pilte, mis on saidil **Vaikimisi** ja **Fabrikam**. Kuid vastavalt vajadusele saate avada tugiteenusepileti, et taotleda vaikesisu koopia lisamist uuele tühjale saidile. Lisateavet leiate teemast [E-kaubanduse saidi loomine](create-ecommerce-site.md).

Pärast uue saidi lähtestamist kuvatakse Commerce'i saidikoosturi leht **Avaleht**. See leht sisaldab linke levinud toimingutele ja juhendsisule, nagu on näidatud järgmisel joonisel toodud näitel.

![Lingid Commerce'i saidiehitaja avalehel](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Võrgupoe kanalite muutmine või võrgupoe kanalite lisamine e-kaubanduse saidile

Pärast e-kaubanduse saidi loomist saate sellega seostatud kanalit muuta, järgides teemas [E-kaubanduse saidi seostamine võrgukanaliga](associate-site-online-store.md) toodud juhiseid. Järgmisel joonisel toodud näide näitab, kuidas kanali tootmisüksuse numbrit (OUN-i) saab muuta lehel **Kanalid** (**Saidi sätted \> Kanalid**). Kui olete muudatuse tegemise lõpetanud, valige kindlasti nupp **Salvesta ja avalda**. Sel viisil tagate muudatuse avaldamise.

![Kanalite leht Commerce'i saidiehitajas](media/e-commerce-site-04.png)

Uute kanalite lisamiseks valige nupp **Lisa kanal**. Kanalile uute keelte lisamiseks valige kanal ja seejärel valige kuvatavas kanalidialoogiboksis käsk **Lisa lokaat**. Enne, kui lokaate dialoogiboksis kuvada saab, peavad need olema Commerce'i peakontori võrgupoe kanali jaoks eelkonfigureeritud.

![Kanali dialoogiboks Commerce'i saidiehitajas](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Azure B2C rentniku häälestamine

Dynamics 365 Commerce kasutab teenust Azure Active Directory (Azure AD) ettevõtja ja tarbija (B2C) vahelist teavet kasutaja mandaadi ja autentimise voogude toetamiseks. Lisateavet Azure B2C rentniku häälestamise kohta leiate teemast [B2C rentniku häälestamine Commerce'is](set-up-b2c-tenant.md), [Kohandatud lehtede häälestus kasutajate sisselogimise jaoks](custom-pages-user-logins.md) ja [Mitme jaekaubandusrentniku konfigureerimine Commerce'i keskkonnas](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Saidi vaikelehtede ülevaade

Saidil **Vaikimisi** ja **Fabrikam** on eelkonfigureeritud mallid, fragmendid ja lehed, mis aitavad teil alustada. Lisateavet vt järgmistest teemadest:

- [Avalehe ülevaade](quick-tour-home-page.md)
- [Toote üksikasjade lehe ülevaade](quick-tour-pdp.md)
- [Ostukorvi ja väljaregistreerimise ülevaade](quick-tour-cart-checkout.md)
- [Kontohalduse lehtede ülevaade](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Saidisätete haldamine

Saidi sätete haldamise kohta lisateabe saamiseks vaadake järgmisi teemasid.

- [E-kaubanduse kasutajate ja rollide haldamine](manage-ecommerce-users-roles.md)
- [Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused](/search-engine-optimization-considerations.md)
- [Sisu turbepoliitika (CSP) haldamine](manage-csp.md)
- [Saidi kujunduse valimine](select-site-theme.md)

## <a name="manage-site-content"></a>Saidi sisu haldamine

Saidi sisu haldamise kohta lisateabe saamiseks vaadake järgmisi teemasid.

- [Lehemudeli sõnastik](page-elements-overview.md)
- [Dokumendi olekud ja töötsükkel](document-states-overview.md)
- [Mallid ja paigutus](templates-layouts-overview.md)
- [Fragmentidega töötamine](work-with-fragments.md)
- [Moodulitega töötamine](work-with-modules.md)
- [Digitaalse varahalduse ülevaade](dam-overview.md)
- [Mooduliteegi ülevaade](starter-kit-overview.md)

## <a name="additional-resources"></a>Lisaressursid

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md)

[Veebisaidi seostamine kanaliga](associate-site-online-store.md)

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)
