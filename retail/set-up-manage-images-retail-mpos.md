---
title: Retail Modern POS-i jaoks piltide seadistamine ja haldamine
description: "See artikkel selgitab toiminguid, mis on seotud mitmesuguste Retail Modern POS-is (MPOS)kuvatavate üksuste piltide seadistamise ja haldamisega."
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 3985d731709eff4085927b277996528e4e448ba9
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017



---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Retail Modern POS-i jaoks piltide seadistamine ja haldamine

[!include[banner](includes/banner.md)]


See artikkel selgitab toiminguid, mis on seotud mitmesuguste Retail Modern POS-is (MPOS)kuvatavate üksuste piltide seadistamise ja haldamisega.

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Meedia baas-URL-i seadistamine ja meediamallide määratlemine pildi URL-ide vormingu konfigureerimiseks
-------------------------------------------------------------------------------------------------

Retail Modern POS-is (MPOS) kuvatavad pildid peavad olema majutatud väliselt, rakendusest Microsoft Dynamics 365 for Retail väljapoole. Tavaliselt majutatakse neid sisuhaldussüsteemis, sisu edastamise võrgus (CDN) või meediserveris. MPOS toob pildid sobivate üksuste (nagu tooted ja kataloogid) juurde ning kuvab need, kasutades sihtkoha URL-i. Väliselt majutatavate piltide toomiseks nõuab MPOS piltide õiget URL-i vormingut. Saate konfigureerida piltidele nõutava URL-i vormingu, seadistades kanali profiilis väärtuse **Meedia baas-URL** ja kasutades iga üksuse puhul funktsiooni **Meediamalli määratlemine**. Samuti saate alistada standardse URL-i vormingu üksuste alamkogumi jaoks, kasutades funktsiooni **Excelis redigeerimine**. **Oluline märkus.** Praeguses rakenduse Dynamics 365 for Retail versioonis ei saate seadistada URL-vormingut, kasutades MPOS-i XML-atribuuti **Pilt** üksuste atribuudigrupis **Vaikimisi**. Kui olete tuttav rakendusega Microsoft Dynamics AX 2012 R3 ja kasutate nüüd rakenduse Dynamics 365 for Retail praegust versiooni, veenduge, et kasutate piltide seadistamiseks alati uut funktsiooni **Meediamallide määratlemine**. Ärge kasutage ega muutke ühegi üksuse (sh tootede) puhul atribuuti **Pilt** atribuudigrupis **Vaikimisi**. Otse atribuudigrupis **Vaikimisi** piltidele tehtud muudatusi ei kajastata. See suvand keelatakse tulevases väljaandes. Järgmistes protseduurides seadistatakse näitena pildid kataloogiüksuse jaoks. Need protseduurid aitavad tagada, et vaikimisi seadistatakse ühist teed kasutavatele kataloogi piltidele õige pildi sihtkoha tee. Näiteks kui olete seadistanud meediaserveri või CDN-i väliselt ja soovite MPOS-is pilte kuvada konkreetse poe jaoks, aitab funktsioon **Meediamalli määratlemine** määrata tee, mille puhul saab MPOS pilte otsida ja neid tuua. **Märkus.** Antud demonandmete näites juurutatakse meediaserver jaemüügiserveris. Samas võib see teil olla igal pool väljaspool rakendust Dynamics 365 for Retail.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Meedia baas-URL.i seadistamine kanalile

