---
title: "Ristlaadimine tootmistellimustest lähetusaladesse"
description: "Selles teemas kirjeldatakse, kuidas hallata lõpetatuks registreeritava materjali ristlaadimise protsessi tootmisliinilt väljaminevasse transpordidokki."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCrossDockOpportunityPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 62194012cfbe101d19e9de3254afb004da79a562
ms.contentlocale: et-ee
ms.lasthandoff: 03/07/2018

---

# <a name="cross-docking-from-production-orders-to-outbound-docks"></a>Ristlaadimine tootmistellimustest lähetusaladesse

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas hallata lõpetatuks registreeritava materjali ristlaadimise protsessi tootmisliinilt väljaminevasse transpordidokki.

<a name="introduction"></a>Sissejuhatus
------------

Ristlaadimine tootmisest väljaminevasse asukohta on vajalik tootjatele, kes valmistavad suuri koguseid ja soovivad ideaaljuhul saata valmis tooted välja kohe, kui need on tootmisliinidel lõpetatuks registreeritud. Eesmärk on saata tooted jaotuskeskustesse, mis asuvad füüsiliselt kliendi nõudlusele lähedal, mitte koguda varusid tootmiskohta.

Kui toote järele pole kohe nõudlust, tuleb see paigutada tootmiskoha laoasukohtadesse. Seda protsessi nimetatakse ka *ristlaadimiseks võimaluse korral*, mis näitab, et kui on olemas nõudlus toote lähetamise järele, tuleb kasutada seda võimalust, mitte paigutada toodet siselattu.

Järgmises näites on kolm variatsiooni voost, mis algab tootmisliini (2) lõpust.

Toode registreeritakse tootmise väljastuskohas (3) lõpetatuna ja kahveltõstuki juht võtab aluse sellest asukohast (3) peale.

-   Kui on olemas plaanitud tegevus (6) toote viimiseks tootmisest (1) jaotuskeskusse (7), suunab süsteem tõstukijuhi viima alust laadimisukse (4) juurde.
-   Kui laadimisuksele on juba määratud treiler, suunatakse tõstukijuht laadima toodet otse treilerile.
-   Kui toote edastamise plaanitud tegevus puudub, suunatakse tõstukijuht viima toodet siselaos (5) olevasse asukohta.

[![ristlaadimine võimaluse korral](./media/scenario1.png)](./media/scenario1.png)

## <a name="configure-cross-docking"></a>Ristlaadimise konfigureerimine
Ristlaadimise protsessi saab konfigureerida **tööpoliitikate** jaotises. Tööpoliitika sisaldab töötellimuse tüüpi, asukohta ja toodet. Järgmises näited konfigureeritakse ristlaadimine tootele X ja asukohale Y.

#### <a name="work-order-types"></a>Töötellimuse tüübid

-   Töötellimuse tüüp: lõpetatud kaupade kõrvalepanek
-   Töö loomise meetod: ristlaadimine
-   Ristlaadimise poliitika nimi: üleviimistellimused

#### <a name="inventory-locations"></a>Lao asukohad

-   Ladu: 51
-   Koht: Y

#### <a name="products"></a>Tooted

-   Kaubakood: X

Praegu saab ristlaadimise konfigureerida ainult kahe töötellimuse tüübi jaoks:

-   Lõpetatud kaupade kõrvalepanek
-   Kaastoodete ja kõrvalsaaduste kõrvalepanek

**Ristlaadimise poliitikas** saate määratleda, milliseid dokumenditüüpe saab ristlaadimise puhul kasutada. Praegu on ainus toetatav dokumenditüüp **Üleviimistellimused**. Järgmises näites näidatakse ristlaadimise poliitika konfiguratsiooni.

### <a name="cross-docking-policy-name-transfer-order"></a>Ristlaadimise poliitika nimi: üleviimistellimus

- Järjekorranumber: 10
  -   Töötellimuse tüüp: edastuse väljaminek
- Ristlaadimise nõue nõuab asukohta: väär
- Ristlaadimise strateegia: kuupäev ja kellaaeg

### <a name="sequence-number"></a>Järjekorranumber

**Järjekorranumber** näitab dokumenditüübi prioriteeti. Praegu on **Edastuse väljaminek** ainus toetatud tüüp. Seega muutub järjekorranumber oluliseks alles siis, kui toetatud on rohkem töötellimuse tüüpe.

