---
title: Andmete eksportimine Attractist ja Onboardist
description: Andmete eksportimine Dynamics 365 Talent - Attractist ja Onboardist.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460869"
---
# <a name="export-data-from-attract-and-onboard"></a>Andmete eksportimine Attractist ja Onboardist

[!include [banner](includes/banner.md)]

Nagu välja kuulutatud jaotises [Rakenduste Dynamics 365 Talent: Attract ja Dynamics 365 Talent: Onboard pensionile jäämine](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), saadame rakendused Dynamics 365 Talent: Attract ja Dynamics 365 Talent: Onboard pensionile 1. veebruaril 2022. Et aidata kaasa teie migreerumisele mõnele muule tootele, pakuvad mõlemad rakendused nüüd andmete eksportimise võimalusi.

## <a name="export-data-from-attract"></a>Andmete eksportimine Attractist

Saate oma andmeid eksportida ilma keskkonnale juurdepääsu piiramata. Võite soovida seda teha testimise eesmärgil või meie andmestruktuuri mõistmiseks. Kui olete valmis migreerima, piirake juurdepääsu oma Attracti keskkonnale, kasutades sellele protseduurile järgnevaid juhiseid. Eksportige oma andmed kindlasti uuesti. 

1. Avage [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Valige jaotises **Andmete eksport** käsk **Taotle andmeid eksportimist**.

   ![[Attractist andmete ekspordi taotlemine](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Kui kuvatakse sõnumit **Teie taotlus on töötluses** valige nupp **OK**. Sõltuvalt ekspordi mahust võib andmete eksport võtta kuni 20 minutit.

4. Kui eksport jõuab lõpuni, valige selle kõrval nupp **Laadi alla**. 

   >[!NOTE]
   >Kõik andmete ekspordid on saadaval seitsme päeva jooksul, pärast mida link **Laadi alla** aegub.</br>
   
Alla laaditav fail sisaldab teie Attracti andmetega .zip faili, sealhulgas on järgmised kaustad.

| Kausta nimi | Kirjeldus |
| --- | --- |
| Administraatori sätted | Attracti halduskeskuse konfiguratsioonid. |
| Kandidaadid | Kõik kandidaadid, kes lisati töödele või talendikaustadesse. |
| E-kirjade mallid | Kõik keskkonnas konfigureeritud meilimallid. |
| Tööpakkumiste paketi mallid | Kõik loodud tööpakkumise paketi mallid ja nendega seotud konfiguratsioonid. |
| Tööpakkumise reeglite komplektid |  Kõik reeglitekomplektide failid, mis laaditi pakkumise haldamiseks üles. |
| Tööpakkumiste mallid | Kõik keskkonnas loodud tööpakkumise dokumendi mallid. |
| Vabad töökohad | Kõik loodud tööd. Kustutatud töid ei ekspordita. Alamkaustad sisaldavad kandidaatide avaldusi koos kandidaatide avalduste manuste allkaustadega ja pakkumiste pakettidega, kui see on kohaldatav. |
| Vaba töökoha mall | Keskkonnas konfigureeritud tööprotsessi meilimallid. |
| Talendikaustad | Kõik loodud talendikaustad, nende toetajate nimekirjad ja talendikaustade kandidaatide nimekirjad. |
| Töötajad | Kõigi töötajate loend, kes on keskkonnas olemas ning nende rollid. |
| (juurkaust) | JSON-skeemifaili, mis kirjeldab andmestruktuuri väljasid. |

### <a name="restrict-access-to-attract"></a>Attracti juurdepääsu piiramine

Kui olete valmis migreerima, piirake mitte-administraatoritele juurdepääs oma Attracti keskkonnale ja eksportige oma andmed.

>[!IMPORTANT]
>Juurdepääsu piiramine teie Attracti keskkonnale on püsiv ja seda ei saa tagasi võtta. Kui soovite, et mitte-administraatoritest kasutajad säilitaksid juurdepääsu teie keskkonnale, jätke see samm vahele.

1. Avage [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Et piirata mitte-administraatoritele juurdepääsu oma Attracti keskkonnale, valige jaotises **Piira sellele rakendusele juurdepääs** käsk **Piira kohe juurdepääs**. Juurdepääsu piiramine võtab maha ka kõik sisestatud aktiivsed tööd.

   ![[Attracti juurdepääsu piiramine mitte-administraatoritele](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Kui näete hoiatust **See on püsiv muudatus**, valige **Keela juurdepääs**, et piirata püsivalt mitte-administraatoritele juurdepääs sellele keskkonnale. Kui te pole valmis seda etappi lõpetama, valige käsk **Tühista**.

   ![[Hoiatus, et juurdepääsu piiramine on püsiv muudatus](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Administraatorid pääsevad jätkuvalt juurde andmetele ekspordile ja isikuaruande leheküljele ka pärast Attracti keskkonna juurdepääsu piiramist.

## <a name="export-data-from-onboard"></a>Andmete eksportimine Onboardist

Kui olete valmis, saate Onboardist laadida alla malle, juhiseid ja kandidaatide andmeid.

1. Avage [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Valige jaotises **Andmete eksport** käsk **Taotle andmeid eksportimist**. 

   ![[Onboardist andmete ekspordi taotlemine](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Kui kuvatakse sõnumit **Teie taotlus on töötluses** valige nupp **OK**. Sõltuvalt ekspordi mahust võib andmete eksport võtta kuni 20 minutit.

4. Kui eksport jõuab lõpuni, valige selle kõrval nupp **Laadi alla**. 

   ![[Andmete ekspordi allalaadimine Onboardist](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Teie andmete eksport on saadaval seitse päeva. Pärast seitset päeva link **Laadi alla** aegub peate taotlema uut eksporti, kui peate oma andmed uuesti alla laadima. Kui alustate uute andmete eksporti, aeguvad kõik olemasolevad allalaadimised pärast uue ekspordi õnnestumist.

Allalaadimine on zip-fail, mis sisaldab järgmist.

- Kaust **Mallid**, mis sisaldab teie Onboardi malle Wordi dokumendi vormingus.

- Kaust **Juhised**, mis sisaldab teie Onboardi juhiseid Wordi dokumendi vormingus.

## <a name="see-also"></a>Vt ka

[Dynamics 365 Talent: Attracti ja Dynamics 365 Talent: Onboardi pensionile saatmine](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)

[!INCLUDE[footer-include](../includes/footer-banner.md)]