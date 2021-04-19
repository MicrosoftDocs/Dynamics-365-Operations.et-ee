---
title: Moodulitega töötamine
description: Selles teemas kirjeldatakse, kuidas ja millal kasutada mooduleid rakenduses Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d872719d3b1aa27ccfdcf36d7739c883e7b4996
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801357"
---
# <a name="work-with-modules"></a>Moodulitega töötamine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas ja millal kasutada mooduleid rakenduses Microsoft Dynamics 365 Commerce.

Moodulid on loogilised koosteüksused, mis moodustavad teie lehe struktuuri, neil on mitmesuguseid eesmärke ja ulatusi. Mõni moodul on kõrgetasemeline konteiner ning nende ainus eesmärk on hoida ja korraldada teisi mooduleid (alammooduleid). Teistel moodulitel, näiteks lihtsal pildipaigutusmoodulil, on väga konkreetne eesmärk. Teised moodulid, nt karussellmoodul, jäävad kusagile nende kahe kategooria vahele.

Vaikimisi sisaldab teie Dynamics 365 Commerce'i sait mooduliteeki, mille abil saate teha kõige üldisemaid e-kaubanduse toiminguid. Vaid neid mooduleid kasutades peaksite saama luua täieliku e-kaubanduse saidi. Kuid võib-olla soovite neid mooduleid kohandada või luua uusi, kohandatud mooduleid, mis vastavad konkreetsetele vajadustele. Kui soovite luua kohandatud mooduleid, aitab mooduli kujundustarkvara arenduskomplekt (SDK) teil luua kohandatud mooduli teegi.

## <a name="container-modules-and-slots"></a>Konteineri moodulid ja pesad

Nagu varem mainitud, on mõni moodul kavandatud sisaldama alammooduleid. Neid mooduleid nimetatakse *konteineriteks* ja need võimaldavad luua pesastatud moodulite hierarhiaid. Konteineri moodulid sisaldavad *pesasid*. Pesasid kasutatakse konteineri alammoodulite paigutuse ja eesmärgiga tegelemiseks. Näiteks üldine lehe konteineri mooduli (mis tahes lehe kõrgema taseme moodul), mis määratleb mitu olulist pesa.

- Päise pesa
- Alampäise pesa
- Põhipesa
- Jaluse pesa
- Alamjaluse pesa

Mooduli arendaja määrab need pesad ning millised alammoodulid ja mitu alammoodulit saab panna otse selle sisse. Näiteks võib päise pesa toetada vaid üht moodulit tüübiga **Päise moodul**, samas kui keha pesa võib toetada piiramatut arvu mis tahes tüüpi mooduleid (v.a teised lehe konteineri moodulid).

Loomistööriistades ei pea autorid ette teadma, milliseid mooduleid saab või ei saa igasse pessa panna. Kui lehe autorid valivad pesa ja proovivad seejärel valida sellele lisamiseks mooduli, näevad nad filtreeritud vaadet mooduli tüüpidest, mida see pesa toetab.

## <a name="content-modules"></a>Sisu moodulid

Sisu moodulid sisaldavad sisu- ja meediaelemente, nt teksti (pealkirjad, lõigud ja lingid) või vara viiteid (nt pildid, video ja PDF-id). Tüüpilised sisu mooduli tüübid hõlmavad sisu plokki, teksti plokki ja promo banneri mooduleid. Need kolme tüüpi moodulid võivad sisaldada teksti või meediat ja neil pole vaja alammooduleid, et midagi lehel nähtavaks muuta.

Suurem osa tüüpilistest igapäevastest lehe ja sisu loomise tegevustest hõlmavad sisu mooduleid, peamiselt seetõttu, et need moodulid määravad tegeliku sisu, mida renderdatakse nende konteineri ülemmoodulites. Saadaval on palju sisu mooduleid ja need on enamasti viimased tükid, mis tuleb lisada lehe pesastatud moodulite hierarhiasse.

Järgmisel joonisel on näha, kuidas moodulid on pesastatud konteineri ülemmooduli pesadesse.

