---
title: Küpsise vastavus
description: Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.
author: BrianShook
ms.date: 07/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 509ae998b4d0fa8ab6dd5e3d242dfb4abc492952cd66addc04050fbaff949326
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747693"
---
# <a name="cookie-compliance"></a>Küpsise vastavus

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.

Privaatsus on oluline tegur, kui e-kaubanduse kliente mõjutavad jälgimistehnoloogiad. Eraelu puutumatuse standardite, nagu üldise andmekaitse määruse (GDPR) tõttu Euroopa Liidus (EL), tuleb arvesse võtta elektroonilisi privaatsuspõhimõtted, mis on tänapäeval aktiivsed. Kuna paljud e-kaubanduse saidid on globaalselt juurdepääsetavad vaikimisi, on oluline vaadata üle oma e-kaubanduse saidi vastavuse standardid.

Lisateavet Microsoft kasutavate üldpõhimõtete kohta leiate [Microsofti usalduskeskusest.](https://www.microsoft.com/trust-center) Sellel saidil saate ka lisateavet vastavuse ja privaatsuse valdkondade kohta.

Järgmises tabelis on toodud Dynamics 365 Commerce'i saitide asetatud küpsiste kehtiv viiteloend.

| Küpsise nimi                               | Kasutus                                                        | Eluiga |
| ------------------------------------------- | ------------------------------------------------------------ |  ------- |
| .AspNet.Cookies                             | Talletage Microsoft Azure Active Directory (Azure AD) autentimisküpsised ühekordse sisselogimise (SSO) jaoks. Talletab kasutaja kohta krüptitud põhiteavet (nimi, perekonnanimi, e-post). | Seanss |
| \_msdyn365___cart_                           | Talletab ostukorvi ID, mida kasutatakse ostukorvi eksemplari lisatud toodete loendi hankimiseks. | Seanss |
| \_msdyn365___checkout_cart_                           | Talletab ostukorvi ID, mida kasutatakse ostukorvi eksemplari lisatud toodete loendi hankimiseks. | Seanss |
| \_msdyn365___ucc_                            | Küpsise vastavuse nõusoleku jälgimine.                          | 1 aasta |
| ai_session                                  | Tuvastab, mitu kasutajategevuse seanssi on hõlmanud konkreetseid rakenduse lehti ja funktsioone. | 30 minutit |
| ai_user                                     | Tuvastab, mitu inimest kasutas rakendust ja selle funktsioone. Kasutajaid loendatakse anonüümsete ID-de abil. | 1 aasta |
| b2cru                                       | Talletab ümbersuunamise URL-i dünaamiliselt.                              | Seanss |
| JSESSIONID                                  | Maksekonnektor Adyen kasutab seda kasutaja seansi talletamiseks.       | Seanss |
| OpenIdConnect.nonce.&#42;                       | Autentimine                                               | 11 minutit |
| x-ms-cpim-cache:.&#42;                          | Kasutatakse päringu oleku säilitamiseks.                      | Seanss |
| x-ms-cpim-csrf                              | Päringuvõltsingu (CRSF) talong, mida kasutatakse päringuvõltsingu eest kaitsmiseks.     | Seanss |
| x-ms-cpim-dc                                | Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari. | Seanss |
| x-ms-cpim-rc.&#42;                              | Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari. | Seanss |
| x-ms-cpim-slice                             | Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari. | Seanss |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Kasutatakse SSO seansi haldamiseks.                        | Seanss |
| x-ms-cpim-trans                             | Kasutatakse toimingute, sealhulgas praeguse toimingu, jälgimiseks (avatud vahekaartide arv, mis autendivad ettevõtte ja tarbija vahelist (B2C) saiti). | Seanss |
| \_msdyn365___muid_                            | Kasutatakse, kui eksperimenteerimine on keskkonna jaoks aktiveeritud; kasutatakse katse eesmärgil kassutaja Id-na. | 1 aasta |
| \_msdyn365___exp_                             | Kasutatakse, kui eksperimenteerimine on keskkonna jaoks aktiveeritud; kasutatakse jõudluse koormuse tasakaalustamise mõõtmiseks.         | 1 tund |
| d365mkt                                       | Kasutatakse juhul, kui asukohapõhine tuvastamine kasutaja IP-aadressi jälgimiseks poe asukohasoovituste jaoks on Commerce saidi koostajas lubatud aadressil **Saidisätted \> Üldine \> Luba asukohapõhine poetuvastus**.      | 1 tund |
| \_msdyn365___tuid_                           | Kasutatakse ainult siis, kui katsed on keskkonna jaoks aktiveeritud; loob kasutaja identifikaatorina toimimiseks GUID-i. Väärtus muutub, kui kasutaja sisselogimisolek muutub.      | 1 aasta |
| \_msdyn365___aud_0                          | Talletab sihtimises kasutatavaid segmendiväärtusi ja seda kasutatakse ainult siis, kui sihtimine on konfigureeritud saidi kasutaja soovitud lehel või fragmendil. Küpsis paigutatakse ainult siis, kui segmendi väärtused pärinevad kolmanda osapoole segmentimise pakkujalt.      | 7 päeva |
| \_msdyn365___aud_1                           | Talletab sihtimises kasutatavaid segmendiväärtusi ja seda kasutatakse ainult siis, kui sihtimine on konfigureeritud saidi kasutaja soovitud lehel või fragmendil. Küpsis paigutatakse ainult siis, kui segmendi väärtused pärinevad kolmanda osapoole segmentimise pakkujalt.      | 7 päeva |
| \_msdyn365___aud_2                           | Talletab sihtimises kasutatavaid segmendiväärtusi ja seda kasutatakse ainult siis, kui sihtimine on konfigureeritud saidi kasutaja soovitud lehel või fragmendil. Küpsis paigutatakse ainult siis, kui segmendi väärtused pärinevad kolmanda osapoole segmentimise pakkujalt.      | 7 päeva |

Kui saidi kasutaja valib saidil sotsiaalmeedia lingid, jälgitakse järgmises tabelis olevaid küpsiseid ka nende brauseris.


| Domeen                      | Küpsis               | Kirjeldus                                                  | Allikas                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | LinkedIn Adsi ID sünkroonimine                                      | LinkedIni Feed ja Insight silt                                |
| .linkedin.com               | li_sugr                  | Brauseri identifikaator                                           | LinkedIn Insighti silt, kui IP-aadress pole määratud riigis |
| .linkedin.com               | BizographicsOptOut       | Määratleb loobumisoleku kolmanda osapoole jälgimiseks.              | LinkedIni külalisjuhtelemendid ja tööstusest loobumise lehed           |
| .linkedin.com               | \_guid                    | Google Adsi brauseri identifikaator.                            | LinkedIn Feed                                                |
| .linkedin.com               | li_oatml                 | Liikme kaudne identifikaator teisenduse jälgimiseks, ümbersuunamiseks ja analüüsimiseks. | LinkedIni Ads ja Insight sildid                                |
| Erinevad esimese osapoole domeenid | li_fat_id                | Liikme kaudne identifikaator teisenduse jälgimiseks, ümbersuunamiseks ja analüüsimiseks. | LinkedIni Ads ja Insight sildid                                |
| .adsymptotic.com            | U                        | Brauseri identifikaator                                           | LinkedIn Insighti silt, kui IP-aadress pole määratud riigis |
| .linkedin.com                | bcookie                  | Brauseri ID küpsis                                            | Taotlused LinkedInile                                         |
| .linkedin.com                | bscookie                 | Turvaline brauseriküpsis                                        | Taotlused LinkedInile                                         |
| .linkedin.com               | lang                     | Määrab vaikelokaadi ja keele.                                 | Taotlused LinkedInile                                         |
| .linkedin.com                | lidc                     | Kasutatakse marsruutimiseks.                                             | Taotlused LinkedInile                                         |
| .linkedin.com               | aam_uuid                 | Adobe'i publikuhalduri küpsis                                                     | ID sünkroonimise määramine                                              |
| .linkedin.com               | \_ga                      | Google Analyticsi küpsis                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analyticsi küpsis                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analyticsi küpsis                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Küpsis sisaldab praegu sisselogitud kasutaja ID-d.  |   Facebook                                                           |
| .facebook.com               | datr                     | Kasutatakse sisselogitud kasutajast sõltumatu Facebook ühenduse loomiseks kasutatava veebibrauseri tuvastamiseks. | Facebook                                                             |
| .facebook.com               | wd                       | Talletab brauseriakna mõõtmed ja seda kasutatakse Facebook lehe renderdamise optimeerimiseks. | Facebook                                                             |
| .facebook.com               | xs                       | Seansi numbrit tähistav kahekohaline number. Väärtuse teine osa on seansi saladus. |  Facebook                                                            |
| .facebook.com               | fr                       | Sisaldab unikaalset brauserit ja kasutaja ID-d, mida kasutatakse sihitud reklaamiks. |  Facebook                                                            |
| .facebook.com               | sb                       | Kasutatakse Facebook sõprade soovituste parandamiseks.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Küpsis sisaldab praegu sisselogitud kasutaja ID-d.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Küpsis sisaldab praegu sisselogitud kasutaja ID-d.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Küpsis sisaldab lehti, kui kasutaja valib Pinteresti nupu.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Küpsis sisaldab lehti, kui kasutaja valib Pinteresti nupu.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Sisaldab kasutaja ID-d ja ajatemplit küpsise loomisel. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Küpsis sisaldab lehti, kui kasutaja valib Pinteresti nupu.      | Pinterest                                                             |
| .pinterest.com              | seanssFunnelEventLogged | Küpsis sisaldab lehti, kui kasutaja valib Pinteresti nupu.      | Pinterest                                                             |
| .pinterest.com              | Kohalik salvestusruum            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Teenindustöötajad          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Saidi kasutaja küpsise nõusolek e-kaubanduse saidil 

Kui e-kaubanduse saidi funktsioon või moodul kasutab ebaolulist küpsist, tuleb enne küpsise jälitamist hankida saidi kasutaja nõusolek. Selleks et saidi kasutajad saaksid e-kaubanduse saidil anda küpsise nõusoleku, peab saidi autor lisama ja konfigureerima lehe päisemoodulisse küpsistega nõustumise mooduli, et tagada nõusoleku küsimine ja vastuvõtmine. Saidi kasutaja peab andma nõusoleku, et saidi lehel oleks võimalik renderdada ebaolulist küpsist kasutavat funktsiooni või moodulit.

## <a name="additional-resources"></a>Lisaressursid

[Hõlbustusfunktsioonid ja -võimalused](accessibility.md)

[Vastavuse ülevaade](compliance-overview.md)

[Privaatsuspoliitika lehe lisamine](add-privacy-page.md)

[Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine](replace-IDs-tracked-changes.md)

[Küpsistega nõustumise moodul](cookie-consent-module.md) 
 
[Päisemoodul](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
