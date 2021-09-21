---
title: Hinnangute ja arvustuste haldus
description: Selles teemas selgitatakse, kuidas hallata rakenduse Microsoft Dynamics 365 Commerce saidiehitajas hinnanguid ja arvustusi.
author: gvrmohanreddy
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dce22b77862c41bc702f46735da8ce1100bb5e7d
ms.sourcegitcommit: 81bc42551e6c9af6ad38908afb606ee1f8d3c44b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473300"
---
# <a name="manage-ratings-and-reviews"></a>Hinnangute ja arvustuste haldus

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas hallata rakenduse Microsoft Dynamics 365 Commerce saidiehitajas hinnanguid ja arvustusi.

Dynamics 365 Commerce kasutab Microsoft Azure’i kognitiivset teenust, et automaatselt ebasündsaid sõnu redigeerides arvustuse teksti modereerida. Lisaks saavad moderaatorid kasutada rakenduse Dynamics 365 Commerce saidiehitajat järgmiste käsitsi tehtavate ülesannete tegemiseks.

- Arvustuste modereerimine neile vastates või need eemaldades.
- Kliendi arvustuste eemaldamine kliendi taotlusel.
- Kõikide toodete hinnangute ja arvustuste andmete hulgi importimine Microsoft Power BI malli, et analüüsida hinnangute ja arvustuste suundumusi.

## <a name="read-a-review"></a>Arvustuse lugemine 

Arvustuse lugemiseks rakenduse Commerce saidiehitajas toimige järgmiselt.

1. Avage **Avaleht \> Arvustused \> Modereerimine**.
1. Kasutage lehe üleval paremal otsinguvälja, et filtreerida kuvatavaid arvustusi toote ID, toote nime või arvustuse teksti alusel.

Täiendavad filtrid võimaldavad teil piirata arvustusi perioodi, hinnangu, kanali või mure oleku järgi (eemaldatud, vastatud või teatatud).

