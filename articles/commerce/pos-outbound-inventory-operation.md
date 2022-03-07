---
title: Varude väljamineku toiming kassas
description: Selles teemas kirjeldatakse kassa varude väljamineku toimingu võimalusi.
author: hhaines
ms.date: 07/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3641e1974ffc277a690ca8b8d15399ac883b0132
ms.sourcegitcommit: 89906aa2f18f16e622fd280433c8fc9fe74d2aec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7581133"
---
# <a name="outbound-inventory-operation-in-pos"></a>Väljaminev laooperatsioon kassas

[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commerce’i versioonis 10.0.10 ja hilisemates asendavad kassa sissetuleku ja väljamineku toimingud komplekteerimis- ja vastuvõtutoimingu.

> [!NOTE]
> Versioonis 10.0.10 ja hilisemates on kõik kassarakenduse uued funktsioonid, mis on seotud poe varude vastuvõtmisega ostutellimuste ja üleviimistellimuste suhtes, lisatud sissetuleku toimingu toimingule. Kui kasutate praegu kassas komplekteerimis- ja vastuvõtutoimingut, soovitame teil töötada välja strateegia, et liikuda sellelt toimingult uutele sissetuleku ja väljamineku toimingutele. Kuigi komplekteerimis- ja vastuvõtutoimingut tootest ei eemaldata, siis pärast versiooni 10.0.9 sellesse enam toimivuse ja jõudluse perspektiivis ei investeerita.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Eeltingimus: asünkroonse dokumendi raamistiku konfigureerimine

Väljamineku toiming hõlmab jõudluse täiustusi tagamaks, et kasutajad, kellel on paljude kaupluste ja ettevõtete üleselt palju sissetulekute sisestusi ja mahukad varude dokumendid, saavad töödelda neid dokumente Commerce'i peakontoris (HQ) ilma aegumiste või tõrgete esinemiseta. Need täiustused nõuavad asünkroonse dokumendi raamistiku kasutamist.

Kui kasutatakse asünkroonset dokumendiraamistikku, saate kinnitada väljamineku dokumendi muudatused kassast Commerce'i peakontorisse (HQ) ja seejärel liikuda edasi järgmiste ülesannete juurde, samas kui taustal toimub töötlemine Commerce'i peakontoris (HQ). Saate kontrollida dokumendi olekut kassa dokumendi loendi lehe **Väljamineku toiming** kaudu, et veenduda, et sisestamine õnnestus. Kassarakenduses saate lisaks kasutada väljamineku toimingu aktiivse dokumendi loendit, et näha mis tahes dokumente, mida Commerce'i peakontorisse (HQ) ei saanud sisestada. Kui dokument nurjub, saavad kassa kasutajad seda parandada ja seejärel proovida seda uuesti Commerce'i peakontoris (HQ) töödelda.

> [!IMPORTANT]
> Enne kui ettevõte proovib väljamineku toiminguid kassas kasutada, peab asünkroonne dokumendi raamistik olema konfigureeritud.

Asünkroonse dokumendi raamistiku konfigureerimiseks viige lõpule järgmised protseduurid.

### <a name="create-and-configure-a-number-sequence"></a>Numbriseeria loomine konfigureerimine

1. Avage **Organisatsiooni haldus \> Numbriseeriad \> Numbriseeriad**.
2. Looge lehel **Numbriseeriad** uus numbriseeria.
3. Sisestage väljadele **Numbriseeria kood** ja **Nimi** kasutaja määratletud väärtused.
4. Valige kiirkaardil **Viited** käsk **Lisa**.
5. Valige väljal **Ala** suvand **Commerce’i parameetrid**.
6. Valige väljal **Viide** suvand **Jaemüügidokumendi toimingu identifikaator**.
7. Kiirkaardil **Üldine** jaotises **Seadistus** määrake suvand **Pidev** valikule **Ei**, et tagada, et ei esineks jõudluse probleeme.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Dokumendi töötlemiseks ja ülesannete jälgimiseks kahe pakett-töö loomine ja ajastamine

> [!NOTE]
> Commerce'i versioonis 10.0.13 ja hilisemas ei pea te pakett-töid pakett-töö raamistiku kaudu konfigureerima. Neid pakktöötlusi saab konfigureerida menüüst **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT**. Kasutage menüüsuvandeid **Jaemüügidokumendi toimingu jälgija** ja **Jaemüügidokumendi toimingu töötlemine** nende pakett-tööde konfigureerimiseks

Loodavaid pakett-töösid kasutatakse dokumentide töötlemiseks, mis nurjuvad või aeguvad. Neid kasutatakse ka siis, kui kassas töödeldavate aktiivsete varude dokumentide arv ületab süsteemi konfigureeritud väärtuse.

1. Avage **Süsteemihaldus \> Päringud \> Pakett-tööd**.
2. Lehel **Pakett-töö** looge kaks pakett-tööd.

    - Konfigureerige üks töö käitama klassi **RetailDocumentOperationMonitorBatch**.
    - Konfigureerige teine töö käitama klassi **RetailDocumentOperationProcessingBatch**.

3. Ajastage uued pakett-tööd korduvalt töötama. Näiteks määrake graafik nii, et tööd käitatakse iga viie minuti järel.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Eeltingimus: väljamineku toimingu lisamine kassa ekraanipaigutusse

Enne kui teie organisatsioon saab väljamineku toimingu funktsiooni kasutada, peab see konfigureerima kassa toimingu **Väljamineku toiming** ühes või mitmes [kassa ekraanipaigutuses](/dynamics365/unified-operations/retail/pos-screen-layouts). Enne uue toiming tootmiskeskkonnas juurutamist veenduge, et katsetaksite seda põhjalikult ja koolitaksite oma kasutajaid seda kasutama.

## <a name="overview"></a>Ülevaade

Väljamineku toiming võimaldab kassa kasutajatel teha järgmisi ülesandeid.

- Sisestada üleviimistellimuse dokumentide saadetisi juhtudel, kui kasutaja pood on määratud väljaminevaks laoks.
- Vaadata ajalooliste üleviimistellimuste saadetiste teavet, mis olid poe poolt sisestatud.
- Uute väljaminekute üleviimistellimuste taotluste loomine.

Kui kassarakenduses käivitatakse väljamineku toiming, ilmub loendilehe vaade. See vaade näitab avatud üleviimistellimuse dokumente, mille kasutaja praegune pood peab saatma ja täitma. Valitud dokumendi otsimiseks saavad kasutajad kerida loendit või kasutada otsingufunktsiooni.

Väljaminevate varude dokumendi loendil on kolm vahekaarti.

- **Aktiivne** – sellel vahekaardil kuvatakse üleviimistellimused, mille olek on **Taotletud** või **Osaliselt saadetud**. Tellimused sisaldavad ridu või koguseid ridadel, mis tuleb kasutaja praegusesse poodi saata. See vahekaart näitab ka tellimusi, mille olek on **Töötluses HQ-s** (st need ootavad Commerce'i peakontorist (HQ) eduka sisestamise kinnitust) või **Töötlemine nurjus** (st Commerce'i peakontorisse (HQ) sisestamine ebaõnnestus ja kasutaja peab andmeid parandama ning proovima tellimused uuesti esitada).
- **Mustand** – sellel vahekaardil kuvatakse uued väljamineku üleviimistellimuse taotlused, mille kasutaja pood lõi. Samas on dokumendid salvestatud ainult lokaalselt. Neid pole veel Commerce'i peakontorisse (HQ) töötlemiseks esitatud.
- **Lõpetatud** – see vahekaart kuvab üleviimistellimuse dokumentide loendi, mille pood on viimase seitsme päeva jooksul täielikult saatnud. Sellel vahekaardil on ainult informatiivne eesmärk. Kogu teave dokumentide kohta on poe jaoks kirjutuskaitstud andmed.

Kui vaatate dokumente mis tahes vahekaardil, aitab väli **Olek** teil mõista etappi, kus dokument on.

- **Mustand** – üleviimistellimuse dokument on salvestatud ainult lokaalselt poe kanali andmebaasi. Teavet üleviimistellimuse taotluse kohta pole veel Commerce'i peakontorisse (HQ) esitatud.
- **Taotletud** – ostutellimus või üleviimistellimus on Commerce'i peakontoris (HQ) loodud ja täielikult avatud. Kasutaja praegune pood on töödelnud mõne saadetise dokumendi suhtes.
- **Osaliselt saadetud** – üleviimistellimuse dokumendil on üks või mitu rida või osalist rea kogust, mis on sisestatud väljamineva lao poolt kui saadetud. Need saadetud read on vastuvõtmiseks saadaval sissetuleku toimingu kaudu.
- **Täielikult saadetud** – üleviimistellimuse kõik read ja täielikud rea kogused on väljamineva lao poolt sisestatud kui saadetud.
- **Pooleli** – seda olekut kasutatakse seadme kasutajate teavitamiseks, et teine kasutaja töötleb dokumenti aktiivselt.
- **Peatatud** – see olek kuvatakse pärast suvandi **Peata vastuvõtmine** valimist vastuvõtmisprotsessi ajutiseks peatamiseks.
- **Töötluses HQ-s** – dokument esitati kassarakendusest Commerce'i peakontorisse (HQ), kuid see ei ole veel edukalt Commerce'i peakontorisse (HQ) sisestatud. Dokument läbib asünkroonse dokumendi sisestamise protsessi. Pärast seda, kui dokument on edukalt Commerce'i peakontorisse (HQ) sisestatud, tuleb selle olek värskendada valikule **Täielikult vastu võetud** või **Osaliselt vastu võetud**.
- **Töötlemine nurjus** – dokument sisestati Commerce'i peakontorisse (HQ) ja lükati tagasi. Paanil **Üksikasjad** kuvatakse sisestamise nurjumise põhjus. Andmeprobleemide parandamiseks tuleb dokumenti redigeerida ja seejärel tuleb see uuesti esitada Commerce'i peakontorisse (HQ) töötlemiseks.

Kui valite loendis dokumendi rea, kuvatakse paan **Üksikasjad**. Sellel paanil kuvatakse lisateave dokumendi kohta, nt saatmise ja kuupäeva teave. Edenemisriba näitab, mitu eset on vaja veel töödelda. Kui dokumenti ei töödeldud edukalt Commerce'i peakontoris (HQ), näitab paan **Üksikasjad** lisaks tõrkega seotud veateateid.

Dokumendi loendi lehekülje vaates saate rakenduse ribal valida suvandi **Tellimuse üksikasjad**, et vaadata dokumendi üksikasju. Saate aktiveerida ka sobivatel dokumendiridadel sissetuleku töötlemise.

Dokumendi loendi lehekülje vaates saate luua poe jaoks ka uue väljamineku üleviimistellimuse.

## <a name="transfer-order-shipping-process"></a>Üleviimistellimuse saatmisprotsess

Pärast üleviimistellimuse dokumendi valimist vahekaardil **Aktiivne**, saate valida suvandi **Tellimuse üksikasjad**, et käivitada täitmise protsess. Kuvatakse vaade **Täielik tellimuste loend**. Sellel lehel näidatakse kõik kaupa sisaldavad dokumendi read. See näitab ka tellitud koguse üksikasju.

Iga vöötkoodi skannimine värskendab kogust väljal **Praegu tarnimisel** ühe ühiku võrra. Teise võimalusena saate sisestada saadetava koguse, valides rakenduse ribal suvandi **Toote lähetus**, sisestades kauba ID ja sisestades seejärel koguse. Kui kaup on asukoha järgi kontrollitava, saate kinnitada või määrata dokumendi rea lähetuse sihtpunkti.

Vaates **Täielik tellimuste loend** saate käsitsi valida loendist rea ja seejärel värskendada **Praegu tarnimisel** kogust valitud rea jaoks paanil **Üksikasjad**.

### <a name="over-delivery-shipping-validations"></a>Ületarne saadetise kinnitamised

Kinnitamine leiab aset dokumendi ridade täitmise protsessi ajal. Nende hulka kuuluvad ületarne kinnitused. Kui kasutaja püüab saata rohkem varusid kui on ülekandekorraldusel tellitud, kuid kas ületarne pole konfigureeritud või kui saadetud kogus ületab ülekandekorralduse rea jaoks konfigureeritud ületarne hälbe, kuvatakse kasutajale veateade ja tal pole võimalik üleliigset kogust saata.

### <a name="underdelivery-close-lines"></a>Alatarne sulgemisread

Commerce'i versiooni 10.0.12 lisati funktsioon, mis lubab kassa kasutajatel väljamineva tellimuse saadetise ajal sulgeda või tühistada ülejäänud kogused, kui väljaminev ladu määratleb, et kogu nõutavat kogust ei saa tarnida. Koguseid saab sulgeda või tühistada ka hiljem. Selle võimaluse kasutamiseks peab ettevõtes olema konfigureeritud üleviimistellimuste alatarnete lubamine. Lisaks peab üleviimistellimuse reale olema määratletud alatarne protsent.

Üleviimistellimuste alatarne lubamise konfigureerimiseks ettevõttes, avage Commerce'i peakontori (HQ) jaotis **Varude haldus \> Seadistus \> Varude ja laohalduse parameetrid**. Lülitage lehe **Varude ja laohalduse parameetrid** vahekaardil **Üleviimistellimused** sisse parameeter **Aktsepteeri alatarneid**. Seejärel käivitage jaotusgraafiku töö **1070**, et sünkroonida parameetri muudatused kaupluse kanalisse.

Toodete üleviimistellimuse rea alatarne protsente saab eelmääratleda Commerce'i peakontoris toote konfiguratsiooni käigus. Teine võimalus on nende seadistamine või üle kirjutamine kindlal üleviimistellimuse real Commerce'i peakontoris (HQ).

Kui organisatsioonis on üleviimistellimuse alatarne konfigureerimine lõpule viidud, kuvatakse kassa kasutajatele paanil **Üksikasjad** uus suvand **Sule ülejäänud kogus**, kui nad valivad väljamineva üleviimistellimuse rea funktsiooni **Väljamineku toiming** kaudu. Kui kasutaja viib seejärel saadetise lõpule toimingu **Lõpeta täitmine** abil, saab ta saata taotluse Commerce'i peakontorisse (HQ) ülejäänud saatmata koguse tühistamiseks. Kui kasutaja sulgeb ülejäänud koguse, kontrollib Commerce, et kinnitada, kas tühistatav kogus jääb üleviimistellimuse real määratletud alatarne hälbeprotsendi piiresse. Alatarne hälbe ületamise korral kuvatakse tõrketeade ja kasutaja ei saa ülejäänud kogust sulgeda enne, kui eelnevalt saadetud ja „läheta kohe” kogused vastavad alatarne hälbele või ületavad seda.

Kui saadetis on sünkroonitud Commerce'i peakontoriga (HQ), uuendatakse väljal **Läheta kohe** kassa üleviimistellimuse rea jaoks määratletud kogused Commerce'i peakontoris (HQ) saadetud olekusse. Kõik lähetamata kogused, mis varasemalt oleksid olnud „saada järelejäänud” kogused (st hiljem saadetavad kogused), on nüüd tühistatud kogused. Üleviimistellimuse rea „saada järelejäänud” koguse väärtuseks määratakse **0** (null) ja rida loetakse täielikult saadetuks.

### <a name="shipping-location-controlled-items"></a>Asukoha järgi kontrollitavate kaupade saatmine

Kui saadetavad kaubad on asukoha järgi kontrollitavad, saavad kasutajad valida asukoha, kust nad soovivad saatmisprotsessi ajal varud väljastada. Soovitame protsessi tõhusamaks muutmiseks konfigureerida oma poe lao vaikimisi väljastamise asukoht. Isegi kui vaikeasukoht on konfigureeritud, saavad kasutajad vajaduse järgi valitud ridadel väljastamise asukoha alistada.

Toiming arvestab konfiguratsiooniga **Määramata sissetulekud lubatud** laoala dimensioonis **Asukoht** ja ei nõua määramata sissetuleku konfigureerimisel, et sisestataks asukoha dimensioon. Kui kauba puhul ei ole tühja sissetuleku asukohad lubatud, kuvab kassarakendus tõrke ja nõuab, et enne kviitungi sisestamist sisestataks asukoht.

### <a name="ship-all"></a>Saada kõik

Vajaduse korral saate valida rakenduse ribal suvandi **Saada kõik**, et kiiresti uuendada kogus **Praegu tarnimisel** kõikide dokumendiridade jaoks maksimaalse saadaoleva väärtuseni, mis nende ridade jaoks täidetakse.

### <a name="cancel-fulfillment"></a>Tühista täitmine

Kasutage rakenduse ribal funktsiooni **Tühista täitmine** ainult siis, kui soovite dokumendist väljuda ja ei soovi ühtegi muudatust salvestada. Näiteks valisite algselt vale dokumendi ja te ei soovi, et ükski eelmistest saadetise andmetest salvestataks.

### <a name="pause-fulfillment"></a>Peata täitmine

Kui te täidate üleminekutellimust, saate kasutada funktsiooni **Peata täitmine**, kui soovite teha protsessis pausi. Näiteks võite soovida teha kassas teise toimingu, nagu kliendi ostu läbilöömine, või lükata edasi saadetise sisestamine Commerce'i peakontorisse (HQ).

Kui valite suvandi **Peata täitmine**, muudetakse dokumendi olekuks **Peatatud**. Seega teab kasutaja, et andmed on dokumenti sisestatud, kuid dokument pole veel kinnitatud. Kui olete täitmise protsessi jätkamiseks valmis, valige peatatud dokument ja seejärel valige suvand **Tellimuse üksikasjad**. Kõik **Praegu tarnimisel** kogused, mis eelnevalt salvestati, säilitatakse ja neid saab vaadata vaates **Täielik tellimuste loend**.

### <a name="review"></a>Ülevaade

Enne täitmise lõplikku lisamist Commerce'i peakontorisse (HQ) saate kasutada funktsiooni **Vaata üle**, et väljaminevat dokumenti kontrollida. See funktsioon teavitab teid võimalikest puuduvatest või valedest andmetest, mis võivad põhjustada töötlemise nurjumise, ja annab teile võimaluse parandada probleemid enne täitmistaotluse esitamist. Et lubada rakenduse ribal funktsioon **Vaata üle**, lubage Commerce'i peakontori (HQ) funktsioonihalduses funktsioon **Luba kassa sissetulevate ja väljaminevate varude toimingute kontrollimine**.

Funktsioon **Vaata üle** kontrollib väljaminevas dokumendis järgmisi probleeme.
- **Ülesaatmine** – nüüd saadetav kogus on suurem kui tellitud kogus. Selle probleemi suuruse määrab Commerce'i peakontori (HQ) ületarne konfiguratsioon.
- **Alasaatmine** – nüüd saadetav kogus on väiksem kui tellitud kogus. Selle probleemi suuruse määrab Commerce'i peakontori (HQ) alatarne konfiguratsioon.
- **Seerianumber** – seerianumbrit pole sisestatud või saadaval seerianumbriga kauba jaoks, mille puhul on vaja laos registreeritud seerianumbrit.
- **Asukohta pole määratud** – asukoht pole määratud asukoha järgi kontrollitava kauba jaoks, mille asukoht ei tohi olla tühi.
- **Kustutatud read** – tellimuselt on kustutanud ridasid Commerce'i peakontori (HQ) kasutaja, keda kassarakendus ei tunne ära.

Kui seate parameetri **Luba automaatne kontrollimine** väärtuseks **Jah** jaotises **Kaubanduse parameetrid** > **Varud** > **Kaupluse varude toimingud**, tehakse kontroll automaatselt, kui valite funktsiooni **Lõpeta täitmine**.

### <a name="finish-fulfillment"></a>Lõpeta täitmine

Kui olete kõigi toodete **Praegu tarnimisel** koguste sisestamise lõpetanud, peate valima rakenduse ribal suvandi **Lõpeta täitmine**.

Kui kasutatakse asünkroonset dokumendi töötlemist, esitatakse kviitung asünkroonse dokumendi raamistiku kaudu. Dokumendi sisestamiseks kuluv aeg sõltub dokumendi suurusest (ridade arvust) ja serveris toimuvast üldisest töötlemise liiklusest. Tavaliselt toimub see protsess mõne sekundiga. Kui dokumendi sisestamine ebaõnnestub, teavitatakse kasutajat dokumendi loendi **Väljamineku toiming** kaudu vahekaardil **Aktiivne**, kus dokumendi olek värskendatakse suvandile **Töötlemine nurjus**. Kasutaja saab seejärel valida kassas nurjunud dokumendi, et vaadata veateateid ja tõrke põhjust paanil **Üksikasjad**. Nurjunud dokument jääb sisestamata ja nõuab, et kasutaja naaseks dokumendi ridadele, valides kassas suvandi **Tellimuse üksikasjad**. Seejärel peab kasutaja tõrgete põhjal uuendama dokumenti parandustega. Pärast dokumendi parandamist saab kasutaja proovida seda uuesti töödelda, valides rakenduse ribal suvandi **Lõpeta täitmine**.

## <a name="create-an-outbound-transfer-order"></a>Väljamineku üleviimistellimuse loomine

Kasutajad saavad luua kassas uusi üleviimistellimuse dokumente. Protsessi alustamiseks valige rakenduse ribal **Uus**, kui olete peamise **Väljamineku tegevuse** dokumendi loendis. Seejärel palutakse teil valida **Kanna üle kohta** ladu või pood, kuhu teie praegune pood varud saadab. Väärtused on piiratud valikuga, mis on määratletud poe täitmise grupi konfiguratsioonis. Väljamineku üleviimise taotluses on teie praegune pood alati üleviimistellimuse jaoks ladu **Kanna üle kohast**. Seda väärtust ei saa muuta.

Saata vajaduse järgi sisestada väärtused väljadele **Lähetuskuupäev**, **Vastuvõtukuupäev** ja **Tarneviis**. Saate lisada ka märkuse, mis salvestatakse koos üleviimistellimuse päisega Commerce'i peakontoris (HQ) dokumendi manusena.

Pärast päise teabe loomist saate lisada üleviimistellimusele kaupu. Kaupade ja taotletud koguste lisamise protsessi alustamiseks skannige vöötkoodid või valige käsk **Lisa toode**.

Pärast seda, kui read on väljamineku üleviimistellimusse sisestatud, tuleb teil valida käsk **Salvesta**, et salvestada dokumendi muudatused lokaalselt, või suvand **Esita taotlus**, et edastada tellimuse üksikasjad edasiseks töötlemiseks Commerce'i peakontorisse (HQ). Kui valite suvandi **Salvesta**, salvestatakse dokumendi mustand kanali andmebaasi ja väljamineku ladu ei saa dokumenti käitada enne, kui see on suvandi **Edasta taotlus** kaudu edukalt töödeldud. Valige suvand **Salvesta** ainult juhul, kui te ei ole valmis taotlust Commerce'i peakontoris (HQ) töötlemiseks kinnitama.

Kui dokument on salvestatud lokaalselt, võite selle leida vahekaardil **Mustandid** dokumendi loendis **Sissetuleku toiming**. Kui dokument on olekus **Mustand**, saate seda redigeerida, kui valite suvandi **Redigeeri**. Saate vajaduse järgi ridu värskendada, lisada või kustutada. Samuti saate kustutada kogu dokumendi, kui see on olekus **Mustand**, valides käsu **Kustuta** vahekaardil **Mustandid**.

Pärast dokumendi mustandi edukat esitamist Commerce'i peakontorisse (HQ) kuvatakse see vahekaardil **Aktiivne** ja selle olek on **Taotletud**. Sel hetkel saavad ainult väljamineva lao kasutajad dokumenti muuta, valides kassarakenduses suvandi **Väljaminev toiming**. Kasutajad sissetuleku laos saavad üleviimistellimust vaadata vahekaardil **Aktiivne** dokumendi loendis **Sissetuleku toiming**, kuid nad ei saa seda redigeerida ega kustutada. Redigeerimise lukustus tagab, et ei esineks konflikte, kuna sissetuleku päringu teinu muudab üleviimistellimust samal ajal, kui väljamineku saatja aktiivselt komplekteerib ja lähetab tellimuse. Kui vajalikud on sissetuleku poe või lao muudatused pärast üleviimistellimuse esitamist, tuleb võtta ühendust väljamineku saatjaga ja paluda sisestada muudatused.

Kui dokument on olekus **Taotletud**, on see väljamineku lao poolt täitmise töötlemiseks valmis. Kuna saadetist töödeldakse väljamineku toimingut kasutades, siis üleviimistellimuse dokumentide olek uuendatakse olekul **Taotletud** olekule **Täielikult saadetud** või **Osaliselt saadetud**. Pärast seda, kui dokumendid on olekus **Täielikult saadetud** või **Osaliselt saadetud**, saab sissetuleku pood või ladu sisestada nendepoolsed sissetulekud, kasutades sissetuleku toimingu vastuvõtmisprotsessi.

Täielikult saadetud üleviimistellimused liigutatakse vahekaardile **Lõpetatud** dokumendi loendis **Väljamineku tegevus**. Seal jäävad need väljamineku poe või lao kasutajatele kirjutuskaitstud režiimis nähtavaks seitsme päeva jooksul.

## <a name="related-topics"></a>Seotud dokumendid

[Varude sissetuleku toiming kassas](pos-inbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]