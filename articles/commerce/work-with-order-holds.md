---
title: Konfigureerimine ja töötamine kõnekeskuse tellimuste ootelolekutega
description: Selles teemas kirjeldatakse, kuidas töötada tellimuste ootelolekutega rakenduses Dynamics 365 Commerce.
author: josaw1
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans, MCROrderEventSetup, MCROrderEventTable
audience: Application User
ms.reviewer: josaw
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f474b5936f2ae154ad54185becd91865642e8efe3cf10e7dcdbb650c6c833b21
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762592"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Kõnekeskuse tellimuse ootelolekute konfigureerimine ja nendega töötamine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse tellimuse ooteloleku funktsioone, mida saab rakenduses Dynamics 365 Commerce kasutada kõnekeskuse tellimuste jaoks.

## <a name="configuring-call-center-order-holds"></a>Kõnekeskuse tellimuse ootelolekute konfigureerimine

Kõnekeskuse tellimuse ooteloleku funktsioonide kasutamiseks peate esmalt määratlema ooteloleku koodid. Kasutaja määratletud ooteloleku koodide kogumi loomiseks teie ettevõtte vajaduste põhjal avage **Müük ja turundus** \> **Häälestamine** \> **Müügitellimused** \> **Tellimuse ooteloleku koodid**. Saate soovi korral märkida ühe ooteloleku koodi lipuga, et kasutada seda ooteloleku vaikekoodina, määrates suvandi **Müügitellimuste vaikesäte** olekuks **Jah**. Seda ooteloleku koodi kasutatakse iga kord, kui müügitellimus pannakse ootele. Kui müügitellimusel on reserveeritud kaubavaru ja reserveeringud tuleb automaatselt eemaldada, kui tellimus pannakse ootele teatud põhjusel, määrake põhjusekoodide jaoks suvandi **Eemalda varude reserveerimised** olekuks **Jah**.

Et määrata märkme tüüp, mis hõivatakse, kui kasutajad, kes panevad müügitellimuse ootele, sisestavad valikulisi märkmeid, avage **Müügireskontro** \> **Häälestamine** \> **Müügireskontro parameetrid** ja seejärel määrake kiirkaardil **Müügihäälestus** vahekaardil **Üldine** väli **Märkuse tüüp**. Kasutage välja **Ootel müügitellimuse olek**, et määrata värv, mida kasutatakse ootel olevate müügitellimuste esiletõstmiseks, kui neid vaadatakse lehel **Klienditeenindus**.

Ooteloleku põhjusekoodide valikulise kogumi loomiseks avage **Jaemüük ja kaubandus** \> **Kanali häälestus** \> **Teabekoodid**. Neid teabekoode saab kasutada teisese põhjusekoodina peamise ooteloleku koodi täpsemaks määratlemiseks. Valige **Uus**, et luua põhjusekoodide kogum, ja seejärel valige **Alamkoodid**, et määratleda täiendavate põhjuste loend. Määratletud teabekoodide linkimiseks kõnekeskuse kanaliga avage **Jaemüük ja kaubandus** \> **Kanalid** \> **Kõnekeskused** \> **Kõik kõnekeskused**. Kiirkaardil **Üldine** määrake väli **Ooteloleku kood**.

## <a name="putting-orders-on-hold"></a>Tellimuste panemine ootele

Tellimusi, mille kõnekeskuse kasutajad loovad kaupluse kontori rakenduse Commerce programmis, saab konkreetsetes olukordades panna ootele käsitsi või automaatselt.

Tellimuse sisestamise ajal, kuid enne tellimuse esitamist ja kinnitamist, võib kõnekeskuse kasutajatel tekkida soov panna tellimus käsitsi ootele, et vältida selle väljastamist lattu edasiseks töötlemiseks. Näiteks võib juhtuda, et tellimust esitav klient ei ole selle kinnitamiseks valmis või kriitilised andmed, mida on vaja tellimuse töötlemiseks, on puudu.

Kõnekeskuse kasutaja saab tellimuse sisestamise lehel panna tellimuse ootele, kasutades tellimuse sisestamise menüüs vahekaardil **Müügitellimus** suvandit **Ootelolevad tellimused**. Teise võimalusena saab kasutaja kasutada menüükäsku **Pane ootele** lehel **Müügitellimuse kokkuvõte**, mis kuvatakse, kui ta valib kõnekeskuse müügitellimusel käsu **Vii lõpule**.

