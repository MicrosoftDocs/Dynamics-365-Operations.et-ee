---
title: Tööajaarvestuse registreerimise ülevaade
description: Kellaaja registreerimisega töötajad saavad sisestada erinevat tüüpi kellaaja registreerimisi, näiteks sisse ja välja registreerimine, kaudsete tegevuste ja puudumiste registreerimine. See teema kirjeldab registreerimisi, nende arvutamist, kinnitamist ja töövoo kasutamist ajatabelite kinnitamise protsessile struktuuri ja automaatse kinnitamise lisamiseks.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr, JmgRegistrationSetup, JmgStampTrans, JmgStampJournalTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "53351"
- intro-internal
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f6b3f682906dacc4e284b77e75e0c6dc99b2e06
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336927"
---
# <a name="time-and-attendance-registration-overview"></a>Tööajaarvestuse registreerimise ülevaade

[!include [banner](../includes/banner.md)]

Kellaaja registreerimisega töötajad saavad sisestada erinevat tüüpi kellaaja registreerimisi, näiteks sisse ja välja registreerimine, kaudsete tegevuste ja puudumiste registreerimine. See teema kirjeldab registreerimisi, nende arvutamist, kinnitamist ja töövoo kasutamist ajatabelite kinnitamise protsessile struktuuri ja automaatse kinnitamise lisamiseks.

## <a name="registrations"></a>Registreerimised

Tööajaarvestust kasutatavates ettevõtetes peavad töötajad registreerima tööl viibitud aja ja kohaloleku. Mõnes ettevõttes võidakse nõuda töötajatelt ainult sisse- ja väljaregistreerimisaja registreerimist. Teistes ettevõtetes, võidakse nõuda töötajatelt ka tegeliku tööaja ja puhkepauside registreerimist. Tööajaarvestuse sihtkasutajad on järgmised.

- Töötajad, kes peavad registreerima aja ja kohaloleku regulaarse intervalliga, näiteks kord päevas, kord nädalas või kord kahe nädala järel.
- Ülevaatajad, juhid ja palgaarvestajad, kes arvutavad, kinnitavad ja edastavad töötaja registreerimised edasiseks töötlemiseks.

| **Märkus.**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kui käivitate tööajaarvestuse koos tootmisega, salvestatakse kõik registreerimised projektides, projektitegevustes, kaudsetes tegevustes, puudumiskoodides ning ületunnitöödes ja paindajas ning neid kasutatakse mõlemas moodulis palga arvutamiseks. |

## <a name="time-registrations-workers"></a> Ajalise registreerimisega töötajad

Aja ja puudumiste registreerimiseks tuleb töötajad seadistada ajalise registreerimisega töötajatena ettevõttes, kus nad töötavad.

Pärast seadistamist saavad töötajad sisestada erinevat tüüpi registreerimisi.

- Sisse- ja väljaregistreerimine tööle saabumisel või sealt lahkumisel.
- Aja- ja kaubatarbimine tootmistöödel.
- Masina kasutamise aeg tootmises, kui masin on määratletud ressursina.

| **Märkus.**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Töötajale saab automaatselt määrata tootmises konkreetsel masinal tehtud ajaregistreerimised, kui töötaja otsustab tootmistööd alustades töötada masina assistendina. |

- Ajalised registreerimised projektides ja projektitegevustes.
- Projektitasude ja kaubatarbimise registreerimine vastavate projektitasu töölehtede ja projekti kauba töölehtede kaudu.
- Planeeritud puudumine.
- Puudumine tööle hilinemisel või plaanitust varem lahkumisel.
- Tööpausid, kas käsitsi registreeritud või süsteemis automaatselt arvutatud.
- Kaudsed tootmisega mitteseotud tegevused, millega töötaja võib tööpäeva jooksul tegeleda. Need tegevused on näiteks koosolekud või töökoha koristamine.
- Ületunnitöö, mille saab registreerida kas lisatundide, paindaja või ületunnitööna.

## <a name="adding-clock-out-registrations"></a>Väljaregistreerimiste lisamine

Kui töötaja unustab tööpäeva lõpul välja registreeruda, saab puuduva registreerimise lisada pakett-töö käitamisega. Süsteemi võrdleb sisseregistreerimise ja väljaregistreerimise aega töötaja seostatud profiiliga ning sisestab puuduva väljaregistreerimisaja automaatselt, et ühitada see profiili lõppajaga. Nii sisse- kui ka väljaregistreerimised on väga olulised järgnevaks arvutuseks ja ajaliste registreerimiste kinnitamiseks, enne kui need saab palgaarvestusse üle kanda.

## <a name="calculating-registrations"></a>Registreerimiste arvutamine

Registreerimisel määratakse töötaja arvutusgruppi, mis seostub tavaliselt kindla töörühma, vahetuse või töögrupiga. Tavaliselt kinnitab töötajate tehtud registreerimised töörühma juht või ülevaataja ja vastutab seega ka iga päev vastavate arvutusgruppide arvutamise käitamise eest. Arvutamisprotsessi osana saab töörühma juht või ülevaataja teha järgmist.

- Ekslike registreerimiste korrigeerimine. Näiteks saab ta muuta vahetusekoode ja korrigeerida tootmistööde tagasisidet.
- Puuduvate registreerimiste lisamine. Näiteks saab ta luua väljaregistreerimisi ja luua puudumiskandeid.
- Valede registreerimiste kustutamine.

