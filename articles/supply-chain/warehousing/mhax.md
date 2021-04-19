---
title: Materjalikäitlusseadmete liides (MHAX)
description: Selles teemas kirjeldatakse, kuidas seadistada materjalikäitlusseadmete liides (MHAX), et saaksite luua ühenduse väliste füüsiliste materjalikäitluse (MH) süsteemidega.
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9273e4a1f6b3f57086c921c4beb0530a67ccd976
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810506"
---
# <a name="material-handling-equipment-interface-mhax"></a>Materjalikäitlusseadmete liides (MHAX)

[!include [banner](../../includes/banner.md)]

*Materjalikäitlusseadmete liidese* (MHAX) abil saate ühendada väliseid füüsilisi materjalikäsitluse (MH) süsteeme laoga, mida haldab täiustatud laohaldusfunktsioon (WMS) Microsoft Dynamics 365 Supply Chain Managementis. WMS-i ja MH-süsteemide vaheline liideses on kaks järjekorda: üks väljaminevatele sündmustele (WMS-ist MH-sse) ja teine sissetulevatele sündmustele (MH-st WMS-i). WMS-süsteem loob väljaminevad sündmused tööridade põhjal, mis luuakse erinevates töö loomise ja käivitamise protsessides. Seejärel pollib MH-süsteem regulaarselt WMS-süsteemi uute sündmuste osas ja töötleb vastuseid. Kui MH-süsteem on tööjuhiste kohaselt sündmuste käitlemise lõpetanud, saadab see sissetulevad sündmused, nt töörea lõpetamine ja kiirelt komplekteerimine.

Järgmine näide kujutab protsesside erinevaid elemente ja toimumisjärjestust MHAX-i integratsiooni kasutamisel.

![MHAX-i komponendid ja suhtlus](media/mhax-components.png "MHAX-i komponendid ja suhtlus")

Eelmisel joonisel kujutatud suhtluste selgitus.

1. Töö loomisel või töö läbiviimisel luuakse väljaminevad sündmused väljaminevas järjekorras.
2. MH-seadmed ühenduvad MH-seadmete teenusega, pollivad asjakohaseid uusi sündmusi ja töötlevad neid sündmusi.
3. Kui MH-seadmed on tagasiaruandeks valmis, luuakse uuesti ühendus teenusega ja esitatakse sissetulevad sündmused. Järjekorra töötleja töötleb need sündmused kohe.
4. Sissetuleva sündmuse andmete põhjal võib järjekorra töötleja olemasoleva töö käivitada, seda muuta või luua uue töö.

## <a name="turn-on-the-mhax-feature"></a>Funktsiooni MHAX sisselülitamine

Enne kui saate MHAX-i funktsiooni kasutada, peate lülitama sisse nii selle funktsiooni kui ka konfiguratsioonivõtme.

