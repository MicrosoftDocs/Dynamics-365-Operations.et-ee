---
title: Robots.txt-failide haldamine
description: See teema kirjeldab failide robots.txt haldamist teenuses Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477704"
---
# <a name="manage-robotstxt-files"></a>Robots.txt-failide haldamine

[!include [banner](includes/banner.md)]

See teema kirjeldab failide robots.txt haldamist teenuses Microsoft Dynamics 365 Commerce.

Robotite välistamise standard või robots.txt on standard, mida veebisaidid kasutavad veebirobotitega suhtlemiseks. See juhendab veebiroboteid veebisaidi mis tahes alade osas, mida ei tohiks külastada. Roboteid kasutavad sageli otsingumootorid veebisaitide indekseerimiseks.

Robotite serverist välistamiseks loote serveris faili. Selles failis määrate robotite juurdepääsupoliitika. Fail peab olema HTTP kaudu juurdepääsetav kohalikul URL-il **/robots.txt**. Fail robots.txt aitab otsingumootoritel teie saidi sisu indekseerida.

Dynamics 365 Commerce võimaldab teil faili robots.txt oma domeenile üles laadida. Iga Commerce’i keskkonna domeeni jaoks saate üles laadida ühe robots.txt-faili ja seostada selle domeeniga.

Lisateavet faili robots.txt kohta leiate teemast [Veebirobotite lehed](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Faili robots.txt üleslaadimine

Pärast seda, kui olete loonud ja redigeerinud faili robots.txt vastavalt [robotite välistamise standardile](https://www.robotstxt.org/orig.html), veenduge, et fail oleks juurdepääsetav arvutis, kus kasutate Commerce’i autorluse tööriistu. Faili nimi peab olema **robots.txt**. Parimate tulemuste saavutamiseks peab see olema standardis märgitud vormingus. Iga Commerce’i klient vastutab oma robots.txt-faili sisu valideerimise ja haldamise eest. Faili robots.txt üleslaadimiseks peate olema Commerce’i süsteemiadministraatorina sisse logitud.

Faili robots.txt Commerce’is üleslaadimiseks toimige järgmiselt.

1. Logige Commerce’i süsteemiadministraatorina sisse.
2. Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).
3. Jaotises **Rentniku sätted** valige **Robots.txt**. Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.
4. Valige käsk **Halda**, et laadida fail robots.txt oma keskkonna domeeni jaoks üles.
5. Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Laadi üles** (ülespoole suunatud nool). Kuvatakse failibrauseri dialoogiboks.
6. Dialoogiboksis sirvige leidmiseks ja valige fail robots.txt, mille soovite seotud domeeni jaoks üles laadida, ja seejärel valige üleslaadimise lõpetamiseks käsk **Ava**.

> [!NOTE] 
> Üleslaadimise ajal kontrollib Commerce, kas fail on tekstifail, kuid see ei valideeri faili sisu.

## <a name="download-a-robotstxt-file"></a>Faili robots.txt allalaadimine

Faili robots.txt Commerce’is allalaadimiseks toimige järgmiselt.

1. Logige Commerce’i süsteemiadministraatorina sisse.
2. Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).
3. Jaotises **Rentniku sätted** valige **Robots.txt**. Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.
4. Valige käsk **Halda**, et laadida fail robots.txt oma keskkonna domeeni jaoks alla.
5. Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Laadi alla** (allapoole suunatud nool). Kuvatakse failibrauseri dialoogiboks.
6. Dialoogiboksis minge oma kohalikul kettal soovitud asukohta, kinnitage või sisestage faili nimi ja seejärel valige allalaadimise lõpetamiseks käsk **Salvesta**.

> [!NOTE]
> Seda protseduuri saab kasutada ainult nende robot.txt-failide allalaadimiseks, mis olid eelnevalt üles laaditud Commerce’i autorluse tööriistade kaudu.

## <a name="delete-a-robotstxt-file"></a>Faili robots.txt kustutamine

Faili robots.txt Commerce’is kustutamiseks toimige järgmiselt.

1. Logige Commerce’i süsteemiadministraatorina sisse.
2. Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).
3. Jaotises **Rentniku sätted** valige **Robots.txt**. Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.
4. Valige käsk **Halda**, et kustutada fail robots.txt oma keskkonna domeeni jaoks.
5. Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Kustuta** (prügikasti sümbol). Kuvatakse failibrauseri aken.
6. Failibrauseri aknas sirvige leidmiseks ja valige fail robots.txt, mille soovite domeeni jaoks kustutada, ja seejärel valige üleslaadimise lõpetamiseks käsk **Ava**. Kuvatakse hoiatusteate aken.
7. Teateaknas valige **Kustuta**, et kinitada faili robots.txt kustutamine.

> [!NOTE] 
> Seda protseduuri saab kasutada ainult nende robot.txt-failide kustutamiseks, mis olid eelnevalt üles laaditud Commerce’i autorluse tööriistade kaudu.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C-rentniku häälestus Commerce'is](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