### <a name="cross-docking-policy"></a>Ristlaadimise poliitika

Ristlaadimise poliitika määrab ka üleviimistellimuse nõudluse tähtsuse määramise poliitika. Näiteks kui sama toote puhul on olemas mitu üleviimistellimust, määravad tellimuste tähtsuse järjekorra koormale määratud ning üleviimistellimusega seostatud kuupäev ja kellaaeg. Plaanitud kuupäeva ja kellaaja saab määrata otse koormal või need saab määrata koormaga seostatud **laadimisgraafikus**. Tähtsuse järjekord määratakse ristlaadimise strateegiaga. Praegu on ainult üks strateegia: **kuupäev ja kellaaeg**.

### <a name="cross-docking-demand-requires-location"></a>Ristlaadimise nõue nõuab asukohta

Ristlaadimise poliitikas saab seadistada kriteeriumi, mis nõuab, et üleviimistellimustele oleks määratud asukoht, et nende puhul saaks ristlaadimist kasutada. See kriteerium on määratud väljal **Ristlaadimise nõue nõuab asukohta**. Laadimisgraafikus olevat koormaga seostatud asukohta kasutatakse ristlaaditavate kaupade lõpliku asukohana. Ristlaaditavate kaupade lõplik asukoht määratakse **edastuse väljamineku** asukohakorraldusega töö tüübi **Asetamine** puhul. Olukorras, kus lõpetatud kaubad tuleks ristlaadida ainult juhul, kui laadimisukse juurde on määratud treiler, võib olla vaja määrata väli **Ristlaadimise nõue nõuab asukohta**. Sel juhul viiakse kaubad otse tootmisliinilt treilerile. Kui laadimisuksele on määratud treiler, määrab kasutaja asukoha laadimisgraafikule ja teeb seega asukoha ristlaadimiseks kättesaadavaks. Järgmistes jaotistes selgitatakse kahte näidet.

#### <a name="scenario-1--cross-docking-from-production-to-transfer-orders"></a>1. stsenaarium – ristlaadimine tootmistellimustest üleviimistellimustesse

Kui toode on tootmisliinil lõpetatuks registreeritud, edastatakse see laadimisukse juurde, kus see laaditakse veokile ja viiakse jaotuskeskusse. Kasutage ettevõtet USMF.

1.  Lubage ristlaadimise jaoks uus numbriseeria. Minge lehele **Numbriseeriad** ja valige nupp **Loo**. Viisard juhatab teid läbi selle protsessi.
2.  Looge ristlaadimise poliitika. Minge lehele **Ristlaadimise poliitika** ja looge uus poliitika nimega **Ristlaadimine üleviimistellimusse**. Pange tähele, et ainus töötellimuse tüüp, mida valida saate, on **Edastuse väljaminek** ja ainus ristlaadimise strateegia, mida saab kasutada, on **Kuupäev ja kellaaeg**.
3.  Looge tööpoliitika. Minge lehele **Tööpoliitikad** ja looge uus tööpoliitika, mille nimi on **Ristlaadimine L0101**.
4.  Seadistage koormad, nii et need luuakse üleviimistellimuste puhul automaatselt. Seadistage laoparameetrites koormad, nii et need luuakse üleviimistellimuste loomisel automaatselt. Koorem on üleviimistellimuse ristlaadimise eeltingimus.
5.  Seadistage kauba koorma vastendus. Minge lehele **Kauba koorma vastendamine** ja seadistage standardkoorma mall kaubagrupile **CarAudio**. See vastendus lisab üleviimistellimuse loomisel automaatselt koormale koormamalli.
6.  Looge üleviimistellimus. Looge üleviimistellimus kaubale numbriga L0101. Kogus = 20.
7.  Väljastage üleviimistellimuse koorma plaanimise töölaualt. Valige vahekaardilt **Läheta** menüüelement koorma plaanimise töölaua jaoks ja tehke koorma rea menüüs **Väljasta** valik **Väljasta lattu**. Nüüd on üleviimistellimuse puhul olemas avatud voo rida tüübiga **Edastuse väljaminek**.
8.  Tootmistellimuse loomine. Minge loendilehele **Tootmistellimus** ja looge tootele L0101 tootmistellimus. Kogus = 20. Hinnake ja alustage tootmistellimust. Pange tähele, et välja **Sisesta komplekteerimisleht kohe** olek on endiselt **Ei**.
9.  Registreerige mobiilselt seadmelt lõpetatuks. Minge mobiilse seadme portaali ja valige menüüelement **Teata lõpetamisest ja pane kõrvale**. Nüüd registreerige L0101 pihuseadmel lõpetatuks. Kogus = 10. Pange tähele, et asetamise koht on **BAYDOOR**. Selle asukoha leiate töötellimuse tüübi **Asetamine** asukohakorraldusest **Edastuse väljaminek**. Pange tähele ka seda, et töö tüübiga **Edastuse väljaminek** on loodud ja lõpetatud. Minge töö kontrollimiseks üleviimistellimuse töö üksikasjadesse.
10. Nüüd saab mobiilsest seadmest aruannetes esitada 10 lisaüksust. Pange tähele, et uuesti asetamise koht on **BAYDOOR**. Pange tähele ka seda, et uus töö tüübiga **Edastuse väljaminek** on loodud 10 üksuse jaoks.
11. Nüüd proovige alustada tootmistellimusel veel 20 ühikut ja siis proovige registreerida 20 ühikut pihuseadmes lõpetatuks. Seekord soovitatakse asetamise kohaks **LP-001**. Selle asukoha leiate **lõpetatud kaupade kõrvalepaneku** asukohakorraldusest. Seda asukohakorraldust kasutatakse sellepärast, et ristlaadimise võimalust enam pole. LP-001 üleviimistellimus täideti täielikult kahe ristlaadimistegevusega etappides 9 ja 10. Pange tähele, et loodi ja töödeldi töö tüübiga **Lõpetatud kaupade kõrvalepanek**.

