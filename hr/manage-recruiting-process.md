---
title: "Värbamisprotsessi haldus"
description: "See artikkel kirjeldab võimalusi, kuidas värbajad saavad jälgida värbamise etappe, sh vabade ametikohtade reklaamimiseks ja kandidaatide värbamiseks, kandidaadi ja avalduse teabe jälgimiseks, kandidaatide intervjueerimiseks ja vaba ametikoha täitmiseks ühe või mitme kandidaadi väljavalimiseks tehtud pingutusi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 551e15ed31953d6e5fc99a1177c1310194ea95d0
ms.lasthandoff: 03/31/2017


---

# <a name="manage-a-recruiting-process"></a>Värbamisprotsessi haldus

Selles teemas on mõiste, mille värbajate saate jälgida värbamise protsessi etappe, sealhulgas avatud positsioonide ja värvata tööle kandidaate, taotleja ja taotluse jälitusteave, intervjueerimine ja valides ühe või teise kandidaadi organisatsiooni avatud kohtade täitmiseks.

<a name="overview"></a>Ülevaade
--------

Värbamisprojektid aitavad organiseerida juriidilise isiku vabade ametikohtade täitmise etappe. Taotleja on isik, kes taotleb oma ettevõtte töö.  Taotlus taotleja väljendab huvi firma töötab ja võib olla seotud värbamisprojekti, et väljendada huvi konkreetse avamine.  Sama hageja võib mitu taotlust sama juriidilise isiku või ettevõtetevaheliselt on teie organisatsioonis.

<a name="recruitment-projects"></a>Värbamisprojektid
--------------------

Värbamisprojektide lubada värbajate alal saavutatud edusamme ühe või mitme täitmata lahtrite täitmine.  Värbamisprojekt seotud osakond ja tööd, mille üks või mitu positsioonid on avatud. Värbamisprojektide kaudu saab vabade ametikohtade osas muuhulgas jälgida järgmist teavet:
-   vabade ametikohtade täpne arv;
-   värbamisjuhi või teise vastutava isiku kontakt, kellega ametikoha asjus suhelda;
-   tellimuse kinnitamise kuupäev;
-   avalduse tähtaeg;
-   eeldatav alguskuupäev.

Värbamisprojekt sisaldab **töötaja iseteeninduses** vaba ametikohta reklaamivat **töökuulutust**. Töötajatele vaba töökoha kohta teabe kuvamiseks peab värbamisprojektil olema **töökuulutus**, väljal** Kuva töötaja iseteeninduses** valitud Jah, **Avalduse tähtaeg** seatud tulevasele kuupäevale ning värbamisprojekti **Projekti olek** Alustatud. Järgmises tabelis on võimalik värbamine projekti olekuid ja nende kirjeldused.

| **Status**    | **Indicates that…**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Plaanitud | Valmistatakse värbamisel jõupingutusi.  Värbamine ei ole veel alanud projektile. |
| Alustatud   | Selle projekti vabadele töökohtadele võetakse nüüd avaldusi vastu.                    |
| Lõpetatud  | Kõik selle projekti vabad töökohad on täidetud.                                          |
| Tühistatud  | Selle projekti värbamine tühistati.                                           |

Värbajad saavad salvestada ka vaba töökoha reklaamimiseks väljaspool organisatsiooni kasutatud **meediakanaleid**, samuti jälgida projekti või avaldusi jaotises **Arengud**.

<a name="applicants"></a>Kandidaadid
----------

Taotleja on isik, kes taotleb oma ettevõtte tööd.  Juriidilised isikud ühiselt taotlejate annab teile suur bassein ande sissetulekukontot organisatsiooni. Saate säilitada kandidaatide pädevusi, soovitusi, erivajaduse taotlusi ja isikuandmeid. Kandidaadi kirje loomisel luuakse selle kandidaadi isiku kirje globaalses aadressiraamatus. Kandidaatide kohta saate globaalses aadressiraamatus olevat järgmist teavet lehekülje **Kandidaat** abil värskendada:
-   Aadressiteave
-   Kontaktteave
-   tuvastamisteave,
-   Nime üksikasjad
-   Isikuandmed

