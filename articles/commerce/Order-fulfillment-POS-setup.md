---
title: Kaupluse tellimuse täitmise seadistamine
description: Teema annab ülevaate kaupluse tellimuse täitmise seadistamisest.
author: rubencdelgado
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5cdf7b2655f62b693a8f2bc137c690fbc43b16a7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796434"
---
# <a name="set-up-order-fulfillment-for-stores"></a>Kaupluse tellimuse täitmise häälestus

[!include [banner](includes/banner.md)]

Paljud jaemüüjad soovivad tellimuste täitmist optimeerida, võimaldades kauplustel tellimusi täita. Tellimuse täitmine kaupluse tasemel aitab leevendada laoülejäägi olukordi kindla kaupluse puhul või võib olla vajalik logistika seisukohalt, kui kauplusel on lisavõimsust või see asub kliendile saatmiseks lähemal. Selle vajaduse täitmiseks on kassas saadaval ühtse tellimuse täitmise toiming.

Kindlas kaupluses täitmist vajavatele tellimustele on määratud kaupluse ladu tellimuse päises või ridadel.

Tellimuse täitmise toiming kassas annab kassas üksiku tööala, mida saab tellimuste töötlemisteks kasutada. See hõlmab kõike alates tellimuse aktsepteerimisest kuni saadetuna märkimise või kauplusest kättesaamise algatamiseni.

## <a name="set-up-the-order-fulfillment-operation"></a>Tellimuse täitmise toimingu seadistamine

Tellimuse täitmist, [toimingu ID 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations), saab kasutada juurdepääsuks kaupluse tellimuse täitmise tööalale kassas.

Määrake kassas tellimuse täitmise käivitamisel kasutatav parameeter, järgides teemas [Nupupaneelile toimingu lisamine](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) kirjeldatud etappe. Pärast tellimuse täitmise toimingute määramist on vaikimisi valitud suvad **Kõik tellimused**. Selle parameetriga konfigureerimisel loetleb toimib kõik praeguses kaupluses täitmiseks mõeldud tellimuseread. Saadaval on ka suvand **Tellimused lähetamiseks**, mille saab määrata nupule ja kasutada, kui kasutaja soovib näha ainult tellimusi, mis saadetakse kauplusest välja. Samuti on siin suvand **Tellimused kättesaamiseks**. Kassas käivitamisel loetleb see ainult kaupluses kättesaamiseks mõeldud tellimused. Erinevatele nuppudele saab määrata erinevad parameetrid, et pakkuda kasutajatele erinevaid võimalusi tellimuse täitmise vaatamiseks.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Saate lubada kasutajatel tellimuse täitmisele juurde pääseda kassas.

Tellimuse täitmise toimingul ei ole oma valmisluba, kuid tulevikus on kasutajatel võimalik taotleda kassast toimingu alustamiseks luba nimega **Luba tellimuse toomine**.

Kaupluse tasemel on saadaval konfiguratsioonisäte määramaks, kas tellimuserida peab olema aktsepteeritud kassas käsitsi. Kui see konfiguratsioonivalik pole määratud, aktsepteeritakse tellimuseread vaikimisi. Selle konfiguratsioonivalik sisselülitamisel peab kasutajatel kassas olema luba nimega **Luba tellimuste aktsepteerimine**, et aktsepteerida tellimused kassas.

### <a name="enable-manual-order-acceptance"></a>Tellimuse käsitsi aktsepteerimise lubamine

Vaikimisi on kauplusele määratud tellimuseridade olekuks märgitud **Aktsepteeritud**. See tähendab, et eeldatakse nende täitmist määratud kaupluses ja edasi neid ei määrata. Teatud juhtudel võivad jaemüüjad soovida tellimusi käsitsi aktsepteerida, enne kui neid saab täita. Näiteks kui kaupluses on vähe töötajaid ja tellimusi ei saa täita, aktsepteerib kaupluse juhataja töötlemiseks ainult nii palju tellimusi, kui arvab, et neid suudetakse sel päeval piisavalt töödelda. Enne kui tellimus on aktsepteeritud, võib varukontor selle teisele kauplusele ümber määrata. Sel viisil annab tellimuse aktsepteerimine viisi näitamaks, et kauplus on tellimuse kinnitanud ja see täidetakse.

Tellimuseread kaupluses kättesaamiseks on olekuga **Ootel** ja neid ei aktsepteerita.

