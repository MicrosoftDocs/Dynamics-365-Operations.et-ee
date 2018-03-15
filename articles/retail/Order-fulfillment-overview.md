---
title: "Kaupluse tellimuse täitmise ülevaade"
description: "Teema annab ülevaate kaupluse tellimuse täitmisest."
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 997b6843fb729ed204e4e8ec5369c5a380efc25e
ms.openlocfilehash: fb36f6ce81c5e781e3c98132f18ecbd84d0d4089
ms.contentlocale: et-ee
ms.lasthandoff: 02/12/2018

---

# <a name="store-order-fulfillment"></a>Kaupluse tellimuse täitmine

[!include[banner](includes/banner.md)]

Paljud jaemüüjad soovivad tellimuste täitmist optimeerida, võimaldades kauplustel tellimusi täita. Tellimuse täitmine kaupluse tasemel aitab leevendada laoülejäägi olukordi kindla kaupluse puhul või võib olla vajalik logistika seisukohalt, kui kauplusel on lisavõimsust või see asub kliendile saatmiseks lähemal. Selle vajaduse täitmiseks on kassas saadaval ühtse tellimuse täitmise toiming.

Kindlas kaupluses täitmist vajavatele tellimustele on määratud kaupluse ladu tellimuse päises või ridadel. 

Tellimuse täitmise toiming kassas annab kassas üksiku tööala, mida saab tellimuste töötlemisteks kasutada. See hõlmab kõike alates tellimuse aktsepteerimisest kuni saadetuna märkimise või kauplusest kättesaamise algatamiseni. 

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Ühtse tellimuse täitmisele juurdepääsemine kassas

Tellimuse täitmist, [toimingu ID 928](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations), saab kasutada juurdepääsuks kaupluse tellimuse täitmise tööalale kassas. 

Tellimuse täitmise toimingul ei ole oma valmisluba, kuid tulevikus on kasutajatel võimalik kasutada kassast toimingu alustamiseks luba nimega **Luba tellimuse toomine**.

Kaupluse tasemel on saadaval konfiguratsioonisäte määramaks, kas tellimuserida peab olema aktsepteeritud kassas käsitsi. Kui see konfiguratsioonivalik pole määratud, aktsepteeritakse tellimuseread vaikimisi. Selle konfiguratsioonivalik sisselülitamisel peavad kasutajad kassas valima loa nimega **Luba tellimuste aktsepteerimine**, et aktsepteerida tellimused kassas.
Tellimuseridu saab kassas ka tagasi lükata. Tellimuserea tagasilükkamine näitab, et seda ei täideta selles kaupluses ja tellimuserida saadetakse tagasi ümbermääramiseks teise kauplusse või lattu. Tellimuserea tagasilükkamise luba antakse loa **Luba tellimuste tagasilükkamine** kaudu. 

## <a name="order-fulfillment-operation-parameters"></a>Tellimuse täitmise toimingu parameetrid

Tellimuse täitmine pakub valmisparameetreid, mille saab toimingule rakendada, kui see kassas avatakse. Kui parameeter **Kõik tellimused** on konfigureeritud, kuvatakse toimingu kasutamisel kõik tellimused. Parameeter **Tellimused saatmiseks** kuvab ainult tellimused, mis tuleb kauplusest saata, ja parameeter **Tellimused kättesaamiseks** näitab tellimusi, millele tullakse kauplusse järele. 

## <a name="orders-for-fulfillment"></a>Tellimused täitmiseks

Tellimuse täitmise toiming kuvab ainult need tellimused, mis praegusest kauplusest kätte saadakse või lähetatakse. Tellimuse täitmise toimingul ei kuvata teistele kauplustele täitmiseks mõeldud tellimusi. 

## <a name="line-selection"></a>Rea valik

Ridu saate valida funktsiooniga **Valimine** toimingupaanil. Kui suvand **Valimine** on lubatud, saab töötlemiseks valida mitu rida. Valitud rea kustutamiseks klõpsake uuesti sama rida. 

## <a name="line-details"></a>Rea üksikasjad

Rea üksikasju saab kuvada rea üksikasjade hüpikmenüü abil. Selle menüü kasutamisel pakutakse kolme vahekaarti valitud rea kohta lisateabe kuvamiseks. Esimesel vahekaardil **Rea üksikasjad** on toodud nii rea enda kui ka tellitud ja järelejäänud koguse üksikasjad. Kuvatakse ka täiendavad üksikasjad, sh komplekteeritud, pakitud ja arveldatud kogus, samuti tarneviis ja tarneaadress. Vahekaardil **Tellimuse üksikasjad** on toodud tellimuse päiseteave, sh klient, kliendi ID, tellimuse number, tellimuse summa ja saldo. Vahekaardil **Varud** kuvatakse teavet valitud rea füüsiliselt laos saadaolevate, reserveeritud ja tellitud varude kohta.

