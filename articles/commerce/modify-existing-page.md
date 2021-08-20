---
title: Olemasoleva saidilehe muutmine
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce olemasolevat saidi lehte muuta.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0039489c266840e5341f2e322fa7783216ac9bb3ebcecff840f591beec9f79c4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751539"
---
# <a name="modify-an-existing-site-page"></a>Olemasoleva saidilehe muutmine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce olemasolevat saidi lehte muuta.

Kui peate lehte muutma, on esimene etapp selle avamine lehe redaktoris. Avage teie lehte sisaldav sait ja seejärel leidke lehtede loendist soovitud leht. Kui te lehte ei leia, saate kasutada autorluse tööriista rikkalikku sisuga otsingufunktsiooni. Sisestage kas lehe täpne nimi või sisestage selle esimesed paar tähte ja seejärel tärn (\*). Kuvatakse filtreeritud lehtede loend. Seda loendit saate kasutada soovitud lehe leidmiseks. Pärast õige lehe leidmist valige lehe nimi, et avada leht lehe redaktoris.

> [!TIP]
> Kui leht on leheinspektoris nähtav, saate valida **Redigeeri** ja lehte enne selle leheredaktoris avamist vaadata. Sel viisil saate registreerida välja mitu lehte korraga.

Kui leht on lehe redaktoris avatud, peate veenduma, et see oleks teile välja registreeritud. Autorluse tööriista käsuriba on dünaamiline, kontekstitundlik ja oleku tundlik. Seetõttu kuvab see ainult toimingud, mida saate lehel praegu teha. Näiteks kui leht ei ole teile välja registreeritud, siis nupud **Salvesta** ja **Lõpeta redigeerimine** käsuribal ei ilmu. Akna paremal küljel on näidatud ka lehe olek.

Kui leht ei ole veel teile välja registreeritud, valige käsuribal käsk **Redigeeri**. Käsuriba muutub, et peegeldada lehe uut olekut. Samuti saate teatise, mis ütleb, et leht registreeriti teile välja.

Järgmine etapp on teha tegelikud muudatused. Sageli kasutate vasakul lehe liigendpuud, et leida ja valida moodul, mida soovite muuta, ja seejärel teete paremal atribuutide paanil muudatused. 

Samas võib teie muudatus hõlmata mudelite või fragmentide lisamist või eemaldamist. Fragmendi või mooduli lisamiseks kasutage lehekülje liigendpuud, et leida pesa, kuhu soovite mooduli või fragmendi lisada, ja valige seejärel selle pesa kolmikpunkti nupp (**...**). Kuvatakse menüü, mis sisaldab mooduli või fragmenti lisamise käske. Mooduli või fragmenti eemaldamiseks leidke ja valige see lehekülje liigendpuus, valige kolmikpunkti nupp ning seejärel valige mooduli või fragmenti kustutamiseks käsk.

> [!TIP]
> Samuti saate vaadata ja redigeerida iga mooduli atribuute, mis on nähtavad visuaalse leheehitaja eelvaates, valides selle otse.

Kui olete muudatuste tegemise ja nende mõju eelvaate vaatamise lõpetanud, tuleb teil leht registreerida, valides käsiribal käsu **Lõpeta redigeerimine**. 

Muudatuste koheseks avaldamiseks valige käsuribal käsk **Avalda**. Avaldatakse uusim muudetud lehe registreeritud versioon ja see muutub kättesaadavaks välistele kasutajatele, kes teie saiti vaatavad. 

## <a name="example-change-the-video-on-the-home-page"></a>Näide: avalehel video muutmine

Järgmine näide selgitab, kuidas muuta avalehte, muutes videopleieri moodulis ilmuva video.

1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Valige navigeerimispaanilt vasakult suvand **Lehed**.
1. Leidke ja valige avaleht, et avada see lehe redaktoris.
1. Klõpsake käsuribal käsku **Redigeeri**.
1. Valige lehe liigenduses pesa **Peamine**.
1. Laiendage pesas **Peamine** kõiki sujuvaid konteinei mooduleid.
1. Leidke ja valige videopleieri moodul.
1. Valige paremalt atribuutide paanil **video** atribuut. Kuvatakse varade valija.
1. Valige varade valijas saadaolev videovara või valige uue videovara üleslaadimiseks suvand **Uue vara üleslaadimine**.
1. Valige nupp **OK**.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Sisestage väljale **Kommentaarid** suvand **Muutsin video** ja valige seejärel **OK**.
1. Uuendatud lehe eelvaate kuvamiseks valige suvand **Eelvaade**. Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.
1. Valige **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Uue saidilehe lisamine](add-new-page.md)

[Lehepaigutuste valimine](select-page-layouts.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)

[Lehe salvestamine, eelvaade ja avaldamine](save-preview-publish-page.md)

[Tootelehe rikastamine](enrich-product-page.md)

[Kategooria sihtlehe rikastamine](enrich-category-page.md)

[Lehe sisu hõlbustusfunktsioonide kinnitamine](verify-accessibility.md)

[Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
