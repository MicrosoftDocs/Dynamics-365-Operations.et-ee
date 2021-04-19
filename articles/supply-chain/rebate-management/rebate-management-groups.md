---
title: Tagasimaksehalduse grupid
description: Selles teemas kirjeldatakse, kuidas seadistada tagasimaksehalduse gruppi. Tagasimaksehalduse gruppe saab kasutada tagasimakse arvutuste ajal ja neid saab siduda koondkirjega.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 2d1f8ed9def03afc97c0b4c5ea86430ff089aac6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819228"
---
# <a name="rebate-management-groups"></a>Tagasimaksehalduse grupid

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tagasimakse ja mahaarvamise arvutused võivad olla seotud gruppidega. Tagasimakse haldusgruppe saab luua klientidele, hankijatele ja üksustele. Neid saab siduda koondkirjega.

## <a name="rebate-management-customer-groups"></a>Tagasimaksehalduse kliendigrupid

Arvutused klientide grupi jaoks luuakse sageli ettevõtete ketile, näiteks supermarketite ketile või frantsiisifirmale. Seda tüüpi kalkulatsioon on tavaliselt seotud tagasimaksega.

Mahaarvamist arvutatakse sageli ilma, et arvestatakse, kellele kvalifitseerumistellimus müüdi. Siiski on erandeid. Näiteks võib litsentsisaaja luua mahaarvamisskeemi, kus kliendigrupp A saab 4 protsenti, kuid kliendigrupp B saab ainult 3 protsenti.

### <a name="set-up-customer-groups"></a>Saate häälestada kliendigruppe.

Tagasimaksehalduse kliendigruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Kliendigrupid**. Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele. Määrake igale grupile järgmised väljad.

- **Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.
- **Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.

### <a name="manage-customer-group-assignments"></a>Kliendigrupi määrangute haldamine

Iga klient võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse. Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või kliendiloendist.

Valitud grupi klientide vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.

1. Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kliendigrupid**.
1. Valige grupp, mida hallata.
1. Valige toimingupaanil **Kliendid**. Kuvatakse leht **Tagasimakse halduse grupid** ja klientide loend, kes on juba valitud grupi liikmed.
1. Uue kliendi lisamiseks gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Kliendikonto** – valige kliendikonto ID.
    - **Nimi** – sisestage kliendi nimi ja/või kirjeldus.

1. Kliendi eemaldamiseks grupist valige klient ja seejärel valige tegevuspaanil käsk **Kustuta**.

Valitud kliendi grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.

1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Valige klient, kellele töötada.
1. Valige toimingupaani vahekaardil **Klient** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**. Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud klient juba kuulub.
1. Kliendi lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Tagasimaksehalduse grupp** – valige grupp, kellele klient lisada.
    - **Kirjeldus** – sisestage grupi kirjeldus (nt selgitamaks, miks klient on grupi liige).

1. Kliendi eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.

## <a name="rebate-management-vendor-groups"></a>Tagasimaksehalduse müüjagrupid

Müüja grupi kalkulatsioon luuakse sageli tarnepunktide grupile. Seda tüüpi kalkulatsioon on tavaliselt seotud tagasimaksega.

### <a name="set-up-vendor-groups"></a>Müüja gruppide häälestus

Tagasimaksehalduse müüjagruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Müüjagrupid**. Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele. Määrake igale grupile järgmised väljad.

- **Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.
- **Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.

### <a name="manage-vendor-group-assignments"></a>Müüjagrupi määrangute haldamine

Iga müüja võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse. Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või müüja loendist.

Valitud grupi müüjate vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.

1. Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Müüjagrupid**.
1. Valige grupp, mida hallata.
1. Valige toimingupaanil **Müüjad**. Kuvatakse leht **Tagasimakse halduse grupid** ja müüjate loend, kes on juba valitud grupi liikmed.
1. Müüja lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Müüja konto** – valige müüja konto ID.
    - **Nimi** – sisestage müüja nimi ja/või kirjeldus.

1. Müüja eemaldamiseks grupist valige müüja ja seejärel valige tegevuspaanil käsk **Kustuta**.

Valitud müüja grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.

1. Avage **Ostureskonto \> Müüjad \> Kõik müüjad**.
1. Valige müüja, kellele töötada.
1. Valige toimingupaani vahekaardil **Müüja** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**. Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud müüja juba kuulub.
1. Müüja lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Tagasimaksehalduse grupp** – valige grupp, kellele müüja lisada.
    - **Kirjeldus** – sisestage grupi kirjeldus (nt selgitamaks, miks müüja on grupi liige).

1. Müüja eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.

## <a name="item-rebate-groups"></a>Kauba tagasimaksegrupid

Kaupade grupeerimisel on teil tagasimaksete ja mahaarvamiste arvutamisel paindlikkust. Selline lähenemine on sageli tõhusam viis seadistada klientidele ja hankijatele tagasimaksed ja mahaarvamised.

### <a name="set-up-item-groups"></a>Saate häälestada kaubagruppe.

Tagasimaksehalduse kaubagruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**. Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele. Määrake igale grupile järgmised väljad.

- **Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.
- **Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.

### <a name="manage-item-group-assignments"></a>Kaubagrupi määrangute haldamine

Iga üksus võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse. Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või kauba loendist. Saate lisada kaupu ka oma kategooriahierarhia alusel.

Valitud grupi kaupade vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.

1. Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**.
1. Valige grupp, mida hallata.
1. Toimingupaanil valige käsk **Kaubad**. Kuvatakse leht **Tagasimakse halduse grupid** ja kaupade loend, kes on juba valitud grupi liikmed.
1. Uue kauba lisamiseks gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Kaubakonto** – valige kaubakonto ID.
    - **Toote nimi** – sisestage kauba nimi ja/või kirjeldus.

1. Kauba eemaldamiseks grupist valige kauba ja seejärel valige tegevuspaanil käsk **Kustuta**.

Valitud kauba grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige kaup, millega töötada.
1. Valige toimingupaani vahekaardil **Toode** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**. Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud kaup juba kuulub.
1. Kauba lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Tagasimaksehalduse grupp** – valige grupp, kellele kaupa lisada.
    - **Kirjeldus** – sisestage grupi kirjeldus (nt selgitamaks, miks kaup on grupi liige).

1. Kauba eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.

Oma kategooriahierarhial põhinevasse gruppi kaupade lisamiseks järgige neid samme.

1. Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**.
1. Valige grupp, mida hallata.
1. Toimingupaanil valige käsk **Lisa kaubad**.
1. Valige dialoogiboksi **Lisa kaubad** väljal **Kategooriahierarhia** ülataseme kategooria.
1. Kauba hierarhia avatakse vasakul paanil. Valige otsitav hierarhiatase. 
1. Valitud hierarhia ja hierarhia taseme kaubad on nüüd loetletud parempoolsel paanil. Paaniga töötamiseks järgige neid samme:

    - Märkige ruut iga kauba puhul, mille soovite lisada.
    - Ruudustiku päises kõikide loetletud kaupade valimiseks märkige see ruut.
    - Ruudustiku filtreerimiseks valige nupp **Kuva valitud**, nii et see näitab ainult seni valitud kaupu. Täieliku loendi juurde naasmiseks valige nupp uuesti.

1. Valige **OK**, et rakendada oma kaubavalik valitud grupile.
