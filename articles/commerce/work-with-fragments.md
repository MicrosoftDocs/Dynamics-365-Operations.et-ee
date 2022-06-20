---
title: Fragmentidega töötamine
description: See artikkel kirjeldab, miks, millal ja kuidas kasutada killust selles Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8824a42e46d94904f50d3f95b486673c231d9828
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896817"
---
# <a name="work-with-fragments"></a>Fragmentidega töötamine 

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, miks, millal ja kuidas kasutada killust selles Microsoft Dynamics 365 Commerce.

Fragmendid tagavad tsentraliseeritud loomiskogemuse mooduli konfiguratsioonidele, mida tuleb kogu saidil uuesti kasutada. Näiteks päiseid, jaluseid ja ribareklaame konfigureeritakse sageli fragmentidena, kuna neid jagatakse paljude lehtede vahel. Mõelge fragmentidest kui miniatuursetest veebisaitidest, mida saab sisestada teie saidi teistele lehtedele. Fragmentidel on oma elutsükkel. Teisisõnu need luuakse, neile viidatakse, neid värskendatakse ja need kustutatakse loomistööriistade sõltumatute üksustena.

Pärast fragmentide konfigureerimist saab neid kasutada kõikjal teie saidi struktuuris, kus saab kasutada mooduleid. Fragmentidele saab lehtedel, paigutustes, mallide ja teistes fragmentides viidata.

> [!NOTE]
> Fragmendid võivad olla kuni seitsme taseme sügavusel teistes fragmentides.

Näiteks kui soovite reklaamida hooajalist sündmust saidi paljudel lehtedel, võite selleks kasutada fragmenti. Uue fragmendi loomise esimene samm on valida mooduli tüüp, millest soovite alustada. Selles näites saate luua fragmendi pannoomoodulist.

> [!NOTE]
> Fragmente saab luua igast mooduli tüübist.

Seejärel saate konfigureerida pannoofragmendi konkreetse kampaaniasisuga. Saate seda ka vajaduse järgi lokaliseerida. Uut eraldiseisevat pannoofragmenti saab seejärel kasutada eelkonfigureeritud moodulina kogu saidil. Saate seda hõlpsasti lisada mallidele, konkreetsetele lehtedele või teistele fragmentidele, mis sisaldavad pannoomooduleid.

Kõik kohad, kuhu fragment lisatakse, on viited loodud kesksele pannoofragmendile. Kui avaldate fragmendi muudatused, kajastuvad need muudatused kohe kõikides kohtades üle saidi, kus fragmendile viidatakse. Seega pakuvad fragmendid võimsat ja tõhusat moodust mooduli konfiguratsioonide uuesti kasutamiseks ja tsentraalselt haldamiseks saidil. Neid tõhusalt kasutades saate muuta töö oluliselt kiiremaks ja vähendada saidi haldamisega seotud kulusid.

Järgmisel joonisel on näha, kuidas saab fragmente kasutada jagatud mooduli konfiguratsioonide loomise tsentraliseerimiseks üle e-kaubanduse saidi.

