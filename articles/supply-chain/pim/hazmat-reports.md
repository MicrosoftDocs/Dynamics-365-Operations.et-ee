---
title: Ohtlike materjalide päringud ja aruanded
description: Selles teemas selgitatakse, kuidas töötada ohtlike materjalidega seotud erinevate aruannetega. Paljud neist aruannetest on nõutavad selleks, et säilitaksite tarne ja nõuetelevastavuse erinevate ohtlike materjalide lähetamis- ja ladustamismäärustega.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 1bb96d117eb3bb2b54be1a376c8789ad73d5fec8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983362"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Ohtlike materjalide päringud ja aruanded

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management pakub erinevaid ohtlike materjalidega seotud aruandeid. Paljud neist aruannetest on nõutavad selleks, et säilitaksite tarne ja nõuetelevastavuse erinevate ohtlike materjalide lähetamis- ja ladustamismäärustega.

Kõik need aruanded, välja arvatud aruanne **Mitmikmodaalsed ohtlikud tooted**, kasutavad saadetise jaoks määratletud tarneviisi, et leida määrus, mida tuleks kasutada kaubasaadetise teksti printimiseks. Tarneviis on seostatud saadetise vedaja ja vedaja teenusega. Seetõttu peate häälestama saadetise vedaja ja vedaja teenuse ning linkima need tarneviisiga. Tarneviis on seotud ohtlike materjalide määrusega.

Järgmine illustratsioon näitab tegevuste jada, mis ilmneb siis, kui süsteem genereerib ohtlike materjalide aruanded.

![Ohtlike materjalide aruannete tegevuste jada](media/hazmat-report-sequence.png "Ohtlike materjalide aruannete tegevuste jada aruanded")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Ohtlike materjalide aruandluse häälestamine

Tavaliselt, kui lähetate ohtlikke materjale sisaldavaid kaupu, tuleb teil luua kindlad aruanded, et aidata kaitsta ohutust ja järgida ohtlike materjalide määrusi. Aruannete häälestamiseks järgige neid toiminguid.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
2. Avage vahekaart **Aruanded**. Määrake kiirkaardil **Ohtlike materjalide aruandeparameeter** järgmised väljad.

    | Lõik | Field | Kirjeldus |
    |---|---|---|
    | Mitmikmodaalsed ohtlikud tooted | Määruse kood | Valige määrus, mida tuleks kasutada aruande **Mitmikmodaalsed ohtlikud tooted** loomisel. |
    | Ohtlike materjalide ladustamispiirangud | Määruse kood | Valige määrus, mida tuleks kasutada varude piirangute hindamisel. |
    | Kaubavedu maanteel | CMR-i grupi toode | CMR tähendab kantserogeenseid, mutageenseid ja reproduktiivtoksilised aineid. Määrake selle suvandi väärtuseks **Jah**, et konfigureerida süsteemi printima kindlaid hoiatusi ja teateid, mis on seotud nende ainete käsitsemisega. |
    | Kaubavedu maanteel | Ohtliku materjali grupikirjeldus | Saate sisestada CMR-i ja kauba maanteeveoga seotud konkreetsete hoiatuste teksti. Tekst kaasatakse aruandesse. |
    | Saatja deklaratsioon | Hoiatus | Sisestage hoiatusteate tekst, mis tuleks printida saatja deklaratsiooni vormile (nt "Hoiatus: ohtlikud kaubad, tuleohtlik"). |
    | Saatja deklaratsioon | Jaluse deklaratsioon | Sisestage teate tekst, mis tuleks printida saadetise deklaratsiooni dokumendi allosas. |
    | Ohtlike kaupade aruande keel | Ohtlike kaupade kodumaise aruande keel | Valige vaikekeel ohtlike materjalide aruannete jaoks, mis on seotud riigisiseste saadetistega. |
    | Ohtlike kaupade aruande keel | Ohtlike kaupade ekspordiaruande keel | Valige vaikekeel ohtlike materjalide aruannete jaoks, mis on seotud rahvusvaheliste saadetistega. |

## <a name="hazardous-materials-report"></a>Ohtlike materjalide aruanne

Aruandes **Ohtlikud materjalid** kuvatakse kõigi häälestatud ja määratletud kaupade loend nii, et neis sisalduks ohtlike toodete andmed. Selle aruande abil saate jälgida ja üle vaadata teavet, mille peate säilitama. Aruande lehel kuvatakse ohtlike materjalide häälestuse väljade piiratud valik. Saate seda siiski vajaduse korral isikupärastada nõutavate lisaväljade lisamisega.

Aruande vaatamiseks avage **Tooteteabe haldus \> Päringud ja aruanded \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtlikud materjalid**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Ohtlike materjalide ladustamispiirangute aruanne

Aruanne **Ohtlike materjalide ladustamispiirangud** võimaldab jälgida ohtlike materjalide varude tasemeid oma lao asukohtades, veendumaks, et need jäävad kehtestatud, ohututesse piiridesse. Need piirangud tulenevad iga väljastatud toote jaoks määratletud piirangutest.

Aruande vaatamiseks avage **Tooteteabe haldus \> Päringud ja aruanded \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtlike materjalide ladustamispiirangud**.