1.  Avage Dynamics 365 for Retaili HQ portaal.
2.  Klõpsake nuppe **Jaemüük** &gt; **Kanali seadistus** &gt; **Kanali profiilid**. [![channel-profile1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  Värskendage kanali profiilis, mida teie kauplus MPOS-ide jaoks kasutab, välja **Meedia baas-URL** oma meediaserveri või CDN-i baas-URL-iga. Baas-URL on esimene URL-i osa, mida jagavad kõik erinevate üksuste pildikaustad.[![channel-profile2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Üksusele meediamalli määratlemine

1.  Klõpsake nuppe **Jaemüük** &gt; **Kataloogi haldus** &gt; **Kataloogi pildid**.
2.  Klõpsake lehe **Kataloogi pildid** tegevuspaanil suvandit **Meediamalli määratlemine**. Dialoogikasti **Meediamalli määratlemine** väljal **Üksus** peab vaikevalikuks olema **Kataloog**.
3.  Sisestage kiirkaardile **Meediumitee** pildi asukoha ülejäänud tee. Meediumitee toetab muutujana atribuuti **LanguageID**. Näiteks demoandmete puhul saate luua kausta **Kataloogid** kõikidele kataloogi piltidele, mis on teie meediaserveri meedia baas-URL-i all (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Siis saate luua kausta igale keelele, nagu en-US või fr-FR, ja kopeerida sobivad pildid iga kausta alla. Kui teil ei ole eri keelte jaoks erinevaid pilte, saate muutuja **LanguageID** oma kaustastruktuurist välja jätta ja osutada otse kaustale Kataloogid, mis sisaldab kataloogi pilte. **Märkus.** Praegune Dynamics 365 for Retaili versioon toetab luba **{LanguageId}** üksuste Kataloog, Toode ja Kategooria puhul. (Luba **{LanguageID}** ei toetata üksuste Klient ja Töötaja puhul vastavalt olemasolevale standardile, mis on kehtinud alates versioonist Microsoft Dynamics AX 6.x.)
4.  Piltide puhul on failinime vorming kataloogi nimele püsiprogrammeeritud ja seda ei saa muuta. Seega muutke piltide nime nii, et neild oleks sobivad katalooginimed. See aitab tagada, et MPOS käsitleb neid õigesti.
5.  Valige väljal **Faililaiend** eeldatav faili nimelaiend olenevalt olemasolevatest pilditüüpidest. Näiteks demoandmete puhul on kataloogipildid laiendiga .jpg. (Ka pildifailid nimetatakse ümbe nii, et neil oleks kataloogi nimed.)
6.  Klõpsake **OK**.
7.  Kinnitamaks, et piltide meediamall on õigesti salvestatud, klõpsake lehel **Kataloogi pildid** uuesti suvandit **Meediamalli määratlemine**. Malli kinnitamiseks ilma dialoogikasti **Meediamalli määratlemine** sulgemata kasutage kiirkaarti **Pildi URL-ide loomine Exceli jaoks**. Kontrollige pildi-URL-i välimust ja kinnitage, et URL on kooskõlas varem mainitud malli standardiga. Dialoogikast **Meediamalli määratlemine** on nüüd määranud pilditee vaikimisi kõikidele kataloogi piltidele, mis kasutavad seda ühist URL-i teed. See URL-i tee khtib kõikidele kataloogi piltidele, kui need ei ole üle kirjutatud. Pilditee esimene osa on võetud meedia baas-URL-ist, mille määratlesite kanali profiilis. Ülejäänud osa teest on võetud teest, mille määratlesite meediamallis. Kaks osa on koondatud, et pakkuda pildi asukoha täielikku URL-i. Näiteks demoandmetes oleva kataloogi nimi on Fabrikam Base Catalog. Seega peab pildi nimi olema Fabrikam Base Catalog.jpg, et see kasutab kataloogi nime ja failinime laiendit .jpg, mis on mallis konfigureeritud. Antud juhul on URL pärast koondamist https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg.
8.  Käitage sünkroonimistöid, et lükata uus mall kanali andmebaasi, nii et MPOS saab kasutada malli piltidele juurdepääsuks.
9.  Kanali poolel kataloogipiltide jaoks meediamalli värskendamiseks veenduge, et käivitate funktsiooni **Kataloogi töö 1150** valikust **Jaemüügi IT** &gt; **Jaotusgraafik**.[![catalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Pildi eelvaatamine üksuse tasemelt
1.  HQ üksuse lehelt saate eelvaadata pilti, mis kasutab pildi URL-i, mis on tuletatud meediamallist. Selle näite puhul avage sobiv kataloog ja klõpsake siis tegevuspaanil suvandeid **Meedia** &gt; **Pildid**. Kasutage ripploendit, et valida erinevaid kauplusi, millel võivad olla erinevad kanali profiilid.
2.  Varjatud meediamalli redigeerimiseks või eemaldamiseks peate naasema dialoogikasti **Meediamalli määratlemine** lehele **Kataloogi pildid**.
3.  Kasutage nuppe **Lisa** ja **Eemalda**, et muuta käsitsi teed, mis põhineb varjatud mallil ja mida kasutatakse kindla pildi jaoks. Lisateabe saamiseks vaadake käesoleva artikli jaotist „Meediumi malli üksuse kaupade ülekirjutamine”.
4.  Pärast pildi eelvaatuse lõpetamist ja nõutavate muudatuste tegemist käivitage sobiva kaupluse MPOS-i eksemplar ja vaadake, kas kataloogi pildid kuvatakse.[![catalog4](./media/catalog4.png)](./media/catalog4.png)

**Märkus.** Saate kasutada sama protseduuri kõigi viie üksuse puhul, mida toetatakse: Töötaja, Klient, Kataloog, Kategooria ja Tooted. Kataloogi tooted (kataloogi tasemel määratud tooted) ja Kanali tooted (kanali tasemel määratud tooted) kasutavad meediamalli, mis on määratud üksusele Tooted. Meediamalli Tooted puhul saate valida toote kohta kuvatavate toote piltide arvu. Samuti saate määrata antud tootele vaikepildi. Sel moel saate vätida MPOS-is tühje pilte ja aitate juhtida, milliseid pilte kasutatakse toote puhul vaikepildina. Järgmises näites on igal tootel viis pilti ja esimene pilt on määratud vaikepildiks. Tootevariante koheldakse põhitoodetega samamoodi. Pildifaili failinimi peab põhinema tootekoodil. Mõned tähemärgid varjestatakse failinime loomisel. Seetõttu tasub failinimi kinnitada, kasutades jaotist **Pildi URL-ide loomine Exceli jaoks**. [![prods](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Sünkroonimistööd meediamalli saatmiseks kanali poolele
Veenduge kõigi viie toetatud üksuse (Töötaja, Klient, Kataloog, Kategooria ja Tooted) puhul pildi seadistamiseks dialoogi **Meediamallide määratlemine** värskendamisel, et käitate kataloogitööd (1150) asukohast **Jaemüügi IT** &gt; **Jaotusgraafik**. See töö võimaldab värskendatud meediamalli kanaliga sünkroonimist ja lubab MPOS-il seda kasutada. Käivitage kataloogitöö (1150) pärast mõne järgmise muudatuse tegemist.

-   Värskendate meediamalli Kataloogi pilt asukohast **Kataloogi pildid** &gt; **Meediamallide määratlemine**.
-   Värskendate meediamalli Töövõtja pilt asukohast **Töövõtja pildid** &gt; **Meediamallide määratlemine**.
-   Värskendate meediamalli Kliendi pilt asukohast **Kliendi pilt** &gt; **Meediamallide määratlemine**.
-   Värskendate meediamalli Toote pilt asukohast **Toote pildid** &gt; **Meediamallide määratlemine**.
-   Värskendate meediamalli Kategooria pilt asukohast **Kategooria pildid** &gt; **Meediamallide määratlemine**. Peate avaldama ka kanali.

## <a name="overwriting-the-media-template-for-entity-items"></a>Üksuste meediamalli ülekirjutamine
Nagu te eelmises jaotises teada saite, toetab antud üksuse meediamall ainult ühte ühist teed. See tee põhineb konfigureeritud meedia baas-URL-il ja määratletud meediumiteel. Kuid paljudel juhtudel soovib jaemüüja üksuse kaupade alamkogu puhul kasutada pilte erinevatest allikatest. Näiteks kasutab kauplus kataloogi piltide ühe kogumi puhul ise hostitud meediaserverit, kuid muu kogumi puhul CDN-i URL-e. Üksuse tasemel üksuse piltide meediamallil põhinevate pildi URL-ide ülekirjutamiseks kasutage funktsioone Excelis redigeerimine ja Käsitsi redigeerimine lehel **Eelvaade**.

### <a name="overwrite-by-using-edit-in-excel"></a>Ülekirjutamine funktsiooniga Excelis redigeerimine

1.  Klõpsake nuppe **Jaemüük** &gt; **Kataloogi haldus** &gt; **Kataloogi pildid**.
2.  Klõpsake lehel **Kataloogi pildid** suvandit **Meediamalli määratlemine**. Dialoogikasti **Meediamalli määratlemine** väljal **Üksus** peab valitud olema **Kataloog**.
3.  Vaadake kiirkaardil **Meediumitee** pildi asukohta.
4.  Klõpsake kiirkaardil **Pildi URL-ide loomine Exceli jaoks** suvandit **Loo**. **Oluline.** Alati kui meediamalli muudetakse, peate klõpsama suvandit **Loo**, enne kui saate kasutada funktsiooni Excelis redigeerimine. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) Näete nüüd eelvaadet pildi URL-idest, mis loodi viimase salvestatud meediamalli alusel. [![excel2](./media/excel2.png)](./media/excel2.png) **Märkus** Excelile loodud URL-id kasutavad määratletud meediamallide teed ja tavasid. Tavad hõlmavad tavasid failinimede osas. Eeldus on, et olete seadistanud füüsilised pildid väljaspool Dynamics 365 for Retaili ja pilte saab tuua URL-idest, mis on tuletatud varem määratletud meediamallist. Saate need tuletatud URL-id üle kirjutada, kasutades funktsiooni Excelis redigeerimine.
5.  Klõpsake funktsiooni **Excelis redigeerimine**.
6.  Pärast Microsoft Exceli töölehe avamist klõpsake viiba avanemisel suvandit **Luba redigeerimine**.
7.  Kui küsitakse, klõpsake parempoolsel paanil suvandit **Usalda seda lisandmoodulit** ja oodake, et lisandmoodul installimise lõpetaks. [![Usalda seda lisandmoodulit](./media/excel4.jpg)](./media/excel4.jpg)
8.  Kui teil palutakse sisse logida, sisestage mandaadid, mida kasutasite HQ-sse sisselogimiseks. [![Sisselogimise viip](./media/excel5.png)](./media/excel5.png)
9.  Pärast sisselogimist peaksite nägema erinevate kataloogiüksuste pildi-URL-ide loendit.
10. Redigeerite, lisate ja eemaldate erinevate üksuste kaupade pildi-URL-e.
11. Kõikide üksuste puhul (v.a Tooted) saate pildi-URL-id üle kirjutada. Muutke olemasolevat pildi-URL-i nii, et see kasutab pildi uut sihtkoha URL-i, ja värskendage pildifaili failinime. Faili nimi peab olema kordumatu, mis tagab, et kirje on kordumatu. [![Pildi-URL-ide ülekirjutamine Excelis](./media/excel6.jpg)](./media/excel6.jpg) **Märkus.** Kui kirjutate üle üksuste Tooted pildi-URL-id, kasutades funktsiooni Excelis redigeerimine või üksuse kauba lehel, näitab MPOS alati kõiki meediamalli pildi-URL-e koos ülekirjutatud pildi-URL-idega.
12. Kui olete muudatuste tegemise lõpetanud, klõpsake suvandit **Avalda Excelis**, et luua uus selgesõnaline seosekirje.
13. Naaske HQ-sse ja klõpsake nuppu **OK**.
14. Käitage üksuse puhul sobivaid sünkroonimistöid ja kontollige eelvaadet üksuse lehel või MPOS-is.

#### <a name="creating-new-records"></a>Uute kirjete loomine

Saate luua uusi kirjeid Excelis. Kuid veenduge, et lisatud teave on õige. Näiteks kataloogile uue kirje loomiseks veenduge, et kataloogi ID ja kataloogi nimi on õiged, samuti peate lisama kordumatu failinime. Kordumatu failinimi on väga oluline, sest Exceli kirjete kordumatust kontrollitakse avaldamisel. Esmalt kopeerige üksikasjad kataloogist, millele soovite uut kirjet luua, ja kopeerige kirje. Peate värskendama vaid failinime ja URL-i, sest ülejäänud teave jääb samaks. Üksuse Toode kaupadele uute kirjete loomiseks kasutage sama põhiprotseduuri. Kopeerige Exceli töölehelt olemasolev kirje tootele, millele soovite uut kirjet luua, ja asendage seejärel pildi URL ja failinimi. Veenduge, et failinimi on kordumatu.

#### <a name="deleting-an-existing-record"></a>Olemasoleva kirje kustutamine

Kustutada saab ainult ülekirjutatud pildi URL-i kirjeid. Pärast pildi kustutamist ja sünkroonimise lõppemist ei kuvata pilti enam lehel **Eelvaade** või MPOS-is. Pildi-URL-i kirjeid, mis on tuletatud meediamallist ei saa kustutada, sest need kirjed on alati tuletatud meediamallist.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Üksuse tasemel lehelt Eelvaade ülekirjutamine

Kõikide üsksute puhul, v.a Tooted, saate pildi-URL-i antud üksuse kauba jaoks üle kirjutada üksuse kauba tasemel lehelt **Eelvaade**. Üksuse Tooted puhul saate kasutada üksuse lehte Kataloogitooted. See näide näitab, kuidas kataloogi pilti üle kirjutada.

1.  Klõpsake valikuid **Kataloogid** &gt; **Meedia** &gt; **Pildid** ja valige värskendamiseks kataloogipilt.
2.  Klõpsake suvandit **Lisa** ja sisestage pildi-URL, et meediamalli URL üle kirjutada.
3.  Kui soovite, et see pilt kuvataks kataloogi MPOS-is, määrake see vaikepildiks.
4.  Klõpsake nupul **OK**. Pildi-URL-i värskendatakse selle kataloogi pildi jaoks ja kuvatakse eelvaade. [![preview3](./media/preview3.png)](./media/preview3.png)
5.  Näete kõkide ülekirjutatud pildi-URL-ide pildi eelvaadet ka galerii lehel **Kataloogi pildid**.

**[![preview-4](./media/preview-4.png)](./media/preview-4.png)Märkus.** Praegu ei näita galerii pildi eelvaateid meediamalli pildi-URL-idele. Üksuste Kataloog, Töötaja, Klient ja Kategooria puhul, kui kasutaja lisab selgesõnaliselt URL-i selle lehe kaudu, soovitame teil viidata, milline on vaikepilt, sest jaemüügiserveri kliendid näitavad ainult ühte pilti üksuse Kataloog, Klient, Töötaja ja Kategooria kohta. Kui kasutaja ei määra vaikepilti, määrab süsteem vaikepildi ja saadab selle jaemüügiteenuse kutsujale (MPOS või Ecommerce).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Kataloogitoote piltide pildi-URL-i ülekirjutamine lehel Eelvaade

Kataloogitoote piltide pildi-URL-ide ülekirjutamiseks peate kasutama lehte **Eelvaade**. Te ei saa kasutada funktsiooni Excelis redigeerimine.

1.  Toote piltide ülekirjutamiseks kataloogi tasemel valige kataloog ja valige siis toode, mille pilti soovite üle kirjutada.
2.  Klõpsake suvandit **Atribuudid**.
3.  Valige järgmisel lehel suvand **Pilt** ja klõpsake seejärel suvandit **Redigeeri**. Leht **Eelvaade** avaneb liugurdialoogikastina.
4.  Klõpsake suvandit **Lisa** ja kirjutage pildi-URL uue URL-iga üle.
5.  Klõpsake nupul **OK**. Näete nüüd uue pildi eelvaadet ja saate määrata selle vaikepildiks.

**[![cat3](./media/cat3.png)](./media/cat3.png)Märkus.** Pärast kategooria pildi seost peate avaldama kanali ja käitama kanali töö tagamaks, et muudatused avaldatakse kanali andmebaasis.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Piltide seadistamine MPOS-i võrguühenduseta režiimis kuvamiseks
MPOS-i saab käitada võrgurežiimis (kui MPOS on ühendatud jaemüügiserveriga) või võrguühenduseta režiimis (kui ei ole jaemüügiserverit või võrguühendust ja kanded talletatakse kohalikus võrguühenduseta andmebaasis). Kui MPOS-i käitatakse võrguühenduseta režiimis, ei saa see pilte välisest pildiserverist jaemüügiserverist kuvamiseks, sest jaemüügiserveri ühendus on katkestatud. Kuid saate endiselt seadistada pilte, nii et need kuvatakse, kui MPOS-i käitatakse võrguühenduseta režiimis.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Tootepiltide seadistamine MPOS-i võrguühenduseta režiimis kuvamiseks

Tootepilte, mida peab kasutama võrguühenduseta režiimis, saab seadistada, laadides nõutava füüsilise pildi üles tootepildi baasi.

1.  Klõpsake valikuid **Tooteteabe haldus** &gt; **Tooted** &gt; **Tooted**.
2.  Valige toode, millele soovite võrguühenduseta pildi määrata.
3.  Klõpsake suvandit **Redigeeri** ja klõpsake siis paremas nurgas olevat noolt parempoolse paani kuvamiseks.
4.  Klõpsake kiirkaardil **Toote pilt** suvandit **Muuda pilti** ja laadige füüsiline pilt, mida soovite kasutada võrguühenduseta režiimis valitud toote puhul.
5.  Salvestage ja sulgege leht.
6.  Kui MPOS on võrgurežiimis, käitage HQ-s funktsiooni Kataloogitöö tagamaks, et andmed saadetakse vähemalt ühe korra võrguühenduseta andmebaasi.
7.  Pange MPOS võrguühenduseta režiimi. Peaksite nägema pilti, mille HQ-s kindlale tootele üles laadisite. [![offline1](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Kataloogi, kategooria, töötaja ja kliendi piltide seadistamine MPOS-i võrguühenduseta režiimis kuvamiseks

Kataloogi, kategooria, töötaja ja kliendi pildid, mida on vaja kasutada võrguhenduseta režiimis, saab seadistada, lisades galeriisse nõutava pildi sihtkoha lingi ja määrates pildi valitud üksuse vaikepildiks.

1.  Avage kataloog ja klõpsake siis tegevuspaanil nuppe **Meedia** &gt; **Pildid**.
2.  Järgige jaotises **Üksuse tasemel lehelt Eelvaade ülekirjutamine** toodud juhiseid, et lisada väline pildi-URL.
3.  Märkige see pilt kataloogi vaikepildiks, valides märkeruudu Pilt on ruudustikud loetletud.
4.  Käitage kataloogitööd. Seda pilti kasutatakse nüüd MPOS-is kataloogi võrguühenduseta pildina.
5.  Järgige muude üksuste (nt Kategooria, Töötaja ja Klient) puhul sama protsessi.

[![offline2](./media/offline2.png)](./media/offline2.png)    