Tellimuse ridade käsitsi aktsepteerimise sisselülitamiseks minge jaotisse **Jaemüük ja kauandu** \> **Kanalid** \> **Kauplused** \> **Kõik kauplused**. Valige kauplus ja klõpsake kaupluse ID-d, et vaadata kaupluse üksikasju. Klõpsake valikut **Redigeeri**. Leidke kiirkaardil **Üldine** alapäis **Tellimuse täitmine** ja muutke suvandi **Käsitsi aktsepteerimine** sätteks **Ei** asemel **Jah**.

### <a name="enable-reject-order-line-capability"></a>Tellimuserea tagasilükkamise lubamise võimalus

Tellimuseridu saab kassas ka tagasi lükata. Tellimuserea tagasilükkamine näitab, et seda ei täideta selles kaupluses ja tellimuserida saadetakse tagasi ümbermääramiseks teise kauplusse või lattu. Tellimuserea tagasilükkamise luba antakse töötajaga seostatud kassa lubade grupis oleva loaga **Luba tellimuse tagasilükkamine**. Rea tagasilükkamisel saavad jaemüüjad lubada oma töötajatel esitada tagasilükkamise põhjus. Selle saavutamiseks kasutage suvandi **Teabekoodi tegevus** infokoode tüübiga **Tellimuse täitmine** ja määrake teabekood kanaliga seostatud funktsionaalsusprofiilis suvandile **Tellimuserea tagasilükkamine**.

> [!NOTE]
> Tegevusele **Tellimuserea tagasilükkamine** saab määrata ainult suvandi **Teabekoodi tegevus** teabekoode tüübiga **Tellimuse täitmine**.

### <a name="synchronize-changes-to-the-channel-database"></a>Muudatuste sünkroonimine kanaliandmebaasiga

Kui nupupaneelile on toiming määratud, sobivad load antud ja kanal konfigureeritud, tuleb muudatused sünkroonida kanali andmebaasiga. Selle tegemiseks navigeerige jaotisse **Jaemüük ja kaubandus** \> **Jaemüügi ja kaubanduse IT** \> **Jaotusgraafik**. Valige nupupaneeli muudatuste sünkroonimiseks graafik 1090-registrid ja siis klõpsake käsku **Käivita kohe**. Seejärel sünkroonige lubade muudatused, valides suvandi 1060-töötajad ja seejärel klõpsates käsku **Käivita kohe**. Seejärel sünkroonige kanalimuudatused, valides suvandi 1070-kanali konfiguratsioon ja seejärel klõpsates käsku **Käivita kohe**. Lõpuks sünkroonige vastloodud tagasilükkamise põhjuse teabekood, valides suvandi 1110-globaalne konfiguratsioon ja klõpsates käsku **Käivita kohe**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Tellimuse täitmise kasutamine kassas

Avage kassa ja valige tellimuse täitmise toiming. Olenevalt konfiguratsioonist on loetletud kõik read, tellimuseread kättesaamiseks või tellimuseread lähetamiseks.

### <a name="order-fulfillment-view"></a>Tellimuse täitmise vaade

Tellimuse täitmise vaatel kuvatakse tellimuseread kaupluses täitmiseks ja see sisaldab järgmisi veerge.

- Tellimuse kood
- Toote number
- Kirjeldus
- Tellitud kogus
- Nõutav tarnekuupäev
- Kliendi nimi
- Täitmisolek

Lisateavet konkreetse tellimuserea kohta saab vaadata, valides tellimuserea ja seejärel avades kassa päises kuvatava sisselogitud kasutaja/vahetuse teabe all asuva hüpikmenüü. Sellel menüül on kaks vahekaarti: üks rea üksikasjade ja teine tellimuse üksikasjade jaoks. Rea üksikasjade vahekaart sisaldab järgmist teavet.

- Tellitud kogus
- Järelejäänud lähetatav/kättesaadav kogus
- Komplekteeritud kogus
- Pakitud kogus
- Arveldatud kogus (juba kätte saadud või lähetatud)
- Tarneviis
- Tarneaadress

Üksikasjade hüpikmenüül on ka vahekaart, mis sisaldab rohkem tellimusetaseme üksikasju, sh järgmisi.

- Kliendi nimi
- Kliendi ID
- Tellimuse kood
- Tellimuse kogusumma
- Tellimuse saldo

