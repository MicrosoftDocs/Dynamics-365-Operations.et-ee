---
title: 'Sisseelamisjuhendite ja mallide redigeerimine rakenduses Dynamics 365 Talent: Onboard'
description: 'See teema selgitab, kuidas lisada Microsoftis sisseelamisjuhendite ja mallide jaoks tegevusi ja muud teavet rakenduses Dynamics 365 Talent: Onboard.'
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7803c7cd2c58b8544d2c8dd711c295d6882f9fca
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010794"
---
# <a name="edit-onboarding-guides-and-templates"></a>Sisseelamisjuhendite ja mallide redigeerimine

[!include [banner](includes/banner.md)]

Pärast seda, kui olete Microsoftis Dynamics 365 Talent: Onboard käivitanud juhendi või malli, tuleb teil lisada sissejuhatus, tegevused, kontaktid ja ressursid. Onboard võimaldab teil lisada rikkalikku sisu sisseelamisjuhenditesse, sealhulgas:

- YouTube'i videod
- Microsoft Sway esitlusi
- Microsoft PowerApps rakendused
- Microsoft Streami videod
- Microsoft Formsi vormid
- Veebisisu sisaldavad iframe'id

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Mallist imporditud asustamise või tegevuste redigeerimine

Kui loote sisseelamisjuhendi mallist või kui impordite tegevusi ühest mallist teise, märkate imporditud tegevuste **Lukustamise** nuppu. Neid kutsutakse *Hallatavaks tegevuseks*.