Kui valitud on mitu rida, kuvatakse tellimuserea üksikasjade hüpikaknas ainult see, et valitud on mitu rida. Üksiku rea üksikasjade kuvamiseks tühistage ridade valikud, kuni valituks on jäänud ainult üks rida. 

## <a name="pending-order-lines"></a>Ootel tellimuseread

Ühtse tellimuse täitmine hõlmab võimalust tellimusi käsitsi aktsepteerida. Vaikimisi on kaupluses täidetavad tellimused juba aktsepteeritud. Kui aga äriprotsessid nõuavad, et tellimused peab aktsepteerima kaupluse tasemel töötaja, saab sisse lülitada käsitsi aktsepteerimise jaekaupluse tasemel. Tellimuse aktsepteerimise lubamiseks minge jaotisse **Jaemüük** > **Kanalid** > **Jaekauplused** > **Kõik jaekauplused**. Avage soovitud kauplus ja leidke vahekaardil **Üldine** alampäis **Tellimuse täitmine**. Sellel alampäisel on suvand **Käsitsi aktsepteerimine**, mille sätteks on vaikimisi määratud **Ei**. Valides selle suvandi sätteks **Jah** ja sünkroonides muudatused kanali andmebaasiga, saavad tellimuseread läbida aktsepteerimisprotsessi.

Töötajad, kellel on luba nimega **Luba tellimuste aktsepteerimine**, saavad avada tellimuse täitmise ja valida aktsepteerimiseks read. Kui read on aktsepteeritud, muutub nende olek sättelt **Ootel** sättele **Aktsepteeritud** ja ülejäänud tellimuse täitmise protsessi saab jätkata. Kui suvand **Käsitsi aktsepteerimine** on sisse lülitatud, ei töödelda tellimusi enne, kui need on aktsepteeritud. 

Tellimuste, mis on mõeldud kauplusest kättesaamiseks, olek pole kunagi **Ootel**. Seda tehakse selleks et vältida olukorda, kus klient saabub kauplusse ja tellimuserida ei saa töödelda, kuna sobiva õigusega töötaja pole saadaval.

## <a name="accepted-order-lines"></a>Aktsepteeritud tellimuseread

Tellimused, mille rea olek on **Aktsepteeritud**, saavad jätkata kassas ülejäänud tellimuse täitmise protsessi läbimist. Pärast tellimuse aktsepteerimist saab tellimusereaga teha kõiki ülejäänud tegevusi. 

Näiteks saab aktsepteeritud tellimuserea valida ja seejärel kätte saada otse ilma komplekteerimist ja pakkimist läbimata.

## <a name="line-actions"></a>Rea tegevused

### <a name="pick"></a>Komplekteeri

Tegevuste kategooria **Komplekteerimine** on mõeldud tellimuseridade riiulitelt komplekteerimise abistamiseks. Komplekteerimistegevuse saab teha ainult eelnevalt aktsepteeritud tellimuseridade puhul. 

**Tegevus: komplekteerimine**

- Kassa tulemolek: komplekteerimine
- Varukontori tulemolek: muudatusteta

Kui tellimus on aktsepteeritud, saab ridu valida ja nende olekuks märkida **Komplekteerimisel**. Kui märgite rea olekuks **Komplekteerimisel**, näitab see, et real juba tehakse komplekteerimistööd. See takistab kahel töötajal samal ajal samade tellimuseridade komplekteerimist.  

**Tegevus: komplekteerimislehe printimine**

- Tulemolek: komplekteerimine
- Varukontori tulemolek: muudatusteta

Komplekteerimislehti saab printida kassas, et aidata töötajaid komplekteerimisprotsessi juures. Prinditud komplekteerimislehte saab komplekteeriv töötaja kaasas kanda ja kui tooted on komplekteeritud, märgib töötaja need komplekteerimislehel käsitsi komplekteerituks. 

