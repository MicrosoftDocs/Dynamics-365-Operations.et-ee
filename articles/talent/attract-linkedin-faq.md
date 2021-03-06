---
title: LinkedIni integreerimise KKK
description: See teema vastab küsimustele, mis võivad olla seotud LinkedIni ja Microsoft Dynamics 365 Talent – Attracti integreerimisega.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 35428da709f480e1d3842b7e92deacba200326ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460893"
---
# <a name="linkedin-integration-faq"></a>LinkedIni integreerimise KKK

[!include [banner](includes/banner.md)]

LinkedIn on maailma suurim tööalane veebivõrgustik. Microsoft Dynamics Talent: Attract integreerub LinkedIniga, et anda juurdepääs maailma tipptalentidele. Attract võimaldab postitada tööpakkumised otse LinkedIni ja samuti kandidaatide teavet LinkedInist Attracti tõmmata.

## <a name="for-recruiters-and-hiring-managers"></a>Värbajatele ja tööd pakkuvatele juhtidele

Siin on vastused korduma kippuvatele küsimustele selle kohta, kuidas koos Attracti ja LinkedIni kasutada.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Millised LinkedIni funktsioonid saan koos Attractiga?

Attracti integreerimine LinkedIniga võimaldab teha järgmisi ülesandeid:

- [Sisestada tööpakkumised LinkedIni](./attract-post-jobs-to-linkedin.md) (tasuta piiratud loenditena).
- [LinkedIn Recruiteriga allikakandidaadid rakenduses Microsoft Dynamics 365 Talent – Attract](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Rakendusega LinkedIn for Microsoft Dynamics 365 Talent – Attract integreerimise seadistamine](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Mida on vaja enne tööpakkmiste sisestamist LinkedIni?

Teie administraator peab [konfigureerima LinkedIni integratsiooni Attractiga](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Pärast seda olete valmis alustama.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Kuidas sisestada tööpakkumisd Attractist LinkedIni?

Pärast tööpakkumise loomist Attractis peate lihtsalt valima **Sisesta kohe** nupu, mis vastab LinkedInile. Lisateabe saamiseks vaadake jaotist [Rakendusest Microsoft Dynamics 365 Talent – Attract LinkedIni postitamine](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Kas ma saan LinkedInist kandidaatide teavet Attracti?

Jah. Kui näete LinkedInis head kandidaati, saate hõlpsalt eksportida selle kandidaadi teabe Attracti. Lisateabe saamiseks vaadake jaotist [LinkedIn Recruiteriga allikakandidaadid rakenduses Microsoft Dynamics 365 Talent – Attract](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Kuidas saada abi LinkedInile ligipääsemiseks Attractist?

Kui teil on probleeme LinkedIni sisselogimisega või töökohtade postitamisega Attractist, vaadake jaotist [LinkedIni ja rakendusega Microsoft Dynamics 365 Talent – Attract integreerimise tõrkeotsing](./attract-troubleshoot-linkedin.md).

Muude Attracti probleemide puhul vaadake jaotist [Microsoft Dynamics 365 Talenti toe hankimine](./talent-support.md). Abi saamiseks LinkedIni kohta vaadake teemat [LinkedIni kasutajatoe leht](https://www.linkedin.com/help).

## <a name="for-admins-and-developers"></a>Administraatoritele ja arendajatele

Siin on vastused korduma kippuvatele küsimustele selle kohta, kuidas konfigureerida integratsiooni Attracti ja LinkedIni vahel.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Kuidas konfigureerida Attracti nii, et värbajad ja tööd pakkuvad juhid saaksid LinkedIni tööpakkumisi sisestada?

Saate konfigureerida saadaolevad valikud vahekaardil **LinkedIni integreerimine** Admin centeris. Lisateavet leiate teemast [Rakendusega LinkedIn for Microsoft Dynamics 365 Talent – Attract integreerimise seadistamine](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>Kas LinkedInist saab eksportida kandidaatide teavet?

Jah, kuid esmalt tuleb teil integratsioon konfigureerida teenusega LinkedIn Recruiter. Lisateavet leiate teemast [Rakendusega LinkedIn for Microsoft Dynamics 365 Talent – Attract integreerimise seadistamine](./attract-admin-linkedin.md).

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>Kuidas saab sisestada LinkedIni Premium tööpakkumisi?

Kuigi Attract pakub LinkedIni tööpakkumiste sisestamiseks võimsat lahendust, võib osutuda vajalikuks täiendav paindlikkus. Näiteks võite soovi korral lisaks tasuta piiratud loenditele sisestada ka Premium tööpakkumisi või soovite, et LinkedIn töötleks teie pakett-töö postitusi rohkem kui üks kord päevas.

#### <a name="types-of-linkedin-job-posts"></a>LinkedIni tööpakkumiste sisestamise tüübid

LinkedIn pakub järgmist tüüpi tööpakkumiste sisestamist:

- **Piiratud loend** – tasuta tööpakkumiste sisestamised, mis ilmuvad otsingutulemustes, kui kandidaadid otsivad tööd LinkedInis ja ettevõtte LinkedIni lehel. Piiratud loendid on suunatud aktiivsetele tööotsijatele. Seda tüüpi kirje on tüüp, mille Attract LinkedInile pakub. LinkedInis ei saa piiratud loendiga töid reklaamida. Kui soovite reklaamida piiratud loendeid, peate töötama koos LinkedIniga, et lubada n-ö tööpakkumiste kokkupakkimist. Lisateavet tööpakkumiste kokkupakkimise kohta vaadake teemast [Piiratud loendid vs Premium tööpakkumised tööpakkumiste kokkupakkimiseks](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) ja [Tööpakkumiste kokkupakkimine Plus – KKK](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **Premium tööpakkumine** – ostetud tööpakkumiste postitused, mis kuvatakse LinkedIni erinevates kohtades, näiteks LinkedIni kanalis, meilides ja alal **Töökohad, mis võivad teile huvi pakkuda**. Premium tööpakkumised on suunatud passiivsetele kandidaatidele, kuid need ilmuvad ka tööpakkumiste otsingutes.

Attract sisestab tööpakkumised LinkedIni piiratud loenditena. Kui soovite kasutada Premium tööpakkumisi, peate kasutama tööpakkumiste kokkupakkimist LinkedIn Recruiteri kaudu. Tööpakkumiste kokkupakkumine nõuab tööpakkumiste kokkupakkumise lepingut LinkedIniga. Lisateavet lugege teemast [Tööpakkumiste kokkupakkimine teenuse LinkedIn Recruiter kaudu – ülevaade](https://www.linkedin.com/help/recruiter/answer/79037).

#### <a name="frequency-of-batch-processing-on-linkedin"></a>Pakktöötluse sagedus LinkedInis

LinkedIn töötleb tööpakkumisi paketis Attracti kaudu üks kord päevas. Seetõttu võib LinkedInis tööpakkumiste ilmumiseks pärast nende sisestamist Attracti kaudu kuluda kuni 48 tundi. Kui soovite, et LinkedInis kuvataks tööpakkumised varem või kui vajate täiendavat paindlikkust, saate LinkedInis kasutada rakenduse Recruiter System Connect programmeerimisliidest (API). Lisateavet leiate teemast [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect).

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>LinkedIni tööpakkumiste valiku tabel

Järgmises tabelis kirjeldatakse erinevaid valikuid tööpakkumiste sisestamiseks LinkedIni. See sisaldab iga võimaluse eeliseid ja lisateavet.

|  | Attract | Tööpakkumiste kokkupakkimine teenuse LinkedIn Recruiter kaudu | Recruiter System Connecti API |
|---|---|---|---|
| **Kirjeldus** | Attract sisestab tööpakkumised LinkedIni XML-kanalina. | Ettevõte sõlmib lepingu LinkedIniga ja pakub tööpakkumiste sisestamiseks XML-kanalit. | Klient kasutab API-t Attracti ja teenuse LinkedIn Recruiter vahelise teabe sünkroonimiseks. |
| **Mis tüüpi tööpakkumisi saab sisestada?** | Piiratud loend | Premium tööpakkumised või piiratud loend | Piiratud loend |
| **Kas LinkedInis saab tööpakkumisi reklaamida?** | Ei | Premium tööpakkumised: jah<br>Piiratud loendid: ei | Ei |
| **Kui tihti LinkedIn postitab tööpakkumisi?** | Korra päevas | Korra päevas | Mitu korda päevas, nagu on määratletud API-s |
| **Soovitab LinkedIn?** | Ei | Jah | Ei |
| **Mida on vaja?** | Attracti ostmine | Tööpakkumiste kokkupakkimise leping LinkedIniga ja Premium töö tööpakkumiste ostmine | API leping LinkedIniga | 
| **Kust leida rohkem teavet?** | [Rakendusega LinkedIn for Microsoft Dynamics 365 Talent – Attract integreerimise seadistamine](./attract-admin-linkedin.md) | [Tööpakkumiste kokkupakkimine teenuse LinkedIn Recruiter kaudu – ülevaade](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> Te ei vaja teenuse LinkedIn Recruiter System Connect litsentsi, et sisestada tööpakkumisi LinkedIni koos Attractiga.

## <a name="see-also"></a>Vt ka

[Rakendusega LinkedIn for Microsoft Dynamics 365 Talent – Attract integreerimise seadistamine](./attract-admin-linkedin.md)

[Rakendusest Microsoft Dynamics 365 Talent – Attract LinkedIni postitamine](./attract-post-jobs-to-linkedin.md)

[LinkedIn Recruiteriga allikakandidaadid rakenduses Microsoft Dynamics 365 Talent – Attract](./attract-linkedin-recruiter.md).

[Rakendusega Microsoft Dynamics 365 Talent – Attract ja LinkedIniga integreerimise tõrkeotsing](./attract-troubleshoot-linkedin.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]