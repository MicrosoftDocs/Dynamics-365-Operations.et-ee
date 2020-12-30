---
title: Saadetise konsolideerimispoliitikad
description: Selles teemas antakse ülevaate funktsioonidest, mis pakuvad saadetise konsolideerimispoliitikate paindlikku konfigureerimist.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f895b13b2e11d4cb341f80b3cfeb40ed998ccfc4
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654216"
---
# <a name="shipment-consolidation-policies"></a>Saadetise konsolideerimispoliitikad

Saadetise konsolideerimisprotsess, mis kasutab saadetise konsolideerimispoliitikaid, lubab automatiseeritud saadetise konsolideerimist automaatsel ja käsitsi väljastamisel lattu. Enne selle funktsiooni kasutuselevõttu saadaval olnud automaatsel konsolideerimisel olid püsiprogrammeeritud väljad ja see põhines väljal **Konsolideeri saadetis lattu väljastamisel**, mis määrati laole.

Saadetise konsolideerimispoliitikaid kasutatakse järgmiste funktsioonide jaoks.

- Automatiseeritud lattu väljastamise pakett-töö
- Käsk **Lattu väljastamine** müügi- või üleviimistellimusel
- Erileht **Lattu väljastamine**
- Käsk **Lattu väljastamine** lehel **Koorma plaanimise töölaud**
- Saadetiste käsitsi konsolideerimine lehed **Saadetiste konsolideerimine** ja **Saadetise konsolideerimise töölaud**

Enne saadetise konsolideerimispoliitikate kasutuselevõttu oli konsolideerimise funktsioon olemas sättena laotasemel. Ühe lao kõikide klientide kõiki tellimusi koheldi selliselt, nagu neil oleks olnud samad konsolideerimise nõuded. Saadetise konsolideerimispoliitikad lisavad tuge stsenaariumides, kus erinevatel organisatsioonidel on saadetise konsolideerimise jaoks erinevad nõuded.

Kehtiva saadetise konsolideerimispoliitika määratlemiseks kasutatakse päringuid ja seejärel määrab redigeeritavate väljade kogum, kuidas koormuse ridu grupeeritakse saadetise tasemel. (See meenutab mustrit, mida kasutavad voo mallid.) Lisaks on igasse poliitikasse lisatud suvand **Konsolideeri olemasolevate saadetistega**. Kui see suvand on sisse lülitatud, otsib protseduur *Lattu väljastamine* konsolideerimiseks saadetisi, otsides olemasolevate saadetiste hulgast, mis loodi sama konsolideerimispoliitika alusel. Sellisel juhul valib süsteem uue saadetise või koormuse loomise asemel olemasoleva. Kuid süsteem konsolideerib ainult olemasolevate saadetistega, mille olek on *Avatud*, voo vabastamisse olekuga *Vabastatud* või kõrgemasse kuuluvaid saadetisi, ei peeta konsolideerimise sihtmärkideks.

Kui saadetise konsolideerimispoliitikad tehakse saadavaks, peidetakse säte **Saadetise konsolideerimine lattu väljastamisel**, mis oli varasemalt saadaval seadistuse lehel **Laod**. Uuele saadetise konsolideerimise funktsioonile ülemineku hõlbustamiseks, loob leht **Saadetise konsolideerimispoliitikad** vaikepoliitika, mis sisaldab automaatselt olemasolevate ladude vana sätet. Kui see vaikepoliitika on loodud, ei võeta enam arvesse sätet **Saadetise konsolideerimine lattu väljastamisel** seadistuse lehel **Laod**.

Saate kasutada lehte **Lattu väljastamine** vastava konsolideerimispoliitika käsitsi alistamiseks, nagu ka saate alistada täitmise poliitikaid.

Enne lattu väljastamist saate lehe **Koorma planeerimise töölaud** käsku **Väljastamine \> Lattu väljastamine** kasutada väljaminevate koormuste loomiseks, mis põhinevad müügi- ja üleviimistellimuseridadel. Need koormused kasutavad sama konsolideerimise loogikat, mis võeti kasutusele koos saadetise poliitikate konsolideerimisega.

Saate kasutada lehte **Saadetise konsolideerimise töölaud** olemasolevate saadetiste konsolideerimiseks, mida pole veel kinnitatud, kuid on juba lattu väljastatud. See funktsioon toetab stsenaariume, kus automatiseeritud väljastamise protsessi, millel on oma saadetise konsolideerimine, käitatakse mitu korda päevas, kuid võimalikud täiendavad konsolideerimised tuvastatakse kinnitamise protsessi käigus käsitsi enne saadetise tarnimist vedajatele. Selle funktsiooni abil saate konsolideerida müügi- või üleviimistellimuse ridadest loodud väljaminevaid saadetisi igal ajal ajal pärast saadetiste lattu väljastamist, kuid enne nende kinnitamist.

