---
title: CSS-i alistamisfailidega töötamine
description: See teema kirjeldab miks, millal ja kuidas kasutada Cascading Style Sheet (CSS) alistamisfaile rakendusega Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ec43b16b1df07400cffe597378ad4035e4d07e0
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411243"
---
# <a name="work-with-css-override-files"></a>CSS-i alistamisfailidega töötamine


[!include [banner](includes/banner.md)]

See teema kirjeldab miks, millal ja kuidas kasutada Cascading Style Sheet (CSS) alistamisfaile rakendusega Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Püsiva tegevuskoha laade peaks tavaliselt käsitlema saidi kujunduse kaudu. Kujundused annavad teie saidi mis tahes leheküljel olevate moodulite jaoks CSS aluselise ja stiili sätted. Kujundused luuakse Dynamics 365 Commerce’i veebitarkvara arenduse komplekti (SDK) abil ja need viiakse teie veebisaitide juurde teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu. Kujunduse silumise võimalused ja mooduli liidese konfiguratsioonid SDK-spikri saidi arendajatel loovad kohandatavad ja sidusad saidi kujunduse paketid. Kui need kujunduse paketid on saidile paigutatud, saavad saidi autorid keskenduda saidi arendamise asemel sisu loomisele, redigeerimisele ja avaldamisele.

Arvestades kujunduse tavalist elutsüklit, võib mõne stsenaariumi puhul olla keelatud arendajate poolne muudatus SDK ja LCS-i juurutamise torujuhtme kaudu. Saidi prototüübid või kiirparandused võivad näida kohmakatena, kui SDK ei ole konigureeritud või kui teil pole aega LCS-i juurutamise ootamiseks.

Nende stsenaariumide korral võib abi olla CSS-i alistamisfailidest. Commerce’i autorluse tööriistades saavad volitatud kasutajad CSS-faili üles laadida, kuvada selle eelvaate ja seejärel aktiveerida selle, et alistada saidi kujundus. SDK või LCS-i juurutuse üldkulu pole nõutav. CSS-i alistamisfailis määratletud alistamised võivad olla nii väikesed kui ühe teksi laadi muutmine, või nii laiaulatuslikud, kui kogu kaubamärgi uuendamine.

Enne CSS-i alistamisfailide kasutamist arvestage järgmiste piirangutega.

- Korraga saab saidil olla ainult üks CSS-i alistumisfail. Seetõttu peavad kõik aktiivsed alistamised olema ühes alistamisfailis.
- Kuigi saate Commerce’i autorluse tööriistades kuvada alistamiste eelvaate, puuduvad spetsiaalsed silumise funktsioonid, mis aitaksid tuvastada mis tahes tõrkeid, mida alistamised tekitavad. Teisisõnu kui kasutate CSS-i alistamisfaile, pole teil sama tööriistakogumit, mida SDK pakub mooduli ja autorluse kinnitamiseks.

Sellegipoolest pakuvad CSS-i alistamisfailid kiiret viisi kujunduse prototüübi loomiseks või kiirparanduse rakendamiseks enne täieliku kujunduse uuenduse arendamist ja juurutamist.

## <a name="create-a-css-override-file"></a>CSS-i alistamisfaili loomine

CSS-i alistufaili loomiseks sate kasutada mis tahes integreeritud arenduskeskkonda (IDE), tekstiredaktorit või lähtekoodi redaktorit. Tüüpiline lähenemine on kasutada brauseris standardseid veebisilurit, et tuvastada teie olemasoleval saidil laadi valijad, atribuudid ja väärtused. Enamik brausereid võimaldavadb teil muuta väärtusi ja kuvada siluris nende eelvaade. Kui olete tuvastanud muudatused, mida soovite teha, saate need salvestada oma CSS-i faili.

## <a name="upload-a-css-override-file"></a>CSS-i alistamisfaili üleslaadimine

CSS-i alistamisfaili Commerce’is üleslaadimiseks toimige järgmiselt.

1. Avage autorluse tööriistades oma sait.
1. Valige navigeerimispaanilt vasakult suvand **Kujundus**.

    > [!NOTE]
    > Sõltuvalt kasutatavast Commerce’i autorluse tööriistade versioonist, peate võib-olla laiendama navigeerimispaani suvandit **Sätted**, enne kui saate valida suvandi **Kujundus**.