Lisateavet väljastatud toote ladustamispiirangute häälestamise kohta vt teemast [Ohtlike toodete ladustamispiirangute määramine](hazmat-items.md#stock-limits).

Ladustamispiirangute määrus on määratletud lehel **Laohalduse parameetrid**. Avage **Laohaldus \> Häälestus \> Laohalduse parameetrid** ja seejärel määrake suvandi **Ohtlike materjalide ladustamispiirangud** vahekaardil **Aruanded** määruse kood. Vaadake lisateavet teemas eespool olevast jaotisest [Ohtlike materjalide aruandluse häälestamine](#set-up).

## <a name="verified-gross-mass-report"></a>Kinnitatud brutomassi dokument

Aruanne **Kinnitatud brutomassi** aruanne võimaldab teil printida teavet saadetise kaalu kohta.

Aruande loomiseks ja printimiseks avage **Laohaldus \> Saadetised \> Kõik saadetised** ja avage vastav saadetis. Seejärel tehke jaotise **Ohtlike materjalide dokument** vahekaardi **Saadetised** toimingupaanil valik **Kinnitatud brutomass**.

## <a name="multimodal-dangerous-goods-report"></a>Mitmikmodaalsete ohtlike toodete aruanne

Aruanne **Mitmikmodaalsed ohtlikud tooted** esitatakse saadetiste kohta, mis tuleb transpordimeetodite kombinatsiooni abil teisaldada. Seda kasutatakse tavaliselt siis, kui saadetis teisaldatakse esmalt maanteel ja hiljem meritsi.

Aruande loomiseks ja printimiseks avage **Laohaldus \> Saadetised \> Kõik saadetised** ja avage vastav saadetis. Seejärel tehke jaotise **Ohtlike materjalide dokument** vahekaardi **Saadetised** toimingupaanil valik **Mitmikmodaalsed ohtlikud tooted**.

Selle aruande loomisel salvestatakse teave nii, et saate seda redigeerida ja/või aruande uuesti printida, kui peate seda tegema. Loodud aruande redigeerimiseks avage **Laohaldus \> Päringud ja aruanded \> Ohtlike materjalide saatmisdokumendid \> Mitmikmodaalsed ohtlikud tooted** ja otsige loendist üles vastav aruanne. Pärast sisu redigeerimise lõpetamist vastavalt vajadusele tehke aruande printimiseks toimingupaanil valik **Prindi**.

## <a name="shippers-declaration-report"></a>Saatja deklaratsiooni aruanne

Aruanne **Saatja deklaratsiooni** võimaldab teil printida teavet, mis on seotud saadetisse kaasatud materjalide deklaratsiooniga.

Aruande loomiseks ja printimiseks avage **Laohaldus \> Saadetised \> Kõik saadetised** ja avage vastav saadetis. Seejärel tehke jaotise **Ohtlike materjalide dokument** vahekaardi **Saadetised** toimingupaanil valik **Saatja deklaratsioon**.

## <a name="carriage-of-merchandise-by-road-report"></a>Kaubavedu maanteel aruanne

Aruanne **Kaubavedu maanteel** sarnaneb veokirjaga, kuid seda kasutatakse tavaliselt maanteetranspordiks ohtlike veoste rahvusvahelise autoveo Euroopa kokkuleppe alusel. See aruanne kasutab kaubasaadetisse prinditavat teksti, kui te ei määra lehel **Laohalduse parameetrid** välja **Ohtliku materjali grupikirjeldus**.

Aruande loomiseks ja printimiseks avage **Laohaldus \> Saadetised \> Kõik saadetised** ja avage vastav saadetis. Seejärel tehke jaotise **Ohtlike materjalide dokument** vahekaardi **Saadetised** toimingupaanil valik **Kaubavedu maanteel**.

Selle aruande loomisel salvestatakse teave nii, et saate seda redigeerida ja/või aruande uuesti printida, kui peate seda tegema. Loodud aruande redigeerimiseks avage **Laohaldus \> Päringud ja aruanded \> Ohtlike materjalide saatmisdokumendid \> Kaubavedu maanteel** ja otsige loendist üles vastav aruanne. Pärast sisu redigeerimise lõpetamist vastavalt vajadusele tehke aruande printimiseks toimingupaanil valik **Prindi**.

## <a name="shipment-summary-report"></a>Saadetise kokkuvõttearuanne

Aruanne **Saadetise kokkuvõte** annab teavet, mille on kokku võtnud väljastatud kaubaga seotud transpordikategooria.

Aruande loomiseks ja printimiseks avage **Laohaldus \> Saadetised \> Kõik saadetised** ja avage vastav saadetis. Seejärel tehke jaotise **Ohtlike materjalide dokument** vahekaardi **Saadetised** toimingupaanil valik **Saadetise kokkuvõte**.

## <a name="bill-of-lading-report"></a>veokirja aruanne

Kui ohtlike materjalide funktsioon on süsteemis sisse lülitatud, sisaldab aruanne **veokiri** veergu **Ohtlikud materjalid**, mis näitab, kas koorem sisaldab ohtlikke materjale. See aruanne on saadaval lehel **Kõik koormad**, nagu tavaliselt.

## <a name="packing-list-report"></a>Saatelehe aruanne

Kui ohtlike materjalide funktsioon on süsteemis sisse lülitatud, sisaldab saateleht lisateavet, mis on seotud kaubasaadetisse prinditava tekstiga. See aruanne on saadaval lehel **Kõik koormad**, nagu tavaliselt.