Mõlemal juhul kuvatakse leht **Ootelolevad tellimused**. Kasutaja saab seejärel valida käsu **Uus**, et panna tellimus ootele. Väljal **Ooteloleku kood** peab kasutaja valima koodi, mis kirjeldab kõige paremini ooteloleku põhjust. Väljal **Põhjuse kood** saab kasutaja soovi korral valida täiendava koodi, et lisada ootelepaneku teise taseme põhjus.

Kiirkaardil **Märkmed** saab kasutaja väljal **Ooteloleku märkmed** sisestada täiendavaid, vabas vormis märkmeid, et lisada ootelepaneku kohta lisakonteksti või -teavet. Need märkmed abistavad teisi kasutajaid, kes vaatavad ootele pandud tellimuse hiljem üle või töötavad sellega.

Kui ooteloleku teave on sisestatud ja salvestatud, saab kasutaja lehe **Ootelolevad tellimused** sulgeda. Seejärel saadetakse kasutaja tagasi müügitellimuse sisestamise lehele. Kui müügitellimusega ei ole rohkem midagi vaja teha, võib kasutaja müügitellimuse sisestamise lehe sulgeda.

Kui kõnekeskuse kanalil on lipp **Tellimuse lõpetamise lubamine** sisse lülitatud, ei tule ootele pandud tellimusele makset rakendada. Kuid müügitellimuse korral, mis pole ootele pandud, ei saa kasutajad müügitellimuse sisestamise lehelt lahkuda enne, kui makse on rakendatud. Muidugi tuleb makse rakendada enne, kui tellimuse ootel olek vabastatakse.

