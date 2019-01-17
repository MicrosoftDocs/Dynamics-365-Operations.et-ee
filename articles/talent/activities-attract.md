---
title: Protsesside tegevused
description: "Selles teemas kirjeldatakse eri tüüpi tegevusi, mida saab kasutada värbamisprotsessis."
author: 
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: 4f59193991420fd9ec05a83049e569058bf81932
ms.contentlocale: et-ee
ms.lasthandoff: 12/07/2018

---

# <a name="activities-in-the-hiring-processes"></a>Värbamisprotsesside tegevused

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract võimaldab värbamisprotsessile lisada tegevusi. Tegevusi saab lisada protsessimallile või neid saab lisada otse tööle värbamise protsessile. Pärast töö määratlemist valitakse protsessimall ja mallis sisalduvad tegevused rakendatakse tööle. Kui mall on valimata, kasutatakse vaikemalli. Värbamisprotsessi saab töö juures muuta ka pärast malli rakendamist.

> [!NOTE] 
> Protsessimallid on saadaval tervikliku värbamise lisandmooduli korral.

## <a name="prospect-activity"></a>Tegevus Potentsiaalselt sobiv kandidaat

Tegevus Potentsiaalselt sobiv kandidaat võimaldab tööle lisada potentsiaalselt sobivaid kandidaate. Vaikimisi saab tööle lisada potentsiaalselt sobivaid kandidaate. Tegevuse Potentsiaalselt sobiv kandidaat väljalülitamiseks määrake suvandi **Luba potentsiaalselt sobivad kandidaadid** olekuks **Väljas**. Kui tegevus Potentsiaalselt sobiv kandidaat on sisse lülitatud, saavad personalijuhid potentsiaalselt sobivaid kandidaate lisada ja vaadata ning töö juures kuvatakse vahekaart **Potentsiaalselt sobiv kandidaat**.

## <a name="application-activity"></a>Tegevus Avaldus

Tegevus Avaldus on värbamisprotsessi mallis kohustuslik. Meilisõnumi saatmiseks kandidaatidele, kui nad on esitanud avalduse või lisatud etappi Avaldus, määrake suvandi **Saada kandidaadile meilisõnum** olekuks **Sees**.

## <a name="scheduler-activity"></a>Tegevus Plaanur

Tegevus Plaanur ei ole kohustuslik. Sellel tegevusel on kaks komponenti: Kandidaadi kättesaadavus ja Graafik. Kandidaadi kättesaadavuse komponent võimaldab kasutada kandidaadi kättesaadavuse küsimiseks meili. Graafiku komponent võimaldab planeerida töövestlusi kandidaadi ja värbamistöörühma vahel. Konfigureerida saab tegevuse Plaanur järgmisi suvandeid: **Küsi kandidaadi kättesaadavust**, **Võrgukoosolek** ja **Saada kandidaadile meilisõnum**.

- Kandidaatidele nende kättesaadavuse kohta küsimiseks meilisõnumi saatmiseks määrake suvandi **Küsi kandidaadi kättesaadavust** olekuks **Sees**. Kui määrate selle suvandi olekuks **Väljas**, seda etappi tööle värbamise protsessis ei kuvata.
- Videoülekande või konverentskõne tegemiseks rakendusega Skype for Business määrake välja **Võrgukoosolek** olekuks **Skype for Business**. Õige link **Liitu Skype’i koosolekuga** lisatakse seejärel intervjueerijatele saadetavale vestluskutsele.
- Kandidaatidele graafiku lõplikuks kinnitamiseks meilisõnumi saatmiseks määrake suvandi **Saada kandidaadile meilisõnum** olekuks **Sees**. Kui määrate selle suvandi olekuks **Väljas**, saavad kandidaadid töövestluste graafiku ainult siis, kui logivad sisse kandidaadi portaali.

## <a name="feedback-activity"></a>Tegevus Tagasiside

