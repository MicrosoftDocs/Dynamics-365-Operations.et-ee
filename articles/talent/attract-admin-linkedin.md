---
title: LinkedIni Attractiga integreerimise seadistamine
description: Selles teemas selgitatakse, kuidas konfigureerida LinkedIni integreerimine rakenduse Dynamics 365 Talent – Attract jaoks, et saaksite hõlpsalt sisestada tööpakkumised rakendusse Attract LinkedIn ja et värbajad saaksid sünkroonida värbamisteavet kandidaadi LinkedIni profiiliga.
author: andreabichsel
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
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4c518fb7036d44aa52c8db859ee3616fc4e58a06
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833180"
---
# <a name="set-up-linkedin-integration-with-attract"></a>LinkedIni Attractiga integreerimise seadistamine

[!include [banner](includes/banner.md)]

LinkedIni integreerimise konfigureerimine rakendusega Microsoft Dynamics 365 Talent: Attract aitab värbajatel ja tööd pakkuvatel juhtidel tipptalente ligi meelitada. Attract võimaldab teil postitada tööpakkumised otse LinkedIni, mis on suurim tööalane veebivõrgustik.

Tööpakkumised, mille sisestate LinkedIni Attracti kaudu kaudu, on piiratud loendiga ja neid pakutakse teie ettevõttele ilma lisatasuta. Need loendid on saadaval ainult LinkedIni tarkvarapartnerite, nt Attracti kaudu. Neid ei kuvata teie ettevõtte LinkedIni lehel paneelil **Karjäär**, kuna seal kuvatakse ainult tasulisi loendeid. Neid näidatakse aga siis, kui potentsiaalsed kandidaadid vaatavad kõiki saadaolevaid töökohti. Piiratud loendeid kuvatakse ka LinkedIni tööotsingutes.

Attract pakub LinkedIniga integreerimiseks kahte võimalust, mis aitavad teil sellelt populaarselt karjäärisaidilt kandidaate leida.

- Tööde sisestamine Attractist LinkedIni
- Kandidaatide otsimine LinkedInist Attractini.

