---
title: Pakkumiskutsed
description: "See artikkel annab ülevaate pakkumiskutsetest, mille organisatsioonid väljastavad, kui neil on vaja osta kaupu või teenuseid ja saada mitmelt hankijalt konkureerivaid pakkumisi. Pakkumiskutses saate hankijatelt küsida teie määratud kaubakoguse hindu ja tarneaegu. Samuti saate hankijatelt küsida, kas on lisatasusid, nagu saatekulud, või allahindlusi suurte tellimuste või hankija arve ennetähtaegse maksmise korral."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d681f4c107a9dbc1ea8c5e1de38b2d45cf19bcfa
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="request-for-quotations-rfqs"></a>Pakkumiskutsed

[!include[banner](../includes/banner.md)]


See artikkel annab ülevaate pakkumiskutsetest, mille organisatsioonid väljastavad, kui neil on vaja osta kaupu või teenuseid ja saada mitmelt hankijalt konkureerivaid pakkumisi. Pakkumiskutses saate hankijatelt küsida teie määratud kaubakoguse hindu ja tarneaegu. Samuti saate hankijatelt küsida, kas on lisatasusid, nagu saatekulud, või allahindlusi suurte tellimuste või hankija arve ennetähtaegse maksmise korral.

Pakkumiskutse (RFQ) protsess hõlmab järgmisi ülesandeid.

-   Pakkumiskutse loomine ja saatmine ühele või mitmele hankijale
-   Pakkumiskutse vastuste (pakkumiste) vastuvõtmine ja registreerimine
-   Aktsepteeritud pakkumiste ülekandmine ostutellimuseks, ostulepinguks või ostutaotluseks

Järgmine näide annab ülevaate pakkumiskutse protsessist.  