Kuna registreeritud aeg peab vastama töötaja ajaprofiiliga enne registreerimiste arvutamist, peate tühistama tööajaprofiili iga töötaja puhul, kellele kehtib tema standardse tööajaprofiili jaoks erand. Juhul kui töötaja profiil on päevane vahetus ja töötaja on nõustunud töötama ilma ületunnitasuta öövahetuses, peab töörühma juht või ülevaataja tühistama töötaja vaikeprofiili, et arvutada tööaeg standardse öötöötasu, mitte ületunnitasu alusel. Arvtuses kuvatakse ka tõrge, kui puudumise registreerimise puudub. See tuleb arvutuse lõpuleviimiseks lisada.

## <a name="approving-registrations"></a>Registreerimiste kinnitamine

Kinnitusgrupi määramine ajalise registreerimisega töötajale toimub samamoodi kui arvutusgrupi määramine. Tavaliselt kehtib grupp kindla töörühma, vahetuse või töögrupi kohta. Peate õigesti (tõrgeteta) arvutatud registreerimised kinnitama, enne kui saate luua tasuüksusi, mille saab seejärel üle kanda palgaarvestussüsteemi. Tavaliselt kinnitab registreerimised palgaarvestuse administraator ja tal on võimalik enne kinnitamist teha järgmist.

- Üksikute töötajate palgalepete tühistamine.
- Käsitsi preemiate lisamine.
- Lisateabe sisestamine puudumiste registreerimiste kohta.

| **Märkus.**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kui mõnele töötajale on arvestatud ületunnitöö, saab selle jaotada konkreetsetele päeva jooksul sooritatud töödele. See on oluline, kui töö kulu arvutatakse töötajate tasu alusel. |

## <a name="approving-registrations-using-workflow"></a> Registreerimiste kinnitamine töövoo abil

Saate seadistada töövoo kinnitamise protsessi, mis kinnitab töövooreeglitele vastavad registreerimised automaatselt, jättes ainult kõrvalekalded käsitsi töötlemiseks. Kui töövookinnitus aktiveeritakse, esitab töörühma juht või ülevaataja arvutatud registreerimised kinnitamiseks. Töövooprotsess loob asjakohased kinnitused ja ülesanded ning määrab need õigetele kasutajatele ja rollidele nii, nagu töövoos on määratud. Tööajaarvestuse jaoks on kaks töövookinnitust.

| Töövoog                                  | Eesmärk                                                                                                   | Registreerimise tüüp                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tööajaarvestuse päevade koguarv            | Töövoog kontrollib registreerimise näiteks päeva eeldatava töötundide arvu suhtes. |                                                                                                                                                                                                                                                       |
| Tööajaarvestuse töölehe registreerimine. | Töövoog kontrollib iga registreerimistüübi puhul registreerimise kuupäeva.                           | Tööajaarvestus • sisseregistreerimine • väljaregistreerimine • puudumine • puhkepaus • lülituse kood • projekt • projektitegevus • kaudse tegevuse tootmistööd • järjekord enne • seadistus • protsess • kattumine • transport • järjekord pärast • alustusabi • lõpetusabi |

## <a name="transferring-approved-registrations"></a>Kinnitatud registreerimiste ülekandmine

Pärast registreerimiste kinnitamist saate need üle kanda perioodilisse palgatöösse. Ülekantud registreerimine sisestatakse mis tahes sellega seotud tegevusse või töösse, näiteks tootmistellimusse või projekti. Palgakanded luuakse iga töötaja kohta registreerimiste põhjal.  

## <a name="reversing-transferred-registrations"></a>Ülekantud registreerimiste tühistamine

Kannete tühistamise ülesanne (nende tagasipööramine) on võimalik kuni palgaperioodi tasu ülekandmiseni. See tähendab, et palgaandmed on üle kantud välisfaili. Tühistamise korral võetakse kõik registreerimised tagasi ja kõik tootmistellimustesse või projektidesse sisestatud kanded tühistatakse tasakaalustuskannetega ja neutraliseeritakse.

| **Märkus.**                                                 |
|----------------------------------------------------------|
| Välisfaili saab importida palgaarvestussüsteemi. |

## <a name="registrations-in-electronic-timecards"></a>Registreerimised elektroonilistel kellakaartidel

Töötajaid, kelle tööülesanded ei nõua kohest tagasisidet, näiteks tootmistööde puhul, kuid kes töötavad projektitegevustega, saavad kasutada elektroonilist kellakaarti. Elektroonilised kellakaardid pakuvad registreerimiste sisestamisel paindlikkust – saate seda teha mis tahes ajal ja oma ärigraafiku järgi sobivaimal viisil: kord päevas, kord nädalas või siis, kui töötaja on kontoris tagasi. Elektrooniliste kellakaartide või nende töötajate kasutamiseks peate määrama töötaja üksikasjades suvandi Kasuta kellakaarti. Elektroonilised kellakaartdid võimaldavad töötajal registreerida järgmist.

- Kuupäev
- Registreerimise tüüp
- Töö viide, nagu projekt, kaudne tegevus või tootmistellimus
- Töö ID
- ajatarbimine.
- Projekti tasud
- Projekti kaubad

[!INCLUDE[footer-include](../../includes/footer-banner.md)]