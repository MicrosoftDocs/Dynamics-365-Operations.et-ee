---
title: Moodulitega töötamine
description: Selles teemas kirjeldatakse, kuidas ja millal kasutada mooduleid rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025875"
---
# <a name="work-with-modules"></a>Moodulitega töötamine

Selles teemas kirjeldatakse, kuidas ja millal kasutada mooduleid rakenduses Microsoft Dynamics 365 Commerce.


[!include [banner](includes/banner.md)]

## <a name="overview"></a>Ülevaade

Moodulid on loogilised koosteüksused, mis moodustavad teie lehe struktuuri, neil on mitmesuguseid eesmärke ja ulatusi. Mõni moodul on kõrgetasemeline konteiner ning nende ainus eesmärk on hoida ja korraldada teisi mooduleid (alammooduleid). Teistel moodulitel, näiteks lihtsal pildipaigutusmoodulil, on väga konkreetne eesmärk. Teised moodulid, nt karussellmoodul, jäävad kusagile nende kahe kategooria vahele.

Vaikimisi sisaldab teie Dynamics 365 Commerce’i sait alustuskomplekti mooduli teeki, mille abil saate luua kõige üldisemaid e-kaubanduse stsenaariume. Vaid neid mooduleid kasutades peaksite saama luua täieliku e-kaubanduse saidi. Kuid võib-olla soovite neid mooduleid kohandada või luua uusi, kohandatud mooduleid, mis vastavad konkreetsetele vajadustele. Kui soovite luua kohandatud mooduleid, aitab mooduli kujundustarkvara arenduskomplekt (SDK) teil luua kohandatud mooduli teegi.

## <a name="container-modules-and-slots"></a>Konteineri moodulid ja pesad

Nagu varem mainitud, on mõni moodul kavandatud sisaldama alammooduleid. Neid mooduleid nimetatakse *konteineriteks* ja need võimaldavad luua pesastatud moodulite hierarhiaid. Konteineri moodulid sisaldavad *pesasid*. Pesasid kasutatakse konteineri alammoodulite paigutuse ja eesmärgiga tegelemiseks. Näiteks üldine lehe konteineri mooduli (mis tahes lehe kõrgema taseme moodul), mis määratleb mitu olulist pesa.

- Päise pesa
- Sisu pesa
- Jaluse pesa

Mooduli arendaja määrab need pesad ning millised alammoodulid ja mitu alammoodulit saab panna otse selle sisse. Näiteks võib päise pesa toetada vaid üht moodulit tüübiga **Päise moodul**, samas kui keha pesa võib toetada piiramatut arvu mis tahes tüüpi mooduleid (v.a teised lehe konteineri moodulid).

Loomistööriistades ei pea autorid ette teadma, milliseid mooduleid saab või ei saa igasse pessa panna. Kui lehe autorid valivad pesa ja proovivad seejärel valida sellele lisamiseks mooduli, näevad nad filtreeritud vaadet mooduli tüüpidest, mida see pesa toetab.

## <a name="content-modules"></a>Sisu moodulid

Sisu moodulid sisaldavad sisu- ja meediaelemente, nt teksti (pealkirjad, lõigud ja lingid) või vara viiteid (nt pildid, video ja PDF-id). Tüüpilised sisu mooduli tüübid on näiteks **Pannoo**, **Funktsioon** ja **Ribareklaam**. Need kolme tüüpi moodulid võivad sisaldada teksti või meediat ja neil pole vaja alammooduleid, et midagi lehel nähtavaks muuta.

Suurem osa tüüpilistest igapäevastest lehe ja sisu loomise tegevustest hõlmavad sisu mooduleid, peamiselt seetõttu, et need moodulid määravad tegeliku sisu, mida renderdatakse nende konteineri ülemmoodulites. Saadaval on palju sisu mooduleid ja need on enamasti viimased tükid, mis tuleb lisada lehe pesastatud moodulite hierarhiasse.

Järgmisel joonisel on näha, kuidas moodulid on pesastatud konteineri ülemmooduli pesadesse.

