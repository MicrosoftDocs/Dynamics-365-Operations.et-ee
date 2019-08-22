---
title: URL-i avamine kassas
description: Selles teemas antakse ülevaade toote ja kliendi otsingufunktsiooni täiustustest rakenduses Microsoft Dynamics 365 for Retail.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 729caf9fad9097a3ecbf7d546c8f8a96f67aec92
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845676"
---
# <a name="open-url-in-pos"></a>URL-i avamine kassas

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas saate URL-i avamiseks konfigureerida nuppu jaemüügikassas. See funktsioon ei vaja koodikohandust ja seda saab konfigureerida mittearendaja rollis. See funktsioon on saadaval rakenduse Dynamics 365 for Finance and Operations versiooni 8.1.3 väljalaske (järk 8.1.227.10014) või uuema osana. 

See funktsioon võimaldab nupu konfigureerimist kassas, kasutades URL-i avamiseks nupupaneeli koostajat. Praegu toetatakse seda järgmistes konfiguratsioonides.

- Ava uues aknas.
- Ava kassas.
- Ava omarakendus.

## <a name="open-in-new-window"></a>Ava uues aknas

Selle konfiguratsioon määratleb, kas avada URL uues aknas või rakendusesiseselt. Kui konfigureeritud on veebi URL-i avamine rakendusesiseselt, on kassa külgmine navigeerimispaan ja ülariba nähtavad ning kasutaja interaktsiooniks saadaval. Kui konfigureeritud on uues aknas avamine, avaneb URL rakendusel Modern POS Windowsi jaoks uues aknas ja kõigil teistel kassaklientidel uuel brauseri vahekaardil. Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** on valitud.

## <a name="open-within-pos"></a>Ava kassas

Veebi URL-i avamist kassas toetatakse praegu ainult tänapäevase kassa jaoks operatsioonisüsteemis Windows. Teistel klientidel on see võimalus arendamisel ja plaanitud välja anda tulevastes uuendustes. Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** pole valitud.

## <a name="open-a-native-app"></a>Ava omarakendus

See funktsioon võimaldab ka määrata mitteveebi URL-id omarakenduse avamiseks. Näiteks saate täpsustada URL-protokolle nagu MailTo, SIP, IM või MSTEAMS, mida seejärel käsitlevad vastavad omarakendused hostiseadmes. Selle lubamiseks peate konfigureerima URL-i, kui suvand **Ava uues aknas** on valitud.

- Vt Windowsi arvutites protokolli vaikeseoste määramiseks jaotist [Rakenduse vaikeseoste eksport või import](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), kui seadistate arvutit funktsiooni Deployment Image Servicing and Management (DISM) kasutades.
- Kui kasutate Windowsi arvutite haldamiseks tarkvara MDM, nagu Intune, vt jaotist [Poliitika konfigureerimisteenuse pakkuja – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).
- Kui olete kohandatud veebisaiti loov arendaja, vt jaotist [Vaikerakenduse kävitamine URI jaoks](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Ava omarakendus sujuvalt

Windows, iOS ja Android võimaldavad samuti rakenduste sujuvamat avamist rakenduse protokolli seose alusel. Kui rakendust pole veebibrauserist avamiseks juba konfigureeritud, võib selleks vaja minna arendajat.

- Operatsioonisüsteemi Windows jaoks vt jaotist [Rakenduste lubamine veebisaitidele rakenduse URI ohjureid kasutades](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).
- Operatsioonisüsteemi iOS jaoks vt jaotist [Universaalsed lingid arendajatele](https://developer.apple.com/ios/universal-links/).
- Androidi puhul vt teemat [Androidi rakenduste linkide käsitlemine](https://developer.android.com/training/app-links/).

| Klient                | Ava uues aknas | Ava omarakendus | Ava kassas | Üksikasjad                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Windowsi tänapäevane kassa | ✓\*                | ✓               | ✓              | \* Avaneb uues tänapäevase kassa aknas |
| Pilve kassa             | ✓\*                | ✓               | X              | \* Avaneb uuel brauseri vahekaardil        |
| Tänapäevane kassa operatsioonisüsteemis iOS     | ✓\*                | ✓               | X              | \* Avaneb uuel brauseri vahekaardil        |
| Modern POS Androidis | ✓\*                | ✓               | X              | \* Avaneb uuel brauseri vahekaardil        |

## <a name="before-you-begin"></a>Enne alustamist

Enne alustamist vaadake üle konfigureerimine jaotises [Kassa ekraanipaigutused](pos-screen-layouts.md).

## <a name="open-url-in-pos"></a>URL-i avamine kassas

URL-i konfigureerimiseks kassas avamise jaoks toimige järgmiselt.

1. Minge peakontoris jaotisse **Jaemüük \> Kanali seadistus \> Kassa seadistus \> Kassa \> Kuvapaigutused**.
2. Valige **Nupupaneelid \> Kujundaja**.
3. Looge uus nupp.
4. Valige **Nupu** atribuudid.
5. Valige tegevuseks **Ava URL**.
6. Sisestage URL, mida soovite kasutada.
7. Konfigureerige, kas URL uues aknas avada.
