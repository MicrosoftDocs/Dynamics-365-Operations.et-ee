---
title: Protsesside tegevused
description: Selles teemas kirjeldatakse eri tüüpi tegevusi, mida saab kasutada värbamisprotsessis.
author: ''
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c32db1f563466f05b9fef1a03578392888c0b7e6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2019
ms.locfileid: "374753"
---
# <a name="activities-in-the-hiring-processes"></a>Värbamisprotsesside tegevused

[!include[banner](../includes/banner.md)]

Rakenduses Microsoft Dynamics 365 for Talent: Attract saab värbamisprotsessile lisada tegevusi. Tegevusi saab lisada protsessimallile või neid saab lisada otse tööle värbamise protsessile. Pärast töö määratlemist valitakse protsessimall ja mallis sisalduvad tegevused rakendatakse tööle. Kui mall on valimata, kasutatakse vaikemalli. Värbamisprotsessi saab töö juures muuta ka pärast malli rakendamist.

> [!NOTE] 
> Protsessimallid on saadaval tervikliku värbamise lisandmooduli korral.

## <a name="prospect-activity"></a>Tegevus Potentsiaalselt sobiv kandidaat

Tegevus Potentsiaalselt sobiv kandidaat võimaldab tööle lisada potentsiaalselt sobivaid kandidaate. Vaikimisi saab tööle lisada potentsiaalselt sobivaid kandidaate. Tegevuse Potentsiaalselt sobiv kandidaat väljalülitamiseks määrake suvandi **Luba potentsiaalselt sobivad kandidaadid** olekuks **Väljas**. Kui tegevus Potentsiaalselt sobiv kandidaat on sisse lülitatud, saavad personalijuhid potentsiaalselt sobivaid kandidaate lisada ja vaadata ning töö juures kuvatakse vahekaart **Potentsiaalselt sobiv kandidaat**.

## <a name="application-activity"></a>Tegevus Avaldus

Tegevus Avaldus on värbamisprotsessi mallis kohustuslik. Meilisõnumi saatmiseks kandidaatidele, kui nad on esitanud avalduse või lisatud etappi Avaldus, määrake suvandi **Saada kandidaadile meilisõnum** olekuks **Sees**.

## <a name="interview-schedule-and-feedback-activity"></a>Vestluse plaanimise ja tagasiside tegevus

Sellel tegevusel on kolm komponenti: Kandidaadi saadavuspäring, Graafik ja Tagasiside. Kasutage vestluse tegevust töömallis, kui soovite kaasata kandidaadi saadavuspäringu, graafiku ja tagasiside protsessi osana, mitte kasutada neid värbamisprotsessis eraldi tegevustena. Lisateavet vt teemast [Vestluse plaanimine ja tagasiside](interview-scheduling-feedback.md).

## <a name="powerapps-activity"></a>PowerAppsi tegevus

PowerAppsi tegevus võimaldab värbamisprotsessi manustada rakenduse Microsoft PowerApps. Rakendus võib olla kohustuslik kõigile kandidaatidele, ainult ettevõttesisestele kandidaatidele, ainult ettevõttevälistele kandidaatidele või mitte ühelegi kandidaadile. Kui see rakendus märgitakse kohustuslikuks, peab enne etapi alustamist selle lõpule viima. Kui see rakendus ei ole kohustuslikuks märgitud, pole see tegevus kohustuslik, ja etappi saab alustada isegi siis, kui rakendus on lõpule viimata.

Värbamisprotsessi jaoks tegevuse PowerApps salvestamiseks peate sisestama PowerAppsi ID. PowerAppsi ID leidmiseks valige [PowerApps](https://web.powerapps.com), **Rakendused** ja seejärel **Üksikasjad**.

Kui valite suvandi **Luba osalejate lisamine sellele tegevusele**, saab rakendusele, mis kasutab tegevust PowerApps, lisada kaasautoreid. Näiteks organisatsioon on loonud PowerAppsi rakenduse, mis on tehniliste rollide jaoks peetavate töövestluste küsimuste teek. See organisatsioon otsib parasjagu uut tarkvaraarendajat ja on lisanud tegevuse PowerApps tarkvaraarendaja rolli värbamisprotsessile. Kui valitud on suvand **Luba osalejate lisamine sellele tegevusele**, saab värbaja või personalijuht, kes vaatab tarkvaraarendaja rolli jaoks olevat kandidaati, tegevusse PowerApps inimesi lisada. Need inimesed saavad siis vaadata töövestluse küsimustega rakendust.

> [!NOTE]
> Tegevus PowerApps on saadaval ainult tervikliku värbamise lisandmooduli korral.

## <a name="youtube-activity"></a>YouTube’i tegevus

YouTube’i tegevus võimaldab värbamisprotsessi osana jagada YouTube’i videot. Värbamisprotsessi jaoks YouTube’i tegevuse salvestamiseks on vajalik YouTube’i video URL. Nii nagu tegevuse PowerApps korral, saate lubada ka sellele tegevusele osalejate lisamist. Kui valite suvandi **Näita ainult kandidaadile**, näidatakse videot ainult kandidaatidele. Seda ei näidata Attractis olevas värbamisprotsessis.

> [!NOTE]
> YouTube’i tegevus on saadaval ainult mitmekülgse värbamise lisandmooduli korral.

## <a name="web-content-activity"></a>Tegevus Veebisisu

Tegevus Veebisisu võimaldab teil värbamisprotsessi manustada veebisisu. Värbamisprotsessi jaoks tegevuse Veebisisu salvestamiseks on vajalik sisu URL. Nii nagu PowerAppsi ja YouTube’i tegevuste puhul, saate lubada ka sellele tegevusele osalejate lisamist. Kui valite suvandi **Näita ainult kandidaadile**, näidatakse sisu ainult kandidaatidele. Seda ei näidata Attractis olevas värbamisprotsessis. Te saate valida kuvatava sisu suuruse.

> [!NOTE]
> Tegevus Veebisisu on saadaval ainult tervikliku värbamise lisandmooduli korral.

## <a name="microsoft-forms-activity"></a>Tegevus Microsoft Forms

Tegevus Microsoft Forms võimaldab värbamisprotsessi manustada Microsoft Formsi vormi. Microsoft Forms võimaldab teil luua viktoriine, uuringuid ja küsitlusi. Värbamisprotsessi jaoks tegevuse Microsoft Forms salvestamiseks on vajalik vormi URL. Nii nagu PowerAppsi, YouTube’i ja veebisisu tegevuste puhul, saate lubada ka sellele tegevusele osalejate lisamist. Kui valite suvandi **Näita ainult kandidaadile**, näidatakse vormi ainult kandidaatidele. Seda ei näidata Attractis olevas värbamisprotsessis.

Rakendusega Microsoft Forms saavad autorid muuta oma sätteid, et organisatsioonivälised kasutajad saaksid nende küsitlustele või viktoriinile vastata. Sel juhul on kasutajate vastused anonüümsed. Kui soovite näha, kes on teie küsitlusele või viktoriinile vastanud, saate küsitluse või viktoriini osana paluda vastajatel sisestada oma nimi.

> [!NOTE]
> Tegevus Microsoft Forms on saadaval ainult tervikliku värbamise lisandmooduli korral.
