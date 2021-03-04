---
title: Lisa värbamisprotsessi tegevusi
description: Selles teemas kirjeldatakse mitmesuguseid tegevuste tüüpe, mida saate värbamisprotsessi lisada rakenduses Microsoft Dynamics 365 Talent – Attract.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
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
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460955"
---
# <a name="add-activities-to-a-hiring-process"></a>Lisa värbamisprotsessi tegevusi

[!include [banner](includes/banner.md)]

Rakenduses Microsoft Dynamics 365 Talent: Attract saab värbamisprotsessile lisada tegevusi. Tegevusi saab lisada protsessimallile või neid saab lisada otse tööle värbamise protsessile. Pärast töö määratlemist valitakse protsessimall ja mallis sisalduvad tegevused rakendatakse tööle. Kui mall on valimata, kasutatakse vaikemalli. Värbamisprotsessi saab töö juures muuta ka pärast malli rakendamist.

> [!NOTE] 
> Protsessimallid on saadaval tervikliku värbamise lisandmooduli korral. Lisateabe saamiseks vaadake jaotist [Milline rakenduse Microsoft Dynamics 365 Talent – Attract versioon?](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Tegevus Potentsiaalselt sobiv kandidaat

Tegevus Potentsiaalselt sobiv kandidaat võimaldab tööle lisada potentsiaalselt sobivaid kandidaate. Vaikimisi saab tööle lisada potentsiaalselt sobivaid kandidaate. Tegevuse Potentsiaalselt sobiv kandidaat väljalülitamiseks määrake suvandi **Luba potentsiaalselt sobivad kandidaadid** olekuks **Väljas**. Kui tegevus Potentsiaalselt sobiv kandidaat on sisse lülitatud, saavad personalijuhid potentsiaalselt sobivaid kandidaate lisada ja vaadata ning töö juures kuvatakse vahekaart **Potentsiaalselt sobiv kandidaat**.

> [!NOTE]
> Et lubada kandidaatide lisamist tööle LinkedInist, peate seadistama suvandi **luba väljavaated** väärtuseks **sees**.

## <a name="application-activity"></a>Tegevus Avaldus

Tegevus Avaldus on värbamisprotsessi mallis kohustuslik. Meilisõnumi saatmiseks kandidaatidele, kui nad on esitanud avalduse või lisatud etappi Avaldus, määrake suvandi **Saada kandidaadile meilisõnum** olekuks **Sees**.

## <a name="interview-schedule-and-feedback-activity"></a>Vestluse plaanimise ja tagasiside tegevus

Sellel tegevusel on kolm komponenti: Kandidaadi saadavuspäring, Graafik ja Tagasiside. Kasutage vestluse tegevust töömallis, kui soovite kaasata kandidaadi saadavuspäringu, graafiku ja tagasiside protsessi osana, mitte kasutada neid värbamisprotsessis eraldi tegevustena. Lisateavet vt teemast [Vestluse plaanimine ja tagasiside](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Power Apps’i tegevus

Power Appsi tegevus võimaldab värbamisprotsessi manustada rakenduse Microsoft Power Apps. Rakendus võib olla kohustuslik kõigile kandidaatidele, ainult ettevõttesisestele kandidaatidele, ainult ettevõttevälistele kandidaatidele või mitte ühelegi kandidaadile. Kui see rakendus märgitakse kohustuslikuks, peab enne etapi alustamist selle lõpule viima. Lõpetatuks lugemiseks peab välja **JobApplicationStatus** olekuks olema määratud **Lõpetatud**. See väli asub üksuses JobApplicationActivity, seega peab Power Appsi rakendus enne etapi alustamist seda välja värskendama. Kui see rakendus ei ole kohustuslikuks märgitud, pole see tegevus kohustuslik, ja etappi saab alustada isegi siis, kui rakendus on lõpule viimata.

Värbamisprotsessi jaoks Power Appsi tegevuse salvestamiseks peate sisestama Power Appsi ID. Power Appsi ID leidmiseks valige [Power Apps](https://web.powerapps.com), **Rakendused** ja seejärel **Üksikasjad**.

Vaikimisi on Power Appsi tegevus saadaval värbamisjuhile, värbajale ja nende delegaatidele. Kui valite suvandi **Luba osalejate lisamine sellele tegevusele**, saab Power Appsi tegevust kasutavale rakendusele lisada värbamistöörühmast osalejaid. Näiteksorganisatsioon on loonud Power Appsi rakenduse, mis on tehniliste rollide jaoks peetavate töövestluste küsimuste teek. See organisatsioon otsib parasjagu uut tarkvaraarendajat ja on lisanud Power Appsi tegevuse tarkvaraarendaja rolli värbamisprotsessile. Kui valitud on suvand **Luba osalejate lisamine sellele tegevusele**, saab tarkvaraarendaja rolli jaoks olevat kandidaati vaatav värbaja või värbamisjuht lisada Power Appsi tegevusele intervjueerijaid. Need inimesed saavad siis vaadata töövestluse küsimustega rakendust.

> [!NOTE]
> Power Apps’i tegevus on saadaval ainult mitmekülgse värbamise lisandmooduli korral. Lisateabe saamiseks vaadake jaotist [Milline rakenduse Microsoft Dynamics 365 Talent – Attract versioon?](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>YouTube’i tegevus

YouTube’i tegevus võimaldab värbamisprotsessi osana jagada YouTube’i videot. Värbamisprotsessi jaoks YouTube’i tegevuse salvestamiseks on vajalik YouTube’i video URL. Sisu nägijaid on võimalik valida suvanditega **Värbamistöörühm**, **Ainult sisekandidaadid**, **Ainult väliskandidaadid** või **Kõik kandidaadid**. Nii nagu Power Appsi tegevuse korral, saate lubada ka sellele tegevusele värbamistöörühma osalejate lisamist. Kui otsustate lasta kandidaatidel näha sisu, näidatakse videot ainult kandidaatidele, mitte värbamisprotsessis.

> [!NOTE]
> YouTube’i tegevus on saadaval ainult mitmekülgse värbamise lisandmooduli korral. Lisateabe saamiseks vaadake jaotist [Milline rakenduse Microsoft Dynamics 365 Talent – Attract versioon?](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Tegevus Veebisisu

Tegevus Veebisisu võimaldab teil värbamisprotsessi manustada veebisisu. Värbamisprotsessi jaoks tegevuse Veebisisu salvestamiseks on vajalik sisu URL. Sisu nägijaid on võimalik valida suvanditega **Värbamistöörühm**, **Ainult sisekandidaadid**, **Ainult väliskandidaadid** või **Kõik kandidaadid**. Nii nagu Power Appsi ja YouTube'i tegevuste korral, saate lubada ka sellele tegevusele värbamistöörühma osalejate lisamist. Kui otsustate lasta kandidaatidel näha sisu, näidatakse veebisisu ainult kandidaatidele, mitte värbamisprotsessis. Te saate valida kuvatava sisu suuruse.

> [!NOTE]
> Tegevus Veebisisu on saadaval ainult tervikliku värbamise lisandmooduli korral. Lisateabe saamiseks vaadake jaotist [Milline rakenduse Microsoft Dynamics 365 Talent – Attract versioon?](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Tegevus Microsoft Forms

Microsoft Formsi tegevus võimaldab värbamisprotsessi manustada Microsoft Formsi tegevuse. Microsoft Forms võimaldab teil luua viktoriine, uuringuid ja küsitlusi. Värbamisprotsessi jaoks Microsoft Formsi tegevuse salvestamiseks on vajalik vormi URL. Sisu nägijaid on võimalik valida suvanditega **Värbamistöörühm**, **Ainult sisekandidaadid**, **Ainult väliskandidaadid** või **Kõik kandidaadid**. Nii nagu Power Appsi, YouTube'i ja veebisisu tegevuste korral, saate lubada ka sellele tegevusele värbamistöörühma osalejate lisamist. Kui otsustate lasta kandidaatidel näha sisu, näidatakse vormi ainult kandidaatidele, mitte värbamisprotsessis.

Rakendusega Microsoft Forms saavad autorid muuta oma sätteid, et organisatsioonivälised kasutajad saaksid nende küsitlustele või viktoriinile vastata. Sel juhul on kasutajate vastused anonüümsed. Kui soovite näha, kes on teie küsitlusele või viktoriinile vastanud, saate küsitluse või viktoriini osana paluda vastajatel sisestada oma nimi.

> [!NOTE]
> Tegevus Microsoft Forms on saadaval ainult tervikliku värbamise lisandmooduli korral. Lisateabe saamiseks vaadake jaotist [Milline rakenduse Microsoft Dynamics 365 Talent – Attract versioon?](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Pakkumise tegevus

Värbamisprotsessi mall nõuab pakkumise tegevust. Integreeritud pakkumiste haldamise rakenduse kasutamiseks määrake sätte **Käivita pakkumiste haldamise rakendus pakkumise koostamisel** olekuks **Sees**. Kui see säte on välja lülitatud, ei kuvata kandidaati pakkumise rakenduses, mistõttu peate kandidaadi pakkumise tegevuse värskendusi jälgima käsitsi. Selleks, et värbamisjuhid saaksid kandidaadi jaoks pakkumise koostada pakkumise rakenduses, määrake sätte **Personalijuhid saavad pakkumise ette valmistada** olekuks **Sees**. Kui tööga on seotud mitu ametikohta, saate otsustada, kas soovite sama ametikoha numbriga seoses ette valmistada mitu pakkumist. Kui soovite lubada ainult ühe pakkumise ühe ametikoha kohta ühe töö kohta, määrake sätte **Luba töös positsioone uuesti kasutada** olekuks **Väljas**.

> [!NOTE]
> Integreeritud pakkumiste haldamise rakendus on saadaval ainult tervikliku värbamise lisandmooduli korral. Lisateabe saamiseks vaadake jaotist [Milline rakenduse Microsoft Dynamics 365 Talent – Attract versioon?](./attract-comprehensive-hiring.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]