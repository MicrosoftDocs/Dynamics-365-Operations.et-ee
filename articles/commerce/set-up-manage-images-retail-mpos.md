---
title: Piltide seadistamine ja haldamine Modern POS-i (MPOS) jaoks
description: See artikkel selgitab toiminguid, mis on seotud mitmesuguste Modern POS-is (MPOS) kuvatavate üksuste piltide seadistamise ja haldamisega.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelProfile, RetailMediaGallery, RetailImages,
audience: Application User
ms.reviewer: josaw
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 31f325d2614d0a01192a0157ee0e89514bc51caa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985757"
---
# <a name="set-up-and-manage-images-for-modern-pos-mpos"></a>Piltide seadistamine ja haldamine Modern POS-i (MPOS) jaoks

[!include [banner](includes/banner.md)]

See artikkel selgitab toiminguid, mis on seotud mitmesuguste Modern POS-is (MPOS) kuvatavate üksuste piltide seadistamise ja haldamisega.

## <a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Meedia baas-URL-i seadistamine ja meediamallide määratlemine pildi URL-ide vormingu konfigureerimiseks

Modern POS-is (MPOS) kuvatavaid pilte tuleb majutada väliselt, st väljaspool rakendust Commerce. Tavaliselt majutatakse neid sisuhaldussüsteemis, sisu edastamise võrgus (CDN) või meediserveris. MPOS toob pildid sobivate üksuste (nagu tooted ja kataloogid) juurde ning kuvab need, kasutades sihtkoha URL-i. Väliselt majutatavate piltide toomiseks nõuab MPOS piltide õiget URL-i vormingut. Saate konfigureerida piltidele nõutava URL-i vormingu, seadistades kanali profiilis väärtuse **Meedia baas-URL** ja kasutades iga üksuse puhul funktsiooni **Meediamalli määratlemine**. Samuti saate alistada standardse URL-i vormingu üksuste alamkogumi jaoks, kasutades funktsiooni **Excelis redigeerimine**.

> [!IMPORTANT]
> Praeguses rakenduse Commerce versioonis ei saa te enam seadistada URL-i vormingut, kasutades MPOS-i XML-atribuuti **Pilt** üksuste atribuudigrupis **Vaikimisi**. Kui olete tuttav Microsoft Dynamics AX 2012 R3-ga ja kasutate praegust Commerce’i versiooni, siis veenduge, et kasutaksite piltide seadistamisel uut funktsiooni **Meediamalli määratlemine**. Ärge kasutage ega muutke ühegi üksuse (sh tootede) puhul atribuuti **Pilt** atribuudigrupis **Vaikimisi**. Otse atribuudigrupis **Vaikimisi** piltidele tehtud muudatusi ei kajastata. See suvand keelatakse tulevases väljaandes.

Järgmistes protseduurides seadistatakse näitena pildid kataloogiüksuse jaoks. Need protseduurid aitavad tagada, et vaikimisi seadistatakse ühist teed kasutavatele kataloogi piltidele õige pildi sihtkoha tee. Näiteks kui olete seadistanud meediaserveri või CDN-i väliselt ja soovite MPOS-is pilte kuvada konkreetse poe jaoks, aitab funktsioon **Meediamalli määratlemine** määrata tee, mille puhul saab MPOS pilte otsida ja neid tuua.

> [!NOTE]
> Antud demonandmete näites juurutatakse meediaserver Commerce’i skaala üksuses. Kuid see võib olla ükskõik kus väljaspool Commerce’i.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Meedia baas-URL.i seadistamine kanalile

1. Avage Commerce HQ portaal.
2. Klõpsake suvandeid **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kanali profiilid**.

    [![Navigeerimine](./media/channel-profile1.png)](./media/channel-profile1.png)

