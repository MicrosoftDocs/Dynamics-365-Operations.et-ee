---
title: Küpsise vastavus
description: Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 95c5801e69396b21a36c4ae12ce17801e6f7fd88
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993496"
---
# <a name="cookie-compliance"></a>Küpsise vastavus

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.

## <a name="overview"></a>Ülevaade

Privaatsus on oluline tegur, kui e-kaubanduse kliente mõjutavad jälgimistehnoloogiad. Eraelu puutumatuse standardite, nagu üldise andmekaitse määruse (GDPR) tõttu Euroopa Liidus (EL), tuleb arvesse võtta elektroonilisi privaatsuspõhimõtted, mis on tänapäeval aktiivsed. Kuna paljud e-kaubanduse saidid on globaalselt juurdepääsetavad vaikimisi, on oluline vaadata üle oma e-kaubanduse saidi vastavuse standardid.

Lisateavet Microsoft kasutavate üldpõhimõtete kohta leiate [Microsofti usalduskeskusest.](https://www.microsoft.com/trust-center) Sellel saidil saate ka lisateavet vastavuse ja privaatsuse valdkondade kohta.

Järgmises tabelis on toodud Dynamics 365 Commerce'i saitide asetatud küpsiste kehtiv viiteloend.

| Küpsise nimi                               | Kasutus                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Talletage Microsoft Azure Active Directory (Azure AD) autentimisküpsised ühekordse sisselogimise (SSO) jaoks. Talletab kasutaja kohta krüptitud põhiteavet (nimi, perekonnanimi, e-post). |
| &#95;msdyn365___cart&#95;                           | Talletab ostukorvi ID, mida kasutatakse ostukorvi eksemplari lisatud toodete loendi hankimiseks. |
| &#95;msdyn365___ucc&#95;                            | Küpsise vastavuse nõusoleku jälgimine.                          |
| ai_session                                  | Tuvastab, mitu kasutajategevuse seanssi on hõlmanud konkreetseid rakenduse lehti ja funktsioone. |
| ai_user                                     | Tuvastab, mitu inimest kasutas rakendust ja selle funktsioone. Kasutajaid loendatakse anonüümsete ID-de abil. |
| b2cru                                       | Talletab ümbersuunamise URL-i dünaamiliselt.                              |
| JSESSIONID                                  | Maksekonnektor Adyen kasutab seda kasutaja seansi talletamiseks.       |
| OpenIdConnect.nonce.&#42;                       | Autentimine                                               |
| x-ms-cpim-cache:.&#42;                          | Kasutatakse päringu oleku säilitamiseks.                      |
| x-ms-cpim-csrf                              | Päringuvõltsingu (CRSF) talong, mida kasutatakse päringuvõltsingu eest kaitsmiseks.     |
| x-ms-cpim-dc                                | Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari. |
| x-ms-cpim-rc.&#42;                              | Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari. |
| x-ms-cpim-slice                             | Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Kasutatakse SSO seansi haldamiseks.                        |
| x-ms-cpim-trans                             | Kasutatakse toimingute, sealhulgas praeguse toimingu, jälgimiseks (avatud vahekaartide arv, mis autendivad ettevõtte ja tarbija vahelist (B2C) saiti). |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Saidi kasutaja küpsise nõusolek e-kaubanduse saidil 

Kui e-kaubanduse saidi funktsioon või moodul kasutab ebaolulist küpsist, tuleb enne küpsise jälitamist hankida saidi kasutaja nõusolek. Selleks et saidi kasutajad saaksid e-kaubanduse saidil anda küpsise nõusoleku, peab saidi autor lisama ja konfigureerima lehe päisemoodulisse küpsistega nõustumise mooduli, et tagada nõusoleku küsimine ja vastuvõtmine. Saidi kasutaja peab andma nõusoleku, et saidi lehel oleks võimalik renderdada ebaolulist küpsist kasutavat funktsiooni või moodulit.

## <a name="additional-resources"></a>Lisaressursid

[Hõlbustusfunktsioonid ja -võimalused](accessibility.md)

[Vastavuse ülevaade](compliance-overview.md)

[Privaatsuspoliitika lehe lisamine](add-privacy-page.md)

[Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine](replace-IDs-tracked-changes.md)

[Küpsistega nõustumise moodul](cookie-consent-module.md) 
 
[Päisemoodul](author-header-module.md)