#### <a name="scenario-2---cross-docking-from-production-to-transfer-orders-with-an-appointment-schedule"></a>Stsenaarium 2 – ristlaadimine tootmisest laadimisgraafikuga üleviimistellimustesse

Kui toode on tootmisliinil lõpetatuks registreeritud, viiakse see laadimisukse asukohta, mis on tähistatud laadimisuste asukohtade laadimisgraafikuga. Kasutage ettevõtet USMF.

1.  Muutke ristlaadimise poliitikat. Muutke ristlaadimise poliitikat, mille 1. stsenaariumis koostasite, märkides ruudu **Ristlaadimise nõue nõuab asukohta**.
2.  Looge uus üleviimistellimus.
3.  Avage **koorma plaanimise töölaud**.
4.  Minge koorma plaanimise töölaualt jaotisse **Koormad** ja valige **Laadimisgraafik** menüüst **Transport** uue laadimisgraafiku loomiseks. Pange tähele, et laadimisgraafiku väljal **Tellimuse number** on viide üleviimistellimusele. Väljal **Plaanitud alguskuupäev/-kellaaeg asukohas** saate määrata laadimise kuupäeva ja kellaaja. Seda kuupäeva ja kellaaega kasutatakse ristlaadimise nõude tähtsuse määramisel ristlaadimise protsessi käigus. Sellel väljal määratud kuupäev ja kellaaeg muudavad vastava koorma välja **Koorma saatmise plaanitud kuupäev ja kellaaeg**. Asukoht kiirkaardil **Saatmise üksikasjad** määravad üleviimistellimuse saatmise asukoha.
5.  Tehke **koorma plaanimise töölaual** väljastus lattu.
6.  Looge tootmistellimus kaubale koodiga **L0101** ja määrake olekuks **Alustatud** ning koguseks 20.
7.  Registreerige mobiilselt seadmelt lõpetatuks.
8.  Minge mobiilse seadme portaali ja valige menüüelement **Teata lõpetamisest ja pane kõrvale**.
9.  Registreerige kaup koodiga **L0101** pihuseadmel lõpetatuks. Pange tähele, et asetamise koht on nüüd **BAYDOOR 2**. Selle asukoha leiate laadimisgraafikust ja mitte asukohakorraldusest **Üleviimistarne**.

### <a name="additional-information"></a>Lisateave

-   Ristlaadimise stsenaariumi toetatakse partii ja seeriaga juhitavate kaupade puhul, nii ülal määratletud partii- ja seerianumbri dimensioonidega kui ka allpool antud asukohaga reserveerimishierarhias. 