3. Värskendage kanali profiilis, mida teie kauplus MPOS-ide jaoks kasutab, välja **Meedia baas-URL** oma meediaserveri või CDN-i baas-URL-iga. Baas-URL on URL-i esimene osa, mida ühiskasutavad kõik erinevate üksuste pildikaustad.

    [![Kanali profiilide leht](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Üksusele meediamalli määratlemine

1. Klõpsake suvandeid **Jaemüük ja kaubandus** &gt; **Kataloogi haldus** &gt; **Kataloogi pildid**.
2. Klõpsake lehe **Kataloogi pildid** tegevuspaanil suvandit **Meediamalli määratlemine**. Dialoogikasti **Meediamalli määratlemine** väljal **Üksus** peab vaikevalikuks olema **Kataloog**.
3. Sisestage kiirkaardile **Meediumitee** pildi asukoha ülejäänud tee. Meediumitee toetab muutujana atribuuti **LanguageID**. bNäiteks demoandmete puhul saate luua kausta **Kataloogid** kõikidele kataloogi piltidele, mis on teie meediaserveri meedia baas-URL-i all (`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`). Siis saate luua kausta igale keelele, nagu en-US või fr-FR, ja kopeerida sobivad pildid iga kausta alla. Kui teil ei ole eri keelte jaoks erinevaid pilte, saate muutuja **LanguageID** oma kaustastruktuurist välja jätta ja osutada otse kaustale Kataloogid, mis sisaldab kataloogi pilte.

    > [!NOTE]
    > Praegune Commerce’i versioon toetab **{LanguageId}** luba üksuste Kataloog, Toode ja Kategooria puhul. (Luba **{LanguageID}** ei toetata üksuste Klient ja Töötaja puhul vastavalt olemasolevale standardile, mis on kehtinud alates versioonist Microsoft Dynamics AX 6.x.)

4. Piltide puhul on failinime vorming kataloogi nimele püsiprogrammeeritud ja seda ei saa muuta. Seega muutke piltide nime nii, et neild oleks sobivad katalooginimed. See aitab tagada, et MPOS käsitleb neid õigesti.
5. Valige väljal **Faililaiend** eeldatav faili nimelaiend olenevalt olemasolevatest pilditüüpidest. Näiteks demoandmete puhul on kataloogipildid laiendiga .jpg. (Ka pildifailid nimetatakse ümbe nii, et neil oleks kataloogi nimed.)
6. Klõpsake **OK**.
7. Kinnitamaks, et piltide meediamall on õigesti salvestatud, klõpsake lehel **Kataloogi pildid** uuesti suvandit **Meediamalli määratlemine**. Malli kinnitamiseks ilma dialoogikasti **Meediamalli määratlemine** sulgemata kasutage kiirkaarti **Pildi URL-ide loomine Exceli jaoks**. Kontrollige pildi-URL-i välimust ja kinnitage, et URL on kooskõlas varem mainitud malli standardiga. Dialoogikast **Meediamalli määratlemine** on nüüd määranud pilditee vaikimisi kõikidele kataloogi piltidele, mis kasutavad seda ühist URL-i teed. See URL-i tee khtib kõikidele kataloogi piltidele, kui need ei ole üle kirjutatud. Pilditee esimene osa on võetud meedia baas-URL-ist, mille määratlesite kanali profiilis. Ülejäänud osa teest on võetud teest, mille määratlesite meediamallis. Kaks osa on koondatud, et pakkuda pildi asukoha täielikku URL-i. Näiteks demoandmetes oleva kataloogi nimi on Fabrikam Base Catalog. Seega peab pildi nimi olema Fabrikam Base Catalog.jpg, et see kasutab kataloogi nime ja failinime laiendit .jpg, mis on mallis konfigureeritud. Sel juhul on URL pärast liitmist `https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`.
8. Käitage sünkroonimistöid, et lükata uus mall kanali andmebaasi, nii et MPOS saab kasutada malli piltidele juurdepääsuks.
9. Kataloogi piltide meediamalli värskendamiseks kanali poolel käivitage kindlasti funktsioon **Kataloogi töö 1150** asukohas **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafik**.

    [![Meediamalli määratlemise dialoogiboks](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Pildi eelvaatamine üksuse tasemelt

1. HQ üksuse lehelt saate eelvaadata pilti, mis kasutab pildi URL-i, mis on tuletatud meediamallist. Selle näite puhul avage sobiv kataloog ja klõpsake siis tegevuspaanil suvandeid **Meedia** &gt; **Pildid**. Kasutage ripploendit, et valida erinevaid kauplusi, millel võivad olla erinevad kanali profiilid.
2. Varjatud meediamalli redigeerimiseks või eemaldamiseks peate naasema dialoogikasti **Meediamalli määratlemine** lehele **Kataloogi pildid**.
3. Kasutage nuppe **Lisa** ja **Eemalda**, et muuta käsitsi teed, mis põhineb varjatud mallil ja mida kasutatakse kindla pildi jaoks. Lisateabe saamiseks vaadake käesoleva artikli jaotist [Meediumi malli üksuse kaupade ülekirjutamine](#overwriting-the-media-template-for-entity-items).
4. Pärast pildi eelvaatuse lõpetamist ja nõutavate muudatuste tegemist käivitage sobiva kaupluse MPOS-i eksemplar ja vaadake, kas kataloogi pildid kuvatakse.

    [![Piltide dialoogiboks](./media/catalog4.png)](./media/catalog4.png)

> [!NOTE]
> Saate kasutada sama protseduuri kõigi viie üksuse puhul, mida toetatakse: Töötaja, Klient, Kataloog, Kategooria ja Tooted. Kataloogi tooted (kataloogi tasemel määratud tooted) ja Kanali tooted (kanali tasemel määratud tooted) kasutavad meediamalli, mis on määratud üksusele Tooted. Meediamalli Tooted puhul saate valida toote kohta kuvatavate toote piltide arvu. Samuti saate määrata antud tootele vaikepildi. Sel moel saate vätida MPOS-is tühje pilte ja aitate juhtida, milliseid pilte kasutatakse toote puhul vaikepildina. Järgmises näites on igal tootel viis pilti ja esimene pilt on määratud vaikepildiks. Tootevariante koheldakse põhitoodetega samamoodi. Pildifaili failinimi peab põhinema tootekoodil. Mõned tähemärgid varjestatakse failinime loomisel. Seetõttu tasub failinimi kinnitada, kasutades jaotist **Pildi URL-ide loomine Exceli jaoks**. Vt selle artikli jaotist [Ülekirjutamine funktsiooniga Excelis redigeerimine](#overwrite-by-using-edit-in-excel).

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Sünkroonimistööd meediamalli saatmiseks kanali poolele

Veenduge kõigi viie toetatud üksuse (Töötaja, Klient, Kataloog, Kategooria ja Tooted) puhul pildi seadistamiseks dialoogi **Meediamallide määratlemine** värskendamisel, et käitate kataloogitööd (1150) asukohast **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafik**. See töö võimaldab värskendatud meediamalli kanaliga sünkroonimist ja lubab MPOS-il seda kasutada. Käivitage kataloogitöö (1150) pärast mõne järgmise muudatuse tegemist.

- Värskendate meediamalli Kataloogi pilt asukohast **Kataloogi pildid** &gt; **Meediamallide määratlemine**.
- Värskendate meediamalli Töövõtja pilt asukohast **Töövõtja pildid** &gt; **Meediamallide määratlemine**.
- Värskendate meediamalli Kliendi pilt asukohast **Kliendi pilt** &gt; **Meediamallide määratlemine**.
- Värskendate meediamalli Toote pilt asukohast **Toote pildid** &gt; **Meediamallide määratlemine**.
- Värskendate meediamalli Kategooria pilt asukohast **Kategooria pildid** &gt; **Meediamallide määratlemine**. Peate avaldama ka kanali.

## <a name="overwriting-the-media-template-for-entity-items"></a>Üksuste meediamalli ülekirjutamine

Nagu te eelmises jaotises teada saite, toetab antud üksuse meediamall ainult ühte ühist teed. See tee põhineb konfigureeritud meedia baas-URL-il ja määratletud meediumiteel. Kuid paljudel juhtudel soovib jaemüüja üksuse kaupade alamkogu puhul kasutada pilte erinevatest allikatest. Näiteks kasutab kauplus kataloogi piltide ühe kogumi puhul ise hostitud meediaserverit, kuid muu kogumi puhul CDN-i URL-e. Üksuse tasemel üksuse piltide meediamallil põhinevate pildi URL-ide ülekirjutamiseks kasutage funktsioone Excelis redigeerimine ja Käsitsi redigeerimine lehel **Eelvaade**.

### <a name="overwrite-by-using-edit-in-excel"></a>Ülekirjutamine funktsiooniga Excelis redigeerimine

1. Klõpsake suvandeid **Jaemüük ja kaubandus** &gt; **Kataloogi haldus** &gt; **Kataloogi pildid**.
2. Klõpsake lehel **Kataloogi pildid** suvandit **Meediamalli määratlemine**. Dialoogikasti **Meediamalli määratlemine** väljal **Üksus** peab valitud olema **Kataloog**.
3. Vaadake kiirkaardil **Meediumitee** pildi asukohta.
4. Klõpsake kiirkaardil **Pildi URL-ide loomine Exceli jaoks** suvandit **Loo**.

    > [!IMPORTANT]
    > Alati kui meediamalli muudetakse, peate klõpsama suvandit **Generate**, enne kui saate kasutada funktsiooni Excelis redigeerimine.

    Näete nüüd eelvaadet pildi URL-idest, mis loodi viimase salvestatud meediamalli alusel.

    [![Pildi URL-ide loomine Exceli kiirkaardi jaoks pärast suvandi Loo valimist.](./media/excel2.png)](./media/excel2.png)

    > [!NOTE]
    > Excelile loodud URL-id kasutavad määratletud meediamallide teed ja tavasid. Tavad hõlmavad tavasid failinimede osas. Eeldus on, et olete seadistanud füüsilised pildid väljaspool Commerce’i ja pilte saab tuua URL-idest, mis on tuletatud varem määratletud meediamallist. Saate need tuletatud URL-id üle kirjutada, kasutades funktsiooni Excelis redigeerimine.

5. Klõpsake funktsiooni **Excelis redigeerimine**.
6. Pärast Microsoft Exceli töölehe avamist klõpsake viiba avanemisel suvandit **Luba redigeerimine**.
7. Kui küsitakse, klõpsake parempoolsel paanil suvandit **Usalda seda lisandmoodulit** ja oodake, et lisandmoodul installimise lõpetaks.

    [![Usalda seda lisandmoodulit](./media/excel4.jpg)](./media/excel4.jpg)

8. Kui teil palutakse sisse logida, sisestage mandaadid, mida kasutasite HQ-sse sisselogimiseks.

    [![Sisselogimise viip](./media/excel5.png)](./media/excel5.png)

9. Pärast sisselogimist peaksite nägema erinevate kataloogiüksuste pildi-URL-ide loendit.
10. Redigeerite, lisate ja eemaldate erinevate üksuste kaupade pildi-URL-e.
11. Kõikide üksuste puhul (v.a Tooted) saate pildi-URL-id üle kirjutada. Muutke olemasolevat pildi-URL-i nii, et see kasutab pildi uut sihtkoha URL-i, ja värskendage pildifaili failinime. Faili nimi peab olema kordumatu, mis tagab, et kirje on kordumatu.

    [![Pildi-URL-ide ülekirjutamine Excelis](./media/excel6.jpg)](./media/excel6.jpg)

    > [!NOTE]
    > Kui kirjutate üle üksuste Tooted pildi-URL-id, kasutades funktsiooni Excelis redigeerimine või tehes seda üksuse kauba lehel, näitab MPOS alati kõiki meediamalli pildi-URL-e koos ülekirjutatud pildi-URL-idega.

12. Kui olete muudatuste tegemise lõpetanud, klõpsake suvandit **Avalda Excelis**, et luua uus selgesõnaline seosekirje.
13. Naaske HQ-sse ja klõpsake nuppu **OK**.
14. Käitage üksuse puhul sobivaid sünkroonimistöid ja kontollige eelvaadet üksuse lehel või MPOS-is.

#### <a name="creating-new-records"></a>Uute kirjete loomine

Saate luua uusi kirjeid Excelis. Kuid veenduge, et lisatud teave on õige. Näiteks kataloogile uue kirje loomiseks veenduge, et kataloogi ID ja kataloogi nimi on õiged, samuti peate lisama kordumatu failinime. Kordumatu failinimi on väga oluline, sest Exceli kirjete kordumatust kontrollitakse avaldamisel. Esmalt kopeerige üksikasjad kataloogist, millele soovite uut kirjet luua, ja kopeerige kirje. Peate värskendama vaid failinime ja URL-i, sest ülejäänud teave jääb samaks. Üksuse Toode kaupadele uute kirjete loomiseks kasutage sama põhiprotseduuri. Kopeerige Exceli töölehelt olemasolev kirje tootele, millele soovite uut kirjet luua, ja asendage seejärel pildi URL ja failinimi. Veenduge, et failinimi on kordumatu.

#### <a name="deleting-an-existing-record"></a>Olemasoleva kirje kustutamine

Kustutada saab ainult ülekirjutatud pildi URL-i kirjeid. Pärast pildi kustutamist ja sünkroonimise lõppemist ei kuvata pilti enam lehel **Eelvaade** või MPOS-is. Pildi-URL-i kirjeid, mis on tuletatud meediamallist ei saa kustutada, sest need kirjed on alati tuletatud meediamallist.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Üksuse tasemel lehelt Eelvaade ülekirjutamine

Kõikide üsksute puhul, v.a Tooted, saate pildi-URL-i antud üksuse kauba jaoks üle kirjutada üksuse kauba tasemel lehelt **Eelvaade**. Üksuse Tooted puhul saate kasutada üksuse lehte Kataloogitooted. See näide näitab, kuidas kataloogi pilti üle kirjutada.

1. Klõpsake valikuid **Kataloogid** &gt; **Meedia** &gt; **Pildid** ja valige värskendamiseks kataloogipilt.
2. Klõpsake suvandit **Lisa** ja sisestage pildi-URL, et meediamalli URL üle kirjutada.
3. Kui soovite, et see pilt kuvataks kataloogi MPOS-is, määrake see vaikepildiks.
4. Klõpsake nupul **OK**. Pildi-URL-i värskendatakse selle kataloogi pildi jaoks ja kuvatakse eelvaade.

    [![URL on värskendatud dialoogiboksis Uus pilt](./media/preview3.png)](./media/preview3.png)

5. Näete kõkide ülekirjutatud pildi-URL-ide pildi eelvaadet ka galerii lehel **Kataloogi pildid**.

    [![Kataloogi piltide galerii leht](./media/preview-4.png)](./media/preview-4.png)

> [!NOTE]
> Praegu ei kuva galerii meediamalli pildi-URL-ide pildi eelvaateid. Üksuste Kataloog, Töötaja, Klient ja Kategooria puhul, kui kasutaja lisab selgesõnaliselt URL-i selle lehe kaudu, soovitame teil viidata, milline on vaikepilt, sest Commerce’i skaala üksuse kliendid kuvavad ainult ühe pildi üksuse Kataloog, Klient, Töötaja ja Kategooria kohta. Kui kasutaja ei määra vaikepilti, määrab süsteem vaikepildi ja saadab selle Commerce’i teenuse kutsujale (MPOS või Ecommerce).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Kataloogitoote piltide pildi-URL-i ülekirjutamine lehel Eelvaade

Kataloogitoote piltide pildi-URL-ide ülekirjutamiseks peate kasutama lehte **Eelvaade**. Te ei saa kasutada funktsiooni Excelis redigeerimine.

1. Toote piltide ülekirjutamiseks kataloogi tasemel valige kataloog ja valige siis toode, mille pilti soovite üle kirjutada.
2. Klõpsake suvandit **Atribuudid**.
3. Valige järgmisel lehel suvand **Pilt** ja klõpsake seejärel suvandit **Redigeeri**. Leht **Eelvaade** avaneb liugurdialoogikastina.
4. Klõpsake suvandit **Lisa** ja kirjutage pildi-URL uue URL-iga üle.
5. Klõpsake nupul **OK**. Näete nüüd uue pildi eelvaadet ja saate määrata selle vaikepildiks.

    [![Pildi eelvaade dialoogiboksis Uus pilt](./media/cat3.png)](./media/cat3.png)

> [!NOTE]
> Pärast kategooria pildi seost peate avaldama kanali ja käitama kanali töö tagamaks, et muudatused avaldatakse kanali andmebaasis.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Piltide seadistamine MPOS-i võrguühenduseta režiimis kuvamiseks

MPOS-i saab käitada võrgurežiimis (kui MPOS on ühendatud Commerce’i skaala üksusega) või võrguühenduseta režiimis (kui ei ole Commerce’i skaala üksust ega võrguühendust ja kanded talletatakse kohalikus võrguühenduseta andmebaasis). Kui MPOS-i käitatakse võrguühenduseta režiimis, ei saa see hankida pilte välisest pildiserverist Commerce’i skaala üksusesse kuvamiseks, sest ühendus on katkenud. Kuid saate endiselt seadistada pilte, nii et need kuvatakse, kui MPOS-i käitatakse võrguühenduseta režiimis.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Tootepiltide seadistamine MPOS-i võrguühenduseta režiimis kuvamiseks

Tootepilte, mida peab kasutama võrguühenduseta režiimis, saab seadistada, laadides nõutava füüsilise pildi üles tootepildi baasi.

1. Klõpsake valikuid **Tooteteabe haldus** &gt; **Tooted** &gt; **Tooted**.
2. Valige toode, millele soovite võrguühenduseta pildi määrata.
3. Klõpsake suvandit **Redigeeri** ja klõpsake siis paremas nurgas olevat noolt parempoolse paani kuvamiseks.
4. Klõpsake kiirkaardil **Toote pilt** suvandit **Muuda pilti** ja laadige füüsiline pilt, mida soovite kasutada võrguühenduseta režiimis valitud toote puhul.
5. Salvestage ja sulgege leht.
6. Kui MPOS on võrgurežiimis, käitage HQ-s funktsiooni Kataloogitöö tagamaks, et andmed saadetakse vähemalt ühe korra võrguühenduseta andmebaasi.
7. Pange MPOS võrguühenduseta režiimi. Peaksite nägema pilti, mille HQ-s kindlale tootele üles laadisite.

    [![Toote pilt ühenduseta režiimis](./media/offline1.png)](./media/offline1.png)

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Kataloogi, kategooria, töötaja ja kliendi piltide seadistamine MPOS-i võrguühenduseta režiimis kuvamiseks

Kataloogi, kategooria, töötaja ja kliendi pildid, mida on vaja kasutada võrguhenduseta režiimis, saab seadistada, lisades galeriisse nõutava pildi sihtkoha lingi ja määrates pildi valitud üksuse vaikepildiks.

1. Avage kataloog ja klõpsake siis tegevuspaanil nuppe **Meedia** &gt; **Pildid**.
2. Järgige jaotises [Üksuse tasemel lehelt Eelvaade ülekirjutamine](#overwrite-from-the-entity-level-preview-page) toodud juhiseid, et lisada väline pildi-URL.
3. Märkige see pilt kataloogi vaikepildiks, valides märkeruudu Pilt on ruudustikud loetletud.
4. Käitage kataloogitööd. Seda pilti kasutatakse nüüd MPOS-is kataloogi võrguühenduseta pildina.
5. Järgige muude üksuste (nt Kategooria, Töötaja ja Klient) puhul sama protsessi.

    [![Ühenduseta pilt](./media/offline2.png)](./media/offline2.png)
