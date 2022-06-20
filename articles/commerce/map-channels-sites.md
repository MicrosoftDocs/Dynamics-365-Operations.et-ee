---
title: Kanalite vastendamine e-kaubanduse saitidega
description: See artikkel kirjeldab mõningaid tavalisemaid kanali vastendamise stsenaariume Microsoft Dynamics 365 Commerce, mida saab enamiku teiste ärinõuete puhul lisada.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902759"
---
# <a name="map-channels-to-e-commerce-sites"></a>Kanalite vastendamine e-kaubanduse saitidega

See artikkel kirjeldab mõningaid tavalisemaid kanali vastendamise stsenaariume Microsoft Dynamics 365 Commerce, mida saab enamiku teiste ärinõuete puhul lisada.

Dynamics 365 Commerce toetab mitut äristsenaariumi võrgukanalite [vastendamiseks](#channels), kus on konfigureeritud toodete, [hindade ja allahindluste kogum klientide e-kaubanduse](#e-commerce-sites) saidikogemustele.

See artikkel hõlmab järgmisi stsenaariume:

- **Ühe keelega kanal, mis omab ühte e-ärisaidi kogemust.** Näiteks võib see stsenaarium sisaldada ühte kaubamärgi saiti, mis on konfigureeritud USA Inglise turu jaoks.
- **Mitme keelega kanal, kus on ühe lokaliseeritud saidikogemus.** Näiteks võib see stsenaarium sisaldada ühte kaubamärgi saiti, mis on konfigureeritud Kanada jaoks prantsuse ja inglise keele toega. Selles stsenaariumis on eri keeltes kasutajatel sama saidikogemus, kuid see lokaliseeritakse iga kasutaja valitud keelde.
- **Mitme keelega kanal, mis omab keele kohta erinevat saidikogemust.** Näiteks võib see stsenaarium sisaldada ühte kaubamärgi saiti, mis on konfigureeritud Kanada jaoks prantsuse ja inglise keele toega. Selles stsenaariumis on iga keele kohta kordumatud saidikogemused.
- **Mitu kanalit (ühe keele ja/või mitme keelega), kellel on ühe lokaliseeritud saidikogemus.** Näiteks võib see stsenaarium sisaldada ühte kaubamärgi saiti, mis on konfigureeritud Austraalia ja Uus-Meremaa jaoks. Selles stsenaariumis jagavad mõlemad riigid sama saidikogemust inglise keeles, kuid iga riik on konfigureeritud erinevate toodete, valuuta, hindade, allahindluste ja tarneviisidega.
- **Mitu kanalit (ühe- ja/või mitmekeelsed), kus on kanali kohta erinev saidikogemus.** Näiteks võib see stsenaarium sisaldada ühte kaubamärgi saiti, mis on konfigureeritud Austraaliale, Kanadale ja Saksamaale mitmes keeles. Selles stsenaariumis on igal riigil kordumatu saidikogemus, mis on konfigureeritud erinevate toodete, valuuta, hindade, allahindluste ja tarneviisidega.

## <a name="channels"></a>Kanalid

Kanal (tuntud ka kui võrgupood või võrgukanal) esindab e-kaubanduse võrguladu, mida kasutatakse toodete, hinnakujunduse, allahindluste, keelte, makseviiside, tarneviiside, täitmiskeskuste ja muude e-äri klientidele kättesaadava võrgukogemuse aspektide vastendamiseks. Kanaleid luuakse ja hallatakse Commerce Headquartersis ja vastendatakse ühe juriidilise [isikuga](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities). Juriidiline isik põhineb tavaliselt riigis, mis nõuab kanali maksuaruandluse süsteemi ja seda saab konfigureerida ainult ühe valuutaga.

Lisateavet kanalite kohta vt kanali [ülevaatest](channels-overview.md). Lisateavet võrgukanali loomise kohta vt häälestage [võrgukanal](channel-setup-online.md).

Järgmine näite näide rakendusest Commerce headquarters näitab vaikimisi võrgukanaleid, mis juurutatakse Dynamics 365 Commerce, kui on valitud demoandmete suvand.

![Vaikimisi demoandmete kanalid Commerce Headquartersis.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>E-kaubanduse saidid

E-kaubanduse sait sisaldab saidilehti, mida kliendid kasutavad sirvimiseks ja ostuks. E-äri saite hallatakse Commerce'i saidi koostajas.

Lisateavet saitide loomise ja haldamise kohta saidikonstruktoris vt [E-äri saidi ülevaatest](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Kanali tavalised vastendamise stsenaariumid

Dynamics 365 Commerce toetab kanali vastendamise stsenaariumite laia valikut. Kanali vastendamise stsenaariumid, mis järgnevad, on vaid kõigi võimalike kanali vastendamise stsenaariumite alamkogum. Need on mõeldud juhendina, mis aitab teil planeerida mis tahes ainulaadsetele äristsenaariume, mis teil on. Fiktiivst Adventure Worksi kaubaladu Dynamics 365 Commerce, mis on lisatud demoandmetele, kasutatakse iga stsenaariumi näitena.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Ühe keelega kanal, kus on üks e-äri saidikogemus

Kõige põhistsenaariumi puhul on ühel kanalil ühel turul müümisel üks keel. Näide selle stsenaariumi kohta on Adventure Worksi e-pood, mis on seadistatud ainult USA inglise turu jaoks.

Järgmises näites on näidatud kanali konfiguratsioon rakenduses Commerce Headquarters. Selles konfiguratsioonis toetab võrgukanal ainult ühte keelt (**en-us**), ühte valuutat (**USD**) ja ühte äriüksust (**usrt**), mida kasutatakse maksuaruandluses.

![Commerce Headquartersis esiletõstetud Adventure Worksi e-poe juriidiline isik, valuuta ja keele väärtused.](media/channel-mapping-3.png)

Üksikut võrgukanalit saab saidikonstruktoris vastendada üksiku e-kaubanduse saidiga. Lisateavet uue saidi loomise ja [selle](#map-a-channel-to-a-site-in-site-builder) kanaliga vastendamise kohta vt selle artikli jaotisest Kanali vastendamine saidiga saidikonstruktoris.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Mitme keelega kanal, kus on ühe lokaliseeritud saidikogemus

Selles stsenaariumis toetab üks kanal rohkem kui ühte keelt. Seetõttu saab tootenimesid, kirjeldusi ja atribuute lokaliseerida Commerce Headquartersis. Täieliku lokaliseeritud saidikogemuse andmiseks saab saidi turundussisu lokaliseerida ka Commerce'i saidi koostajas.

Selle stsenaariumi piirang on see, et ühte kanalit saab konfigureerida ainult ühe valuutaga, ühe juriidilise isikuga ning ühe toote- ja hinnakomplektiga. See konfiguratsioon toimib kõige paremini riikides, kus on ühe valuuta ja mitu keelt (nt Kanada, millel on inglise ja prantsuse keeled), üks juriidiline isik ning üks toodete ja hindade kogum.

Kanali iga keelt saab konfigureerida oma domeeninimega. Näiteks saab domeeni `www.adventure-works.ca` konfigureerida Kanada inglise versiooni jaoks `www.adventure-works-fr.ca` ja domeeni saab konfigureerida Kanada prantsuse versiooni jaoks. Teise võimalusena saab kanalis erinevaid keeli konfigureerida ühes domeenis ja siis saab iga keele jaoks kasutada erinevat teed. Näiteks saab domeeni `www.adventure-works.ca` konfigureerida Kanada inglise versiooni jaoks ja `www.adventure-works.ca/fr` seejärel teed saab kasutada Kanada prantsuse versiooni jaoks. [Geotuvastusel](geo-detection-redirection.md) võib lubada ka kasutaja automaatse ümbersuunamise õigele saidile, põhinedes kasutaja asukohale.

Teavet selle kohta, kuidas lubada klientidel keelte vahel käsitsi lülituda, [vt selle artikli jaotisest Lisa ja konfigureeri](#add-and-configure-the-site-picker-module) saidi valija moodul. Lisateavet lokaliseeritud lehtede ja killustamise kohandamise kohta vt jaotisest [Mitme kanali ja keelega saidi sisu](#manage-site-content-that-has-multiple-channels-and-languages) haldamine.

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Mitme keelega kanal, mis omab keele kohta erinevat saidikogemust

Võite eelistada stsenaariumi, kus üks kanal toetab rohkem kui ühte keelt, kuid iga keele jaoks renderdatakse täiesti erinev saidikogemus. Selle stsenaariumi rakendamise soovitatav meetod on kasutada lehekülje [variante](#implement-page-variants-for-each-language) ühel saidil.

Teine meetod on luua uus e-äri sait saidi iga keele jaoks saidikonstruktoris ja seejärel vastendada iga sait ühe võrgukanali ja keelega. Tulemuseks on üks võrgukanal, mis on vastendatud mitme e-äri saidiga, üks iga keele kohta. See mitmesaidiline meetod nõuab lisahaldusressursse, kuna saidikonstruktoriga tuleb hallata rohkem kui üks sait.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Mitu kanalit (ühe keele ja/või mitme keelega), kellel on ühe lokaliseeritud saidikogemus

Kaubamärgiga sait võib vajada mitut võrgukanalit regiooni kohta, et toetada eri valuutat, toodete kogumeid ja igale kanalile ühe kanali hinnakomplekti. Näiteks võib Adventure Worksil olla võrgukanal Kanada turu jaoks, kus on mitu keelt, USA turu kanal, mis omab ühte keelt, ja kanaliks Saksa turu jaoks, kus on üks keel. Selles stsenaariumis konfigureeritakse iga võrgukanal piirkonnaspetsiifilise juriidilise isiku jaoks ja sel võib olla sama toodete kogum, mis teistel kanalitel on, nende toodete alamkogum või muu tootekogum. Igal kanalil on oma hinnad ka piirkonna valuutas, maksud, allahindlused ja saatmisviisid.

Selles stsenaariumis saab iga turu konfigureerida oma domeeninimedega. Näiteks saab domeeni `www.adventure-works.com` konfigureerida USA turu jaoks ja `www.adventure-works.de` domeeni saab konfigureerida Saksa turu jaoks. Teise võimalusena saab iga turg konfigureerida kasutama erinevat teed. Näiteks saab `www.adventure-works.com` domeeni konfigureerida USA turu jaoks ja `www.adventure-works.com/de` seejärel kasutada teed Saksa turu jaoks. [Geotuvastusel](geo-detection-redirection.md) võib lubada ka kasutajate automaatset ümbersuunamist õigele saidile, põhinedes nende piirkonnal.

Võite soovida, et teie sait pakuks ripploendit, mis võimaldab kasutajatel käsitsi konkreetsele turule lülituda. Lisateavet vt selle artikli jaotisest [Saidi valija mooduli](#add-and-configure-the-site-picker-module) lisamine ja konfigureerimine.

Teavet selle kohta, kuidas konfigureerida ühe saidi jaoks mitut kanalit, [vt e-äri saidi jaotisest Mitme kanali konfigureerimine](#configure-multiple-channels-on-an-e-commerce-site).

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Mitu kanalit (ühe keele ja/või mitme keelega), kellel on kanali kohta erinev saidikogemus

Teil võib tekkida soovi korral mitu kanalit ühe kaubamärgi jaoks erinevates regioonides ja võite soovida, et igal piirkonnal oleks erinev saidikogemus. Selle stsenaariumi rakendamiseks on kaks võimalust:

- Kasutage [lehekülje variante](#implement-page-variants-for-each-language).
- Konfigureerige erinev sait iga võrgukanali jaoks saidikonstruktoris ja seejärel vastendage iga saiti erineva võrgukanali ja keelega. See meetod nõuab lisahaldusressursse, kuna saidikonstruktoris tuleb hallata rohkem kui üks sait.

## <a name="cross-channel-sharing"></a>Kanaliülene ühiskasutus

Kanaliülene ühiskasutus on kasulik, kui ühe saidi mitu kanalit saavad sisu jagada. Näiteks saab jaemüüja, kellel on mitu kaubamärki ja kauplust, mis on toodud ühele saidile, jagada osa sisust mõne või kõigi kauplustega. Ühiskasutuses sisu võib sisaldada lehekülgi tingimuste, maksetingimuste, saatmismeetodite ja korduma kippuvate küsimuste (KKK) jaoks. Lisateavet vt jaotisest Luba [ja kasutage kanaliülest ühiskasutust](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Vastenda kanal saidiga saidikonstruktoris

Saitide loomiseks ja konfigureerimiseks erinevate võrgukanalite kasutamiseks on mitu meetodit.

### <a name="create-a-new-site"></a>Uue saidi loomine

Uue kaubamärgiga saidi saate luua saidikonstruktoris, avades saitide **loendilehe** ja valides **uue saidi**. Seejärel saate kuvatavas **dialoogiboksis** Uus sait valida vaikimisi saidi võrgukanali ja keele, nagu näha järgmises näite näites.

![Uue kanali loomine saidikonstruktoris.](media/channel-mapping-4.png)

Sel viisil loov sait on tühi ja ei sisalda ühtegi saidilehte (nt kodulehekülge, kategooria lehekülgi ja toote lehekülgi).

Lisateavet leiate teemast [E-kaubanduse saidi loomine](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Uue saidi loomine saidi koopiatoimingu abil

Selle asemel, et luua uus, tühi sait eelmises jaotises kirjeldatud viisil, on parim tava alustada koopiaga ühest Commerce'i mooduli teeki antud algsaidist, nagu Fabrikam või Adventure Worksi sait.

Olemasoleva saidi kopeerimiseks minge saidikonstruktori **saitide** loendilehele ja valige suvand Kopeeri **sait**. Seejärel saate kuvatavas **dialoogiaknas** Kopeeri sait valida lähtesaidi ja määrata sihtsaidi nime.

Nüüd ei saa te veel valida saidi vaikimisi võrgukanalit ja keelt. Te saate neid atribuute siiski konfigureerida pärast saidi kopeerimistoimingu lõpetamist. Kui valite saidi saidi loendilehel **saidikonstruktoris**, **ilmub** teie saidi häälestusdialoog, kus saate valida vaikekanali ja -keele.

Lisateavet saidi kopeerimise toimingu kohta vt teemast E-ärisaidi [kopeerimine](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Olemasoleva saidikanali haldamine

Kui sait on kanaliga konfigureeritud, **\>** saate hallata ja värskendada valitud saidi kanalit saidi sätete kanalites saidikonstruktori kaudu, nagu näha järgmises näite näites.

![Kanali vastendamise haldamine saidikonstruktoris.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Mitme saidi tugi ühe rentniku puhul

Paljud kaubamärgiga saidid võivad ühe rentniku puhul koos eksisteerida. Järgmises näites on näha kolm erinevat kaubamärgiga sasaiti (Adventure Works, Adventure Works Business ja Fabrikam), millest igaüks on vastendatud erineva võrgukanaliga.

![Saidiloend saidikonstruktoris.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Ühe domeeninime konfigureerimine mitme saidi teede abil

Mitme saidi puhul saab kasutada ühte domeeninime ning seejärel saab teid kasutada eraldi saitide või keelte jaoks. Domeen on konfigureeritud `www.mycompany.com` näiteks kahele erinevale e-kaubanduse saidile: üks Fabrikamile ja teine Adventure Worksi jaoks. Sel juhul saab Vaiketee (`www.mycompany.com`) ehk tühi tee- kasutada Fabrikami saidi jaoks ja teist teed (`www.mycompany.com/adventureworks` nt) saab kasutada Adventure Worksi saidi jaoks. Teise võimalusena kasutatakse kohandatud teed (nt `www.mycompany.com/fabrikam`) ka Fabrikami saidi vaiketee asemel.

Teise võimalusena saab iga saidi (nt ja ) puhul kasutada erinevat domeeninime`www.adventure-works.com``www.fabrikam.com`. Seejärel saab teid kasutada eri keeltes või regioonides (nt `www.adventure-works.com/fr-ca` Kanada prantsuse).

## <a name="configure-multiple-languages-on-a-site"></a>Mitme keele konfigureerimine saidil

E-äri saidi jaoks saab keeli konfigureerida saidikonstruktoris saidi sätete **kanalites \>**. Järgmises näite näites on iga keel konfigureeritud tee lokaadi abil, nii et igal keelel on kordumatu URL.

![Mitu saiti konfigureeritud keelt.](media/channel-mapping-10.png)

Uue kanali keele lisamiseks minge saidisätete kanalisse **\> ja** valige kanali link. Parempoolsel paanil valige lisa **lokaadi** lisamine, et valida kanal ja lokaadi, mille soovite lisada. Seejärel määrake tee, mida valitud kanali puhul kasutada.

### <a name="add-and-configure-the-site-picker-module"></a>Saidi valijamooduli lisamine ja konfigureerimine

Pärast mitme keele ja kanaliga saidi konfigureerimist võite soovida lisada keelevalija saidi lehekülje päisele, nii et kasutajad saavad käsitsi valida oma keele või riigi. Moodulteegi [päisemoodulil](author-header-module.md) on sisseehitatud tugi kasutajatele keele valimiseks saidi valija [mooduli abil](site-selector.md). Saidivalija mooduli saab päise killus päisemoodulisse lisada.

Lisateavet selle kohta, kuidas lisada ja konfigureerida saidi valija moodulit, vt saidi [valija moodulit](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Juuruta lehekülje variandid iga keele jaoks

Selles stsenaariumis on ainult üks kanal, kuid keeli on mitu. Valitud keele põhjal saate muuta lehekülje ilmet, luues selle jaoks lehekülje variandi. Seejärel saate varianti lisada lokaliseeritud sisu.

Kui olete saidikonstruktoris avanud lehekülje ja valite lingi ülemises parempoolses lingis, mis näitab praegust kanalit ja keelt, kuvatakse kanali ja keele valija, nagu näha järgmises näite näites. Kui soovite praeguse keele lehe alistada, valige teine lokaadiks ja seejärel valige **muuda**. Kui haldate saiti, kus on mitu kanalit [ja keelt, saate kanalit ka muuta](#manage-site-content-that has-multiple-channels-and-languages).

![Lehe keele muutmine saidikonstruktoris.](media/channel-mapping-14.png)

Kui valitud lehe või killusta varianti pole veel loodud, saate hoiatusteate, nagu näha järgmises näite näites. Sellisel juhul valige teate tekstis **link** Loo lehe variant. Kuvatavas dialoogiboksis on valikud, mis lasevad teil alustada olemasoleva variandi koopiaga või luua mallist uue kaubamärgiga lehe.

![Küsi saidikonstruktoris lehevariandi loomiseks](media/channel-mapping-16.png)

Kui te varianti ei loo, renderdatakse algleht ja kuvatakse Commerce Headquartersi moodulistringide ja tooteteabe jaoks sobiv keel. Kui aga tekst, nt lehe pealkiri või muu turundussisu on määratud otse vaikelehe moodulites, jäävad selle teksti stringid algses keeles.

Iga lehekülje ja killusta käsitsi loomise asemel saate eksportida iga lehekülje ja killusta XML-lokaliseerimise vahetuse failivormingu (XLIFF) faili, mida saab seejärel saata lokaliseerimiseks. Pärast iga XLIFF-i lokaliseerimist saab selle importida lokaliseeritud lehekülje variandina. XLIFF-faili eksportimiseks leheküljelt või killusta saidikonstruktoris või XLIFF-faili importimiseks lehele või killu, valige **käsuribal** lokaliseerimine. Seejärel valige ekspordi **XLIFF või** **Impordi XLIFF**, nagu näha järgmises näite näites.

![Lehe või killu importimine või eksportimine XLIFF-vormingus.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Mitme kanali ja keelega saidisisu haldamine

Mitme kanali ja/või keelega sait talletab iga lehekülje kordumatu variandi ja killust iga kanali ja keele kombinatsiooni jaoks. Selline käitumine võimaldab lehevariantidel sisaldada lokaliseeritud andmeid, kuid võimaldab teil ka paindlikkust muuta konkreetse variandi lehe ilmet ja tunde.

Teavet selle kohta, kuidas lehe variantidega töötada, vt [selle artikli iga keelejao](#implement-page-variants-for-each-language) lehekülje variantide juurutamine.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Konfigureerige e-äri saidil mitu kanalit

Saate lisada kanaleid e-äri saidile saidikonstruktoris, kui valite **saidisätete \> kanalid** ja **valides suvandi Lisa kanal**. Seejärel saate kuvatavas **kanali dialoogiboksis** valida võrgukanali ja vaikeasukanali.

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Võrgukanali häälestamine](channel-setup-online.md)

[Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Saate häälestada geotuvastust ja ümbersuunamist](geo-detection-redirection.md)

[Kanaliülese ühiskasutuse lubamine ja kasutamine](cross-channel-sharing.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[E-kaubanduse saidi kopeerimine](copy-ecommerce-site.md)

[Saidi valija moodul](site-selector.md)