Komplekteerimislehe vorming konfigureeritakse rakenduses Dynamics 365 for Retail ja lisatakse kviitungiprofiilile. Lisateavet kviitungiprofiilide seadistamise kohta vt teemast [Kviitungite mallid ja printimine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

Kui read on valitud ja nende ridade kohta komplekteerimisleht prinditud, värskendatakse nende olekuks automaatselt **Komplekteerimine**. 

**Tegevus: komplekteerituks märkimine**

- Tulemolek: komplekteeritud või osaliselt komplekteeritud
- Varukontori tulemolek: komplekteeritud või osaliselt komplekteeritud

Kui füüsiline komplekteerimisprotsess on tehtud, saab ridade olekuks märkida **Komplekteeritud**. Rea valimine ja selle olekuks **Komplekteeritud** märkimine teeb reaalajas taotluse värskendada tellimuserida rakenduses Dynamics 365 for Retail. Kui rea olekuks on kassas märgitud **Komplekteeritud**, värskendatakse ka varukontoris selle olekuks **Komplekteeritud** ja laokanded kajastavad, et määratud kogust on vähendatud.

Tellimuste töötlemisel aja jooksul saab kindla rea puhul töödelda osalisi koguseid. Kui rida on valitud ja tegevus **Komplekteerituks märkimine** tehtud ning kogus on suurem kui üks, küsitakse kasutajalt kogust. Järelejäänud komplekteeritav kogus sisestatakse automaatselt. Kui määratud kogus on järelejäänud kogusest väiksem, muutub rea olekuks **Osaliselt komplekteeritud**. Tellimuserea värskendamisel varukontoris kajastab see ka osaliselt komplekteeritud olekut ja varude värskendamiseks kasutatakse kasutaja sisestatud kogust. 

Kui tellimuserida on komplekteeritud ekslikult, tuleb varukontoris teha tellimusereal komplekteerimise tühistamise protsess. Komplekteerimise tühistamise protsessi praegu kassas ei toetata. 

Tellimuseridu erinevatelt tellimustelt saab valida ja märkida nende olekuks **Komplekteerimine**, printida samale komplekteerimislehele ja märkida olekuks **Komplekteeritud**. 

### <a name="pack"></a>Pakkimine

Tellimuseridu saab pakkida igal ajal pärast seda, kui tellimuserida on aktsepteeritud. 

**Tegevus: saatelehe printimine**

- Tulemolek: pakitud või osaliselt pakitud
- Varukontori tulemolek: tarnitud või osaliselt tarnitud

See tegevus märgib read pakituks või osaliselt pakituks ja prindib saatelehe. Saatelehe saab välja printida, et kontrollida kokku pakitud tooteid. Saatelehe vorming konfigureeritakse rakenduses Dynamics 365 for Retail ja lisatakse kviitungiprofiilile. Lisateavet kviitungiprofiilide seadistamise kohta vt teemast [Kviitungite mallid ja printimine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/receipt-templates-printing).

**Tegevus: pakituks märkimine**

- Tulemolek: pakitud või osaliselt pakitud
- Varukontori tulemolek: tarnitud või osaliselt tarnitud

Tegevusega **Pakituks märkimine** saab näidata, et read on pakitud saatelehte printimata. Nii **Saatelehe printimine** kui ka **Pakituks märkimine** annavad tulemuseks laokanded varukontoris. Saatelehe read kassas annavad tulemuseks varukontoris saatelehe töölehtede loomise. 

Kui tellimuserida on pakitud ekslikult, tuleb saatelehe töölehte korrigeerida varukontoris. 

Korraga saab pakkida ainult samal real olevaid ja sama tarneviisiga ridu.

Praegu on suvand, mis võimaldab märkida kaupluse kättesaamisridade olekuks **Pakitud**, keelatud. See võimalus lisatakse tulevases väljaandes. Saatelehe loomise protsessi täiustatakse, nii et see toetaks muu osapoole lähetusteabe sisestamist saatelehe protsessi.

### <a name="pick-up"></a>Komplekteeri

Kauplusest kättesaadavad tellimused on võimalik kätte saada, kui need on toodud kassasse. Kauplusest kättesaadavaid tellimusi ei aktsepteerita. 

**Tegevus: kättesaamine**

- Tulemolek: arveldatud või osaliselt arveldatud
- Varukontori tulemolek: arveldatud või osaliselt arveldatud

Kui rida on valitud kättesaamiseks ühtse tellimuse täitmisest, laaditakse kogu tellimus kassasse ja valitud rea puhul märgitakse täielik kogus. Tellimuse ülejäänud read laaditakse kassas samuti kandevaatesse, kuid koguseks märgitakse null. 

Kui kättesaamisread on laaditud kandevaatesse, saab kande eest maksta tavapärasel viisil. 

Ridu, mis on kättesaamise kaudu täielikult arveldatud, ei kuvata enam ühtse tellimuse töötlemisel. Ridu, mis on osaliselt kätte saadud, kuvatakse ühtse tellimuse täitmises seni, kuni need on täielikult kätte saadud. 

Kui mõni rida saadakse kätte ekslikult, tuleb vea parandamiseks teha tagastus.  

Korraga on võimalik kätte saada ainult samal real olevaid ja sama tarneviisiga ridu. 

### <a name="shipping"></a>Lähetamine

Kauplusest lähetatavaid tellimuseridu saab töödelda ühtse tellimuse täitmise kaudu, kasutades tegevust **Lähetamine**. Kui käsitsi tellimuserea aktsepteerimine konfigureeritakse kanalitasemel, tuleb tellimused enne lähetamist aktsepteerida. Kui tellimuserida on aktsepteeritud ja selle oleku on **Ootel** või mõni muu, saab ridu lähetada. 

**Tegevus: lähetamine**

- Tulemolek: arveldatud või osaliselt arveldatud
- Varukontori tulemolek: arveldatud või osaliselt arveldatud

Ühtse tellimuse täitmisest lähetatud read arveldatakse varukontoris samamoodi kui siis, kui tellimus arveldatakse otse varukontorist. Ühtse tellimuse täitmisest lähetatavaid ridu ei laadita kandevaatesse ja ridade lähetamise ajal ei toimu mingit maksmist. 

Täielikult lähetatud tellimuseridu ei kuvata enam ühtse tellimuse täitmisel. Osaliselt lähetatud ridu kuvatakse ühtse tellimuse täitmises seni, kuni need on täielikult lähetatud. 

Korraga saab lähetada ainult sama tellimuse ridu. Kui sama tellimuse ridadel on erinevad tarneviisid, saab neid samal ajal lähetamiseks siiski valida. 

### <a name="reject"></a>Lükka tagasi

Ridu või osalisi ridu saab tagasi lükata. See võimaldab neid varukontorist ümber määrata teise kauplusse või lattu. Ridu saab tagasi lükata ainult siis, kui need pole veel komplekteeritud või pakitud. Juba komplekteeritud või pakitud rea tagasilükkamiseks tuleb selle rea komplekteerimine või pakkimine varukontoris tühistada. 

**Tegevus: tagasilükkamine**

- Tulemolek: tagasi lükatud
- Varukontori tulemolek: muudatusteta 

Tagasilükatud ridu saab vaadata tööruumis **Müügitellimuse töötlemine ja päring**. Kõigi tagasilükatud tellimuseridade nägemiseks kõigis kauplustes eemaldage tööruumis isikufilter. Vahekaardil **Tagasilükatud tellimuseread** jaotises **Tellimused ja lemmikud** kuvatakse tellimuserea üksikasjad. Peale selle saavad kasutajad klõpsata nuppu **Tagasilükatud tellimuseread** jaotises **Kokkuvõte**, et minna müügitellimuse vaatesse. Kuvatakse kõik tellimused, millel on üks või mitu tagasilükatud tellimuserida. Kui jaotatud tellimusehaldus (DOM) on lubatud, määratakse tagasilükatud tellimused täitmiseks automaatselt ümber sobivatesse kauplustesse, kuid neid tellimuseridu saab ka käsitsi ümber määrata. Selleks valige rida, mille suvandi **Täitmise olek** sätteks on **Tagasi lükatud**, ja muutke vajadust mööda laoala/ladu. Klõpsake rippmenüüd **Rea värskendamine** ja klõpsake valikut **Lähtesta täitmise olek**, et muuta täitmise olek sättelt **Tagasi lükatud** sättele **Aktsepteeritud** või **Ootel** olenevalt tellimuse täitmise seadistusest. Kui täitmise olek on lähtestatud, saavad kaupluse töötajad vaadata tellimusridu kassas.

## <a name="line-quantity-tracking"></a>Reakoguse jälgimine

Üht tellimuserida, mille kogus on suurem kui üks, saab töödelda aja jooksul, mis annab tulemuseks tellimuseridade mitu alamolekut. Näiteks kui ehitajal on projekt, mis nõuab 500 plaati, kuid ta võtab vastu või talle tarnitakse projekti vältel ainult mõned plaadid korraga, võib tellimusel olla koguseid, mida komplekteeritakse, pakitakse ja lähetatakse samal ajal. 

Iga kord, kui rida valitakse, täidetakse rea järelejäänud summa automaatselt, eeldades, et järelejäänud kogust töödeldakse. Kasutades ülaltoodud näidet – kui 200 plaati on juba kätte saadud ja plaatide rida on komplekteerimiseks valitud, sisestatakse koguseväljale automaatselt järelejäänud kogus 300 plaati. Sama kehtib ka siis, kui 200 plaati on juba arveldatud. Sel juhul saab automaatselt sisestada ainult järelejäänud koguse. 

Jätkates ülaltoodud näitega – kui 200 plaati on märgitud pakituks ja lähetamine on valitud, sisestatakse automaatselt kogusumma 500. Kui lähetatakse ainult 200 plaati, eeldab süsteem, et varem pakitud plaadid on lähetamisel, ja pakitud kogust vähendatakse. Kui lähetatud on 201 plaati, vähendatakse pakitud plaate esmalt järelejäänud ühe plaadi võrra, mis vähendatakse järelejäänud kogusest. 

## <a name="line-statuses"></a>Rea olekud

Tellimuseridadel kassas on mitu olekut, mis kajastavad tellimuserea olekut. Olekud kassas ja varukontoris ei pruugi alati ühtida. Tellimuserea olekut saab vaadata kassa kaudu, kasutades tellimuse täitmise toiminguid. Varukontoris saab tellimuseridu vaadata tellimuse üksikasjadest. Tellimuse üksikasjadele pääseb juurde jaotisest **Jaemüük** > **Kliendid** > **Kõik kliendi tellimused**. Tellimuse üksikasjade vaatamiseks valige suvand **Tellimuse ID**. Tellimuse üksikasjades valige vahekaart **Müügitellimus** ja siis valige alapäise **Vaade** all suvand **Üksikasjalik olek**. 

**Ootel** – kauplusele määratud, kuid veel aktsepteerimata tellimuseridade olek on kassas vaadatuna **Ootel**. Kassas aktsepteerimise ootel olevate ridade olek on varukontoris **Tellimuse töötlemine**.

**Aktsepteeritud** – käsitsi aktsepteeritud või automaatselt aktsepteeritud ridade olek on kassas vaadatuna **Aktsepteeritud**. Ridade, mille olek on **Aktsepteeritud**, olek on varukontoris **Tellimuse töötlemine**.

**Komplekteerimine** – parasjagu kauplusetasemel komplekteeritavate ridade olek on **Komplekteerimine**. Samade ridade olek varukontorist vaadatuna on **Tellimuse töötlemine**.

**Komplekteeritud** ja **Osaliselt komplekteeritud** – kassas komplekteeritud või osaliselt komplekteeritud ridade olek on **Komplekteeritud** või **Osaliselt komplekteeritud**. Samade ridade olek varukontoris on samuti **Komplekteeritud** või **Osaliselt komplekteeritud**.

**Pakitud** ja **Osaliselt pakitud** – kassas pakitud või osaliselt pakitud ridade olek on **Pakitud** või **Osaliselt pakitud**. Samade ridade olek varukontoris on samuti **Tarnitud** või **Osaliselt tarnitud**.

**Osaliselt arveldatud** – osaliselt kättesaadud või osaliselt lähetatud ridade olek on kassas ja varukontoris **Osaliselt arveldatud**.

**Arveldatud** – kassas täielikult arveldatud ridu enam täitmises ei kuvata. Varukontoris on nende ridade olek **Arveldatud**.

## <a name="order-fulfillment-filtering"></a>Tellimuse täitmise filtrimine

Tellimuse täitmine kassas hõlmab filtrimist, et aidata kasutajal otsitavat hõlpsasti leida. Filtreid saab muuta kuva **Kassa** alaservas oleva toimingupaani kaudu. Vaikimisi on olenevalt toimingu seadistusest rakendatud filter **Tarnetüüp**. Kui toiming on seadistatud parameetriga **Kõik tellimused**, rakendatakse seda filtrit tellimuse täitmise kasutamisel. Sama kehtib ka parameetrite **Kauplusest kättesaamine** ja **Kauplusest lähetamine** puhul. Muud tellimuse täitmisele rakendatavad filtrid on järgmised.

  - Kliendi number
  - Kliendi nimi
  - Kliendi meiliaadress
  - Tellimuse kood
  - Tarneviis
  - Kviitungi number
  - Kanaliviite ID
  - Algse poe number
  - Rea olek
  - Loomise kuupäev
  - Tarnekuupäev
  - Tarnekuupäev

