---
title: Laokande üksikasjad
description: See artikkel annab ülevaate kannete üksikasjade lehest, mis näitab valitud laokande üksikasju.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 55e29d5804f57cd86fb5ddac5d6c5576b7ea5f61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859383"
---
# <a name="inventory-transaction-details"></a>Laokande üksikasjad

Kasutage lehte **Kannete üksikasjad** mis tahes valitud laokande üksikasjade vaatamiseks.

## <a name="open-the-transaction-details-page"></a>Kande üksikasjade lehe avamine

Kannete üksikasjade **lehe avamiseks** järgige neid samme.

1. Minge varude **halduse päringutele \> ja aruannete kannetele \>**.
1. Valige kanne, mida soovite üle vaadata.
1. Tegevuspaanil valige kande **üksikasjad**.

## <a name="fasttabs-overview"></a>Kiirkaartide ülevaade

Kannete **üksikasjade leht** on tükeldatud mitmeks kiirkaardiks. Järgmises tabelis kirjeldatakse iga kiirkaardi eesmärki.

| Kiirkaart | Kirjeldus |
|---|---|
| Üldine | Sellel kiirkaardil kuvatakse valitud laokande põhiteave. Lisaks laokannete lehel kuvatavatele väljadele **sisaldab** see ka täiendavaid välju, mida kirjeldatakse selles artiklis. |
| Uuendused | See kiirkaart näitab teavet, mis on seotud valitud laokande füüsiliste, finantsilisi ja tasakaalustusaspekte. Sõltuvalt kande praegusest olekust, võivad mõned väljad olla tühjad. Need väljad seatakse kannete sisestamisel automaatselt. Lisaks laokannete lehel kuvatavatele väljadele sisaldab **see** kiirkaart täiendavaid välju, mida kirjeldatakse selles artiklis hiljem. |
| Pearaamatu sisestused | See kiirkaart näitab sisestamise tüüpi ja pearaamatu kontot, mida kasutatakse valitud laokandega seotud füüsiliseks uuendamiseks, finantsiliseks uuendamiseks, füüsiliseks tuluks, füüsilisteks kuludeks, finantskuludeks ja finantskuludeks. |
| Viited | See kiirkaart näitab lisateavet valitud laokande loonud lähtekande kohta. Näiteks võib see teave sisaldada üksikasju ostutellimusest või müügitellimusest. |
| Seostuv teave | See kiirkaart kuvab täiendavat teavet valitud laokande kohta. Neid välju ei saa seada, kui te ei kasuta mõnda funktsiooni, nt hankekategooriaid või projekte. |
| Finantsdimensioonid – füüsiline | See kiirkaart näitab finantsdimensiooni väärtusi, mida kasutati füüsilise värskenduse sisestamisel. Kui füüsilist värskendust pole sisestatud, on väljad tühjad. |
| Finantsdimensioonid – finantsid | See kiirkaart näitab finantsdimensiooni väärtusi, mida kasutati finantsvärskenduse sisestamisel. Kui finantsvärskendust pole sisestatud, on väljad tühjad. |
| Varude dimensioonid | See kiirkaart näitab varude dimensiooni väärtusi, mis on määratud valitud laokandele. Need väärtused hõlmavad laoala, ladu, suurust, värvi, konfiguratsiooni, asukohta, partiinumbrit, seerianumbrit, varude olekut, litsentsiplaati ja omanikku. |

## <a name="fields-on-the-general-fasttab"></a>Kiirkaardi Üldine väljad

Järgmises tabelis kirjeldatakse väljasid kiirkaardil **Üldine**, mida ei kuvata ka laokannete **lehel**.

