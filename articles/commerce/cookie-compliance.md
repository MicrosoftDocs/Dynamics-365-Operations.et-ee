---
title: Küpsise vastavus
description: Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.
author: BrianShook
ms.date: 05/21/2021
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
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088383"
---
# <a name="cookie-compliance"></a>Küpsise vastavus

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.

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
| \_msdyn365___muid_                            | Kasutatakse, kui eksperimenteerimine on keskkonna jaoks aktiveeritud; kasutatakse katse eesmärgil userId-na. |
| \_msdyn365___exp_                             | Kasutatakse, kui eksperimenteerimine on keskkonna jaoks aktiveeritud; kasutatakse jõudluse koormuse tasakaalustamise mõõtmiseks.         |
| d365mkt                                       | Kasutatakse juhul, kui asukohapõhine tuvastamine kasutaja IP-aadressi jälgimiseks poe asukohasoovituste jaoks on Commerce saidi koostajas lubatud aadressil **Saidisätted > Üldine > Luba asukohapõhine poetuvastus**.      |

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
