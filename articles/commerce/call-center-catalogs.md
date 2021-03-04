---
title: Kõnekeskuse kataloogid
description: Selles teemas kirjeldatakse kõnekeskusepõhiseid funktsioone rakenduse Dynamics 365 Commerce kataloogidele.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9abe493746719d2e229ef09c2eb5f436b91b2171
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/24/2020
ms.locfileid: "4411821"
---
# <a name="call-center-catalogs"></a>Kõnekeskuse kataloogid

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse kõnekeskusepõhiseid funktsioone, mis on seotud Dynamics 365 Commercei kataloogide võimalustega.

Commerce'i kataloogide funktsioone saab kasutada mitmel eesmärgil. Kataloogide funktsioonid loodi algselt kolmanda isiku e-kaubanduse integratsioonide toetamiseks. Kataloogide seadistus võimaldas ettevõtetel luua toodete ja atribuutide rühmi, mida on võimalik avaldada väliselt kolmanda isiku e-kaubanduse lahendusele kasutuseks.

Kui ile lisati kõnekeskuse kanali tugi, siis laiendati kataloogi mõistet – lisati rohkem võimalusi traditsiooniliste „vahetult tarbijale “ turunduskataloogide funktsioonide toetamiseks ja haldamiseks. „Vahetult tarbijale“ ettevõtted trükivad sageli kataloogid välja ja saadavad need seejärel ühele või mitmele kliendirühmale. Need kataloogid sisaldavad tavaliselt kindlaid kampaaniad või pakkumisi, mille kasutamiseks peab klient esitama tellimuse tegemise ajal kataloogi ID-koodi.

„Vahetult tarbijale“ turundusettevõtted on huvitatud nende kataloogide kasutamise teabest, et tagada, et kataloogide tootmise ja saatmise kulud oleks õigustatud. Kataloogide kasutamise jälgimiseks trükitakse tavaliselt kataloogi tagaküljele kood, mille kataloogi kasutaja peab esitama, kui ta telefoni teel tellimuse esitab (või tänapäeval tavapärasemalt sisestab koodi Interneti kaudu tellides). Kuigi kataloogi jälgimiskoodi jaoks on kasutusel eri termineid (sh võtmekood, kampaaniakood, kataloogikood, lähtekood), kasutame Commerce'is selleks mõistet **Lähtekoodi ID**.

## <a name="basic-catalog-setup"></a>Kataloogi põhiseadistus

Kataloogi konfigureerimiseks klõpsake valikuid **Jaemüük ja kaubandus** \> **Kataloogid ja sortimendid** \> **Kõik kataloogid**.