| Väli | Kirjeldus |
|---|---|
| Osapool | Valitud laokandega seotud osapoole nimi. Näiteks ostutellimuse kandes kuvatakse ostutellimusel hankija nimi ja müügitellimuse kandes kuvatakse kliendi nimi. See väli ei ole saadaval igat tüüpi laokannete puhul. |
| Lao viide | Kui valitud laokandega on seotud teine laokanne, siis selle teise kande tüüp. Näiteks kui ostutellimus on müügitellimuse vastu märgitud, **seatakse** ostutellimuse kande laoviite välja väärtuseks *Müügitellimus*. Otsetarne tellimuste ja kontsernisiseste tellimuste märkimine toimub automaatselt. Kui kasutate märkimist muude kuluarvestusmeetoditega *kui standardkulu* *ja* liikuva keskmisega, loob süsteem tasakaalustused ja korrektsioonid täpsetele kannetele, mis on märgitud. Sel viisil saate saavutada "tegeliku" kuluarvestuse, mis alistab FIFO-loogika. LIFO; või kaalutud keskmine. |
| Laonumber | Konkreetne kanne, mis on seotud valitud laokandega. Näiteks kui ostutellimus on müügitellimuse suhtes märgitud, **seatakse** ostutellimuse kande laonumbri välja väärtuseks müügitellimuse number. |
| Projekti ID | Kui valitud laokanne on seotud projektiga, seatakse selle välja väärtuseks projekti number. |
| Saatepartii ID | Partii kordumatu ID, mille süsteem on määranud valitud laokandele. |
| Viitepartii | Kui valitud laokandega on seotud teine laokanne, siis selle teise kande saatelehe ID. Näiteks kui ostutellimus on märgitud müügitellimuse suhtes, **·** **on ostutellimuse kande viite saatelehe väli müügitellimuse rea laokande saatelehe ID** väärtus. |
| Dimensiooni number | Kordumatu ID, mis esindab kõigi valitud laokandele määratud varude dimensiooniväärtuste kombinatsiooni. |
| Avatud väärtus | Väärtus, mis näitab, kas valitud laokanne on lao sulgemise protsessis tasakaalustatud. Kui see väli on seatud väärtusele *Jah*, pole kannet tasakaalustatud. |
| Eeldatav kuupäev | Sissetulekukannete puhul kuupäev, mil lao sissetulekut eeldatavasti esineb. Näiteks võib see väli näidata varude blokeerimistellimuse eeldatavat vastuvõtukuupäeva või ostutellimuse rea tarnekuupäeva. |
| Lao kuupäev | See väli seadistatakse siis, kui registreerimiskanne tehti sissetulekuorderil enne füüsilise sissetuleku sisestamist. |
| Mitterahaline üleviimine | Väärtus, mis näitab, kas valitud laokanne on mitterahaline ülekanne. Mitterahaline ülekanne leiab aset, kui varude dimensioonide muudatust ei jälgita finantsiliselt kauba **mudeligrupi** lehel. |
| Üleviimise saatepartii ID | Kui valitud laokanne ei ole finantsiline ülekanne, seadistatakse selle välja väärtuseks saatelehe ID **väärtus teises laokandes,** millega valitud kanne tasakaalustatakse. |

## <a name="fields-on-the-updates-fasttab"></a>Värskenduste kiirkaardi väljad

Järgmises tabelis kirjeldatakse kiirkaardi Uuendused **välju**, mida ei kuvata ka laokannete **lehel**.

| Väli | Kirjeldus |
|---|---|
| Füüsiline kanne | Pearaamatu kandenumber, kus loodi valitud laokande füüsiline sisestamine. |
| Marsruut | Valitud laokandega seotud protsess. See väli seadistatakse ainult tootmise komplekteerimislehe kannetele, kus kooslus või valemi rida on seotud kindla kaubaga. |
| Saateleht | Ostutellimuse toote sissetuleku kande jaoks sisestatud saatelehe number. |
| Füüsiline omahind | Summa, mis sisestati füüsiliseks uuendamiseks pearaamatusse. Standardkulu toote puhul näitab see summa standardkulu. Muude kuluarvestusmeetodite puhul näitab see toote kaalutud keskmist sisestamise ajal. |
| Füüsiline tulu | Füüsiliseks uuendamiseks pearaamatusse sisestatud viittulu summa. |
| Koorma ID | Kui praegune kanne on seotud transpordihalduse koormaga, kuvatakse sellel väljal kauba kaasanud koorma kordumatu number. |
| Füüsiliselt sisestatud | Väärtus, mis näitab, kas valitud laokanne on füüsiliselt sisestatud. Kui praegune kanne sisestatakse pearaamatusse, on olemas ka füüsiline kanne. |
| Finantsiliselt sisestatud | Väärtus, mis näitab, kas valitud laokanne on finantsiliselt sisestatud. Kui praegune kanne sisestatakse pearaamatusse, on olemas ka finantskanne. |
| Sisestatud füüsiline tasu | Väärtus, mis näitab, kas valitud laokandega seotud füüsilised kulud on sisestatud. |
| Sisestatud finantstasu | Väärtus, mis näitab, kas valitud laokandega seotud finantskulud on sisestatud. |
| Finantskanne | Pearaamatu kandenumber, kus finantsi sisestamine loodi. |
| Arve | Arve number, mis loodi näiteks ostutellimuse või müügitellimuse jaoks. |
| Korrigeerimine | Summa, mida korrigeeriti valitud laokandel lao sulgemise ja korrigeerimise protsessist. |
| Kasum ja kahjum, sisestatud summa | Kasumi- ja kahjumiaruandesse sisestatud valitud laokande summa. |
| Sisestamata arve | Seotud ostutellimuse arve number, mis kuvatakse ootel **hankija arve lehel**. |
| Finantsiliselt suletud | Kande täieliku tasakaalustamise kuupäev. |
| Kaetud tegeliku kaalu kogus | Tasakaalustusega kaetud tegeliku kaalu kogus |
| Tasakaalustatud kogus | Valitud laokande jaoks tasakaalustatud kogus. |
| Tasakaalustatud summa | Valitud laokande jaoks tasakaalustatud väärtus. |