Leht **Saadetise konsolideerimise töölaud** toimib sarnaselt koormuse loomise töölauaga, kus saate hinnata mitut saadetist korraga ja määrata mitte-konsolideeritud tellimuse kindlale saadetisele. Saate rakendada saadetise konsolideerimise malle, et hinnata pakutud konsolideerimisi mitu korda ja neid kinnitada. Osasid reegleid rakendatakse volitamata konsolideerimise vältimiseks ja võimalikest tõrgetest hoiatamiseks.

## <a name="overview-of-new-functionality"></a>Uue funktsiooni ülevaade

Selles jaotises kirjeldatakse muudetud või lisatud lehti, käske ja funktsioone, kui lülitate sisse ja kasutate funktsiooni *Saadetise konsolideerimispoliitikad*.

### <a name="shipment-consolidation-policies-page"></a>Saadetise konsolideerimispoliitikate leht

Poliitikaid eristatakse töökäsu tüübi järgi. Tüüp **Müügitellimused** tähistab saadetisi _Müügitellimus_ ja tüüp **Üleviimistellimused** tähistab saadetisi _Edastuse väljaminek_.

Igal saadetise konsolideerimispoliitikal on päring, mis määratleb, millal seda rakendatakse, ja seerianumber, mis määrab täitmise järjekorra. Konsolideerimist rakendatakse igale valitud väljade kordumatule kombinatsioonile. Täiendav parameeter on saadaval olemasolevate (avatud) saadetistega konsolideerimiseks. Poliitikaid hinnatakse ja rakendatakse iga kord, kui luuakse uus saadetis (enne voo töötlemist).

Kui poliitikal puudub mõni kohustuslik väli või kui see sisaldab keelatud välju, märgitakse poliitika kehtetuks jaotises **Valitud**. Kohustuslike ja keelatud väljade loendid on püsiprogrammeeritud ja neid saab laiendada.

Järgmises loendis kuvatakse kohustuslikud väljad. Kuna saadetisi tükeldatakse alati nende väljade põhjal, ei saa te grupeerida mitut saadetist, millel on nendel väljadel erinevad väärtused.