1. Kui see ei ole juba valitud, valige põhidisaini vahekaardil **CSS-i alistamine**.
1. Jaotises **Saadaolevad CSS-i alistamised** valige käsk **Laadi CSS-fail üles**. Kuvatakse File Exploreri aken.
1. File Exploreris sirvige ja valige CSS-fail ning seejärel valige **Ava**. Üleslaaditud CSS-fail kuvatakse nüüd asukohas **Saadaolevad CSS-i alistamised**.

## <a name="preview-a-css-override-file"></a>CSS-i alistamisfaili eelvaade

CSS-i alistamisfaili eelvaate kuvamiseks enne, kui selle oma avaldatud saidil aktiveerite, tehke järgmist.

1. Valige vasakpoolsel navigeerimispaanil suvand **Kujundus**ja seejärel otsige vahekaardil **CSS-i alistamine** jaotises **Saadaolevad CSS-i alistamised** üles CSS-fail, mille eelvaate soovite kuvada.
1. CSS-faili nime kõrval valige suvand **Saidi eelvaade**.
1. Valige dialoogiaknas **URL-i valimine** saidi URL, mille suhtes soovite alistused rakendada, ja seejärel valige **OK**.
1. Kui valitud URL-il on mitu varianti, valige kuvatavas dialoogiaknas **Eelvaate variatsioonid** soovitud variant.

Avatakse uus brauseri vahekaart või aken, kus saate kinnitada oma saidi laadi alistused. Seejärel saate jagada URL-i teiste autenditud Commerce’i kasutajatega ülevaatamiseks ja tagasisideks.

## <a name="activate-a-css-override-file-on-your-live-site"></a>CSS-i alistamisfailide avaldatud saidil aktiveerimine

Kui olete vaadanud ja kinnitanud CSS-i alistamisfaili, saate selle oma avaldatud saidil aktiveerida.

> [!NOTE]
> Korraga saab teie saidil olla ainult üks CSS-i alistamisfail. Kui aktiveerite uue alistamisfaili, eelmine alistamisfail desaktiveeritakse. Seetõttu veenduge, et kõik nõutavad alistamised on olemas ühes CSS-i alistamisfailis.

CSS-i alistamisfaili aktiveerimiseks toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanil suvand **Kujundus** ja seejärel otsige vahekaardi **CSS-i alistamine** jaotises **Saadaolevad CSS-i alistamised**üles CSS-fail, mille soovite aktiveerida.
1. CSS-faili nime all valige **Aktiveeri**. Alistamisfail muutub kohe teie avaldatud saidil aktiivseks.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>CSS-i alistamisfailide avaldatud saidil desaktiveerimine

Oma saidil CSS-i alistamisfaili desaktiveerimiseks toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanil suvand **Kujundus** ja seejärel otsige vahekaardi **CSS-i alistamine** jaotises **Saadaolevad CSS-i alistamised** üles CSS-fail, mille soovite desaktiveerida.
1. CSS-faili nime all valige **Desaktiveeri**. Alistamisfail muutub kohe teie avaldatud saidil passiivseks.

> [!TIP]
> CSS-i alistamisfailide täiendavate suvanditele juurdepääsuks valige kolmikpunkt (**...**) CSS-faili nime kõrval. Suvandid **Laadi alla**, **Nimeta ümber** ja **Asenda** on kasulikud olemasoleva CSS-i alistamisfaili kiireks muutmiseks.

## <a name="additional-resources"></a>Lisaressursid

[Logo lisamine](add-logo.md)

[Saidi kujunduse valimine](select-site-theme.md)

[Töö stiili eelseadistustega](style-presets.md)

[Leheikooni lisamine](add-favicon.md)

[Tervitussõnumi lisamine](add-welcome-message.md)

[Autoriõiguste teatise lisamine](add-copyright-notice.md)

[Saidile keelte lisamine](add-languages-to-site.md)

[Telemeetria toetamiseks saidile skriptikoodi lisamine](add-telemetry.md)