[![Pakkumiskutse protsess](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Saate luua pakkumiskutse plaanitud tellimustelt, ostutaotluselt või käsitsi kirjest. Loodud pakkumiskutset nimetatakse pakkumiskutse juhtumiks ja see on alusdokument, mida kasutate pakkumiskutse väljastamiseks igale hankijale. Pärast pakkumiskutse juhtumi ettevalmistamist ja hankijate lisamist klõpsake pakkumiskutse juhtumis käsku **Saada**. Iga hankija jaoks, kellele saatsite pakkumiskutse, luuakse pakkumiskutse tööleht. Saate konfigureerida saatmistegevuse prindihaldussätteid kas printima iga hankija kohta aruande arhiivi või saatma aruande iga hankija meiliaadressile. Peale selle saab iga hankija pakkumiskutse töölehe abil luua aruande, mille saate hankijale saata kohe või hiljem. Samuti saate konfigureerida saatmistegevust, et luua vastuseleht, mille hankija saab täita.  

Kui peate pakkumiskutset pärast saatmist muutma, saate selle hankijatele uuesti saata, kui olete lõpetanud.  

Pakkumiste vastuvõtmisel peate sisestama need lehel **Pakkumiskutse vastused**. Kui valite suvandi **Kopeeri andmed vastuseväljadele**, kopeeritakse vastuseväljadele pakkumiskutse juhtumi andmed, nagu kogus ja kuupäevad. Saate neid andmeid muuta, et kajastada hankija pakkumist.  

Kui konkreetse hankija puhul on nõutav vastuse teine iteratsioon, klõpsake lehel**Pakkumiskutse vastus** käsku **Tagasta**. Tagastustegevus loob uue töölehe ja aruande, mis prinditakse, arhiivitakse ja saadetakse teie prindihaldussätete järgi.  

Kui olete lisanud pakkumiskutse juhtumile hindamiskriteeriumid, on pakkumiskutse vastusel hindamispaneel, kuhu saate punktisummad sisestada. Punktide kogusumma kuvatakse, kui võrdlete vastuseid lehel **Vastuste võrdlemine**, kus saate võrrelda ka muid vastuseandmeid, nagu rea hind, tarnekuupäev ja koguhind.  

Kui otsustate mõne pakkumise või osalise pakkumise kasuks, saate selle vastu võtta ja ülejäänud tagasi lükata. Luuakse kinnitamise töölehed, tagasilükkamise töölehed ja vastavad aruanded. Need prinditakse, arhiivitakse ja saadetakse teie prindihalduse sätete järgi. Kui aktsepteerite pakkumise või pakkumise konkreetsed read, luuakse kas ostuleping või ostutellimus või värskendatakse ostutaotlust olenevalt pakkumiskutse ostutüübist. Saate luua kaubandusleppe, mida saate hiljem kasutada mis tahes vastuste puhul olenemata sellest, kas olete need aktsepteerinud või tagasi lükanud.  

Pakkumiskutse olek kuvatakse pakkumiskutse päises ja see oleneb pakkumiskutse ridade olekust. Olek näitab, mil määral olete pakkumiskutset töödelnud. Igal pakkumiskutsel on kaks oleku väärtust: madalaim ja kõrgeim. Madalaim olek on pakkumiskutse ükskõik millise rea kõige vähemarenenum etapp ja kõrgeim olek on pakkumiskutse ükskõik millise rea kõige arenenum etapp. Näiteks kui pakkumiskutse kõige vähemarenenum etapp on loodud rea kohta, siis on pakkumiskutse madalaim olek **Loodud**. Kui pakkumiskutse kõige arenenum etapp on hankijatele saadetud rea kohta, siis on pakkumiskutse kõrgeim olek **Saadetud**. Pakkumiskutse töötlemisel värskendatakse olekuid automaatselt.  

Saate pakkumiskutse päise madalaimaid ja kõrgeimaid olekuid vaadata lehel **Kõik pakkumiskutsed**. Saate pakkumiskutse rea madalaimaid ja kõrgeimaid olekuid vaadata lehe **Pakkumiskutsed** vahekaardil **Read**.  

Pakkumiskutsete töötlemise olekute järjestus on järgmine.

1.  **Loodud**
2.  **Saadetud**
3.  **Vastu võetud**
4.  **Aktsepteeritud**/**Tühistatud**/**Tagasi lükatud**

Olekuid kirjeldatakse üksikasjalikumalt selle artikli allpool olevates jaotistes.

## <a name="setting-up-rfq-functionality"></a>Pakkumiskutse funktsiooni seadistamine
Enne pakkumiskutse juhtumi loomist peate seadistama pakkumiskutse teabe lehel **Hankeparameetrid**. Pakkumiskutse juhtumi loomisel saate määrata vaikeväärtused, mis kopeeritakse pakkumiskutsele. Saate määrata järgmised vaikeväärtused.

-   Uus pakkumiskutsete ostutellimuse tüüp: **Ostutellimuse** või **Ostuleping**
-   Aegumiskuupäeva ja -kellaaja sätted
-   Tarneteave ja maksetingimused
-   Väljad, mis peavad olema pakkumiskutse vastuses

Saate need väärtused kindla pakkumiskutse juhtumi puhul tühistada. Peate seadistama ka parandusprotsessi. Selle konfiguratsiooni osana saate väljalukustuse sisse lülitada. Kui väljalukustus on sisse lülitatud, peab hankespetsialist, kes soovib pakkumiskutset parandada, klõpsama esmalt vahekaardi **Pakkumine** jaotises **Parandus** käsku **Loo**. Pärast pakkumiskutse värskendamist parandusega peab hankespetsialist viima protsessi lõpule, klõpsates käsku **Vii sisse**.** **Sisseviimistegevus koostab meilisõnumi, mis teavitab hankijaid parandatud pakkumiskutsest. Valige hankijatele saadetava meiliteatise mall lehelt **Hankeparameetrid**. Malli loomisel võib see sisaldada järgmisi asendussõnesid.

-   %Pakkumise tagastamise põhjus%
-   %Paranduse põhjus%
-   %Paranduse ettevalmistaja%
-   %Ettevõte%

Sõned %Pakkumise tagastuse põhjus% ja %Paranduse põhjus% asendatakse tekstiga, mille hankespetsialist saab sisestada paranduse tegemisel viisardis **Parandus**. Sõned %Paranduse ettevalmistaja% ja %Ettevõte% võetakse automaatselt pakkumiskutselt.  

Kui soovite kasutada pakkumiskutse vastusel põhjusekoode, et näidata pakkumise tagasilükkamise või aktsepteerimise põhjust, peate seadistama põhjusekoodid lehel **Hankija põhjused**.  

Saate konfigureerida prinditud või salvestatud pakkumiskutsedokumentide välimust mooduli Hanked lehel **Vormiseadistus**.  

Kui loote pakkumiskutse ostutellimuse jaoks ja lisate pakkumiskutsele laokauba, luuakse ka laokanne, mille sissetuleku olek on **Saadud pakkumine**. Koondplaani abil varude arvutamisel arvestatakse vaid selle olekuga pakkumiskutse ridu. Kui soovite, et koondplaan sisaldaks pakkumiskutse ridu eeldatava sissetulekuna, peate konfigureerima selle käitumise koondplaneerimise seadistamisel.  

Ostujuhi või -agendina saate luua kutsetüüpe oma organisatsiooni hankenõuete täitmiseks. Iga kutsetüüp võib reguleerida hindamismeetodeid. Hindamismeetodid koosnevad kriteeriumitest, mida saab kasutada pakkumiste hindamisel. Peate seadistama kutsetüübid, hindamismeetodid ja hindamiskriteeriumid lehtedel **Kutsetüüp** ja **Hindamismeetod**.

## <a name="creating-and-sending-an-rfq"></a>Pakkumiskutse loomine ja saatmine
Looge pakkumiskutse, valige hankijad, kellelt soovite pakkumiskutse kohta pakkumisi saada, ja saatke seejärel pakkumiskutse hankijatele. Prindihalduse abil saate pakkumiskutse aruande ja vastuselehe aruanded suunata soovitud sihtkohta.  

Saate luua pakkumiskutse ostutellimuse tüübile **Ostutellimuse** või **Ostuleping**.  

Kui pakkumiskutse luuakse ostutellimuselt, määratakse automaatselt tüüp **Ostutaotluse**. Pakkumiskutset, mille tüüp on **Ostutaotlus**, ei saa käsitsi luua. Kui pakkumiskutse tüüp on **Ostutellimus**

-   Pakkumiskutse ridade loomisel luuakse laokanded, mille sissetuleku olek on **Pakkumise sissetulek**.
-   Pakkumise aktsepteerimisel luuakse ostutellimus.

Kui pakkumiskutse tüüp on **Ostuleping**

-   Pakkumiskutset kasutatakse hankijalt pikema aja vältel kindlas koguses või väärtuses toote ostmiseks. Peate valima ostulepingule kehtiva kuupäevavahemiku ja ostulepingut haldava isiku nime.
-   Pakkumise aktsepteerimisel luuakse ostuleping.

Saate luua on pakkumiskutse ostutaotluselt ainult siis, kui ostutaotluse olek on **Ülevaatusel**ja teile on määratud järgmine töövooülesanne. Ostutaotluse ridu värskendatakse automaatselt, kui aktsepteerite hankijalt saadud pakkumiskutse vastuste (pakkumiste) ridu. Te ei saa ostutaotlust lõpule viia, tagasi lükata, kinnitada ega sellega muid toiminguid teha, kuni pakkumiskutse on pooleli.  

Pakkumiskutse loomisel saate valida kindla kutsetüübi. Kutsetüüp määrab hindamiskriteeriumite komplekti, mida kasutatakse pakkumiskutse vastuste hindamiseks.  

Saate lisada pakkumiskutse juhtumile küsimustiku. Seejärel kuvatakse küsimustik pärast pakkumiskutse saatmist kõigil vastustel.  

Hankijate lisamiseks pakkumiskutse juhtumile on kolm võimalust.

-   Hankijate lisamine ükshaaval.
-   Kindlatele kriteeriumitele vastavate hankijate otsimine.
-   Kõigi hankijate automaatne lisamine, kes on pakkumiskutse ridadel kasutatud hankekategooriate puhul kinnitatud.

Kui pakkumiskutse on valmis, klõpsake käsku **Saada**. Saatmistegevus loob töölehed ja aruanded, mis prinditakse, arhiivitakse ja saadetakse teie prindihaldussätete järgi.  

Kui märkisite pakkumiskutse saatmisel hankijatele lehel **Pakkumiskutse saatmine** ruudud **Kasuta hindade ümberarvutamiseks hankijat** ja **Kasuta hankijakohast kaubateavet**, sisestatakse osa hankijakohast teavet automaatselt. Saate seda teavet muuta lehel **Pakkumiskutse vastus**.  

Järgmises tabelis kuvatakse pakkumiskutse oleku muudatused, kui loote pakkumiskutse ja saadate selle hankijatele.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Tegevus**                         | **Madalaim pakkumiskutse päise olek** | **Kõrgeim pakkumiskutse päise olek**                   | **Madalaim pakkumiskutse rea olek** | **Kõrgeim pakkumiskutse rea olek** |
| Looge pakkumiskutse päis ja rida.    | Loodud                      | Loodud                                         | Loodud                    | Loodud                     |
| Saatke pakkumiskutse kindlale hankijale. | Saadetud                         | Saadetud                                            | Saadetud                       | Saadetud                        |
| Lisage teine hankija.                | Loodud                      | Saadetud (pakkumiskutse on saadetud ainult ühele hankijale.) | Loodud                    | Saadetud                        |
| Saatke pakkumiskutse teisele hankijale. | Saadetud                         | Saadetud                                            | Saadetud                       | Saadetud                        |

**Märkus.** Saate igal ajal pakkumiskutsele täiendavaid hankijaid lisada ning madalaimad ja kõrgeimad olekud muutuvad kajastamaks uusi hankijaid. Näiteks kui saite pakkumisi kõikidelt hankijatelt ja nõustusite vähemalt ühe pakkumise reaga, siis on pakkumiskutse päise madalaim olek **Tagasi lükatud** ja kõrgeim olek **Aktsepteeritud**. Kui lisate uue hankija, on ükskõik millise rea madalaim olek nüüd **Loodud**. Seega saab pakkumiskutse päise madalaimaks olekuks **Loodud** ja kõrgeimaks olekuks jääb **Aktsepteeritud**.

## <a name="amending-an-rfq"></a>Pakkumiskutse parandamine
Mõnikord peate pakkumiskutset pärast selle saatmist muutma. See võib juhtuda näiteks siis, kui tarnekuupäevad on muutunud või kui soovite täiendavaid tooteid või teistsuguseid tootekoguseid. Saate konfigureerida parandusprotsessi nii, et see oleks rohkem või vähem piirav.  

Kui kasutate rohkem piiravat parandusprotsessi, peate klõpsama paranduskutse juhtumil käsku **Loo**, et käivitada parandus enne, kui saate pakkumiskutse juhtumi välju muuta. Kui olete muudatuste tegemise lõpetanud, peate klõpsama käsku **Vii lõpule**. Seejärel suunatakse teid läbi teabe lisamise protsessi, et saata hankijatele paranduse kohta meilisõnum. Värskendatud pakkumiskutse aruanne, mis sisaldab paranduse märkust, lisatakse sõnumile automaatselt.  

Kui kasutate vähem piiravat parandusprotsessi, ei pea te enne saadetud pakkumiskutse juhtumi väljade muutmist parandust looma. Siiski peate paranduse märkuse käsitsi pakkumiskutsele lisama.

## <a name="receiving-and-registering-rfq-replies"></a>Pakkumiskutse vastuste vastuvõtmine ja registreerimine
Pakkumiskutse saatmisel luuakse automaatselt vastuseleht. Pärast pakkumiskutsele vastuste (pakkumiste) saamist peate sisestama iga hankija teabe hankijakohase pakkumiskutse vastuselehele. Kui olete lisanud hindamiskriteeriumid, saate vastuseid hinnata. Seejärel saate hankijate pakkumisi võrrelda ja hinnata oma hindamiskriteeriumite järgi, nagu parim koguhind või parim lõplik tarneaeg.  

Kui pakkumiskutse juhtumile on lisatud küsimustik, peate küsimuste vastused vastuselehele käsitsi sisestama.  

Kui peate sisestama alternatiivseid ridu ja pakkumiskutse juhtub seda võimaldab, klõpsake kiirkaardil **Ostupakkumise read** käsku **Lisa rida**. Seejärel sisestage toote teave, nagu kaubakood või hankekategooria, kogus, hind ja allahindlus.  

Kui olete sisestanud vastuse, kuid nõuate hankijalt uut pakkumist, saate pakkumiskutse uuesti saata. See loob uue töölehe ja aruande, mida saate kasutada hankijalt muudatuste taotlemiseks.  

Kõigi pakkumiskutsete ülevaadet ja nende vastuste olekuid saate vaadata lehel **Pakkumiskutse järeltoimingud**.  

Järgmises tabelis kuvatakse pakkumiskutse oleku muudatused, kui saate pakkumisi ja registreerite teabe pakkumiskutse vastuselehel.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Tegevus**                                     | **Madalaim pakkumise olek** | **Kõrgeim pakkumise olek** | **Madalaim pakkumiskutse päise olek** | **Kõrgeim pakkumiskutse päise olek** | **Madalaim pakkumiskutse rea olek** | **Kõrgeim pakkumiskutse rea olek** |
| Registreerige ühe hankija pakkumine ja salvestage see.        | Saadetud                  | Saadud               | Saadetud                         | Saadud                      | Saadetud                       | Saadud                    |
| Registreerige teise hankija pakkumine ja salvestage see. | Saadud              | Saadud               | Saadud                     | Saadud                      | Saadud                   | Saadud                    |

**Märkus.** Kui tagastate pakkumise hankijale edasiste läbirääkimiste eesmärgil, jäävad madalaimaks ja kõrgeimaks olekuks **Vastu võetud**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Pakkumiste aktsepteerimine ja tagasilükkamine ning aktsepteeritud pakkumiste ülekandmine allavoolu dokumentidele

Pärast parima pakkumise tuvastamist, nt parima koondhinnaga pakkumine, aktsepteerite pakkumise. Pakkumiskutse vastuse olek selle hankija puhul värskendatakse olekule **Aktsepteeritud**. Pakkumise või selle konkreetsete ridade aktsepteerimisel luuakse automaatselt ostutellimus või ostuleping ja teil on võimalik pakkumised teistelt hankijatelt tagasi lükata.  

Kui aktsepteerite pakkumiskutse vastuse, mille tüüp on **Ostutaotlus**, värskendavad pakkumiskutse vastuse read ostutaotluse ridu järgmise teabega.

-   Ühiku hind
-   Allahindlusprotsent
-   Allahindluse summa
-   Ostukulud
-   Reatasud
-   Hankija
-   Väline number
-   Väline kirjeldus

Saate vastusele lisada põhjusekoodi, millega selgitada pakkumise aktsepteerimist või tagasilükkamist.  

Saate pakkumises mõne rea aktsepteerida ja ülejäänud tagasi lükata. Samuti saate aktsepteerida ridu teistelt hankijatelt. Võtke siiski arvesse, et mõne rea aktsepteerimisel palutakse teil kõik teised read tagasi lükata. Seega kui soovite teised read aktsepteerida, peate viiba kuvamisel klõpsama käsku **Tühista**.  

Järgmises tabelis kuvatakse pakkumiskutse oleku muudatused, kui hankija pakkumisi aktsepteerite või tagasi lükkate.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Tegevus**              | **Madalaim pakkumise olek** | **Kõrgeim pakkumise olek** | **Madalaim pakkumiskutse päise olek** | **Kõrgeim pakkumiskutse päise olek** | **Madalaim pakkumiskutse rea olek** | **Kõrgeim pakkumiskutse rea olek** |
| Aktsepteerige üks pakkumistest. | Saadud              | Aktsepteeritud               | Saadud                     | Aktsepteeritud                      | Saadud                   | Aktsepteeritud                    |
| Lükake teised pakkumised tagasi.  | Tagasi lükatud              | Aktsepteeritud               | Tagasi lükatud                     | Aktsepteeritud                      | Tagasi lükatud                   | Aktsepteeritud                    |