Tegevus Tagasiside ei ole kohustuslik. See tegevus võimaldab töövestluse osalejatel sisestada kandidaadile soovitusi. Samuti saavad nad sisestada oma tagasisidekommentaarid. Kui lülitate sisse suvandi **Tuleta tagasisides osalejad värbamistöörühmast**, sisestatakse värbaja, personalijuht ja intervjueerijad automaatselt tegevusse Tagasiside. Organisatsioonid võivad lubada intervjueerijatel enne tagasiside andmist vaadata teiste inimeste tagasisidet. Organisatsioonid võivad ka lubada pärast tagasiside andmist intervjueerijatel seda muuta.

## <a name="interview-activity"></a>Tegevus Töövestlus

Tegevus Töövestlus ei ole kohustuslik. Sellel tegevusel on kolm komponenti: Kandidaadi kättesaadavus, Graafik ja Tagasiside. Kandidaadi kättesaadavuse komponent võimaldab kasutada kandidaadi kättesaadavuse küsimiseks meili. Graafiku komponent võimaldab planeerida töövestlusi kandidaadi ja värbamistöörühma vahel. Konfigureerida saab tegevuse Plaanur järgmisi suvandeid: **Küsi kandidaadi kättesaadavust**, **Võrgukoosolek** ja **Saada kandidaadile meilisõnum**.

- Kandidaatidele nende kättesaadavuse kohta küsimiseks meilisõnumi saatmiseks määrake suvandi **Küsi kandidaadi kättesaadavust** olekuks **Sees**. Kui määrate selle suvandi olekuks **Väljas**, seda etappi tööle värbamise protsessis ei kuvata.
- Videoülekande või konverentskõne tegemiseks rakendusega Skype for Business määrake välja **Võrgukoosolek** olekuks **Skype for Business**. Õige link **Liitu Skype’i koosolekuga** lisatakse seejärel saadetavale vestluskutsele.
- Kandidaatidele graafiku lõplikuks kinnitamiseks meilisõnumi saatmiseks määrake suvandi **Saada kandidaadile meilisõnum** olekuks **Sees**. Kui määrate selle suvandi olekuks **Väljas**, saavad kandidaadid töövestluste graafiku ainult siis, kui logivad sisse kandidaadi portaali.

>[!NOTE]
> - Kõik üks-ühele intervjuude meeldetuletused saadetakse küsitlejatele iga 24 tunni tagant, kui intervjueerija ei vastanud (nõustunud või keeldunud) vestluse taotlusele.
> - Kõikide paneeli intervjuude jaoks pole intervjuu taotluse automatiseeritud meeldetuletusi. Meeldetuletuse käivitamiseks käsitsi redigeerige intervjuu ja kasutage **värskendada ja saata** valikut, et saata taotlus tagasi küsitlejatele.

Tagasiside komponent võimaldab inimestel sisestada kandidaadile soovitusi. Samuti saavad nad sisestada oma tagasisidekommentaarid. Kui lülitate sisse suvandi **Tuleta tagasisides osalejad värbamistöörühmast**, sisestatakse värbaja, personalijuht ja intervjueerijad automaatselt komponenti Tagasiside. Organisatsioonid võivad lubada intervjueerijatel enne tagasiside andmist vaadata teiste inimeste tagasisidet. Organisatsioonid võivad ka lubada pärast tagasiside andmist intervjueerijatel seda muuta.

## <a name="powerapps-activity"></a>Tegevus PowerApps

Tegevus PowerApps võimaldab värbamisprotsessi manustada rakenduse Microsoft PowerApps. Rakendus võib olla kohustuslik kõigile kandidaatidele, ainult ettevõttesisestele kandidaatidele, ainult ettevõttevälistele kandidaatidele või mitte ühelegi kandidaadile. Kui see rakendus märgitakse kohustuslikuks, peab enne etapi alustamist selle lõpule viima. Kui see rakendus ei ole kohustuslikuks märgitud, pole see tegevus kohustuslik, ja etappi saab alustada isegi siis, kui rakendus on lõpule viimata.

