---
title: Varude sissetuleku toiming kassas
description: Selles teemas kirjeldatakse kassa varude sissetuleku toimingu võimalusi.
author: hhaines
manager: annbe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 16a786a4b3ca1bcbd202f6753bdf3bf7233a4333
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710305"
---
# <a name="inbound-inventory-operation-in-pos"></a>Varude sissetuleku toiming kassas

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce’i versioonis 10.0.10 ja hilisemates asendavad kassa sissetuleku ja väljamineku toimingud komplekteerimis- ja vastuvõtutoimingu.

> [!NOTE]
> Commerce'i versioonis 10.0.10 ja hilisemates on kõik kassarakenduse uued funktsioonid, mis on seotud kaupluse varude vastuvõtmisega ostutellimuste ja üleviimistellimuste alusel, lisatud kassatoimingule **Sissetuleku toiming**. Kui kasutate praegu kassas komplekteerimis- ja vastuvõtutoimingut, soovitame teil töötada välja strateegia, et liikuda sellelt toimingult uutele sissetuleku ja väljamineku toimingutele. Kuigi komplekteerimis- ja vastuvõtutoimingut tootest ei eemaldata, siis pärast versiooni 10.0.9 sellesse enam toimivuse ja jõudluse perspektiivis ei investeerita.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Eeltingimus: asünkroonse dokumendi raamistiku konfigureerimine

Sissetuleku toiming hõlmab jõudluse täiustusi tagamaks, et kasutajad, kellel on paljude poodide ja ettevõtete üleselt suured kogused sissetulekute sisestusi ja mahukad varude dokumendid, saavad töödelda neid dokumente Commerce Headquartersis ilma aegumiste või tõrgete esinemiseta. Need täiustused nõuavad asünkroonse dokumendi raamistiku kasutamist.

Kui kasutatakse asünkroonset dokumendi raamistikku, saate kinnitada sissetuleku dokumendi muudatused kassast Commerce Headquartersisse ja seejärel liikuda edasi järgmistele ülesannetele, samas kui Commerce Headquartersi töötlemine toimub taustal. Saate kontrollida dokumendi olekut kassa dokumendi loendi lehe **Sissetuleku toiming** kaudu, et veenduda, et sisestamine õnnestus. Kassarakenduses saate lisaks kasutada sissetuleku toimingu aktiivse dokumendi loendit, et näha mis tahes dokumente, mida Commerce Headquartersisse ei saanud sisestada. Kui dokument nurjub, saavad kassa kasutajad teha sellele parandusi ja seejärel proovida seda uuesti Commerce Headquartersisse töödelda.

> [!IMPORTANT]
> Enne kui ettevõte proovib sissetuleku toiminguid kassas kasutada, peab asünkroonne dokumendi raamistik olema konfigureeritud.

Asünkroonse dokumendi raamistiku konfigureerimiseks viige lõpule järgmised protseduurid.

### <a name="create-and-configure-a-number-sequence"></a>Numbriseeria loomine konfigureerimine

1. Avage **Organisatsiooni haldus \> Numbriseeriad \> Numbriseeriad**.
2. Looge lehel **Numbriseeriad** uus numbriseeria.
3. Sisestage väljadele **Numbriseeria kood** ja **Nimi** kasutaja määratletud väärtused.
4. Valige kiirkaardil **Viited** käsk **Lisa**.
5. Valige väljal **Ala** suvand **Commerce’i parameetrid**.
4. Valige väljal **Viide** suvand **Jaemüügidokumendi toimingu identifikaator**.
5. Kiirkaardil **Üldine** jaotises **Seadistus** määrake suvand **Pidev** valikule **Ei**, et tagada, et ei esineks jõudluse probleeme.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Dokumendi töötlemiseks ja ülesannete jälgimiseks kahe pakett-töö loomine ja ajastamine

> [!NOTE]
> Commerce'i versioonis 10.0.13 ja hilisemas ei pea te neid pakett-töid pakett-töö raamistiku kaudu konfigureerima. Neid pakktöötlusi saab konfigureerida menüüst **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT**. Kasutage menüüsuvandeid **Jaemüügidokumendi toimingu jälgija** ja **Jaemüügidokumendi toimingu töötlemine** nende pakett-tööde konfigureerimiseks.