Konfigureerite mõlemad valikud vahekaardil **LinkedIni integreerimine** Admin centeris. Admin centeri avamiseks minge aadressile <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> LinkedIn Recruiter integreerimise kasutamiseks Attractiga on teil vaja [Põhjalik värbamise lisandmoodul](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) and [LinkedIn Recruiter licenses](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Lisateabe saamiseks vaadake jaotist [Milline rakenduse Microsoft Dynamics 365 Talent – Attract versioon?](./attract-comprehensive-hiring.md).

Kui teil on probleeme LinkedIni töökohtade postitamisega, vaadake jaotist [LinkedIni ja rakendusega Microsoft Dynamics 365 Talent – Attract integreerimise tõrkeotsing](./attract-troubleshoot-linkedin.md).

Lisateavet LinkedIni töökohtade postitamise muude viiside kohta leiate jaotisest [Attracti integreerimine LinkedIni KKK-ga](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Tööpakkumiste sisestamise konfigureerimine LinkedIni

Enne tööpakkumiste postitamist Attractist LinkedIni on teil vaja [LinkedIni ettevõtte ID-d](https://aka.ms/findID). LinkedIni jaoks kasutatav ettevõtte ID on kordumatu numbrijada, mis eristab teie ettevõtet LinkedInis. Lisateavet leiate teemast [LinkedIni ettevõtte ID seostamine LinkedIni töölauaga – korduma kippuvad küsimused](https://aka.ms/findID).

Attract saadab teie tööpakkumiste kanali LinkedIni ja LinkedIn kontrollib voogu umbes üks kord päevas. Tööpakkumiste sisestamiseks saidile võib kuluda kuni 48 tundi.

LinkedIni sisestatud töökohad ilmuvad otse LinkedIni saidil. LinkedInil puudub katsekeskkond töökohtade sisestamiseks. Seetõttu veenduge, et te ei sisesta kogemata ühtegi testtööpakkumist. 

1. Valige ülemises parempoolses nurgas olevast menüüst **Seadistus** (hammasratta sümbol) suvand **Halduskeskus**. Teise võimalusena võite avada <https://attract.talent.dynamics.com/adminsettings>.
2. Valige vahekaart **LinkedIni integreerimine**.
3. Sisestage jaotises **Ettevõtte nimi** oma ettevõtte nimi ja väljale **Ettevõtte ID** oma LinkedIni ettevõtte ID. Veenduge, et ettevõtte nimi vastaks teie ettevõtte LinkedIni lehel kuvatavale nimele. Lisateavet LinkedIni ettevõtte ID kohta leiate teemast [LinkedIni ettevõtte ID sidumine LinkedIni töölauaga – korduma kippuvad küsimused](https://www.linkedin.com/help/linkedin/answer/98972).

    Kui teil on vaja oma organisatsiooni teavet muuta, lugege teemat [Organisatsiooni aadressi, tehnilise kontakti ja muu teabe muutmine](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Kui teil on endiselt probleeme, pöörduge [LinkedIni toe](https://www.linkedin.com/help/linkedin) poole.

4. Valige käsk **Salvesta**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Platvormi LinkedIn Recruiter ja rakenduse Attract seadistamine 

Et lubada värbajatel rakenduse LinkedIn Recruiter kaudu tööd pakkuda, peate Attractis konfigureerima integreerimise rakendusega LinkedIn Recruiter. Konfigureerimise lõpuleviimiseks peate töötama kasutajaga, kes on teie ettevõtte LinkedIn Recruiter lepingu järgi administraator.

1. Valige ülemises parempoolses nurgas olevast menüüst **Seadistus** (hammasratta sümbol) suvand **Halduskeskus**. Teise võimalusena võite avada <https://attract.talent.dynamics.com/adminsettings>.
2. Valige vahekaart **LinkedIni integreerimine**.

    [![Attracti administraatori vaade LinkedIn Recruiteri integreerimise käivitamiseks](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Seadistamise alustamiseks valige **Ühenda**. Teid juhendatakse LinkedIni sisselogimisprotsessi kaudu.
4. Kui teil on töökohad mitmes LinkedIni lepingus, valige leping, mida soovite Attracti süsteemiga ühendada. Kui teil on töökoht ainult ühes LinkedIni lepingus, saate selle toimingu vahele jätta.
5. Valige **Recruiter System Connect (RSC)** all **Taotlus**.

    [![Attracti administraatori vaade LinkedIn Recruiteri integreerimise taotlemiseks](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. **Recruiter System Connect (RSC)** säte peaks nüüd ilmuma kujul **Partner on valmis**. Kui näete sellel lehel teadet **Teavita partnerit**, oodake paar sekundit, valige teade **Teavita partnerit** ja seejärel värskendage lehekülge. Säte peaks nüüd ilmuma kujul **Partner on valmis**.

    [![Attracti administraatori vaade, mis näitab, et Attracti pool taotlusest on täidetud](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Järgmiste toimingute tegemiseks peavad teie rakenduse LinkedIn Recruiter lepingul olema administraatoriõigused.

    1. Logige administraatorikonto abil LinkedIni sisse ja valige paremas ülanurgas **LinkedIn Recruiter**. 
    2. Valige lehe ülaosas olevas menüüs **Rohkem** **Administraatori sätted** ja seejärel valige **ATS** vahekaardil.
    3. Ühe klõpsuga ekspordi lubamiseks ainult ühe lepingu puhul lülitage sisse **Lepingu taseme juurdepääs (iga selle lepingu töökoha kohta**. Kogu ettevõtte lubamiseks lülitage sisse **Ettevõtte taseme juurdepääs (iga lepingu puhul teie ettevõttes.**

    [![Attracti integratsiooni sisselülitamine LinkedIn Recruiteri administraatori vaatest](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Valige Attract Admin centeris vahekaart **LinkedIni integreerimine**. **Recruiter System Connect (RSC)** säte peaks nüüd olema kujul **Lubatud**.

    [![LinkedIn Recruiter integratsioon on lõpetatud](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>LinkedIniga kandideerimise häälestamine Attractis

Saate lubada kandidaatidel kandideerida tööle nende LinkedIni profiilide abil. Lisateavet funktsiooni Kandideeri LinkedIniga kohta leiate teemast [LinkedIni võimsus kõikjal: kandideerige LinkedIniga](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

See funktsioon on praegu eelvaateversioonis. Enne nende toimingute tegemist veenduge, et Kandideeri LinkedIniga on lubatud. Lisateavet eelvaatefunktsioonide lubamise kohta vaadake jaotisest [Eelvaatefunktsioonide juurdepääs rakenduses Microsoft Dynamics 365 Talent](./access-preview-feature.md).

1. Valige ülemises parempoolses nurgas olevast menüüst **Seadistus** (hammasratta sümbol) suvand **Halduskeskus**. Teise võimalusena võite avada <https://attract.talent.dynamics.com/adminsettings>.
2. Valige vahekaart **LinkedIni integreerimine**.

    [![Attracti administraatori vaade LinkedIn Recruiteri integreerimise käivitamiseks](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Valiku **Kandideeri LinkedIniga** kõrval valige seadistamise alustamiseks **Ühenda**. Teid juhendatakse ülejäänud protsessis LinkedIni kaudu.

## <a name="see-also"></a>Vt ka

[Attracti integreerimine LinkedIni KKK-ga](./attract-linkedin-faq.md)

[Tööde sisestamine Attracti-välistele karjäärisaitidele](./posting-jobs-external.md)

[LinkedIn Recruiteriga allikakandidaadid rakenduses Microsoft Dynamics 365 Talent – Attract](./attract-linkedin-recruiter.md).

[Tööde loomine, kinnitamine ja sisestamine Attractis](./creating-jobs-attract.md)

[Rakendusega Microsoft Dynamics 365 Talent – Attract ja LinkedIniga integreerimise tõrkeotsing](./attract-troubleshoot-linkedin.md).