Uue kataloogi loomisel tuleb see esmalt siduda ühe või enama kanaliga. Seda saate teha vormi **Kataloogi seadistus** kiirkaardil **Kaubanduse kanalid**. Klõpsake nuppu **Lisa** ja valige üks või mitu kanalit. Kataloogi loomiseks saab kasutada ainult kaupu, mis on seotud teie valitud kanalite [sortimentidega](https://docs.microsoft.com/dynamics365/unified-operations/retail/assortments).

Toodete lisamiseks kataloogi tuleb valida navigeerimishierarhia. Navigeerimishierarhia toetab kataloogi jaoks kategooriastruktuuri. Peate valima ühe navigeerimishierarhia, mis on seotud lehe **Kataloog** kiirkaardilt **Ärikanalid** valitud jaemüügikanaliga. Kui navigeerimishierarhiat pole varem kanaliga seotud, siis valige **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Kanali kategooriad ja toote atribuudid**, et vaikimisi siduda navigeerimishierarhia iga kanaliga.

Kataloogi lisamiseks klõpsake menüü vahekaardi **Kataloogid** lehel **Kataloogi seadistus** käsku **Lisa tooted** või valige navigeerimishierarhias sõlm (sõlme valimine muudab ekraani esitlust ja võimaldab lisada tooteid otse kataloogi kategooriasse).

Peamisse kataloogi päise vaatesse naasmiseks klõpsake kataloogihierarhias kõige ülemist sõlme. Konfigureerige vajaduse korral jõustumis- ja aegumiskuupäevi kiirkaardil **Üldine**.

Kataloogi kasutamiseks saadavaks muutmiseks tuleb see enne avaldada. Kinnitamise töötlemiseks klõpsake menüüs **Kataloogid** käsku **Kataloogi kinnitamine**. See on nõutav tegevus ja kinnitab, et nõutav seadistus on õige. Kinnituse üksikasjade vaatamiseks klõpsake **Tulemuste kuvamine**. Kui leitakse vigu, tuleb andmed parandada ja kinnitamine uuesti käivitada, kuni see läbitakse edukalt.

Kui kinnitamine on edukas, klõpsake menüüs valikut **Töövoog**, et käivitada kinnitamise töövoog. Toimingu käivitamiseks klõpsake menüüs **Edasta** käsku **Töövoog**. Töövoo etappide ja volitatud kasutajate konfigureerimiseks valige **Jaemüük ja kaubandus** \> **Peakontori seadistamine** \> **Kaubanduse töövood**. Töövoog määratleb etapid, mis on vajalikud kataloogi olekusse **Kinnitatud** saamiseks. Kui kataloog on olekus **Kinnitatud**, saate menüüs **Kataloogid** klõpsata suvandit **Avalda**, et toiming lõpetada. Kui kataloogi olek on **Avaldatud**, siis saab seda kasutada kõnekeskuse tellimuste sisestamisel ja kataloogitoimingute saatmisel.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Kataloogide kasutamine müügitellimuste hindade ja kampaaniate määratlemiseks

Üks tähtsaimaid põhjuseid, miks kujundada kataloogi kõnekeskusega kasutamiseks, on võimalus selle kataloogi jaoks konkreetseid hindu ja kampaaniad määratleda. Sellest kataloogist kaupu tellivad kliendid saavad kasutada kirjeldatud hindu ja kampaaniaid, kui esitavad kõnekeskuse kaudu tellides kataloogi **lähtekoodi ID** tellimuse päise või ridade jaoks.

Konkreetse kataloogi hindade konfigureerimiseks valige vahekaardilt **Kataloogid** suvand **Hinnagrupid**, et siduda üks või enam hinnagruppi kataloogiga. Kui kliendid sellest kataloogist tellivad, rakenduvad kõik selle hinnagrupiga seotud kaubanduslepped, hinna korrigeerimise töölehed ja täpsemad allahindlused (lävi, kogus, segamine ja sobitamine).

Sellele kataloogile ühe või mitme **lähtekoodi ID** identifikaatori lisamiseks klõpsake kiirkaardil **Lähtekoodid** käsku **Lisa**. Seda koodi kasutatakse kõnekeskuse tellimuse sisestamisel müügitellimuse päises (ja ridades). Seda koodi kasutatakse müügitellimuse sidumiseks kataloogiga ja sealt edasi konfigureeritud hinnagruppide ja erihindade ning kampaaniatega.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Lähtekoodi ID kasutamine kulude ja kasutamismäärade jälgimiseks

**Lähtekoodi ID** määratlemisel võite selle valikuliselt siduda **sihtturu ID-ga**. **Sihtturu ID**-d saate määratleda valides **Jaemüük ja kaubandus** \> **Kliendid** \> **Sihtturg**. Sihtturg on loend klientidest ja/või potentsiaalsetest klientidest, kes kuuluvad kasutaja määratletud segmenti. Klientide või potentsiaalsete klientide andmete sidumine lähtekoodi ID-ga võimaldab saada paremat ülevaadet kataloogi adressaatide kohta. Kui klient on seotud sihtturuga ja see omakorda on seotud aktiivse lähtekoodi ID-ga/kataloogiga, siis on kõnekeskuse kasutajal võimalik näha, millise kataloogi klient saanud on, kui ta valib lehe **Klienditeenindus** menüü vahekaardilt **Kliendid** suvandi **Lähtekoodid**. Kõnekeskuse kasutajad saavad müügitellimuse päises olevast ripploendist **Allikas** näha tellimuse sisestamise ajal ka konkreetseid katalooge, mida kliendile on varem saadetud. Filtri muutmine olekult **Kõik** olekule **Sihitud** võimaldab kasutajatel näha konkreetseid aktiivseid katalooge, mida kliendile saadetud on. See on kasulik, kui klient helistab müügitellimuse loomiseks ja on unustanud oma kataloogi või ei leia või ei suuda lugeda kataloogi koodi.

Kataloogiga on võimalik siduda mitu lähtekoodi ID-d. Seda läheb tihtipeale vaja, kui ettevõttel on vaja jälgida eri segmentide kasutusandmeid. Ettevõte annab igale kliendisegmendile kordumatu kataloogikoodi, mis võimaldab jälgida iga segmendi kasutamismäära konkreetse kataloogisündmuse puhul.

Valides konkreetse **lähtekoodi ID** kirje ja klõpsates kiirkaardi **Lähtekoodid** suvandil **Üksikasjad** avanevad lisaväljad, kuhu saate sisestada müügiprognoose, postikulusid ja postituse kuupäevi. Need andmed on abiks kataloogi tõhususe kohta üksikasjaliku analüüsi tegemiseks. Kasutajad saavad sellele lehele hiljem naasta ja kasutada nuppe **Lähtekoodi analüüs** ja **Kampaaniate võrdlus**, et käivitada praegustel müügiandmetel tuginevad analüütilised aruanded ning võrrelda kulusid ja eelarveid tegelikkusega.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Konkreetse kataloogi tellimuste ja kauba skriptide konfigureerimine

Kui kõnekeskuse kasutaja loob müügitellimuse, saab ta kasutada ekraanil olevaid skripte. Need tekstipõhised skriptid võivad esitada lisateavet, mida kasutaja peaks kliendile edastama, või kuvada rakendusesiseseid märkusi/meeldetuletusi, mida kõnekeskuse kasutaja peaks üle vaatama ja millele peaks müügitellimuse loomise ajal reageerima.

Sageli on kasulik seada eri kataloogide jaoks üles eri skriptikogumid. Kiirkaardil **Skriptid** saab eelmääratletud skripte kataloogiga siduda. Kasutage välja **Ajastus**, et määratleda, kas skript kuvatakse tellimuse alguses (niipea kui lähtekoodi ID sisestatakse tellimuse päisesse) või tellimuse lõpus (müügitellimuse kokkuvõte vormil).

Kui kasutajad valivad kataloogi hierarhias sõlme ja töötavad kiirkaardil **Tooted** andmetega, saavad nad siduda ka konkreetsetele kataloogidele või kaupdale mõeldud skripte, kasutades tegevust **Skriptid**.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Konkreetse kataloogi ülesmüügi ja kaasmüügi kaupade konfigureerimine

Üles-/kaasmüügi soovitusi saab siduda toodetega toodete häälestuse kaudu, kuid mõnel juhul võib ettevõte soovida pakkuda erilist üles-/kaasmüügi kaupa klientidele, kes tellivad konkreetse kauba konkreetsest kataloogist. Valige kiirkaardil **Tooted** kaup ja klõpsake valikut **Kaupade ülesmüük/kaasmüük**, et konfigureerida kaupu üles- või kaasmüügiks klientidele, kes ostavad kataloogist valitud kauba. Kõnekeskuse tellimuse sisestamise ajal kuvatakse ekraanil tavapäraste üles-/kaasmüügi kaupade asemel konkreetse kataloogi üles-/kaasmüügi kaubad, mida on selle kauba jaoks konfigureeritud tavapärase toote konfigureerimise kaudu.

Üles-/kaasmüügi kaupade puhul saab ära kasutada ka skriptide funktsioone, et kuvada kasutajale konkreetseid teateid üles-/kaasmüügi kauba kuvamisel tellimuse sisestamise ajal. Üles-/kaasmüügi kaupadega, mis on konfigureeritud konkreetse kataloogi kauba jaoks, seotud skriptid ilmuvad vaid siis, kui selle kataloogi lähtekoodi kasutatakse kõnekeskuse tellimuse sisestamisel.

## <a name="catalog-page-analysis"></a>Kataloogi lehekülje analüüs

Vahekaardil **Kataloogid** on olemas suvandid **Kataloogi lehekülgede** konfigureerimiseks. See funktsioon võimaldab teil määratleda trükitud kataloogi jaoks kindlaid lehekülgi ja lehekülgede tüüpe ning nendega seotud kulusid.

Kataloogi toodete konfigureerimisel kasutage tegevust **Toote lehe paigutus**, et määratleda konkreetseid lehekülgi, lehekülje protsenti ja kauba üksikasjade paigutust lehel. Nende andmete konfigureerimine võimaldab kasutajatel kasutada **Kataloogiala analüüsi aruannet**. Selle aruande leiate, kui valite **Jaemüük ja kaubandus** \> **Kõnekeskuse aruanded** \> **Kataloogiala analüüs**-i aruanne. Selles aruandes analüüsitakse müüke võrdluses kataloogiga (müügitellimused, mille puhul kataloogi lähte-ID oli seotud tellimuse päise või reaga) ning nendega seotud leheküljeprotsenti ja kulusid, et koostada traditsiooniline otseturustamise **Ruuttolli analüüsi** aruanne.

## <a name="catalog-requests"></a>Kataloogi taotlused

Commerce'is konfigureeritud ja avaldatud kataloogide puhul saab kasutada funktsioon **Saada kataloog**. See funktsioon on saadaval lehtedel **Kliendiotsing** ja **Klienditeenindus**. Pärast **Kliendiotsingu** kaudu kliendikirje valimist või lehe **Klienditeenindus** kaudu valitud kliendi konto vaatamisel saavad kasutajad valida suvandi **Saada kataloog**, mis avab dialoogiboksi, mis võimaldab kasutajal valida avaldatud ja aktiivsete kataloogide loendist. Kasutaja saab saatmiseks valida kataloogi, koguse ja konkreetse lähtekoodi ID. Kui ta klõpsab nuppu **Saada**, siis talletatakse taotlus, mida saab seejärel hallata, kui trükkida **Kataloogi taotluste** aruanne. Selle aruande leiate, kui valite **Jaemüük ja kaubandus** \> **Kõnekeskuse aruanded** \> **Kataloogipäringu aruanne**. Selles loetletakse kõik kataloogi taotlused, sh kataloogi taotlenud kliendi nimi ja aadress. Seda aruannet saate kasutada ettevõttesiseselt või saate edastada aruande andmed kolmandale isikule, täiendades väliseid toiminguid kliendile füüsiliselt kataloogi saatmise puhul.

## <a name="additional-features"></a>Lisafunktsioonid

Vahekaardil **Kataloogid** on olemas ka võimalused suvandite **Maksegraafik** ja **Tasuta tooted** konfigureerimiseks. Kui kõnekeskuse tellimuse sisestamise ajal kasutatakse kataloogiga seotud lähtekoodi ID-d, siis on kasutajal õigus tasuta toodetele või kasutada konkreetse kataloogi maksegraafikut nagu määratletud. Kui on vaja piirata klienti, et ta saaks valida vaid kataloogiga seotud maksegraafikuid ja mitte kõiki aktiivseid maksegraafikuid süsteemis, siis tuleb piirangu rakendamiseks tähistada märkeruut **Ainult kataloogiplaanide lubamine** ühele või enamale määratletud lähtekoodi ID-le.

## <a name="additional-notes"></a>Lisamärkmed

Kui kõnekeskuses kasutatakse müügitellimuse koostamisel lähtekoodi ID-d, siis edastatakse sellega praegu konkreetse kataloogi hindu, kampaaniaid, skripte ja üles-/kaasmüüke. Süsteem ei keela ega takista müügitellimuse kaudu toote tellimist, mis ei ole kataloogis. Kui tellitakse kaup, mida kataloogis pole, siis kasutab süsteem esmalt **hinnagruppi**, mis on määratletud kõnekeskuse kanalis (**Jaemüük ja kaubandus** \> **Kanalid** \> **Kõnekeskused** \> **Kõik kõnekeskused**) kauba hinna või kampaaniate jaoks. Kui ei leita konkreetset kanali hinda, siis kasutatakse kauba põhihinda.


[!INCLUDE[footer-include](../includes/footer-banner.md)]