---
title: Attracti integreerimine LinkedIni KKK-ga
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
ms.openlocfilehash: b77ad598ba209dbbd73765c49947e84a3995153d
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550363"
---
# <a name="attract-integration-with-linkedin-faq"></a>Attracti integreerimine LinkedIni KKK-ga

[!include [banner](includes/banner.md)]

LinkedIn on maailma suurim tööalane veebivõrgustik. Microsoft Dynamics Talent: Attract integreerub LinkedIniga, et anda juurdepääs maailma tipptalentidele. Attract võimaldab postitada tööpakkumised otse LinkedIni ja samuti kandidaatide teavet LinkedInist Attracti tõmmata.

## <a name="for-recruiters-and-hiring-managers"></a>Värbajatele ja tööd pakkuvatele juhtidele

Siin on vastused korduma kippuvatele küsimustele selle kohta, kuidas koos Attracti ja LinkedIni kasutada.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Millised LinkedIni funktsioonid saan koos Attractiga?

Attracti integreerimine LinkedIniga võimaldab teha järgmisi ülesandeid:

- [Sisestada tööpakkumised LinkedIni](./attract-post-jobs-to-linkedin.md) (tasuta piiratud loenditena).
- [Eksportida kandidaatide teavet LinkedInist Attracti](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Lubada kandidaatidel teie tööpakkumistele LinkedIniga kandideerida](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Mida on vaja enne tööpakkmiste sisestamist LinkedIni?

Teie administraator peab [konfigureerima LinkedIni integratsiooni Attractiga](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Pärast seda olete valmis alustama.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Kuidas sisestada tööpakkumisd Attractist LinkedIni?

Pärast tööpakkumise loomist Attractis peate lihtsalt valima **Sisesta kohe** nupu, mis vastab LinkedInile. Lisateavet vaadake teemast [Tööpakkumiste sisestamine Attractist LinkedIni](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Kas ma saan LinkedInist kandidaatide teavet Attracti?

Jah. Kui näete LinkedInis head kandidaati, saate hõlpsalt eksportida selle kandidaadi teabe Attracti. Lisateavet leiate artiklist [Kandidaatide leidmine rakendusega LinkedIn Recruiter](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Kuidas saada abi LinkedInile ligipääsemiseks Attractist?

Kui teil on probleeme sisselogimise või LinkedInist Attracti tööpakkumiste sisestamisega, lugege teemat [LinkedIniga integreerimise tõrkeotsing](./attract-troubleshoot-linkedin.md).

Muude Attractiga seotud probleemide korral vaadake teemat [Abi saamine Talenti jaoks](./talent-support.md). Abi saamiseks LinkedIni kohta vaadake teemat [LinkedIni kasutajatoe leht](https://www.linkedin.com/help).

## <a name="for-admins-and-developers"></a>Administraatoritele ja arendajatele

Siin on vastused korduma kippuvatele küsimustele selle kohta, kuidas konfigureerida integratsiooni Attracti ja LinkedIni vahel.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Kuidas konfigureerida Attracti nii, et värbajad ja tööd pakkuvad juhid saaksid LinkedIni tööpakkumisi sisestada?

Saate konfigureerida saadaolevad valikud vahekaardil **LinkedIni integreerimine** Admin centeris. Lisateavet vaadake teemast [Integreerimise häälestamine LinkedIniga](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>Kas LinkedInist saab eksportida kandidaatide teavet?

Jah, kuid esmalt tuleb teil integratsioon konfigureerida teenusega LinkedIn Recruiter. Lisateavet vaadake teemast [Integreerimise häälestamine LinkedIniga](./attract-admin-linkedin.md).

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
| **Kust leida rohkem teavet?** | [LinkedIn-iga integreerimise seadistamine](./attract-admin-linkedin.md) | [Tööpakkumiste kokkupakkimine teenuse LinkedIn Recruiter kaudu – ülevaade](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> Te ei vaja teenuse LinkedIn Recruiter System Connect litsentsi, et sisestada tööpakkumisi LinkedIni koos Attractiga.

## <a name="see-also"></a>Vt ka

[LinkedIn-iga integreerimise seadistamine](./attract-admin-linkedin.md)

[Tööde sisestamine Attractist LinkedIn-i](./attract-post-jobs-to-linkedin.md)

[Kandidaatide hankimine teenuse LinkedIn Recruiter abil](./attract-linkedin-recruiter.md)

[LinkedIniga integreerimise tõrkeotsing](./attract-troubleshoot-linkedin.md)
