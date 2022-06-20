---
title: Lehe URL-i loomine
description: See artikkel hõlmab saidi lehe URL-i loomise põhimõisteid ja protseduure.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1798c4812b535ef007cbd5ff310b534e64a2f11e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892300"
---
# <a name="create-a-page-url"></a>Lehe URL-i loomine

[!include [banner](includes/banner.md)]

See artikkel hõlmab saidi lehe URL-i loomise põhimõisteid ja protseduure.

Teie saidi lehele viitav täielik või absoluutne URL koosneb eraldi osadest. Näiteks on URL-il `https://www.contoso.com/en-us/contactus` järgmised osad:

- `https://www.contoso.com` – HTTP-protokoll ja saidi domeen.
- `/en-us` – saidi keele tee.
- `/contactus` – suhteline URL lehe **Võtke meiega ühendust** jaoks. Suhteline URL on tuntud ka kui URL-i *komponent*.

Oma saidi domeeni ja valikulise keele tee loote saidi seadistamisel. Saate lisada saidile rohkem domeene ja keelte teesid läbi saidi sätete veebipoodide lehe.

Lehe URL-i komponent on olemas eraldiseisva üksusena saidi autorluse keskkonnas. Lehe URL koosneb kahest osast: URL-i komponendi esindav nimi ja teie saidil või välisel saidil olevale lehele osutaja. Lehe URL-i saab konfigureerida ka käituma teie saidil või välisel saidil olevale teisele lehele suunajana.

## <a name="create-a-page-url"></a>Lehe URL-i loomine

Lehe URL-ide loomiseks on kaks võimalust.

- Automaatselt lehe loomisel
- Käsitsi **URL-ide** lehelt

### <a name="create-a-page-url-when-you-create-a-page"></a>Lehe loomisel lehe URL-i loomine

Kui sisestate uue lehe loomisel väljale **URL** nime, luuakse **URL-ide** lehel automaatselt lehe URL, mis sellele lehele suunab. Pärast URL-i ja lehe, millele see suunab, avaldamist, pääsevad saidi kasutajad (teie kliendid) URL-iga seostatud lehele ligi.

> [!NOTE]
> Kui avaldate URL-i ilma, et avaldaksite lehe, millele see osutab, saavad saidi kasutaja lehe avamise proovimisel tõrke 404. Kui avaldate lehe ilma, et avaldaksite URL-i, mis sellele osutab, ei ole lehele võimalik URL-i kasutades ligi pääseda.

### <a name="manually-create-a-page-url"></a>Lehe URL-i käsitsi loomine

Uute lehtede loomisel ei ole lehe URL-i määramine nõutud. Kui jätate URL-i välja tühjaks, luuakse leht seostamata olekus. Sel juhul ei pääse kliendid lehele ligi, isegi kui see on avaldatud. Lehe kättesaadavaks tegemiseks peate käsitsi looma URL-i ja linkima selle lehega.

Lehe jaoks käsitsi lehe URL-i loomiseks tehke järgmist.

1. Valige lehel **URL-id** suvand **Uus**.
1. Valige saidi leht,mille URL-iga seostada.
1. Sisestage URL-i komponent ja valige seejärel **OK**.

Sel hetkel on URL mustandi olekus. See tuleb avaldada, enne kui saidi kasutajad pääsevad seotud lehele ligi.

## <a name="update-a-page-url"></a>Lehe URL-i värskendamine

Lehe URL-i sihtlehe värskendamiseks järgige järgmisi samme.

1. Valige lehel **URL-id** värskendamiseks URL.
1. Valige parempoolsel atribuudipaanil sihtlehe välja kõrval kolmikpunkti nupp (**...**).
1. Valige dialoogiaknas erinev leht ja valige seejärel nupp **OK**.
1. Salvestage ja avaldage URL.

## <a name="redirect-a-page-url"></a>Lehe URL-i ümbersuunamine

Mõnikord võite soovida, et kliendid näeksid konkreetse URL-i taotlemisel erinevat lehte. Sellisel juhul on sageli parim ja lihtsaim lahendus muuta lehte, kuhu lehe URL osutab. Samas võivad teil olla legaalsed põhjused HTTP 301 või 3023 ümbersuunamiste kasutamiseks, et suunata URLi taotlused erinevale URL-ile.

URL-i erinevale URL-i ümbersuunamiseks toimige järgmiselt.

1. Valige lehel **URL-id** värskendamiseks URL.
1. Valige paremalt atribuutide paanilt suvand **Ümbersuunamine**.
1. Valige ümbersuunamise sihtkoht.

    - Saidi teisele leheküljele osutamiseks valige suvand **Sisemine URL**, valige kolmikpunkti nupp (**...**) ja seejärel valige URL, millele ümber suunata.
    - Välisel saidil olevale lehele osutamiseks valige suvand **Väline URL** ja sisestage seejärel tolle lehekülje täielik URL. Kaasake kindlasti protokoll. Sisestage näiteks `https://domain.com/new/page`. Kui URL juba suunab ümber sisemisele URL-ile, peate enne välise URL-i sisestamist valima suvandi **Tühjenda valik**.

1. Valige ümbersuunamise tüüp.

    - **Püsiv ümbersuunamine (301)** – valige see suvand, kui teate, et teie sisu teisaldatakse jäädavalt ja seda ei saa selle eelmisele URL-ile taastada. Otsimootorid määravad ümbersuunava URL-i otsimootori optimeerimise (SEO) väärtuseks URL-i väärtuse, mis on ümber suunatud ja värskendavad oma kirjet, et uut URL-i näidata. 
    - **Ajutine ümbersuunamine (302)** – valige see suvand liikluse ümbersuunamiseks otsingumootorit uuendamata. Seda lähenemist kasutatakse tavaliselt siis, kui sisu naaseb peagi eelmisele URL-ile.

1. Kui olete ümbersuunamise juurutamiseks valmis, salvestage ja avaldage URL.

## <a name="additional-resources"></a>Lisaressursid

[Saidil navigeerimise kohandamine](customize-site-navigation.md)

[Uue saidilehe lisamine](add-new-page.md)

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Saidile keelte lisamine](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