Värbamisprotsessi jaoks tegevuse PowerApps salvestamiseks peate sisestama PowerAppsi ID. PowerAppsi ID leidmiseks valige [PowerApps](https://web.powerapps.com), **Rakendused** ja seejärel **Üksikasjad**.

Kui valite suvandi **Luba osalejate lisamine sellele tegevusele**, saab rakendusele, mis kasutab tegevust PowerApps, lisada kaasautoreid. Näiteks organisatsioon on loonud PowerAppsi rakenduse, mis on tehniliste rollide jaoks peetavate töövestluste küsimuste teek. See organisatsioon otsib parasjagu uut tarkvaraarendajat ja on lisanud tegevuse PowerApps tarkvaraarendaja rolli värbamisprotsessile. Kui valitud on suvand **Luba osalejate lisamine sellele tegevusele**, saab värbaja või personalijuht, kes vaatab tarkvaraarendaja rolli jaoks olevat kandidaati, tegevusse PowerApps inimesi lisada. Need inimesed saavad siis vaadata töövestluse küsimustega rakendust.

> [!NOTE]
> Tegevus PowerApps on saadaval ainult tervikliku värbamise lisandmooduli korral.

## <a name="youtube-activity"></a>Tegevus YouTube

Tegevus YouTube võimaldab värbamisprotsessi osana jagada YouTube’i videot. Värbamisprotsessi jaoks tegevuse YouTube salvestamiseks on vajalik YouTube’i video URL. Nii nagu tegevuse PowerApps korral, saate lubada ka sellele tegevusele osalejate lisamist. Kui valite suvandi **Näita ainult kandidaadile**, näidatakse videot ainult kandidaatidele. Seda ei näidata Attractis olevas värbamisprotsessis.

> [!NOTE]
> Tegevus YouTube on saadaval ainult tervikliku värbamise lisandmooduli korral.

## <a name="web-content-activity"></a>Tegevus Veebisisu

Tegevus Veebisisu võimaldab teil värbamisprotsessi manustada veebisisu. Värbamisprotsessi jaoks tegevuse Veebisisu salvestamiseks on vajalik sisu URL. Nii nagu tegevuste PowerApps ja YouTube korral, saate lubada ka sellele tegevusele osalejate lisamist. Kui valite suvandi **Näita ainult kandidaadile**, näidatakse sisu ainult kandidaatidele. Seda ei näidata Attractis olevas värbamisprotsessis. Te saate valida kuvatava sisu suuruse.

> [!NOTE]
> Tegevus Veebisisu on saadaval ainult tervikliku värbamise lisandmooduli korral.

## <a name="microsoft-forms-activity"></a>Tegevus Microsoft Forms

Tegevus Microsoft Forms võimaldab värbamisprotsessi manustada Microsoft Formsi vormi. Microsoft Forms võimaldab teil luua viktoriine, uuringuid ja küsitlusi. Värbamisprotsessi jaoks tegevuse Microsoft Forms salvestamiseks on vajalik vormi URL. Nii nagu tegevuste PowerApps, YouTube ja Veebisisu korral, saate lubada ka sellele tegevusele osalejate lisamist. Kui valite suvandi **Näita ainult kandidaadile**, näidatakse vormi ainult kandidaatidele. Seda ei näidata Attractis olevas värbamisprotsessis.

Rakendusega Microsoft Forms saavad autorid muuta oma sätteid, et organisatsioonivälised kasutajad saaksid nende küsitlustele või viktoriinile vastata. Sel juhul on kasutajate vastused anonüümsed. Kui soovite näha, kes on teie küsitlusele või viktoriinile vastanud, saate küsitluse või viktoriini osana paluda vastajatel sisestada oma nimi.

> [!NOTE]
> Tegevus Microsoft Forms on saadaval ainult tervikliku värbamise lisandmooduli korral.