- Müügitellimuste puhul

    - **Konto number:** _WHSShipmentTable.AccountNum_
    - **Tarne saaja:** _WHSShipmentTable.DeliveryName_
    - **Postiaadress (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Ladu:** _WHSShipmentTable.InventLocationId_

- Üleviimistellimuste puhul.

    - **Laost:** _InventTransferTable.InventLocationIdFrom_
    - **Lattu:** _InventTransferTable.InventLocationIdTo_

Järgmised väljad pole ühelegi dokumenditüübile saadaval. Neid väljasid ei kuvata kasutajaliideses (UI) ja neid ei saa kasutada konsolideerimiseks.

- **Saadetise ID:** _WHSShipmentTable.ShipmentId_
- **Olek:** _WHSShipmentTable.ShipmentStatus_
- **Saadetise konsolideerimispoliitika:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Töö kande tüüp:** _WHSShipmentTable.WorkTransType_
- **Voo ID:** _WHSShipmentTable.WaveId_
- **Koormuse ID:** _WHSShipmentTable.LoadId_
- **Saadetise ID:** _WHSLoadLine.ShipmentId_
- **Koormuse ID:** _WHSLoadLine.LoadId_

Poliitika loomisel kasutatakse vaikimisi kohustuslike väljade kogumit konsolideerimise väljadena. Kuid saate seda loendit muuta vasak- ja paremnoole nuppude abil. (See protsess sarnaneb voomallide meetodite valimise protsessi.)

Väärtusi, mida kasutajad nendel väljadel valivad, kasutatakse kõigi vastloodud saadetiste puhul või need lisatakse olemasolevatele saadetistele nende saadetistega konsolideerimisel. Kui kahel saadetisel on sama väärtus väljal, mis on valitud nende saadetiste konsolideerimiseks, konsolideeritakse saadetised. Sama põhimõte kehtib kõigi järgnevate valitud konsolideerimise väljade kohta. Kui need väärtused on erinevad, hüljatakse teine saadetis ja see valitakse uue saadetise jaoks. Automatiseeritud konsolideerimisprotsess koosneb kõigi kordumatute väärtuste kombinatsioonide loomisest saadetise konsolideerimise väljadel ja seejärel saadetise määramisest vastavale kombinatsioonile.

Konsolideerimisprotsessi käigus eiratakse valimata välju. Kui kahel saadetisel on valimata väljal erinevad väärtused, tühjendatakse väli (st see määratakse tühjaks). Kui mõlemal saadetisel on valimata väljal sama väärtus, täidetakse see väli.

Konsolideerimata väljade loend (st väljad, mis tühjendatakse, kui nende väärtused on erinevad) on püsiprogrammeeritud. Loend sisaldab kõiki välju, mis käivitatakse uue saadetise loomisel müügi- või üleviimistellimuse realt. Teisisõnu, kui välja ei käivitata müügi- või üleviimistellimuse realt, siis seda eiratakse olemasolevale saadetisele uute andmete lisamisel.

### <a name="release-to-warehouse-page"></a>Lattu väljastamise leht

- Alumises ruudustikus olev uus väli kuvab rakendatud konsolideerimispoliitika.
- Uus nupp võimaldab teil konsolideerimispoliitika käsitsi valida ja/või alistada.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Käsk Lattu väljastamine lehel Koorma plaanimise töölaud

- Loogikat korrigeeriti nii, et see kasutaks rakendatud konsolideerimispoliitikaid.
- Saadetisi konsolideeritakse nüüd ainult ühe koormuse piires.

### <a name="consolidate-shipments-page"></a>Saadetise konsolideerimise leh

- Sarnaste saadetiste otsimist (st konsolideerimise kandidaadid) muudeti nii, et see kasutaks saadetise konsolideerimispoliitikas valitud välju.
- Eri saadetiste erinevate väärtustega väljad on nüüd määratud tühjaks. (Varasemalt kasutati valitud alussaadetise väärtusi.)

### <a name="shipment-consolidation-workbench-page"></a>Saadetise konsolideerimise töölaua leht

- Uus funktsioon kopeerib käsitsi konsolideerimisprotsessi suuremas mahus.
- Nüüd saate avada selle lehe mooduli **Laohaldus** menüüs **Lattu väljastamine**.
- Algoritm analüüsib olemasolevaid saadetisi, mida pole veel saadetud. Seejärel pakub konsolideerimist konsolideerimispoliitikates valitud väljade põhjal.

## <a name="comparison-of-functionality"></a>Funktsiooni võrdlus

Järgmises tabelis võetakse kokku, kuidas saadetise konsolideerimine toimib, kui te ei kasuta saadetise konsolideerimispoliitikaid ja vastupidi.

| Ilma saadetise konsolideerimispoliitikateta | Saadetise konsolideerimispoliitikatega |
|---|----|
| Pole kohaldatav | Konsolideerimiseks valitud müügi- või üleviimissaadetisel peab olema loodava saadetisega sama konsolideerimispoliitika või need tuleb määrata avatud saadetisele (kui suvand **Konsolideerida olemasolevate saadetistega** on sisse lülitatud). |
| Protseduur *Lattu väljastamine* ei otsi konsolideeritava saadetise leidmiseks olemasolevate saadetiste seast. Konsolideeritava saadetise otsimiseks kasutatakse ainult praeguse *Lattu väljastamise* eksemplariga loodud saadetisi. | Kui suvand **Konsolideeri olemasolevate saadetistega** on sisse lülitatud praegu kasutusel oleva konsolideerimispoliitika jaoks, otsib protseduur *Lattu väljastamine* konsolideeritava saadetise leidmiseks olemasolevate saadetiste hulgast, mis loodi sama konsolideerimispoliitika alusel. Seega, kui teil on kaks poliitikat, ei konsolideerita kunagi 2. poliitika põhjal loodavat saadetist 1. poliitika põhjal loodud saadetisega. |
| Pole kohaldatav | Kui konsolideerimispoliitikate loend on tühi või kui poliitikat ei leita, luuakse iga müügi- või üleviimistellimuse rea kohta uus saadetis. |
| Järgmine konsolideerimise väli määratleb nende väärtuste kordumatu kombinatsiooni, mida kasutatakse saadetiste konsolideerimiseks *üleviimisrea* jaoks. (Kõiki teisi välju eiratakse.)<ul><li>Tellimuse number (OrderNum)</li></ul> | Järgmised konsolideerimise väljad määratlevad nende väärtuste kordumatu kombinatsiooni, mida kasutatakse saadetiste konsolideerimiseks *üleviimisrea* jaoks. (Kõiki teisi välju eiratakse.)<ul><li>Tellimuse number (OrderNum)</li><li>Tarne saaja (DeliveryName)</li><li>Postiaadress (DeliveryPostalAddress)</li><li>ISO riigikood (CountryRegionISOCode)</li><li>Aadress (Address)</li><li>Sait (InventSiteId)</li><li>Ladu (InventLocationId)</li><li>Saadetise vedaja (CarrierCode)</li><li>Vedaja teenus (CarrierServiceCode)</li><li>Tarneviis (ModeCode)</li><li>Vedaja grupp (CarrierGroupCode)</li><li>Tarnetingimused (DlvTermId)</li></ul>Need on ainsad saadaolevad väljad ja käivitatakse uue saadetise loomisel. |
| Järgmised konsolideerimise väljad määratlevad nende väärtuste kordumatu kombinatsiooni, mida kasutatakse saadetiste konsolideerimiseks *müügirea* jaoks. (Kõiki teisi välju eiratakse.)<ul><li>Tellimuse number (OrderNum)</li><li>Kliendi viide (CustomerRef)</li><li>Kliendi ostutellimus (CustomerReq)</li><li>Tarnetingimused (DlvTermId)</li></ul> | Järgmised konsolideerimise väljad määratlevad nende väärtuste kordumatu kombinatsiooni, mida kasutatakse saadetiste konsolideerimiseks *müügirea* jaoks. (Kõiki teisi välju eiratakse.)<ul><li>Tellimuse number (OrderNum)</li><li>Kontonumber (AccountNum)</li><li>Tarne saaja (DeliveryName)</li><li>Postiaadress (DeliveryPostalAddress)</li><li>ISO riigikood (CountryRegionISOCode)</li><li>Aadress (Address)</li><li>Sait (InventSiteId)</li><li>Ladu (InventLocationId)</li><li>Saadetise vedaja (CarrierCode)</li><li>Vedaja teenus (CarrierServiceCode)</li><li>Tarneviis (ModeCode)</li><li>Vedaja grupp (CarrierGroupCode)</li><li>Peatöövõtja ID (BrokerCode)</li><li>Suund (LoadDirection)</li><li>Tarnetingimused (DlvTermId)</li><li>Kliendi viide (CustomerRef)</li><li>Kliendi ostutellimus (CustomerReq)</li></ul>Need on ainsad saadaolevad väljad ja käivitatakse uue saadetise loomisel. |
| Pole kohaldatav | Järgmised konsolideerimise väljad *müügirea* jaoks kohustuslikud ja neid ei saa eemaldada.<ul><li>Kontonumber (AccountNum)</li><li>Tarne saaja (DeliveryName)</li><li>Postiaadress (DeliveryPostalAddress)</li><li>Ladu (InventLocationId)</li></ul>Vaikimisi määratakse need väljad uue poliitika loomisel. Neid ei saa eemaldada. |
| Lehe **Koorma planeerimise töölaud** protseduur *Koormuste lattu väljastamine* kasutab eraldi koodi saadetiste ja voogude loomiseks. | Saadetiste konsolideerimispoliitikaid rakendatakse selleks, et määratleda, milliseid välju tuleks konsolideerimiseks hinnata. Saadetisi konsolideeritakse ainult ühe koormuse piires. |
| Saate käsitsi valida lehel **Kõik saadetised** suvandi **Saadetiste konsolideerimine** ja seejärel valida sihtmärgiks alussaadetise. Filter soovitab kõiki olemasolevaid saadetisi, mille peamistel väljadel on mitu ühtivat väärtust. | Saate käsitsi valida lehel **Kõik saadetised** suvandi **Saadetiste konsolideerimine** ja seejärel valida sihtmärgiks alussaadetise. Süsteem soovitab teisi olemasolevaid saadetisi, sobitades mitme peamise välja väärtusi, mis on konfigureeritud vastavate saadetise konsolideerimispoliitikate jaoks. |
| Lehe **Kõik saadetised** käsku **Saadetiste konsolideerimine** saate kasutada ainult ühe saadetise jaoks. | Leht **Saadetise konsolideerimise töölaud** aitab leida saadetiste kogumit, mis pole veel saadetud olekus. Neid saadetisi analüüsitakse mitme peamise välja alusel, mis on konfigureeritud teie saadetise konsolideerimispoliitikates. Kõiki saadetisi, kus nende väljade väärtused ühtuvad, soovitatakse konsolideerimiseks.<p>Saate konsolideerimist käsitsi hallata, eemaldades saadetisi soovitatud konsolideerimistest ja/või lisades neile saadetisi. Esineda võib mitut tüüpi tõrkeid, kuid võite osasid neist alistada.</p> |
| **Kujunduse märkus:** protseduur *Müügitellimuste automaatne lattu väljastamine* jaotab müügiread gruppidesse. Igal grupil on oma kordumatu väärtus **ReleaseToWarehouseId** ja protseduur *Lattu väljastamine* töötleb seda eraldi. See protseduur loob uue töö, sõltumata tööjaotuse seadistusest. | **Kujunduse märkus:** protseduur *Müügitellimuste automaatne lattu väljastamine* määrab sama väärtuse **ReleaseToWarehouseId** kõigile töödeldavatele müügiridadele. Protseduur *Lattu väljastamine* töötleb kõiki müügiridu korraga. Varasema käitumise tagamiseks peate konfigureerima tööjaotuse saadetise ID kohta. |

## <a name="additional-resources"></a>Lisaressursid

- [Saadetise konsolideerimispoliitikate konfigureerimine](configure-shipment-consolidation-policies.md)