Lisaks saavad kõnekeskuse kasutajad mingil põhjusel kahtlaseid tellimusi pettuse ohu tõttu käsitsi ootele panna. Tellimusi saab ka automaatselt ootele panna, kui need vastavad aktiivsetele pettuse kriteeriumidele ja reeglitele. Lisateavet tellimuse ooteloleku selle tüübi kohta vt teemast [Pettuseteatiste seadistamine](/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Ootel olevate tellimuste vaatamine ja haldamine

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Üksiku müügitellimuse ooteloleku teabe vaatamine

Lehel **Klienditeenindus** saavad kasutaja visuaalselt tuvastada ootel olevaid tellimusi, sest tellimuse read on kindla värviga esile tõstetud. See värv on määratletud väljaga **Ootel müügitellimuse olek** lehel **Müügireskontro parameetrid**.

> [!NOTE]
> Kui lehel valitakse rida, ei ole esiletõstu värv nähtav.

Kasutajad saavad vaadata ka müügitellimuse üksikasjalikku olekuteavet, et näha, kas tellimus on ootel. Üksikasjalikku olekuteavet saab vaadata lehel **Kõik müügitellimused** või **Klienditeenindus**. Kui tellimus on ootel, on selle jaoks määratud lipp **Ära töötle** ja välja **Üksikasjalik olek** olek on kas **Ootel** või **Pettusest tulenev ootelolek**, olenevalt stsenaariumist.

Kasutajad saavad üksiku tellimuse ooteloleku üksikasjade vaatamiseks avada lehelt **Klienditeenindus** lehe **Ootelolev tellimus** üksikasjaliku vaate, kasutades valitud tellimuse jaoks menüüd **Suvandid**. Kasutajad pääsevad sellele vaatele juurde ka lehelt **Kõik müügitellimused**, valides vahekaardil **Müügitellimus** menüükäsu **Ootelolevad tellimused**.

### <a name="viewing-all-orders-that-are-on-hold"></a>Kõigi ootel olevate tellimuste vaatamine

Kõigi käsitsi või automaatselt ootele pandud tellimuste vaatamiseks avage **Jaemüük ja kaubandus** \> **Kliendid** \> **Ootelolevad tellimused**.

Töölaud **Ootelolevad tellimused** kuvab loendivaate kõigist tellimustest, mis on pandud ootele käsitsi või pettuse tõttu. Kasutajad saavad lehel olevate standardsete filtreerimis- ja päringusuvandite abil luua vaateid, mis võimaldavad neil kasutada või hallata kindlaid ooteloleku koode, mille ülevaatamise eest nad vastutavad. Töölaud **Ootelolevad tellimused** kuvab ka päevade arvu, mille jooksul tellimus on ootel olnud. See teave aitab kasutajatel järjekorda prioriseerida.

Ootel olevate tellimuste üksikasjalikuma vaate nägemiseks saavad kasutajad menüüs klõpsata suvandil **Ootelolev tellimus**. See vaade sisaldab teavet kliendi kohta ning märkmeid, mis on lisatud tellimusele, kliendile või ootelepaneku tegevusele. Vaade näitab ka teavet automaatselt ootele paneku põhjuse kohta, kui tellimus pandi ootele, sest see vastas pettuse reeglile.

Kasutajad saavad nii loendivaates kui ka lehe **Ootelolevad tellimused** üksikasjalikumas vaates vaadata või lisada täiendavat tellimusega seotud teavet, nagu maksed, kogusummad ja märkmed.

Suvandid vahekaardil **Väljaregistreerimise ootelepanek** võivad osutuda kasulikuks, kui mitu kasutajat teie ettevõttes töötavad ooteloleku järjekorraga samal ajal. Suvandi **Registreeri välja** valimisega saavad kasutajad näidata, et nad töötavad tellimuse ootelepaneku ülevaatamise ja uurimise kallal. Sel viisil ei raiska teised kasutajad aega sama töö tegemise üritamisega. Lehe **Ootelolevad tellimused** üksikasjalikumas vaates saavad kasutajad vaadata teavet väljaregistreerimise kuupäeva ja kellaaja ning ootelolekukirje väljaregistreerinud kasutaja kohta.

Kui ootelolekukirje on välja registreeritud, saab väljaregistreerimise tühjendada ainult selle välja registreerinud kasutaja. See piirang takistab kasutajatel nende kirjete võtmist, mille kallal teised kasutajad juba töötavad. Tellimuse vabastamiseks tagasi järjekorda, et teised kasutajad saaksid sellega töötada, peab kirje väljaregistreerinud kasutaja valima suvandi **Tühjenda väljaregistreerimine**.

> [!NOTE]
> Ootelolekut ei vabastata, kui väljaregistreerimine on tühjendatud.

Mõnes olukorras, nt kui kasutaja on haiguslehel või ettevõttest lahkunud, võib juhtuda, et sellele kasutajale väljaregistreeritud kirjed tuleb teisele kasutajale ümber määrata. Juht saab kirjeid ümber määrata, kasutades suvandit **Väljaregistreerimise alistamine**.

## <a name="releasing-orders-that-are-on-hold"></a>Ootel olevate tellimuste vabastamine

Nii loendivaates kui ka lehe **Ootelolevad tellimused** üksikasjalikumas vaates sisaldab vahekaart **Eemalda ootelolek** suvandeid, mida kasutatakse tellimuse ooteloleku vabastamiseks. Kasutage suvandit **Tühjenda ootelolekud**, et vabastada tellimus valitud ooteloleku koodist.

Kõnekeskuse tellimused nõuavad makset. Seetõttu ei saa ootelolekut täielikult enne tühjendada, kui tellimusele on rakendatud makse. Veenduge, et lehel **Kõnekeskuse parameetrid** vahekaardil **Ootel** oleks parameeter **Esita tühjendamisel** sisse lülitatud. See säte aitab tagada, et tühjendatud ootelolev tellimus läheb maksete kinnitamiseks ja autoriseerimiseks läbi õige tellimuse esitamise loogika. Kui maksed on puudu, saab kasutaja tõrke ja ooteloleku koodi ei tühjendata.

Kui parameeter **Esita tühjendamisel** on määramata, peaksid kasutajad valima suvandi **Eemalda ja saada** menüüst **Eemalda ootelolek**, et tagada, et tellimus läheb läbi kõigi nõutud maksekinnituste. Kui tellimuse esitamine nurjub, kui lipp **Tellimuse lõpetamise lubamine** on kõnekeskuse kanalil sisse lülitatud, vabastatakse tellimus ootelolekust, kuid lippu **Ära töötle** ei eemaldata. Seetõttu ei väljastata tellimust lattu enne, kui õiged maksed on rakendatud ja kinnitatud.

Kui kasutajad soovivad ooteloleku tühjendada, kuid teevad tellimusele enne selle väljastamist edasiseks töötlemiseks täiendavaid muudatusi, saavad nad valida suvandi **Eemalda ja muuda**. See suvand eemaldab ooteloleku koodi ja avab müügitellimuse üksikasjad, nii et kasutajad saavad tellimusele teha lisamuudatusi. Kasutajad saavad ka rakendada makse ja esitada müügitellimuse makse kinnitamise loogika kaudu, kui lipp **Tellimuse lõpetamise lubamine** on kõnekeskuse kanalil sisse lülitatud.

## <a name="reporting-options"></a>Aruandlusvalikud

Avage **Jaemüük ja kaubandus** \> **Päringud ja aruanded** \> **Kõnekeskuse aruanded** \> **Tellimuse ootelolekute aruanne**, et käivitada aruanne tellimuste ooteloleku kohta kuupäevavahemiku, ooteloleku koodi või muude valitud kriteeriumide alusel.


[!INCLUDE[footer-include](../includes/footer-banner.md)]