---
title: Värbamisprotsesside haldus
description: Selles teemas kirjeldatakse kontseptsiooni, mida värbajad saavad värbamisprotsessi sammude jälgimiseks kasutada.
author: andreabichsel
ms.date: 01/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: anbichse
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fa1d5201fcc52d49b9d954356f1ca39b7619cd2
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075471"
---
# <a name="manage-recruiting-processes"></a>Värbamisprotsesside haldus

> [!IMPORTANT]
> Selles teemas märgitud funktsioonid on praegu saadaval inimressursside klientidele finance infrastruktuuris.  


See teema kirjeldab võimalusi, kuidas värbajad saavad jälgida värbamise etappe, sh vabade ametikohtade reklaamimiseks ja kandidaatide värbamiseks, kandidaadi ja avalduse teabe jälgimiseks, kandidaatide intervjueerimiseks ja vaba ametikoha täitmiseks ühe või mitme kandidaadi väljavalimiseks tehtud pingutusi.

## <a name="overview"></a>Ülevaade

Värbamisprojektid aitavad organiseerida juriidilise isiku vabade ametikohtade täitmise etappe. Kandidaat on isik, kes taotleb töökohta teie ettevõttesse. Avaldus näitab kandidaadi huvi ettevõttes töötamise vastu ja võib olla seotud kindla värbamisprojekti töökoha suhtes huvi üles näitamisega. Üks kandidaat võib esitada mitu avaldust samale juriidilisele isikule või mitmele ettevõttele teie organisatsiooni sees.

## <a name="recruitment-projects"></a>Värbamisprojektid

Värbamisprojektid lubavad värbajatel jälgida ühe või mitme vaba ametikoha täitmist. Värbamisprojekt tuvastab osakonna ja töö, kus üks või rohkem vabu ametikohti on. Värbamisprojektide kaudu saab vabade ametikohtade osas muuhulgas jälgida järgmist teavet:

- vabade ametikohtade täpne arv;
- värbamisjuhi või teise vastutava isiku kontakt, kellega ametikoha asjus suhelda;
- tellimuse kinnitamise kuupäev;
- avalduse tähtaeg;
- eeldatav alguskuupäev.

Värbamisprojekt sisaldab **töökuulutamisväärtust**, mida kasutatakse **lehel Töötaja iseteenindus** avamise reklaamimiseks. Avamist saab töötajatele kuvada ainult juhul, kui värbamisprojektil **on projekti reklaamiväärtus**, **välja Kuva töötaja iseteeninduses** väärtuseks **on seatud Jah**, **väljal Kandideerimise tähtaeg** on seatud tulevasele kuupäevale ja värbamisprojekti **projekti oleku** väärtus **Alustatud**. Järgmises tabelis loetletakse värbamisprojekti võimalikud olekud ja nende kirjeldus.

| Olek    | Näitab, et …                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Plaanitud | Värbamist valmistatakse ette. Sellele projektile ei ole värbamine veel alanud. |
| Alustatud   | Selle projekti vabadele töökohtadele võetakse nüüd avaldusi vastu.                   |
| Lõpetatud  | Kõik selle projekti vabad töökohad on täidetud.                                         |
| Tühistatud  | Selle projekti värbamine tühistati.                                          |

Värbajad saavad salvestada ka vaba töökoha reklaamimiseks väljaspool organisatsiooni kasutatud **meediakanaleid**, samuti jälgida projekti või avaldusi jaotises **Arengud**.

## <a name="applicants"></a>Kandidaadid

Kandidaat on isik, kes taotleb töökohta teie ettevõttesse. Taotlejad jagatakse kõigi teie organisatsiooni juriidiliste isikute vahel. Seetõttu on teil suur hulk talente, mida otsida. Saate säilitada kandidaatide pädevusi, soovitusi, erivajaduse taotlusi ja isikuandmeid. Kandidaadi kirje loomisel luuakse selle kandidaadi isiku kirje globaalses aadressiraamatus. Kandidaatide kohta saate globaalses aadressiraamatus olevat järgmist teavet lehekülje **Kandidaat** abil värskendada:

- Aadressiteave
- Kontaktteave
- tuvastamisteave,
- Nime üksikasjad
- Isikuandmed

## <a name="applications"></a>Rakendused

Saadud kandideerimisavalduste teabe saate salvestada leheküljel **Avaldus**. Avaldus näitab kandidaadi huvi teie organisatsioonis töötamise vastu. Avalduse loomiseks peab kandidaat süsteemis juba kandidaadi või inimesena olemas olema.

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

Rakenduse kirjavahetuse toiming määrab dokumendi või e-posti malli, mida kasutate taotluse esitanud taotlejaga suhtlemiseks. Seostades rakenduse järjehoidjaid **kirjavahetustoimingutega, saate taotlejatega suhtlemisel kasutada rakenduse**, **kandidaadi**, **intervjuu** ja **värbamisprojekti** lehtede väärtusi **.** **Luues kirjavahetustoimingute jaoks rakenduse e-posti malle**, saate kiiresti saata e-kirju taotlejatele, kelle rakendustel on konkreetne oleku ja kirjavahetuse tegevuse kombinatsioon. Näiteks saate saata kinnitusmeili kõigile rakendustele, mille **olekuväärtus** **on Vastuvõetud** ja **kirjavahetuse** toimingu **väärtus Received**. Pärast meilisõnumi saatmist on teil võimalus rakenduste olekut automaatselt värskendada.

## <a name="application-routing"></a>Avalduse marsruutimine

Kui avalduse peab läbi vaatama mitu töötajat, siis saate protsessi haldamiseks luua töötaja ringluse loendi, kasutades lehekülge **Avalduse marsruutimine**.

## <a name="interviews"></a>Vestlused

**Töövestlusi kandidaatidega** saab plaanida lehel **Avaldused**. Kandidaadile ja intervjueerijale planeeritud töövestluse kalendrifaili saatmiseks kasutage nuppu **Koosolekuteabe saatmine**.

## <a name="skill-mapping"></a>Oskuste kaardistamine

Vabale töökohale sobiva kandidaadi tuvastamiseks saate kasutada vorme **Oskuste kaardistamine** ja **Oskuste kaardistamise reeglid**.

## <a name="hiring-applicants"></a>Kandidaatide palkamine

Kandidaadi palkamiseks kasutage lehekülge **Avaldused**. Kandidaadi palkamisel muudetakse avalduse kirje olekuks **Tööle võetud** ja kandidaadi isikukirje globaalses aadressiraamatus seostatakse uue töötaja kirjega. Globaalses aadressiraamatus uue töötaja kirjes tehtud muudatused kuvatakse ka kandidaadi kirjes. See aitab vähendada andmete sisestamiseks kuluvat aega, kui uus töötaja tulevikus ettevõttesiseselt teisele töökohale kandideerib. Olemasoleva töötaja uuele ametikohale palkamiseks avage lehekülg **Avalduse olek** ja klõpsake üleviimisprotsessi käivitamiseks valikut **Ametikoha muutmine**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