![Modereerimise avaleht.](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Arvustusele vastamine 

Mõnikord väljendavad toote ostnud kliendid rahulolu või rahulolematust või ei oska toodet kasutada. Moderaatorina saate sisestada arvustusele vastuse. See vastus kuvatakse saidil koos arvustusega. 

Arvustusele vastamiseks rakenduse Commerce saidiehitajas toimige järgmiselt.

1. Avage **Avaleht \> Arvustused \> Modereerimine**.
1. Otsige ja valige arvustus, mis vajab vastamist.
1. Parempoolsel atribuutide paanil valige suvand **Lisa vastus**.
1. Sisestage vastuse tekst ja nimi, mis tuleks vastajale näidata. Vastaja vaikenimi on **Moderaator.**
1. Kui olete lõpetanud, valige **Sisesta vastus**.

![Arvustusele vastamine.](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Arvustuse eemaldamine 

Vahel on moderaatoritel äriliselt põhjendatud kliendi arvustused eemaldada. 

Arvustuse eemaldamiseks rakenduse Commerce saidiehitajast toimige järgmiselt.

1. Avage **Avaleht \> Arvustused \> Modereerimine**.
1. Leidke ja valige arvustus, mis tuleb eemaldada.
1. Valige paremal atribuudipaanil eemaldamise põhjus väljal **Arvustuse eemaldamine** ja seejärel valige suvand **Eemalda**.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Kliendi arvustuste eemaldamine kliendi taotlusel 

Mõnikord soovivad kliendid oma hinnangud ja arvustuste andmed e-kaubanduse veebisaitidelt jäädavalt kustutada. Moderaator, kes saab kliendilt eemaldamise taotluse, saab kliendi andmed eemaldada, kasutades läbivaatuse kustutamise funktsiooni. Kliendiandmete otsimiseks ja kustutamiseks vajab moderaator meiliaadressi, mida klient sisselogimiseks ja arvustuste esitamiseks kasutas. 

Kliendiandmete leidmiseks ja kustutamiseks rakenduse Commerce saidiehitajas toimige järgmiselt.

1. Avage **Avaleht \> Arvustused \> Kustuta**.
1. Sisestage kasti **Kasutajate otsing meiliaadressi järgi** kliendi meiliaadress ja valige seejärel käsk **Otsi**.
1. Kui kliendil on mis tahes arvustuste tegevusi (nt esitatud arvustused, hääletused teiste klientide arvustuste kasulikkuse kohta või kommentaarid teiste klientide arvustuste kohta), kuvatakse tulemused. Iga üksuse jaoks on nupp **Kustuta**.
1. Valige iga üksuse jaoks, mis tuleb kustutada, käsk **Kustuta**. Kui teilt küsitakse kinnitust, valige **Jah**. 
    
![Kliendiandmete kustutamine.](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Andmete süsteemist täielikuks eemaldamiseks võib kuluda kuni seitse päeva. Moderaatorid peaksid kliente sellest viivitusest teavitama.
> - Kui kliendid on muutnud konto sätetes oma nime, võidakse otsingutulemustes kuvada mitu üksust. Sel juhul peab moderaator kliendiandmete täielikuks kustutamiseks valima iga üksuse jaoks käsu **Kustuta.** 

## <a name="download-ratings-and-reviews-data"></a>Hinnangute ja arvustuste andmete allalaadimine

Rakenduse Commerce saidiehitaja võimaldab moderaatoritel importida hinnangute ja arvustuste andmeid hulgi, et analüüsida nende suundumusi. Saadaval on Power BI mall, mis sisaldab põhilisi mõõdikuid. Moderaatorid saavad kasutada seda malli, et ühendada hulgi imporditud andmed ja kuvada armatuurlaud. Nad ei pea looma kohandatud armatuurlauda. Samuti saavad moderaatorid kohandada Power BI malli, et see vastaks nende konkreetsetele vajadustele. 

Arvustuste ja hinnangute andmete allalaadimiseks rakenduse Commerce saidiehitajas toimige järgmiselt.

1. Avage **Avaleht \> Arvustused \> Aruandlus**.
1. Valige suvand **Arvustuse andmete allalaadimine**, et laadida hinnangute ja kommentaaride andmed hulgi alla komaeraldusega väärtuste (CSV) vormingus.

## <a name="view-ratings-and-reviews-trends"></a>Hinnangute ja arvustuste suundumuste vaatamine

Moderaatorid saavad laadida alla Power BI malli, et nad saaksid vaadata armatuurlaual suundumusi.

Arvustuste ja hinnangute suundumuste vaatamiseks rakenduse Commerce saidiehitajas toimige järgmiselt.

1. Avage **Avaleht \> Arvustused \> Aruandlus**.
1. Malli allalaadimiseks valige suvand **PowerBI mall**.

    ![Laadige alla Power BI mall.](media/rnr-moderation-reports.png) 

1. Avage allalaaditud mall Power BI rakendust kasutades. Sulgege ilmuv dialoogiaken **Juurdepääs veebisisule** ja seejärel sulgege kuvatav tõrketeade „Värskenda”.
1. Avage suvand **Avaleht**, valige **Päringute redigeerimine** ja valige seejärel **Andmeallika sätted**.
1. Valige dialoogiaknas **Andmeallika sätted** suvand **Muuda allikat**.
1. Sisestage väljale **URL** eelmises protseduuris allalaaditud arvustuste andmete tee (nt **c:\\arvustused\\ArvustusteAndmed.CSV**).

    ![URL-i väli komaeraldusega väärtuste dialoogiaknas.](media/rnr-powerbi-datasource-settings.png) 

1. Valige **OK** ja seejärel valige käsk **Rakenda muutused**. Andmeallikale muudatuste rakendamiseks kulub üks kuni kaks minutit.
1. Hinnangute ja arvustuste suundumuste vaatamiseks valige suvand **Suundumuste leht**.

    ![Hinnangute ja arvustuste suundumused.](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)

[Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
