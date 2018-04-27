---
title: Varade soetamine hankega
description: "See teema kirjeldab, kuidas seadistada integratsiooni põhivarade ja ostureskontro vahel, et luua ostutellimustest või hankija arvetest automaatselt põhivarad, või sisestada automaatselt põhivarade soetamise- ja soetamiskorrigeeringu kanded."
author: twheeloc
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1e9b1dc6297f33ea25ca498895740596ebd020b8
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="acquire-assets-through-procurement"></a>Varade soetamine hankega

[!INCLUDE [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada integratsiooni põhivarade ja ostureskontro vahel, et luua ostutellimustest või hankija arvetest automaatselt põhivarad, või sisestada automaatselt põhivarade soetamise- ja soetamiskorrigeeringu kanded.

 Põhivarade ja ostureskontro integreerimiseks on saadaval järgmised meetodid. Kõigi põhivarade puhul tuleb kasutada sama meetodit.
-   Enne põhivara numbri lisamist ostutellimuse või hankija arve reale looge põhivara käsitsi. Hankija arve sisestamisel sisestatakse vara soetamiskanne automaatselt. See on vaikeviis.
-   Enne põhivara numbri lisamist ostutellimuse või hankija arve reale looge põhivara käsitsi. Hankija arve sisestamisel vara soetamiskannet automaatselt ei sisestata.
-   Põhivara luuakse automaatselt, kui sisestate toote sissetuleku või hankija arve, mille puhul on valitud ruut Uue põhivara loomine. Hankija arve sisestamisel sisestatakse vara soetamiskanne automaatselt.
-   Põhivara luuakse automaatselt, kui sisestate toote sissetuleku või hankija arve, mille puhul on valitud ruut Uue põhivara loomine. Hankija arve sisestamisel vara soetamiskannet automaatselt ei sisestata.

Kui eelistate põhivarasid käsitsi luua, valige üks kahest esimesest meetodist ja seejärel määrake põhivara kood ostutellimusele või hankija arvele. Kui eelistate paindlikumat lähenemist, valige üks viimasest kahest meetodist: vahel võite põhivarasid käsitsi luua ja vahel võite uue põhivara automaatselt luua, võttes aluseks kauba üksikasjade real oleva põhivara teabe. 

Ükskõik, kas loote põhivarasid käsitsi või kasutate paindlikumat lähenemist, peate otsustama, kas soetamiskannet saab sisestada üksnes jaotises Põhivarad või seda saab sisestada, kui sisestate hankija arve. Mõned organisatsioonid eelistavad varianti, kus kasutajad loovad käsitsi soetamisi ja soetamiskandeid jaotises Põhivarad, sisestades töölehe kirjeid või soovitusi käsitsi. 

Siin teemas käsitletakse iga meetodi üksikasju.

## <a name="methods-for-manually-creating-fixed-assets"></a> Põhivarade käsitsi loomise meetodid
Kui lehel Põhivarade parameetrid on valitud suvand Luba vara soetamine ostmiselt ning sisestate hankija arve, mille ridadele on sisestatud põhivarakood, sisestatakse soetamine automaatselt ja vara olekuks saab Avatud. 

Kui soetamist ei saa sisestada, saate kas soetamiskande käsitsi jaotisesse Põhivarad sisestada või kasutada soetamissoovitust põhivarade töölehel, et luua korraga mitu soetamiskannet.

> [!NOTE]                                                                                                                              
> Kui põhivarad on seadistatud piirama soetamiskande sisestust konkreetsele kasutajagrupile, peate arvetelt soetamiskannete sisestamiseks olema selle kasutajagrupi liige.

## <a name="methods-for-automatically-creating-fixed-assets"></a> Põhivarade automaatse loomise meetodid
Kui sisestate toote sissetuleku, mille rea puhul on valitud suvand Uue põhivara loomine, luuakse uus põhivara olekuga Veel soetamata. Seejärel, kui sisestate hankija arve uue põhivaraga, sisestatakse uue põhivara soetamiskanne ja vara olekuks saab Avatud, kui põhivarad on seadistatud lubama vara kandeid ostureskontrost ja te olete selle kasutajagrupi liige, mis saab soetamiskandeid sisestada. 

Kui suvand Uus põhivara? polnud toote sissetuleku sisestamise ajal ostureal märgitud, kuid oli märgitud siis, kui sisestasite hankija arve, luuakse ja soetatakse uus põhivara olekuga Avatud, kui põhivarad on seadistatud loomist ja soetamist lubama. Täiendavat vara ei looda hankija arve sisestamisel, juhul kui toote sissetuleku sisestamisel loodi juba üks.

### <a name="capitalization-threshold"></a>Kapitaliseerimislävi

Kui kasutate meetodit, kus vara luuakse ja soetatakse automaatselt, saate seadistada süsteemi kontrollima, kas põhivara ostusumma vastab vara kulumi määratletud kapitaliseerimislävele. Kui nii, märgitakse ruut Kulum vara raamatutes, kui see luuakse ostureskontrost. 

Kapitaliseerimislävi on valuutasumma, mis määrab, kas varasid amortiseeritakse, kui need vastavad määratletud summale. Näiteks kui te ostate vara ja ostusumma on kapitaliseerimislävest väiksem, ei ole vara amortiseerimiseks määratud; kui ostusumma vastab lävele või ületab selle, on vara amortiseerimisele määratud. 

Kapitaliseerimisläve saate seadistada leheküljel Põhivaragrupid.

## <a name="scenario"></a>Stsenaarium
Järgmises stsenaariumis käsitletakse Põhivarade ja Ostureskontro integratsiooni täielikku tsüklit. Näidatakse näidisseadistust ja samuti kirjeldatakse soetamissoovituste kasutamist. 

Selles stsenaariumis on süsteem seadistatud järgmiselt:

-   Varad luuakse automaatselt toote sissetuleku või hankija arve sisestamise ajal, kuid põhivarad on seadistatud tõkestama soetamiskannete sisestamist ostureskontrost.
-   Põhivara sissetuleku- ja põhivara väljaminekukontode tüübid on määratletud leheküljel Kaubagrupid väljal Konto tüüp.
-   Arvutite grupi (COMP) kapitaliseerimislävi on 1500.
-   Teie ülesanne on sisestada ostutellimus töötaja uuele sülearvutile, sisestada ostutellimus, kontrollida, et lähetusametnik sisestab toote sissetuleku, sisestada hankija arve ja seejärel kontrollida, et raamatupidaja värskendab sülearvuti olekusse Avatud.

Alustage leheküljelt Ostutellimus, et sisestada üksikasjad sülearvuti kohta, mille hind on 1600. Valige ostutellimuse ridade kiirkaardil Põhivarad suvand Uus põhivara?, valige põhivaragrupiks COMP ja salvestage ostutellimus. 

Kui sülearvuti on kätte saadud, sisestab ja saadab lähetusametnik toote sissetuleku, et kirjendada sülearvuti sissetulek. Luuakse sülearvuti vara olekuga Veel soetamata. Summa ületab kapitaliseerimisläve. Seetõttu valitakse sülearvuti vara jaoks raamatutes suvand Kulum. Toimusid järgmised kanded.

| Kirjeldus                               | Konto             | Deebet    | Kreedit   |
|-------------------------------------------|---------------------|----------|----------|
| Ost, toote sissetuleku ost        | Arveldamata sissetulekud | 1 600,00 |          |
| Ost, toote sissetuleku ostu vastaskonto | Tekkepõhised ostud   |          | 1 600,00 |

Järgmiseks sisestage sülearvuti hankija arve. Sülearvuti olek ei muutu, sest põhivarad on seadistatud tõkestama vara soetamiskannet sisestamast, kui sisestatakse hankija arvet. Hankija arve sisestamisel valiti suvand Uue põhivara loomine. Seepärast kasutati kontot Põhivara sissetulek. Kontot Põhivara väljaminek ei kasutatud, kuna soetust ei sisestatud. Seda kasutatakse hiljem, kui teie organisatsiooni raamatupidaja sisestab põhivaradesse soetamissoovitusi kasutades soetamiskande. 

Toimusid järgmised kanded.

| Kirjeldus                               | Konto             | Deebet    | Kreedit   |
|-------------------------------------------|---------------------|----------|----------|
| Ost, toote sissetuleku ostu vastaskonto | Tekkepõhised ostud   | 1 600,00 |          |
| Hankija saldo                            | Ostureskontro    |          | 1 600,00 |
| Ost, põhivara sissetulek             | Arvutikulud    | 1 600,00 |          |
| Ost, toote sissetuleku ost        | Arveldamata sissetulekud |          | 1 600,00 |

Lõpuks vaatab raamatupidaja üle kõik põhivarad, millel on olek Veel soetamata. Seega vaadatakse üle uus sülearvuti vara. Seejärel avab raamatupidaja tööleheridadelt Põhivarad lehekülje Soetussoovitus ja loob soetamiskande kõigile varadele, millel on arve, kuid mille olek on ikka Veel soetamata. Kui tööleht on sisestatud, muudetakse sülearvuti vara olekuks Avatud. Põhivara väljaminekukonto krediteeritakse ja vara soetamiskonto debiteeritakse. 

Järgnevalt sama stsenaariumi variandid:

-   Kui põhivarad on seadistatud lubama vara soetamiskannete sisestamist hankija arvete sisestamisel, ei pea raamatupidaja kasutama soetussoovitusi Põhivarades, kuna soetamiskanne on loodud. Samuti värskendatakse erinevad kontod hankija arve sisestamisel. Arvuti kulude asemel debiteeritakse põhivara sissetuleku laokontot ja ilmneb kaks uut kannet: vara soetamiskontot debiteeritakse ja põhivara väljamineku laokontot krediteeritakse.
-   Kui suvand Uue põhivara loomine pole märgitud toote sissetuleku sisestamise ajal, ei looda sel hetkel põhivara. Kui märgite suvandi Uue põhivara loomine enne hankija arve sisestamist, luuakse põhivara olekuga Veel soetamata või olekuga Avatud, juhul kui sisestate ka soetamiskanded koos hankija arve sisestamisega.
-   Kui sülearvuti maksab 1600 asemel 1400, ei jõuta kapitaliseerimisläveni. Seega luuakse vara ja suvand Kulum on tühi.
-   Arveregistri kasutamisel kasutage pärast arveregistri sisestamist kande toomiseks lehekülge Arve kinnitamise tööleht, seostage ostutellimus hankija arvega, valige suvand Uue põhivara loomine ja sisestage hankija arve. Kui olete sellise kasutajagrupi liige, kes saab luua soetamiskandeid, luuakse soetamine ja vara on olekuga Avatud.
-   Kui saadakse üksnes osaline kogus, ei looda vara soetamist esimese hankija arve puhul kasutajagrupi piirangute tõttu. Ainus viis hankija teise, lõpliku kogusega arvega soetamise sisestamiseks on see, kui soetamiskanne on juba hankija esimese arve puhul sisestatud ja olete sellise kasutajagrupi liige, mis saab soetusi sisestada.


Lisateavet leiate jaotisest [Põhivarade integreerimine](fixed-asset-integration.md).