1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.
2. Lülitage tööruumis **[Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** sisse funktsioon nimega *Materjalikäitlusseadmete liides*.
3. Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
4. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
5. Laiendage valikut **Valdkond \> Lao- ja transpordihaldus** ning märkige ruut **Materjalikäitlusseadmete liides**.
6. Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

## <a name="set-mhax-parameters"></a>MHAX-i parameetrite seadistamine

Funktsiooni konfigureerimiseks peate lehel **Materjalikäitlusseadmete liidese parameetrid** seadistama mõned üldised parameetrid.

1. Avage **Materjalikäitlusseadmete liides \> Seadistamine \> Materjalikäitlusseadmete liidese parameetrid**.
2. Vahekaardil **Üldine** määrake järgmised väljad.

    - **Kasutaja ID** – valige töötaja. Seda töötajat kasutatakse kõikide sissetuleva järjekorra kaudu töödeldavate töötoimingute (komplekteerimised ja ladustamised) käivitamiseks.
    - **Luba sissetuleva sõnumi ID** – kui see suvand on seatud väärtusele *Jah* ja kui saabub sissetuleva sõnumi ID duplikaat, lükatakse sõnum tagasi ja veateade näitab, et sõnum on juba olemas. Kui see suvand on seatud väärtusele *Ei*, siis lubatakse sissetulevate sõnumite ID-de duplikaadid.

3. Valige vahekaardil **Numbriseeriad** kogu süsteemi hõlmavad numbriseeriad, mida tuleks kasutada kordumatute ID-de loomiseks sissetuleva järjekorra kaupadele, väljamineva järjekorra kaupadele ja tööreapaaridele.

## <a name="outbound-events"></a>Väljaminevad sündmused

Teatud etappides töö loomise või töö läbiviimise ajal määrab süsteem, kas tuleb luua väljaminevad sündmused MH-süsteemi saatmiseks. Kui laotöötluse ajal on teatud etappi konfigureeritud kordustellimus, loob süsteem sündmuse vastavalt kordustellimuse seadistustele.

### <a name="structure-of-outbound-events"></a>Väljaminevate sündmuste struktuur

Iga väljaminev sündmus on kordumatult identifitseeritav väljamineva järjekorra ID-ga. Väljamineva kande tüüp määratleb sündmuse tüübi. Sündmusele salvestatakse ka ladu ja sündmuse loonud kordustellimuse ID.

Andmete MH-süsteemi viimiseks sisaldab väljaminev sündmus 10 andmevälja (**andmed01** kuni **andmed10**). Need andmeväljad on üks-ühele (1:1) vastendatud olemasolevate andmebaasiväljadega. Täpsemalt eraldatakse need töörea ja tööpäise tabelite väljadest. Välju saab vabalt valida. Need seadistatakse kordustellimuse loomisel.

Lisaks 10 andmeväljale, mis on 1:1 vastendatud olemasolevate andmebaasiväljadega, võib sündmus sisaldada täiendavat andmevälja, mida nimetatakse *lastiks*. Selle välja sisu luuakse kohandatud X++ koodiga, mida nimetatakse *lasti generaatoriks*. Iga kasutatav lasti generaator seadistatakse kordustellimuses.

Kindlustamaks, et MH-süsteem saab iga väljamineva järjekorra ID ainult üks kord, kasutatakse olekuvälja, et määratleda, kas sündmus on välissüsteemi saatmiseks valmis või on juba saadetud.

### <a name="outbound-queue-subscriptions"></a>Väljamineva järjekorra kordustellimused

Enne sündmuste loomist tuleb seadistada kordustellimus, mis ütleb MHAX-i funktsioonile, kas ja kuidas sündmusi luua. Loodud sündmused märgistab kordustellimuse identifikaator. Seetõttu saab mitu MH-süsteemi ühenduda sama WMS-süsteemiga, kuid hoida oma sündmused eraldi. Kui MHAX-i teenust pollitakse uute sündmuste osas, on kordustellimus üks saadaolevaid valikuid sündmuste toomiseks.

Kordustellimuse loomiseks avage **Materjalikäitlusseadmete liides \> Seadistamine \> Kordustellimused**. Iga kordustellimuse jaoks on saadaval järgmised parameetrid.

- **Kordustellimuse ID** – kordumatu nimi, mis identifitseerib kordustellimuse.
- **Kirjeldus** – kordustellimuse kirjeldus vaba tekstina.
- **Ladu** – konkreetsed laod, mille järgi tuleks sündmusi filtreerida.
- **Väljamineva kande tüüp** – sündmuste tüüp, mida kordustellimus peaks sisaldama.
- **Lasti generaator** – valikuline koodilaiend, mis võib sisestada lisateavet väljamineva sündmuse väljale **Last**.

Iga kordustellimusega saab seostada päringu. See päring filtreerib tööread ja -päised, et veelgi piirata tööd, mis kasutab kordustellimust sündmuste loomiseks. Kordustellimusele päringu lisamiseks märkige lehel **Kordustellimused** asjakohase kordustellimuse juures ruut **Käivita päring** ja seejärel valige toimingupaanil **Redigeeri päringut**. Kuvatakse standardne Supply Chain Managementi päringuredaktor.

Lisaks sisaldab kordustellimus *kordustellimuste kaarti*, mis vastendab kas tööpäise või töörea väljad väljamineva sündmuse mõne või kõigi 10 vaba andmeväljaga, nagu vajalik. Teabe tagastamiseks MHAX-teenusesse kaasate tavaliselt töörea kirje ID või *töörea paari ID*. (Töörea paari ID on uus atribuut, mis võimaldab süsteemil kasutada ühte tagastuskäsku komplekteerimise ja ladustamise ridade töötlemiseks.) Ülejäänud väljad sõltuvad kasutusjuhtumist. Mõned näited tuuakse selles teemas allpool.

Kordustellimuste kaardi häälestamiseks valige lehel **Kordustellimused** kohane kordustellimus ja seejärel valige toimingupaanil **Kordustellimuse kaart**. Kuvatavas dialoogiaknas **Kordustellimuse kaart** saate vastavalt vajadusele määrata igale saadaolevale andmeväljale tabeli ja välja.

### <a name="outbound-event-types"></a>Väljaminevate sündmuste tüübid

Selles jaotises kirjeldatakse erinevaid saadaolevaid sündmusetüüpe. (Sündmuse tüüpe nimetatakse ka *kandetüüpideks*.) Samuti selgitatakse, millal sündmusetüübid WMS-süsteemis luuakse.

#### <a name="work-creation-events"></a>Töö loomise sündmused

Töö loomise sündmused luuakse pärast töö loomist rakenduse poolt. Selline tegevusmuster rakendub enamikule töö loomise protsesside tüüpidele, näiteks komplekteerimis- ja täiendamistöö loomisele. Üldjuhul luuakse töö loomise sündmus, kui töö on loodud olekus *Avatud*, mis näitab, et töö on töötaja poolt käivitamiseks valmis. Lisaks luuakse töö loomise sündmused tvaliste liikumise tööde jaoks (mitte liikumisel malli tööga), kuigi neid töid ei looda avatud tööna.

Sellise tegevusmustri oluliseks erandiks on tsüklilise inventuuri töö, mida praegu ei toetata. MH-süsteemi laoinventuurid jäävad MHAX-i ulatusest väljaspoole ja inventuuride tulemused tuleb importida varude inventuuritöölehele.

Pärast töö loomist töötleb MHAX-i teenus loodud tööridu ja määrab töörea paari ID kõigile loodud tööridadele iga tööpäise jaoks. Eesmärk on grupeerida iga komplekteerimise töörida koos sellele järgneva ladustamisega ühe töörea paari ID alla. (Grupid vastavad töömallide komplekteeri/ladusta paaridele.) Sel viisil saab ühte ID-d kasutada töö lõpetamise aruandluseks kõigi seotud komplekteerimise ja ladustamise ridade jaoks. Grupeerimisprotsess algab esimesest reast ja jätkub sama ID-ga kuni järgmise komplekteeri/ladusta tööridade paari saabumiseni. Käitamise ID määratakse selle paari komplekteerimisreale. Paarile järgnevast komplekteerimisreast edasi kasutatakse uut ID-d. Protsess jätkub seni, kuni kõik tööpäisesse kuuluvad read on töödeldud.

Kui tööpäises on suvandi **Blokeeritud voog** väärtuseks seatud *Jah*, on töö loomise sündmuste erifunktsioonina loodud sündmuste olekuks *Blokeeritud*, mitte tavaline olek *Valmis*, mida kasutatakse nende saatmiseks MH-süsteemi. Lipp **Blokeeritud voog** tööpäises näitab, et tööpäis pole veel töötajate poolt käivitamiseks valmis, võib-olla lõpetamata täiendamistöö tõttu. Kui lipp **Blokeeritud voog** eemaldatakse, siis juba loodud sündmuste blokeering tühistatakse ja need on MH-süsteemile järjekorrast toomiseks saadaval.

#### <a name="work-initiation-events"></a>Töö algatamise sündmused

Töö algatamise sündmused käivitatakse, kui töö olek muudetakse töö värskendamise käigus olekust *Avatud* olekuks *Pooleli*.

#### <a name="work-completion-events"></a>Töö lõpetamise sündmused

Töö lõpetamise sündmused käivitatakse, kui töö olek muudetakse töö värskendamise käigus olekust *Pooleli* olekuks *Suletud*.

#### <a name="work-cancellation-events"></a>Töö tühistamise sündmused

Töö tühistamise sündmused käivitatakse, kui töö olek muudetakse töö värskendamise käigus mis tahes olekust peale oleku *Tühistatud* olekuks *Tühistatud*. Lisaks kustutatakse järjekorrast kõigi kordustellimuste kõik muud tööpäisega seotud sündmused. Sel moel välditakse väliste süsteemide ebavajalike sündmuste töötlemist.

#### <a name="pickput-completion-events"></a>Komplekteerimise/ladustamise lõpetamise sündmused

Komplekteerimise/ladustamise lõpetamise sündmused käivitatakse, kui komplekteerimise/ladustamise rea olek muudetakse töörea värskendamise käigus olekust *Pooleli* olekuks *Suletud*.

### <a name="monitor-the-outbound-queue"></a>Väljamineva järjekorra jälgimine

Väljamineva järjekorra ülevaatamiseks avage **Materjalikäitlusseadmete liides \> Üldine \> Väljaminev järjekord**. Lehel **Väljaminev järjekord** loetletakse kõik väljamineva järjekorra kaubad ja nende olek. Valige järjekorra kaup, et vaadata selle üksikasju. Üksikasjad hõlmavad kauba kande tüüpi, selle kasutatavat kordustellimust ja iga andmevälja väärtusi (**andmed01** kuni **andmed10**) ning lasti.

### <a name="clean-up-the-outbound-queue"></a>Väljamineva järjekorra puhastamine

Teatud aja jooksul hakkab väljaminev järjekord täituma juba saadetud järjekorrakaupadega. Nende kaupade eemaldamiseks avage **Materjalikäitlusseadmete liides \> Perioodilised ülesanded \> Puhastamine \> Väljamineva järjekorra puhastamine**.

## <a name="inbound-events"></a>Sissetulevad sündmused

Selles jaotises kirjeldatakse erinevaid sissetulevate sündmuste tüüpe, millest MH-süsteem saab WMS-süsteemile tagasi teatada. Selgitatakse ka MH-süsteemi esitatavaid andmeid ja mida iga sissetulev sündmus WMS-süsteemis teeb.

### <a name="structure-of-inbound-events"></a>Sissetulevate sündmuste struktuur

Sissetuleva sündmuse edastamisel peab väline süsteem esitama sissetuleva kande tüübi koos kuni 10 parameetriga (**andmed01** kuni **andmed10**). Valikulise valideerimise abil saab tagada, et MHAX-teenus ei saak sama sissetulevat sündmust rohkem kui üks kord. Valideerimise lubamiseks peab igal sissetuleval sündmusel olema kordumatu sõnumi ID. Kui saabub sõnumi ID duplikaat ja kui lehel **Materjalikäitlusseadmete liidese parameetrid** on suvand **Luba sissetuleva sõnumi ID** seatud väärtusele *Jah*, lükatakse sõnum tagasi. Tõrketeade näitab, et sõnum on juba olemas.

Lisaks sissetulevatele andmeväljadele määrab süsteem sündmusele kordumatu sissetuleva järjekorra ID.

### <a name="inbound-event-types"></a>Sissetulevate sündmuste tüübid

Selles jaotises kirjeldatakse toetatud sissetulevate sündmuste tüüpe (kandetüüpe) ja andmeid, mis tuleb töödeldavate sündmuste kohta esitada.

#### <a name="work-confirm-events"></a>Töökinnitamise sündmused

Töökinnitamise sündmused vajavad sissetulevatel andmeväljadel järgmist teavet.

- **andmed01** – töörea paari ID.
- **andmed02** – töörea kirje ID (`RecId` väärtus).

    > [!NOTE]
    > *Olemas peab olema* kas väli **andmed01** *või* väli **andmed02**.

- **andmed03** – selle litsentsiplaadi ID, millelt komplekteeritakse.
- **andmed04** – tööpäise sihtlitsentsiplaadi ID.

Kui on olemas töörea paari ID, käitatakse järjest kõik tööread, mis on töörea paari ID-ga märgitud ja mille olek on *Avatud* või *Pooleli*. Kui on olemas töörea kirje ID (`RecId` väärtus), peab töörida olema komplekteerimine, ladustamine või kohandatud töörida, mille olekuks on *Avatud* või *Pooleli*.

Litsentsiplaadiga juhitavatest asukohtadest pärit komplekteerimisread vajavad, et **andmed03** määratleks litsentsiplaadi, millelt komplekteeritakse, olenemata sellest, kas read on märgitud töörea kirje ID-ga või töörea paari ID-ga. Väli **andmed04** peab määratlema komplekteerimise tööpäise sihtlitsentsiplaadi.

Ladustamisread ei aktsepteeri lisateavet. Need käivitatakse ainult praeguse töörea asukoha ja töö sihtlitsentsiplaadi alusel. Kui ladustamine tuleb teha teises asukohas, muutke töörea asukohta vastavalt kirjeldusele jaotises [Alistamissüdnmused](#override-events) selles teemas allpool.

Kohandatud tööread ei vaja ega toeta mingisugust sissetuleva sündmuse lisateavet.

#### <a name="short-pick-events"></a>Kiire komplekteerimise sündmused

Kiire komplekteerimise sündmused vajavad sissetulevatel andmeväljadel järgmist teavet.

- **andmed02** – töö kirje ID (`RecId` väärtus).
- **andmed03** – selle litsentsiplaadi ID, millelt komplekteeritakse.
- **andmed04** – komplekteeritav kogus.
- **andmed05** – kiire komplekteerimise erandi kood.
- **andmed06** – tööpäise sihtlitsentsiplaadi ID.

> [!NOTE]
> Välja **andmed01** kiire komplekteerimise sündmuste korral ei kasutata.

See sündmus sarnaneb töökinnitamise sündmusele, kuid kehtib ainult komplekteerimisridadele.

#### <a name="override-events"></a><a id="override-events"></a>Alistamissüdnmused

Alistamissüdnmused vajavad sissetulevatel andmeväljadel järgmist teavet.

- **andmed01** – töö kirje ID (`RecId` väärtus).
- **andmed02** – uue asukoha ID.

Töörea olek peab olema kas *Avatud* või *Pooleli* ja olemas peab olema uus asukoht.

#### <a name="license-plate-receipt-events"></a>Litsentsiplaadi sissetuleku sündmused

Litsentsiplaadi sissetuleku sündmused vajavad sissetulevatel andmeväljadel järgmist teavet.

- **andmed01** – vastuvõetava sissetuleva litsentsiplaadi ID.

Süsteem teeb litsentsiplaadi vastuvõtmise toimingu litsentsiplaadiga, mis edastatakse välja **andmed01** väärtusena.

### <a name="monitor-the-inbound-queue"></a>Sissetuleva järjekorra jälgimine

Sissetuleva järjekorra ülevaatamiseks avage **Materjalikäitlusseadmete liides \> Üldine \> Sissetulev järjekord**. Lehel **Sissetulev järjekord** loetletakse kõik sissetuleva järjekorra kaubad ja nende olek. Valige järjekorra kaup, et vaadata selle üksikasju. Üksikasjad hõlmavad kauba kande tüüpi, sõnumi ID-d ja iga andmevälja väärtusi (**andmed01** kuni **andmed10**).

Kui sissetulevate sündmuste töötlemisel ilmnes tõrge või logikauba muu tüüp, saate logi üle vaadata, valides toimingupaanil **Tõrkelogi**.

### <a name="inbound-event-processing"></a>Sissetuleva sündmuse töötlus

Sissetulevad sündmused kirjutatakse esmalt andmebaasi ja käivitatakse seejärel kohe (sünkroonselt). Kui töötlemisel ilmneb tõrge, kirjutatakse sündmus järjekorda, kuid olekuks määratakse *Tõrkega*. MHAX-teenus tagastab MH-süsteemile tõrketeate ja talletab hilisemaks uurimiseks sissetuleva sündmuse kirjesse tõrkelogi.

Sündmusi olekuga *Tõrkega* saab hiljem uuesti töödelda, kui tõrkeseisund kõrvaldatakse. Nende uuesti töötlemiseks tehke üks järgmistest toimingutest.

- Avage **Materjalikäitlusseadmete liides \> Üldine \> Sissetulev järjekord**. Valige vastav sissetulev järjekord ja seejärel valige toimingupaanil **Töötle uuesti**.
- Avage **Materjalikäitlusseadmete liides \> Üldine \> Tõrkega sissetuleva järjekorra uuesti töötlemine**. Kuvatakse standardne pakett-töö dialoogiaken. Seal saate seadistada kirjefiltri ja planeerida või käivitada pakett-töö järjekorra uuesti töötlemiseks.

Kõik töötoimingud (komplekteerimised ja ladustamised) käivitatakse, kasutades töötajat, kes on valitud lehe **Materjalikäitlusseadmete liidese parameetrid** väljal **Kasutaja ID** .

### <a name="clean-up-the-inbound-queue"></a>Sissetuleva järjekorra puhastamine

Teatud aja jooksul hakkab sissetulev järjekord täituma juba töödeldud järjekorrakaupadega. Nende kaupade eemaldamiseks avage **Materjalikäitlusseadmete liides \> Perioodilised ülesanded \> Puhastamine \> Sissetuleva järjekorra puhastamine**.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Järjekorrahalduri abil kiire ülevaate saamine

Kõigist sissetulevate ja väljaminevate järjekordadega seotud tegevustest kiire ülevaate saamiseks avage **Materjalikäitlusseadmete liides \> Tööruum \> Järjekorrahaldur**. Lehel **Järjekorrahaldur** on komplekt vahekaarte ja paane, mille abil saate järjekordi jälgida ja uurida. Lisaks leiate sealt kasulikud lingid enamikule teistele selles teemas mainitud lehtedele.

## <a name="connect-to-the-mhax-service"></a>Ühendamine MHAX-teenusega

MHAX juurutatakse kohandatud teenusena. Seetõttu on see juurdepääsetav SOAP- ja REST-kõnedega. SOAP-i ja REST-i lõpp-punktide aadressid on järgmised.

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Väljaminevast järjekorrast sõnumite toomine

Väljaminevast järjekorrast sõnumite toomiseks kasutage ühte järgmistest meetoditest.

- Kasutage `readOutboundSubscriptionQueue` sündmuste toomiseks kordustellimuse ID alusel.
- Kasutage `readOutboundWarehouseQueue` sündmuste toomiseks sündmuse tüübi ja lao ID alusel mitme kordustellimuse ulatuses.