![Moodulite pesastamine](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Moodulite lisamine või eemaldamine

Järgmistes protseduurides kirjeldatakse, kuidas mooduleid lisada lisada ja eemaldada.

### <a name="add-a-module"></a>Mooduli lisamine

Mooduli lisamiseks pesasse või konteinerisse lehel tehke järgmist.

1. Valige vasakult liigenduspaanilt konteiner või pesa, kuhu võib lisada alammooduli.

    > [!NOTE]
    > Mooduli koostaja määrab loendi mooduli tüüpidega, mida saab konkreetsesse mooduli pesasse lisada. Malli autorid saavad seejärel täpsustada lubatud mooduli suvandid, et tagada järjepidev otsingumootori optimeerimine (SEO) ja loomise tõhusus kõikidel lehtedel, mis luuakse konkreetsest mallist.

1. Valige mooduli kolmikpunkti nupp (**...**) ja seejärel valige käsk **Lisa moodul**. Ilmub dialoogiboks **Lisa moodul**. See dialoogiboks filtreeritakse automaatselt, nii et kuvatakse ainult moodulid, mida toetatakse valitud konteineris või pesas. Moodulite loend määratletakse lehe malli või konteineri mooduli määratlusega.

    > [!NOTE]
    > Kui konteiner või pesa ei toeta uusi alammooduleid, ei ole käsk **Lisa moodul** saadaval.

1. Otsige ja valige lehele lisamiseks dialoogiboksist moodul.

    > [!TIP]
    > **Funktsioon** ja **Pannoo** on sobivad mooduli tüübid algajatele.

1. Valige nupp **OK**, et lisada valitud moodul valitud konteinerisse või pesasse oma lehel.

### <a name="remove-a-module"></a>Mooduli eemaldamine

Mooduli eemaldamiseks pesast või konteinerist lehel tehke järgmist.

1. Vasakult liigenduspaanilt valige eemaldatava mooduli kõrvalt kolmikpunkti nupp ja seejärel valige prügikasti nupp.
1. Kui teil palutakse kinnitada, et soovite moodulit eemaldada, valige nupp **OK**.

## <a name="configure-modules"></a>Moodulite konfigureerimine

Järgmistes protseduurides kirjeldatakse, kuidas sisu ja konteineri mooduleid konfigureerida.

### <a name="configure-a-content-module"></a>Sisu mooduli konfigureerimine

Sisu mooduli konfigureerimiseks lehel tehke järgmist.

1. Vasakul liigenduspaanil laiendage puud ja valige mis tahes sisu moodul (nt **Funktsioon**, **Pannoo** või **Ribareklaam**).
1. Parempoolsel atribuutide paanil leidke mooduli sisu ja sätete juhtelemendid.
1. Sisestage mis tahes soovitud mooduli juhtelementide atribuudid.
1. Valige käsuribal suvand **Salvesta**. See värskendab ka eelvaate lõuendit.

### <a name="configure-a-container-module"></a>Konteineri mooduli konfigureerimine

Konteineri mooduli konfigureerimiseks lehel tehke järgmist.

1. Valige lehel konteineri moodul (nt karussell- või sujuva konteineri moodul).
1. Laiendage paremal atribuutide paanil pesastatud juhtelemente, valides päised, ja määrake juhtelementidele vajalikud väärtused.
1. Vasakult liigenduspaanilt valige konteineri või konteineri sees oleva pesa nime kõrvalt kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul**. Seejärel lisage alammoodulid valitud konteinerile. Lisateavet vaadake jaotisest [Moodulitega töötamine](#add-a-module) selles teemas üleval.
1. Kui ülemmoodulis on mitu õdeüksusena eksisteerivat alammoodulit, saate muuta nende kuvamisjärjekorda ülemkonteineris. Valige mooduli kolmikpunkti nupp ja seejärel kasutage üles- ja allanoole nuppe.

## <a name="additional-resources"></a>Lisaressursid

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Mallidega töötamine](work-with-templates.md)

[Eelmääratud paigutustega töötamine](work-with-layouts.md)

[Fragmentidega töötamine](work-with-fragments.md)

[Konteineri mooduli lisamine lehele](add-container-module.md)

[Avaldamisrühmadega töötamine](publish-groups.md)