![Moodulite pesastamine](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Moodulite lisamine või eemaldamine

Järgmistes protseduurides kirjeldatakse, kuidas mooduleid lisada lisada ja eemaldada.

### <a name="add-a-module"></a>Mooduli lisamine

Mooduli lisamiseks pesasse või konteinerisse lehel tehke järgmist.

1. Valige vasakult liigenduspaanilt või otse põhilõuendilt konteiner või pesa, kuhu võib lisada alammooduli.

    > [!NOTE]
    > Mooduli koostaja määrab loendi mooduli tüüpidega, mida saab konkreetsesse mooduli pesasse lisada. Malli autorid saavad seejärel täpsustada lubatud mooduli suvandid, et tagada järjepidev otsingumootori optimeerimine (SEO) ja loomise tõhusus kõikidel lehtedel, mis luuakse konkreetsest mallist. Mooduli pesasse lisamisel filtreeritakse dialoogiboks **Lisa moodul** automaatselt, nii et kuvatakse ainult moodulid, mida toetatakse valitud konteineris või pesas. See lubatud moodulite loend määratletakse lehe malli või konteineri mooduli määratlusega.

1. Kui kasutate liigenduspaani, valige kolmikpunkt (**...**) mooduli nime kõrval ja seejärel valige **Lisa moodul**. Kui kasutate juhtelemente otse lõuendi sees, valige pluss sümbol (**+**) tühjas pesas või praegu valitud mooduli kõrval ja seejärel valige **Lisa moodul**.

    > [!NOTE]
    > Kui konteiner või pesa ei toeta uusi alammooduleid, ei ole käsk **Lisa moodul** saadaval.

1. Otsige ja valige lehele lisamiseks dialoogiboksist **Lisa moodul** moodul.

    > [!TIP]
    > **Sisu plokk** on hea mooduli tüüp algajatele töötamiseks.

1. Valige nupp **OK**, et lisada valitud moodul valitud konteinerisse või pesasse oma lehel.

### <a name="remove-a-module"></a>Mooduli eemaldamine

Mooduli eemaldamiseks pesast või konteinerist lehel tehke järgmist.

1. Vasakult liigenduspaanilt valige eemaldatava mooduli kõrvalt kolmikpunkti (**...**) ja seejärel valige prügikasti tähis. Alternatiivselt saate põhilõuendil valitud mooduli tööristaribal valida prügikasti tähise.
1. Kui teil palutakse kinnitada, et soovite moodulit eemaldada, valige nupp **OK**.

## <a name="move-a-module-to-a-new-position"></a>Mooduli liigutamine uude asendisse

Lehel mooduli teisaldamiseks uude asukohta kasutage järgmisi meetodeid.

### <a name="move-a-module-using-the-outline-pane"></a>Mooduli teisaldamine liigenduspaani abil

Mooduli teisaldamiseks liigenduspaani abil toimige järgmiselt.

1. Valige ja hoidke all moodulit, mida soovite teisaldada liigenduspaanil, seejärel lohistage moodul liigenduses uude asukohta. Sinine rida liigenduses ja lõuendil näitab, kuhu saab mooduli paigutada.
1. Vabastage moodul, et see uude asukohta kukutada.

### <a name="move-a-module-directly-within-the-canvas"></a>Mooduli teisaldamine otse lõuendil

Mooduli teisaldamiseks otse lõuendil toimige järgmiselt.

1. Valige moodul, mida soovite teisaldada lõuendil. 
1. Valige mooduli tööriistaribal kas üles- või allapoole osutava noole tähis ja lohistage seejärel nool uude asukohta leheküljel. Sinine rida lõuendil ja liigenduses näitab, kuhu saab mooduli paigutada. Kui moodulit ei saa üles või alla nihutada, on noole sümbol halli värvi. 
1. Vabastage moodul, et see uude asukohta kukutada.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Mooduli teisaldamine kolmikpunkti menüü abil

Mooduli teisaldamiseks kolmikpunkti menüü abil toimige järgmiselt.

1. Valige moodul kas liigenduses või lõuendil.
1. Valige kolmikpunkt (**...**) mooduli nime kõrval liigenduspaanil või lõuendi mooduli tööriistaribal.
1. Kui moodulit saab konteineris või pesas üles või alla nihutada, näete suvandeid **Nihuta üles** või **Nihuta alla**. Valige soovitud teisaldamise suvand, et liigutada moodulit oma alamosade suhtes üles või alla.

## <a name="configure-modules"></a>Moodulite konfigureerimine

Järgmistes protseduurides kirjeldatakse, kuidas sisu ja konteineri mooduleid konfigureerida.

### <a name="configure-a-content-module"></a>Sisu mooduli konfigureerimine

Sisu mooduli konfigureerimiseks lehel tehke järgmist.

1. Vasakul liigenduspaanil laiendage puud ja valige mis tahes sisu moodul (nt **Sisu blokk**). Lisaks saade valida mooduli valida põhilõuendil.
1. Sisestage parempoolse mooduli atribuutide paanil kõik soovitud mooduli juhtelementide atribuudid.
1. Valige käsuribal suvand **Salvesta**. See värskendab ka eelvaate lõuendit.

### <a name="edit-module-text-properties"></a>Mooduli tekstiomaduste muutmine

Mooduli tekstiatribuute, mis ei ole kirjutuskaitstud, saab redigeerida otse lõuendile.

Mooduli tekstiatribuutide redigeerimiseks toimige järgmiselt.

1. Valige lõuendi teksti juhtelement, seejärel asetage kursor sinna, kus soovite teksti redigeerida.
1. Sisestage soovitud teksti sisu.
1. Muu sisu redigeerimise jätkamiseks valige teksti sisust väljaspoole.

### <a name="inline-image-selection"></a>Tekstisisese pildi valik

Mooduli pilte, mis ei ole kirjutuskaitstud, saab muuta otse lõuendile.

Sisu mooduli uue pildi valimiseks järgige järgmisi samme.

1. Topeltklõpsake lõuendi pildil. See avab meedia valija akna.
1. Leidke ja valige uus pilt, mida soovite kasutada, ja seejärel valige **OK**. Uus pilt on nüüd lõuendile sobitatud.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