Tellimuse täitmise vaate alaservas asub toimingupaan. See sisaldab kõiki tegevusi, mida saab tellimusereal teha. Kui mõni tegevus pole olenevalt rea olekust saadaval, ei saa seda teha.

Vaikimisi on tellimuste olek **Aktsepteeritud**. Tellimuse olekut saab vaadata tellimuseridade loendi veerus. Kui kanalitasemel on konfigureeritud suvand **Käsitsi aktsepteerimine**, kuvatakse kõigi lähetatavate ridade olekuna **Ootel** ja need tuleb enne täitmist aktsepteerida. Kaupluses kättesaadavate tellimuste olek on vaikimisi **Ootel** ja neid ei pea aktsepteerima.

### <a name="order-fulfillment-line-actions"></a>Tellimuse täitmise rea tegevused

- **Redigeeri** – kui tellimuse olek on Ootel, saab seda redigeerida kassas. Tellimusi, mis on juba osaliselt komplekteeritud, pakitud või arveldatud, ei saa tellimuse täitmise vaatel redigeerida.
- **Aktsepteeri** – kui kanalitasemel on konfigureeritud suvand **Käsitsi aktsepteerimine**, tuleb read esmalt aktsepteerida, enne kui need saavad läbida tellimuse täitmise protsessi.
- **Komplekteerimine** – komplekteerimissuvand toetab mitut tegevust. Kõigepealt värskendab tegevus **Komplekteerimine** tellimuserea olekut, et teised kaupluses ei püüaks sama rida komplekteerida. Seejärel prindib tegevus **Komplekteerimislehe printimine** valitud rea või ridade jaoks komplekteerimislehe ja värskendab nende oleku ka sättele **Komplekteerimisel**. Komplekteerimislehe vorminguid juhitakse kviitungivormingute osana. Lisateavet kviitungivormingute seadistamise kohta vt teemast [Kviitungite mallid ja printimine](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing). Lõpuks näitab tegevus **Komplekteerituks märkimine**, et rida on komplekteeritud. **Komplekteerituks märkimine** näitab varukontoris vastavaid laokandeid. Komplekteerimistegevusi saab teha korraga mitme tellimuserea puhul kõigi tellimuste ja tarneviiside korral.
- **Lükka tagasi** – ridu või osalisi ridu saab tagasi lükata. See võimaldab neid varukontorist ümber määrata teise kauplusse või lattu. Ridu saab tagasi lükata ainult siis, kui need pole veel komplekteeritud või pakitud. Juba komplekteeritud või pakitud rea tagasilükkamiseks tuleb selle rea komplekteerimine või pakkimine varukontoris tühistada.
- **Paki** – pakkimissuvand toetab kaht tegevust: **Prindi saateleht** prindib valitud ridade jaoks saatelehe ja **Märgi pakituks** märgib read pakituks ning märgib read varukontoris tarnituks. Korraga saab pakkida ainult samasse tellimusse kuuluvaid ja sama tarneviisiga tellimuseridu. Saatelehe vorminguid juhitakse kviitungivormingute osana. Lisateavet kviitungivormingute seadistamise kohta vt teemast [Kviitungite mallid ja printimine](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).
- **Läheta** – lähetamistegevus märgib valitud ridade olekuks varukontoris **Tarnitud**. Kui rida on täielikult lähetatud, siis seda tellimuse täitmise vaates enam ei kuvata.
- **Kättesaamine** – kättesaamistegevus lisab read kättesaamiseks kandevaatele. Kui tellimusel on muid ridu, mis pole praegu kättesaamisel, lisatakse need kandevaatele nullkogusega. Kui rida on täielikult kätte saadud, siis seda tellimuse täitmise vaates enam ei kuvata.

### <a name="order-fulfillment-filtering"></a>Tellimuse täitmise filtrimine

Tellimuse täitmine kassas hõlmab filtrimist, et aidata kasutajal otsitavat hõlpsasti leida. Filtreid saab muuta kuva **Kassa** alaservas oleval toimingupaanil. Vaikimisi on olenevalt toimingu seadistusest rakendatud filter **Tarnetüüp**. Kui toiming on seadistatud parameetriga **Kõik tellimused**, rakendatakse seda filtrit tellimuse täitmise kasutamisel. Sama kehtib ka parameetrite **Kauplusest kättesaamine** ja **Kauplusest lähetamine** puhul. Muud tellimuse täitmisele rakendatavad filtrid on järgmised.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