![Näide sellest, kuidas saab fragmente kasutada jagatud mooduli konfiguratsioonide loomise tsentraliseerimiseks üle e-Commerce saidi.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Fragmendi loomine

Saate kas luua uue fragmendi või salvestada olemasoleva mooduli konfiguratsiooni fragmendina.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Olemasoleva mooduli konfiguratsiooni salvestamine fragmendina

Varem konfigureeritud mooduli teisendamiseks korduskasutatavaks fragmendiks Commerce'i saidiehitajas, toimige järgmiselt.

1. Avage leht või mall, mis sisaldab moodulit, mida soovite teisendada fragmendiks.
1. Valige vasakul liigenduspaanil või otse visuaalses leheehitajas eelnevalt konfigureeritud moodul.
1. Valige kolmikpunkt (**...**) mooduli nime kõrval kas liigenduspaanil või visuaalses leheehitajas valitud mooduli tööriistaribal. 
1. Valige **Jaga fragmendina**. 
1. Sisestage dialoogiboksis **Salvesta fragmendina** fragmendi nimi.
1. Valige nupp **OK**, et salvestada mooduli konfiguratsioon fragmendina, mida saab lisada teistele lehtedele.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Loo uus fragment

Uue fragmendi loomiseks Commerce'i saidiehitajas, toimige järgmiselt.

1. Valige navigeerimispaanilt vasakult suvand **Fragmendid**.
1. Valige suvand **Uus**. Kuvatakse dialoogiboks **Uus fragment**, kus on näha kõik saadaolevad mooduli tüübid. Nagu varem mainitud, fragmente saab luua igast mooduli tüübist.
1. Valige oma fragmendi jaoks mooduli tüüp.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Valides üldkonteineri mooduli tüübi, on teil hiljem fragmendi värskendamise ja konfigureerimise vajadusel kõige rohkem vabadust.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Fragmentide lisamine, eemaldamine või redigeerimine lehel

Järgmistes protseduurides kirjeldatakse, kuidas fragmente lisada, eemaldada ja redigeerida.

### <a name="add-a-fragment"></a>Fragmendi lisamine

Lehele uue fragmendi lisamiseks Commerce'i saidiehitajas, toimige järgmiselt.

1. Valige vasakult liigenduspaanilt või otse visuaalsest leheehitajast konteiner või pesa, kuhu võib lisada alammoodulid.
1. Valige kolmikpunkt (**...**) konteineri või pesa nime kõrval.  Kui kasutate visuaalset leheehitajat, valige teise võimalusena pluss-sümbol (**+**).  
1. Valige **Lisa fragment**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Kui konteiner või pesa ei toeta uusi alammooduleid, ei ole suvand **Lisa fragment** saadaval.
    
1. Otsige dialoogiboksist **Lisa fragment** fragmenti ja valige see lisamiseks. Kui ühtegi saadaolevat fragmenti loendis pole, peate kõigepealt looma fragmendi mooduli tüübist, mida valitud konteiner või pesa toetab.
1. Valige soovitud fragment, et lisada see oma lehel konteinerile või pesale.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> Konteineris või pesas lubatud moodulid on määratletud lehe malli või moodulite enda määratlustega.

### <a name="remove-a-fragment"></a>Fragmendi eemaldamine

Fragmendi eemaldamiseks pesast või konteinerist Commerce'i saidiehitaja lehel, toimige järgmiselt.

1. Vasakult liigenduspaanilt valige eemaldatava fragmendi kõrvalt kolmikpunkt (**...**) ja seejärel valige prügikasti tähis.  Alternatiivselt saate valida visuaalses leheehitajas fragmendi ja valida fragmendi tööriistaribal prügikasti tähise.
1. Kui teil palutakse kinnitada, et soovite fragmenti eemaldada, valige nupp **OK**.

> [!NOTE]
> Kui fragmendi lehelt eemaldate, eemaldate lehelt vaid viite sellele. Te **ei** kustuta fragmenti saidilt. Fragmentide kustutamiseks saidilt peate kasutama fragmendi kontrollija kasutajaliidest (UI). Fragmente saate saidilt kustutada ainult siis, kui neile ei viita parasjagu ükski leht, mall või teine fragment.

### <a name="edit-a-fragment"></a>Fragmendi redigeerimine

Fragmentide redigeerimiseks peate kasutama fragmendi redaktori kasutajaliidest. See piirang on kavandatud. See aitab tagada, et autorid ei ajaks segi konkreetse lehe moodulite redigeerimise protsessi paljude lehtede vahel jagatavate fragmentide redigeerimise protsessiga.

Fragmendi redigeerimiseks Commerce'i saidiehitajas, toimige järgmiselt.

1. Valige navigeerimispaanilt vasakult suvand **Fragmendid**.
1. Valige jaotisest **Fragmendid** redigeerimiseks fragment.
1. Redigeerige fragmendi mooduli atribuute ja struktuuri vajaduse järgi. Protsess meenutab moodulite redigeerimise protsessi, mis toimub lehe redaktori vaates.

Saate fragmenti redigeerida ka nii, et valite selle lehelt, mallist või ülemfragmendist ja seejärel valite paremalt atribuutide paanilt suvandi **Fragmendi redigeerimine**.

### <a name="rename-a-fragment"></a>Killu ümbernimetamine

Olemasoleva tüki ümber nimetamiseks saidikonstruktoris järgige neid samme.

1. Valige vasakul navigeerimispaanil **tükid**.
1. Valige selle tüki killu nimi, mida soovite ümber nimetada.
1. **Tüki** redigeerimise alustamiseks klõpsake nuppu Redigeeri. Võtke arvesse, et killust ei saa redigeerida, kui keegi teine juba tükke redigeerib.
1. Killu atribuutide paanil valige killusta nime kõrvalt amplige märgiks.
1. Redigeerige killusta nime vastavalt vajadusele.
1. Nime muudatuse kinnitamiseks märkige see ruut.
1. Valige **Lõpeta redigeerimine**.

Tüki nime saate ümber nimetada pärast selle loomist, redigeerides seda ja valides seejärel atribuudipaanil tüki nime kõrvalt tükimärgi.

## <a name="additional-resources"></a>Lisaressursid

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Mallidega töötamine](work-with-templates.md)

[Eelmääratud paigutustega töötamine](work-with-layouts.md)

[Avaldamisrühmadega töötamine](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