Loodavaid pakett-töösid kasutatakse dokumentide töötlemiseks, mis nurjuvad või aeguvad. Neid kasutatakse ka siis, kui kassas töödeldavate aktiivsete varude dokumentide arv ületab süsteemi konfigureeritud väärtuse.

1. Avage **Süsteemihaldus \> Päringud \> Pakett-tööd**.
2. Lehel **Pakett-töö** looge kaks pakett-tööd.

    - Konfigureerige üks töö käitama klassi **RetailDocumentOperationMonitorBatch**.
    - Konfigureerige teine töö käitama klassi **RetailDocumentOperationProcessingBatch**.

2. Ajastage uued pakett-tööd korduvalt töötama. Näiteks määrake graafik nii, et tööd käitatakse iga viie minuti järel.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Eeltingimus: sissetuleku toimingu lisamine kassa ekraanipaigutusse

Enne kui teie organisatsioon saab sissetuleku toimingu funktsiooni kasutada, peab see konfigureerima kassa toimingu **Sissetuleku toiming** ühes või mitmes [kassa ekraanipaigutuses](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Enne uue toiming tootmiskeskkonnas juurutamist veenduge, et katsetaksite seda põhjalikult ja koolitaksite oma kasutajaid seda kasutama.

## <a name="overview"></a>Ülevaade

Sissetuleku toiming võimaldab kassa kasutajatel teha järgmisi ülesandeid.

- Varude vastuvõtmine poe lattu kas kinnitatud ostutellimuse dokumentidest või saadetud üleviimistellimuse dokumentidest.
- Ajalooliste varude kviitungite kohta teabe vaatamine ajavahemikul seitse päeva pärast dokumendi täielikku vastuvõtmist.
- Uute sissetulekute üleviimistellimuste taotluste loomine.

Kui kassarakenduses käivitatakse sissetuleku toiming, ilmub loendilehe vaade. See vaade näitab avatud ostutellimust ja üleviimistellimuse dokumente, millel on praeguse poe poolt vastuvõtmiseks plaanitud varude read. Konkreetse dokumendi otsimiseks ja valimiseks saavad kasutajad kerida loendit või kasutada otsingufunktsiooni.

Sissetulevate varude dokumendi loendil on kolm vahekaarti.

- **Aktiivne** – sellel vahekaardil kuvatakse täielikult või osaliselt avatud dokumendid, mis sisaldavad ridu või koguseid ridadel, mis peab veel saabuma.
- **Mustand** – sellel vahekaardil kuvatakse uued sissetuleku üleviimistellimuse taotlused, mille pood on loonud. Samas on dokumendid salvestatud ainult lokaalselt. Neid pole veel Commerce Headquartersis töötlemiseks esitatud.
- **Lõpetatud** – see vahekaart kuvab ostutellimuse või üleviimistellimuse dokumentide loendi, mille pood on viimase seitsme päeva jooksul täielikult vastu võtnud. Sellel vahekaardil on ainult informatiivne eesmärk. Kogu teave dokumentide kohta on poe jaoks kirjutuskaitstud andmed.

Kui vaatate dokumente mis tahes vahekaardil, aitab väli **Olek** teil mõista etappi, kus dokument on.

- **Mustand** – üleviimistellimuse dokument on salvestatud ainult lokaalselt poe kanali andmebaasi. Teavet üleviimistellimuse taotluse kohta pole veel Commerce Headquartersisse esitatud.
- **Taotletud** – ostutellimus või üleviimistellimus on Commerce Headquartersis loodud ja on täielikult avatud. Dokumendi suhtes ei ole veel töödeldud ühtegi sissetulekut. Ostutellimuse dokumendi tüüpi dokumentide puhul võib vastuvõtmine alata mistahes ajal, kui olek on **Taotletud**.
- **Osaliselt saadetud** – üleviimistellimuse dokumendil on üks või mitu rida või osalist rea kogust, mis on sisestatud väljamineva lao poolt kui saadetud. Need saadetud read on vastuvõtmiseks saadaval sissetuleku toimingu kaudu.
- **Täielikult saadetud** – üleviimistellimuse kõik read ja täielikud rea kogused on väljamineva lao poolt sisestatud kui saadetud. Kogu dokument on vastuvõtmiseks saadaval sissetuleku toimingu kaudu.
- **Osaliselt vastu võetud** – pood on saanud osa ostutellimuse või üleviimistellimuse dokumendi ridadest või rea kogustest, kuid mõned read jäävad avatuks.
- **Täielikult vastu võetud** – kõik ostutellimuse või üleviimistellimuse dokumendi read ja kogused on täielikult vastu võetud. Dokumendid on juurdepääsetavad ainult vahekaardil **Lõpetatud** ja on poe kasutajate jaoks kirjutuskaitstud.
- **Pooleli** – seda olekut kasutatakse seadme kasutajate teavitamiseks, et teine kasutaja töötleb dokumenti aktiivselt.
- **Peatatud** – see olek kuvatakse pärast suvandi **Peata vastuvõtmine** valimist vastuvõtmisprotsessi ajutiseks peatamiseks.
- **Töötluses HQ-s** – dokument esitati kassarakendusest Commerce Headquartersisse, kuid see ei ole veel edukalt Commerce Headquartersisse sisestatud. Dokument läbib asünkroonse dokumendi sisestamise protsessi. Pärast seda, kui dokument on edukalt Commerce Headquartersisse sisestatud, tuleb selle olek värskendada valikule **Täielikult vastu võetud** või **Osaliselt vastu võetud**.
- **Töötlemine nurjus** – dokument sisestati Commerce Headquartersisse ja lükati tagasi. Paanil **Üksikasjad** kuvatakse sisestamise nurjumise põhjus. Andmeprobleemide parandamiseks tuleb dokumenti redigeerida ja seejärel tuleb see uuesti esitada Commerce Headquartersisse töötlemiseks.

Kui valite loendis dokumendi rea, kuvatakse paan **Üksikasjad**. Sellel paanil kuvatakse lisateave dokumendi kohta, nt saatmise ja kuupäeva teave. Edenemisriba näitab, mitu eset on vaja veel töödelda. Kui dokumenti edukalt Commerce Headquartersisse ei töödeldud, näitab paan **Üksikasjad** lisaks tõrkega seotud veateateid.

Dokumendi loendi lehekülje vaates saate rakenduse ribal valida suvandi **Tellimuse üksikasjad**, et vaadata dokumendi üksikasju. Saate aktiveerida ka sobivatel dokumendiridadel sissetuleku töötlemise.

Dokumendi loendi lehekülje vaates saate luua poe jaoks ka uue sissetuleva üleviimistellimuse taotluse. Dokumendid jäävad olekusse **Mustand** ja neid saab muuta või kustutada, kuni need edastatakse töötlemiseks Commerce Headquartersisse. Pärast nende Commerce Headquartersisse edastamist ei saa üleviimistellimuse ridu enam kassarakendusest muuta.

## <a name="receiving-process"></a>Vastuvõtmise protsess

Pärast ostutellimuse või üleviimistellimuse dokumendi valimist vahekaardil **Aktiivne**, saate valida suvandi **Tellimuse üksikasjad**, et käivitada vastuvõtmise protsess.

Vaikimisi on näidatud kuva **Praegu vastuvõtmisel**. See vaade on optimeeritud vöötkoodi skannimiseks. Seda saab kasutada skannitud kaupade loendi koostamiseks, et saaksite need kaubad vastu võtta. Vastuvõtu protsessi alustamiseks saate alustada kaupade vöötkoodide skannimisega.

Kuna kauba vöötkoodid skannitakse vaates **Praegu vastuvõtmisel**, kontrollib rakendus kaupasid valitud ostu-või üleviimistellimuse dokumendi suhtes tagamaks, et iga skannitud kaup vastaks dokumendil olevale kaubale. Vaates **Praegu vastuvõtmisel** eeldatakse, et vöötkoodi iga skannimine kajastab ühe ühiku koguse vastuvõtmist, välja arvatud juhul, kui kogus on vöötkoodi manustatud. Selles vaates saate vöötkoode korduvalt skannida, et koostada kõigi vastuvõetud kaupade ja koguste loend.

### <a name="example-scenario"></a>Näidisstsenaarium

Kasutaja saab ostutellimuse, mis sisaldab 10 ühikut vöötkoodi 5657900266. Kasutaja saab skannida seda vöötkoodi 10 korda, et uuendada välja **Praegu vastuvõtmisel** ühe ühiku võrra skannimise kohta. Kui kasutaja on skannimise lõpetanud, näitab kauba rea väli **Praegu vastuvõtmisel**, et saadud kogus on 10.

Teise võimalusena, stsenaariumi korral, kus kauba kogus on suur, võib kasutaja eelistada iga vastu võetud kauba vöötkoodi skannimise asemel sisestada koguse käsitsi. Sellisel juhul saab kasutaja skannida vöötkoodi üks kord, et lisada kaup loendisse **Praegu vastuvõtmisel**. Kasutaja saab seejärel valida seostuva rea vaates **Praegu vastuvõtmisel** ja siis lehe paremal pool ilmuval paanil **Üksikasjad** uuendada kauba jaoks välja **Vastuvõetav kogus**.

Olgugi vöötkoodi skannimiseks on optimeeritud vaade **Praegu vastuvõtmisel**, saavad kasutajad rakenduse ribal valida ka suvandi **Võta toode vastu** ja seejärel sisestada kauba ID või vöötkoodi andmed dialoogiboksi kaudu. Pärast sisestatud kauba kinnitamist palutakse kasutajal sisestada kviitungi kogus.

Vaade **Praegu vastuvõtmisel** annab kasutajatele keskendunud viisi näha, milliseid tooteid nad vastu võtavad. Teise võimalusena saab kasutada vaadet **Täielik tellimuste loend**. See vaade kuvab valitud ostu- või üleviimistellimuse dokumendi jaoks dokumendi ridade täisloendi. Kasutajad saavad käsitsi valida ridu loendis ja seejärel värskendada paanil **Üksikasjad** valitud rea välja **Vastuvõetav kogus**. Vaates **Täieliku tellimuste loend** saavad kasutajad skannida vöötkoode või kasutada funktsiooni **Võta toode vastu**, et sisestada kauba ID või vöötkood ja andmed vastuvõetud koguse kohta, ilma et peaksid esmalt valima loendis vastava kauba rea.

### <a name="over-receiving-validations"></a>Üleliigse koguse vastuvõtmise kontrollid

Kinnitamine leiab aset dokumendi ridade vastuvõtmise protsessi ajal. Nende hulka kuuluvad ületarne kinnitused. Kui kasutaja püüab võtta vastu rohkem varusid kui ostutellimusel tellitud, kuid kas ületarne pole konfigureeritud või kui saadud kogus ületab ostutellimuse rea jaoks konfigureeritud ületarne hälbe, kuvatakse kasutajale viha ja tal pole võimalik üleliigset kogust vastu võtta.

Üleliigse koguse vastuvõtmine ei ole üleviimistellimuse dokumentide puhul lubatud. Kasutajatele kuvatakse alati veateade, kui nad püüavad võtta vastu rohkem, kui üleviimistellimuse rea jaoks saadeti.

### <a name="receiving-location-controlled-items"></a>Asukoha järgi kontrollitavate kaupade vastuvõtmine

Kui vastu võetud kaubad on asukoha järgi kontrollitavad, saavad kasutajad valida asukoha, kus nad kauba vastu võtavad. Soovitame protsessi tõhusamaks muutmiseks konfigureerida oma poe lao vaikimisi vastuvõtmise asukoht. Isegi kui vaikeasukoht on konfigureeritud, saavad kasutajad vajaduse järgi valitud ridadel vastuvõtmise asukoha alistada.

Toiming arvestab konfiguratsiooniga **Määramata sissetulekud lubatud** laoala dimensioonis **Asukoht** ja ei nõua määramata sissetuleku konfigureerimisel, et sisestataks asukoha dimensioon. Kui kauba puhul ei ole tühja sissetuleku asukohad lubatud, kuvab kassarakendus tõrke ja nõuab, et enne kviitungi sisestamist sisestataks asukoht.

### <a name="receive-all"></a>Võta kõik vastu

Vajaduse korral saate valida rakenduse ribal suvandi **Võta kõik vastu**, et kiiresti uuendada kogus **Praegu vastuvõtmisel** kõikide dokumendiridade jaoks maksimaalse saadaoleva väärtuseni, mis nende ridade jaoks on saadaval.

### <a name="receipt-of-unplanned-items-on-purchase-orders"></a>Ostutellimuste plaanimata kaupade vastuvõtmine

Rakenduse Commerce versioonis 10.0.14 ja uuemates versioonides saavad kasutajad vastu võtta toote, mis ei olnud algselt ostutellimusel. Selle funktsiooni lubamiseks lülitage sisse **Ridade lisamine ostutellimusse kassa vastuvõtmise ajal**.  

See funktsioon töötab ainult ostutellimuse vastuvõtmise puhul. Üleviimistellimuste jaoks ei saa kaupu vastu võtta, kui kaupu pole eelnevalt tellitud ega väljaminevast laost lähetatud.

Kasutajad ei saa ostutellimusele kassa vastuvõtmise ajal uusi tooteid lisada, kui ostutellimuse [muutuste halduse töövoog](https://docs.microsoft.com/dynamics365/supply-chain/procurement/purchase-order-approval-confirmation) on lubatud Commerce'i peakontoris (HQ). Muutuste halduse lubamiseks tuleb enne vastuvõtmise kinnitamist kõik ostutellimuse muudatused esmalt kinnitada. Kuna see protsess lubab vastuvõtjal lisada ostutellimusele uusi ridu, nurjub vastuvõtmine, kui muudatuste haldamise töövoog on lubatud. Kui muudatuste haldus on lubatud kõigi ostutellimuste jaoks või ostutellimusega seotud hankija jaoks, keda kassas aktiivselt vastu võetakse, ei saa kasutaja kassa vastuvõtmisel uusi tooteid ostutellimusse lisada.

Ridade lisamist võimaldavat funktsiooni ei saa kasutada juba ostutellimuses olevate toodete lisakoguse vastuvõtmisel. Üleliigse koguse vastuvõtmist hallatakse tavalise [üleliigse koguse vastuvõtmise](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation#over-receiving-validations) sätete kaudu ostutellimusel oleva tootesarja jaoks.

Kui **Ridade lisamine ostutellimusse kassa vastuvõtmise ajal** on lubatud ja kasutaja võtab kassas vastu **Sissetuleku toiminguga**, kui kasutaja skannib või sisestab toote vöötkoodi või tootekoodi, mida praegusel ostutellimusel ei tuvastata, kuid tuvastatakse sobiva kaubana, saab kasutaja teate kauba ostutellimusele lisamise kohta. Kui kasutaja lisab kauba ostutellimusele, loetakse kogus, mis on sisestatud kohta **Praegu vastuvõtmisel**, ostutellimuse rea tellitud koguseks.

Kui ostutellimuse vastuvõtmine on lõpule viidud ja HQ-sse töötlemiseks edastatud, luuakse lisatud read ostutellimuse koonddokumendile. HQ ostutellimuse real kuvatakse ostutellimuse rea vahekaardil **Üldine** lipp **Kassas lisatud**. Lipp **Kassas lisatud** tähistab seda, et kassa vastuvõtutoiming lisas ostutellimuse rea ja see polnud rida, mis oli ostutellimusel olemas enne vastuvõtmist.

### <a name="cancel-receiving"></a>Tühista vastuvõtmine

Peaksite kasutame rakenduse ribal funktsiooni **Tühista vastuvõtmine** ainult siis, kui soovite dokumendist väljuda ja ei soovi ühtegi muudatust salvestada. Näiteks valisite algselt vale dokumendi ja te ei soovi, et ükski eelmistest vastuvõtmise andmetest salvestataks.

### <a name="pause-receiving"></a>Peata vastuvõtmine

Kui te võtate varusid vastu, saate kasutada funktsiooni **Peata vastuvõtmine**, kui soovite teha vastuvõtmise protsessis pausi. Näiteks võite soovida teha kassas teise toimingu, nagu kliendi ostu läbi löömine, või viivitada vastuvõtu sisestamisega.

Kui valite suvandi **Peata vastuvõtmine**, muudetakse dokumendi olekuks **Peatatud**. Seega teavad kasutajad, et dokumendi andmed on sisestatud, kuid dokument pole veel kinnitatud. Kui olete vastuvõtmise protsessi jätkamiseks valmis, valige peatatud dokument ja seejärel valige suvand **Tellimuse üksikasjad**. Kõik **Praegu vastuvõtmisel** kogused, mis eelnevalt salvestati, säilitatakse ja neid saab vaadata vaates **Täielik tellimuste loend**.

### <a name="review"></a>Ülevaade

Enne sissetuleku lõplikku lisamist Commerce'i peakontorisse (HQ) saate kasutada ülevaatamise funktsiooni, et sissetulevat dokumenti kontrollida. Ülevaatamine teavitab teid võimalikest puuduvatest või valedest andmetest, mis võivad põhjustada töötlemise nurjumise, ja annab teile võimaluse parandada probleemid enne sissetulekutaotluse esitamist. Et lubada rakenduse ribal funktsioon **Vaata üle**, lubage Commerce'i peakontori (HQ) tööruumis **Funktsioonihaldus** funktsioon **Luba kassa sissetulevate ja väljaminevate varude toimingute kontrollimine**.

Funktsioon **Vaata üle** kontrollib sissetulevas dokumendis järgmisi probleeme.

- **Ülevastuvõtt** – nüüd vastuvõetav kogus on suurem kui tellitud kogus. Selle probleemi suuruse määrab Commerce'i peakontori (HQ) ületarne konfiguratsioon.
- **Alavastuvõtt** – nüüd vastuvõetav kogus on väiksem kui tellitud kogus. Selle probleemi suuruse määrab Commerce'i peakontori (HQ) alatarne konfiguratsioon.
- **Seerianumber** – seerianumbrit pole sisestatud või kontrollitud seerianumbriga kauba jaoks, mille puhul on vaja laos registreeritud seerianumbrit.
- **Asukohta pole määratud** – asukoht pole määratud asukoha järgi kontrollitava kauba jaoks, millel ei tohi olla tühja asukohta.
- **Kustutatud read** – tellimuselt on kustutanud ridasid Commerce'i peakontori (HQ) kasutaja, keda kassarakendus ära ei tunne.

Seadke parameetri **Luba automaatne kontrollimine** väärtuseks **Jah** jaotises **Kaubanduse parameetrid** > **Varud** > **Kaupluse varud**, et teha kontroll automaatselt, kui valitakse funktsioon **Lõpeta vastuvõtmine**.

### <a name="finish-receiving"></a>Lõpeta vastuvõtmine

Kui olete kõigi toodete **Praegu vastuvõtmisel** koguste sisestamise lõpetanud, peate vastuvõtmise töötlemiseks valima rakenduse ribal suvandi **Lõpeta vastuvõtmine**.

Kui kasutajad lõpetavad ostutellimuse vastuvõtmise, palutakse neil sisestada väljale **Kviitungi number** väärtus, kui see funktsioon on konfigureeritud. Tavaliselt võrdub see väärtus hankija saatelehe identifikaatoriga. **Kviitungi numbri** andmed talletatakse Commerce Headquartersis toote sissetuleku töölehel. Kviitungi numbreid ei talletata üleviimistellimuse sissetulekute jaoks.

Kui kasutatakse asünkroonset dokumendi töötlemist, esitatakse kviitung asünkroonse dokumendi raamistiku kaudu. Dokumendi sisestamiseks kuluv aeg sõltub dokumendi suurusest (ridade arvust) ja serveris toimuvast üldisest töötlemise liiklusest. Tavaliselt toimub see protsess mõne sekundiga. Kui dokumendi sisestamine ebaõnnestub, teavitatakse kasutajat dokumendi loendi **Sissetuleku toiming** kaudu, kus dokumendi olek värskendatakse suvandile **Töötlemine nurjus**. Kasutaja saab seejärel valida kassas nurjunud dokumendi, et vaadata veateateid ja tõrke põhjust paanil **Üksikasjad**. Nurjunud dokument jääb sisestamata ja nõuab, et kasutaja naaseks dokumendi ridadele, valides kassas suvandi **Tellimuse üksikasjad**. Seejärel peab kasutaja tõrgete põhjal uuendama dokumenti parandustega. Pärast dokumendi parandamist saab kasutaja proovida seda uuesti töödelda, valides rakenduse ribal suvandi **Lõpeta täitmine**.

## <a name="create-an-inbound-transfer-order"></a>Sissetuleku üleviimistellimuse loomine

Kasutajad saavad luua kassas uusi üleviimistellimuse dokumente. Protsessi alustamiseks valige rakenduse ribal **Uus**, kui olete peamise **Sissetuleku tegevuse** dokumendi loendis. Seejärel palutakse teil valida **Kanna üle kohast** ladu või pood, kust saate oma poe asukoha jaoks varusid. Väärtused on piiratud valikuga, mis on määratletud poe täitmise grupi konfiguratsioonis. Sissetuleku üleviimise taotluses on teie praegune pood alati üleviimistellimuse jaoks ladu **Kanna üle koht**. Seda väärtust ei saa muuta.

Saata vajaduse järgi sisestada väärtused väljadele **Lähetuskuupäev**, **Vastuvõtukuupäev** ja **Tarneviis**. Saate lisada ka märkuse, mis salvestatakse koos üleviimistellimuse päisega Commerce Headquartersis dokumendi manusena.

Pärast päise teabe loomist saate lisada üleviimistellimusele kaupu. Kaupade ja taotletud koguste lisamise protsessi alustamiseks valige käsk **Lisa toode**. Panil **Üksikasjad** saate samuti lisada töölehe ridade jaoks reapõhise märkuse. Need märkused salvestatakse rea manusena.

Pärast seda, kui read on sissetuleku üleviimistellimusse sisestatud, tuleb teil valida käsk **Salvesta**, et salvestada dokumendi muudatused lokaalselt, või suvand **Esitada taotlus**, et edastada tellimuse üksikasjad edasiseks töötlemiseks Commerce Headquartersisse. Kui valite suvandi **Salvesta**, salvestatakse dokumendi mustand kanali andmebaasi ja väljamineku ladu ei saa dokumenti käitada enne, kui see on suvandi **Edasta taotlus** kaudu edukalt töödeldud. Valige suvand **Salvesta** ainult juhul, kui te ei ole valmis taotlust Commerce Headquartersis töötlemiseks kinnitama.

Kui dokument on salvestatud lokaalselt, võite selle leida vahekaardil **Mustandid** dokumendi loendis **Sissetuleku toiming**. Kui dokument on olekus **Mustand**, saate seda redigeerida, kui valite suvandi **Redigeeri**. Saate vajaduse järgi ridu värskendada, lisada või kustutada. Samuti saate kustutada kogu dokumendi, kui see on olekus **Mustand**, valides käsu **Kustuta** vahekaardil **Mustandid**.

Pärast dokumendi mustandi Commerce Headquartersile edukat esitamist kuvatakse see vahekaardil **Aktiivne** ja selle olek on **Taotletud**. Praegusel hetkel ei saa sissetulevaku poe või lao kasutajad enam taotletud sissetuleku üleviimistellimuse dokumenti muuta. Ainult väljamineva lao kasutajad saavad dokumenti muuta, valides kassarakenduses suvandi **Väljaminev toiming**. Redigeerimise lukustus tagab, et ei esineks konflikte, kuna sissetuleku päringu teinu muudab üleviimistellimust samal ajal, kui väljamineku saatja aktiivselt komplekteerib ja lähetab tellimuse. Kui vajalikud on sissetuleku poe või lao muudatused pärast üleviimistellimuse esitamist, tuleb võtta ühendust väljamineku saatjaga ja paluda sisestada muudatused.

Kui dokument on olekus **Taotletud**, on see nähtav vahekaardil **Aktiivne**. Samas seda sissetuleku pood ega ladu ei saa seda veel vastu võtta. Kui väljamineku ladu on osa või kogu üleviimistellimuse teele pannud, saab sissetuleku pood või ladu sisestada sissetulekud kassas. Kui väljamineku pool töötleb üleviimistellimuse dokumente, uuendatakse nende olekut suvandilt **Taotletud** olekule **Välja saadetud** või **Osaliselt saadetud**. Pärast seda, kui dokumendid on olekus **Välja saadetud** või **Osaliselt saadetud**, saab sissetuleku pood või ladu sisestada nendepoolsed sissetulekud, kasutades sissetuleku toimingu vastuvõtmisprotsessi.

## <a name="related-topics"></a>Seotud dokumendid

[Varude väljamineku toiming kassas](pos-outbound-inventory-operation.md)