## <a name="applications"></a>Rakendused
Saadud kandideerimisavalduste teabe saate salvestada leheküljel **Avaldus**. Taotlus on oma sooviavaldusele avamine organisatsiooni töösse.  Taotluse loomiseks taotleja peab olemas olema taotleja või isik oma süsteemi.
Kandidaatide veebi kaudu esitatud avaldused on kas kindlast töökuulutusest lähtuvad soovitud avaldused või soovimatud avaldused. Soovitud avaldused seostatakse automaatselt värbamisprojektiga, kuhu töökuulutus loodud oli. Soovimatud avaldused seostatakse värbamisprojektiga, mis on määratud lehekülje **Inimressursside parameetrid** alal **Värbamine**.
### <a name="application-status"></a>Avalduse olek

Avalduse olek näitab, millises faasis avaldus värbamisprotsessis on. Järgmises tabelis loetletakse avalduse võimalikud olekud ja nende kirjeldus.

| Olek    | Näitab, et …                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Saadud  | Avaldus on vastu võetud.                                                             |
| Kinnitatud | Kandidaadile saab avalduse kättesaamise kinnituseks teate saata.            |
| Vestlus | Kandidaadile saab saata töövestluse kutse.                                     |
| Tagasilükkamine | Kandidaadile saab saata tagasilükkamiskirja.                                          |
| Tühistatud  | Kandidaadile saab saata loobumise kinnituse. See olek määratakse käsitsi. |
| Tööle võetud  | Kandidaadile saab saata tööpakkumise.                                         |

### <a name="correspondence-actions"></a>Vastamistegevused

**Avalduse** vastamistegevus määrab, millist dokumendi- või meilimalli avalduse esitanud kandidaadiga suhtlemiseks kasutatakse. Saate seostada **avalduste järjehoidjad** koos teie taotluse väärtuste kasutamiseks vastamistegevuste, taotleja ja intervjuu värbamise projekti Internetis teie suhtlus teiste taotlejate.  **Rakenduse meilisõnumimallid** saab luua vastamistegevuste kiiresti saata e-kirju, kes on taotluse ja teatud koht ja kirjavahetus meetmete kombinatsiooni. Näiteks võib kõigi rakenduste kinnitusmeil saata on **staatus**, Vastuvõtuaeg ja on **kirjavahetus tegevus**, Vastuvõtuaeg.  Pärast meili saatmist on teil võimalus automaatse uuendamise taotluste olekut.

## <a name="application-routing"></a>Avalduse marsruutimine

Kui avalduse peab läbi vaatama mitu töötajat, siis saate protsessi haldamiseks luua töötaja ringluse loendi, kasutades lehekülge **Avalduse marsruutimine**.

## <a name="interviews"></a>Vestlused

**Kandidaatidega** kavandamiseks selle **rakenduste** lehel.  Kasutamine on **saada koosoleku teavet** nuppu ja intervjueerija ning kalendri faili vestluse ajakava teabe saatmiseks.

## <a name="skill-mapping"></a>Oskuste kaardistamine

Vabale töökohale sobiva kandidaadi tuvastamiseks saate kasutada vorme**Oskuste kaardistamine** ja **Oskuste kaardistamise reeglid**.

## <a name="hiring-applicants"></a>Kandidaatide palkamine

Kandidaadi palkamiseks kasutage lehekülge **Avaldused**. Kandidaadi palkamisel muudetakse avalduse kirje olekuks **Tööle võetud** ja kandidaadi isikukirje globaalses aadressiraamatus seostatakse uue töötaja kirjega. Globaalses aadressiraamatus uue töötaja kirjes tehtud muudatused kuvatakse ka kandidaadi kirjes. See aitab vähendada andmete sisestamise, kui uus töötaja kunagi oma ettevõttes erinevaid töökohta.  Olemasoleva töötaja palgata uut asukohta, klõpsake **asend muutub** ja selle **taotluse staatuse** rippmenüüst algatada edastusprotsessi.