[![Hallatud tegevused](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Hallatud tegevuste valimisel saate kuvada allikamalli tegevuste ülaosas.

[![Hallatud tegevuste allikas](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Kui redigeerite mõnda tegevust mallis, lükkab Onboard muudatused ümber kõigile mallil põhinevatele mallidele ja saatmata juhenditele. Kui valite saatmata juhendi, mis põhineb redigeeritud mallil ja valite seejärel vahekaardi **Tegevused**, kuvatakse teade, et teie juhend on muutunud. Teatise lõpetamiseks valige **OK**. 

[![Teatise muutmine.](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Kuvatakse värskendatud tegevuste kõrval must täpp.

[![Muudetud tegevus](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Hallatavaid tegevusi ei saa redigeerida algsest mallist väljaspool, välja arvatud selleks, et lisada õiguste, tähtaja või muu teave tegevuse parempoolses jaotises.

Kui soovite hallatavate tegevuste redigeerimist või kui te ei soovi, et see võtaks vastu värskendusi mallist, kust see pärineb, valige selle toimingu jaoks **Lukustamise** nupp. **Lukustuse** nupp kaob. Algne mall ei halda enam seda tööd ja see ei saa enam selle malli värskendusi. Tegevused, mida teete, ei mõjuta algset malli.

Kui kustutate tegevuse juhendist ja vajutate selle juhendi mallist muudatusi, jääb tegevus juhendist kustutatuks.

> [!NOTE]
> Mallid ei halda kontakte ja ressursse. Lisaks ei hallata sektsioone, nii et kui lisate või redigeerite malli jaotist, ei lükatata muudatusi selle malli kasutavatele juhenditele või mallidele.
> 
> Kui lisate mallile uusi tegevusi, lükatakse uued tegevused selle malli põhjal juhenditele ja mallidele ning uued tegevused kuvatakse ülaosas.

## <a name="import-activities-from-another-template"></a>Tegevuste importimine muust mallist

Saate importida tegevusi ühest või mitmest mallist juhendisse või malli.

1. Valige juhend või mall, mida soovite redigeerida.

2. Valige vahekaart **Toimingud**.

3. Valige parempoolse jaotise vahekaart **Impordi**.

   [![Impordi tegevused](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Ülesannete eelvaate kuvamiseks brauseri uuel vahekaardil valige iga malli puhul nupp **Ava uuel vahekaardil.**

   [![Impordi tegevused](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. Lohistage ja kukutage soovitud mall juhendi mallil kohta, kus soovite tegevused kuvada. Jätkake juhendi või malli redigeerimist.

Imporditud tegevused sisaldavad **Lukustamise** nuppu, mis näitab, et neid tegevusi haldab teie imporditud mall. Kui teete imporditud mallile muudatusi, värskendatakse need tegevused malli, kuhu te need impordite. Kuid muudatusi ei lükata automaatselt mis tahes juhenditele, mis on loodud teie poolt imporditava malli põhjal.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Muude mallide või juhendite muutmine mallist

Kui redigeerite malli, mis sisaldab muudes mallides või juhendites kasutatavaid tegevusi, peate muudatustele vajutama, kui soovite, et need kuvataks muudes mallides või juhendites.

Kui te pole kindel, kas teie malli tegevusi kasutatakse muudes mallides või juhendites, valige vahekaardil **Kasutatav**, et vaadata, kus need tegevused ilmuvad.

   [![Vaadake juhendeid ja mallide tegevusi rakenduses](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Muudatustele vajutamine:

1. Salvestage muudatused, klõpsates nuppu **Salvesta**. Kui te seda ei tee, palutakse teil muudatused salvestada järgmises etapis.

2. Valige käsk **Lükake need muudatused sisse**.

   
## <a name="add-or-edit-an-introduction"></a>Sissejuhatuse lisamine või muutmine

1. Sisestage vahekaardil **Sissejuhatus** oma juhendi pealkiri ja avasõnum. Näidisteksti kasutamiseks valige **Kasuta seda teadet.**

    [![Sissejuhatuse vahekaart Onboardi mallis](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Kasutage vormingunuppe, et saata tekst välja nii, nagu vaja, või lisada pilte või linke.
3. Oma töö salvestamiseks valige **Salvesta**.

## <a name="add-or-edit-activities"></a>Tegevuste lisamine või redigeerimine

1. Vahekaardil **Tegevused** lohistage üksused paremalt redigeerimise alale.
2. Juhendite sektsioonideks korraldamiseks lohistage üksus **Uus sektsioon** redigeerimise alale ja sisestage jaotise nimi ja valikuline kirjeldus.

    ![[Uue jaotise lisamine sisseelamisjuhendisse või -mallile] (./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Uue töötaja tegevuste lõpuleviimisel tegevuste lisamiseks lohistage üksus **Uus tegevus** redigeerimise alale ja sisestage tegevuse nimi ja kirjeldus.

    ![[Uue tegevuse lisamine sisseelamisjuhendisse või -mallile](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. Lisage sisseelamisjuhendisse rikkalik sisu:

    - YouTube'i video lisamiseks lohistage **YouTube**'i üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus ning sisestage YouTube'i video URL.
    - Sway esitluse või infolehe lisamiseks lohistage **Sway** üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus ning sisestage Sway esitluse või infolehe varjatud URL.
    - PowerAppsi rakenduse lisamiseks lohistage **PowerAppsi** üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus ning valige kas PowerAppsi rakendus või sisestage PowerAppsi rakenduse ID.
    - Microsoft Streami video lisamiseks lohistage **Microsoft Stream**i üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus ning sisestage Microsoft Streami video URL.
    - Microsofti vormide vormi lisamiseks lohistage **Microsoft Forms** üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus, sisestage vormi Microsoft Forms URL ja määrake ekraani ala suurus.
    - Veebisisu sisaldava iframe'i lisamiseks lohistage **Veebisisu (iframe)** üksus redigeerimise alale, sisestage tegevuse nimi ja kirjeldus, sisestage veebisisu URL ja määrake ekraani ala suurus.

    ![[Rikkaliku sisu lisamine sisseelamisjuhendile või -mallile](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. Valikuline: määrake iga tegevuse paremal alal tegevus kindlale isikule või rollile, lisage tähtaeg ja kontaktisik ning määrake kategooria värv. Kui määrate tegevuse isikule või rollile, luuakse ülesanne igale üksikisikule. See ülesanne kuvatakse Onboardi menüüs **Ülesanded**.

    [![Tegevuse määramine sisseelamisjuhendis või -mallis](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. Oma töö salvestamiseks valige **Salvesta**.

Tegevuse või sektsiooni kustutamiseks valige tegevuse või sektsiooni ülemises parempoolses nurgas nupp **Kustuta** (prügikasti sümbol).

Tegevuste ja sektsioonide ümberkorraldamiseks lohistage need uude asukohta.

## <a name="add-or-edit-contacts"></a>Kontaktide lisamine või redigeerimine

Saate lisada kontaktisikuid, kes saavad aidata teie uuel töötajal algusest peale edu saavutada. Need kontaktid võivad olla värbajad, meeskonnakaaslased, sisseelamissõbrad, mentorid, administraatorid ja IT-toe töötajad.

1. Vahekaardil **Kontaktid** valige **Uus kontakt**.
2. Sisestage dialoogiboksi **Lisa meeskonnaliige** kontaktisiku nimi või meiliaadress, sisestage lühikirjeldus, mis selgitab, kuidas kontaktisik saab uut töötajat aidata ja seejärel valige **Lisa**. 

    ![[Kontaktide lisamine sisseelamisjuhendile või -mallile](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Teise võimalusena saate valida ühe või mitu kontakti jaotises **Soovitused**.

3. Oma töö salvestamiseks valige **Salvesta**.

Kontaktkirje kustutamiseks valige nupp **Kustuta** (prügikasti sümbol), mis on kontaktkirjest paremal.

Kontaktkirje redigeerimiseks valige nupp **Redigeeri** (pliiatsi sümbol), mis on kontaktkirjest paremal.

## <a name="add-or-edit-resources"></a>Ressursside lisamine või redigeerimine

Saate lisada kasulikke faile, kaarte ja linke sisseelamisjuhendis olevasse jaotisse **Ressursid**.

1. Vahekaardil **Ressursid** valige **Uus ressurss**.
2. Järgige üht neist sammudest.

    - Faili lisamiseks valige vahekaart **Fail** ja lohistage fail määratud alale. (Teise võimalusena klõpsake sellel alal suvalist kohta, et sirvida faili arvutis või valige **Sirvi OneDrive**.) Sisestage faili nimi ja seejärel valige **Lisa**.
    - Lingi lisamiseks valige vahekaart **Link**, sisestage lingile nimi ja aadress ning seejärel valige **Lisa**.
    - Kaardi lisamiseks valige vahekaart **Kaart**, sisestage kaardile nimi ja aadress ning seejärel valige **Lisa**. Onboard sisaldab teie määratud aadressi kaarti.

    ![[Ressursi lisamine sisseelamisjuhendisse või -mallile](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. Oma töö salvestamiseks valige **Salvesta**.

Ressursi kustutamiseks valige nupp **Kustuta** (prügikasti sümbol), mis on ressursikirjest paremal.

Ressursikirje redigeerimiseks valige nupp **Redigeeri** (pliiatsi sümbol), mis on ressursikirjest paremal.

## <a name="next-steps"></a>Järgmised etapid

- [Sisu jagamine teiste kaasautoritega](./onboard-share-template.md)
- [Vaadake tööülesannete ja töötajate töölevõtmise olekut](./onboard-view-status.md)
- [Looge Onboardis värbamismeeskonnad](./onboard-create-team.md)

### <a name="see-also"></a>Vt ka

- [Proovige või ostke Onboardi rakendus](https://dynamics.microsoft.com/talent/onboard/)
- [Mis on uut?](./whats-new.md)
- [Väljalaskemärkmed](https://docs.microsoft.com/business-applications-release-notes/index)
- [Toe hankimine](./talent-support.md)
