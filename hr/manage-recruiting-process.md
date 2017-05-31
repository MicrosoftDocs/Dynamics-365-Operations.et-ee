---
title: "Värbamisprotsessi haldus"
description: "See artikkel kirjeldab võimalusi, kuidas värbajad saavad jälgida värbamise etappe, sh vabade ametikohtade reklaamimiseks ja kandidaatide värbamiseks, kandidaadi ja avalduse teabe jälgimiseks, kandidaatide intervjueerimiseks ja vaba ametikoha täitmiseks ühe või mitme kandidaadi väljavalimiseks tehtud pingutusi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 56fba251b9f3a67d79e787a2460c17d0bb81de34
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="manage-a-recruiting-process"></a>Värbamisprotsessi haldus

[!include[banner](includes/banner.md)]


See teema kirjeldab võimalusi, kuidas värbajad saavad jälgida värbamise etappe, sh vabade ametikohtade reklaamimiseks ja kandidaatide värbamiseks, kandidaadi ja avalduse teabe jälgimiseks, kandidaatide intervjueerimiseks ja vaba ametikoha täitmiseks ühe või mitme kandidaadi väljavalimiseks tehtud pingutusi.

<a name="overview"></a>Ülevaade
--------

Värbamisprojektid aitavad organiseerida juriidilise isiku vabade ametikohtade täitmise etappe. Kandidaat on isik, kes taotleb töökohta teie ettevõttesse.  Avaldus näitab kandidaadi huvi ettevõttes töötamise vastu ja võib olla seotud kindla värbamisprojekti töökoha suhtes huvi üles näitamisega.  Üks kandidaat võib esitada mitu avaldust samale juriidilisele isikule või mitmele ettevõttele teie organisatsiooni sees.

<a name="recruitment-projects"></a>Värbamisprojektid
--------------------

Värbamisprojektid lubavad värbajatel jälgida ühe või mitme vaba ametikoha täitmist.  Värbamisprojekt tuvastab osakonna ja töö, kus üks või rohkem vabu ametikohti on. Värbamisprojektide kaudu saab vabade ametikohtade osas muuhulgas jälgida järgmist teavet:
-   vabade ametikohtade täpne arv;
-   värbamisjuhi või teise vastutava isiku kontakt, kellega ametikoha asjus suhelda;
-   tellimuse kinnitamise kuupäev;
-   avalduse tähtaeg;
-   eeldatav alguskuupäev.

Värbamisprojekt sisaldab **töötaja iseteeninduses** vaba ametikohta reklaamivat **töökuulutust**. Töötajatele vaba töökoha kohta teabe kuvamiseks peab värbamisprojektil olema **töökuulutus**, väljal**Kuva töötaja iseteeninduses** valitud Jah, **Avalduse tähtaeg** seatud tulevasele kuupäevale ning värbamisprojekti **Projekti olek** Alustatud. Järgmises tabelis loetletakse värbamisprojekti võimalikud olekud ja nende kirjeldus.

| **Olek**    | **Näitab, et …**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Plaanitud | Värbamist valmistatakse ette.  Sellele projektile ei ole värbamine veel alanud. |
| Alustatud   | Selle projekti vabadele töökohtadele võetakse nüüd avaldusi vastu.                    |
| Lõpetatud  | Kõik selle projekti vabad töökohad on täidetud.                                          |
| Tühistatud  | Selle projekti värbamine tühistati.                                           |

Värbajad saavad salvestada ka vaba töökoha reklaamimiseks väljaspool organisatsiooni kasutatud **meediakanaleid**, samuti jälgida projekti või avaldusi jaotises **Arengud**.

<a name="applicants"></a>Kandidaadid
----------

Kandidaat on isik, kes taotleb töökohta teie ettevõttesse.  Kandidaatide jagamine kõigi teie organisatsiooni kuuluvate juriidiliste isikute vahel annab teile hulga talente, kelle hulgast sobivat otsida. Saate säilitada kandidaatide pädevusi, soovitusi, erivajaduse taotlusi ja isikuandmeid. Kandidaadi kirje loomisel luuakse selle kandidaadi isiku kirje globaalses aadressiraamatus. Kandidaatide kohta saate globaalses aadressiraamatus olevat järgmist teavet lehekülje **Kandidaat** abil värskendada:
-   Aadressiteave
-   Kontaktteave
-   tuvastamisteave,
-   Nime üksikasjad
-   Isikuandmed

## <a name="applications"></a>Rakendused
Saadud kandideerimisavalduste teabe saate salvestada leheküljel **Avaldus**. Avaldus näitab kandidaadi huvi teie organisatsioonis töötamise vastu.  Avalduse loomiseks peab kandidaat süsteemis juba kandidaadi või inimesena olemas olema.
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

**Avalduse** vastamistegevus määrab, millist dokumendi- või meilimalli avalduse esitanud kandidaadiga suhtlemiseks kasutatakse. Vastamistegevustega saate seostada **avalduse järjehoidjad**, mis lubavad kasutada kandidaatidega suhtlemisel väärtusi lehekülgedelt Avaldus, Kandidaat, Töövestlus ja Värbamisprojekt.  Teatud avalduse oleku ja vastamistegevuse kombinatsiooniga kandidaatidele saab kiiresti meili saata, kui loote **avalduse meilimallid**. Näiteks võite saata kinnitusmeili kõigile kanditaatidele, kelle **Olek** on Saadud ja **Vastamistegevus** Saadud.  Meili saatmise järel on teil võimalik automaatselt avalduste olekut värskendada.

## <a name="application-routing"></a>Avalduse marsruutimine

Kui avalduse peab läbi vaatama mitu töötajat, siis saate protsessi haldamiseks luua töötaja ringluse loendi, kasutades lehekülge **Avalduse marsruutimine**.

## <a name="interviews"></a>Vestlused

**Töövestlusi kandidaatidega** saab plaanida lehel **Avaldused**.  Kandidaadile ja intervjueerijale planeeritud töövestluse kalendrifaili saatmiseks kasutage nuppu **Koosolekuteabe saatmine**.

## <a name="skill-mapping"></a>Oskuste kaardistamine

Vabale töökohale sobiva kandidaadi tuvastamiseks saate kasutada vorme**Oskuste kaardistamine** ja **Oskuste kaardistamise reeglid**.

## <a name="hiring-applicants"></a>Kandidaatide palkamine

Kandidaadi palkamiseks kasutage lehekülge **Avaldused**. Kandidaadi palkamisel muudetakse avalduse kirje olekuks **Tööle võetud** ja kandidaadi isikukirje globaalses aadressiraamatus seostatakse uue töötaja kirjega. Globaalses aadressiraamatus uue töötaja kirjes tehtud muudatused kuvatakse ka kandidaadi kirjes. See aitab vähendada andmete sisestamiseks kuluvat aega, kui uus töötaja tulevikus ettevõttesiseselt teisele töökohale kandideerib.  Olemasoleva töötaja uuele ametikohale palkamiseks avage lehekülg **Avalduse olek** ja klõpsake üleviimisprotsessi käivitamiseks valikut **Ametikoha muutmine**.






