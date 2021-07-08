---
title: Varude saadavuse arvutamine jaemüügikanalite jaoks
description: See teema kirjeldab, kuidas ettevõte saab kasutada rakendust Microsoft Dynamics 365 Commerce, et vaadata toodete võrgu- ja poekanalite hinnangulist toodete vaba varu.
author: hhainesms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 96a600279b7a90d6626d23ee8868de13e9dd0f14
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270881"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Varude saadavuse arvutamine jaemüügikanalite jaoks

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas ettevõte saab kasutada rakendust Microsoft Dynamics 365 Commerce, et vaadata toodete võrgu- ja poekanalite hinnangulist toodete vaba varu.

## <a name="accuracy-of-inventory-availability"></a>Varude saadavuse täpsus

Commerce kasutab skaleeritavuse ja jõudluse tagamiseks mitmeid servereid ja andmebaase. Seetõttu on oluline, et mõistaksite, et kassarakenduse, e-Commerce’i varude saadavuse rakenduse programmeerimisliideste (API-d) ja Commerce Headquartersi vabade varude lehtede kaudu esitatavad varude väärtused ei pruugi olla reaalajas 100% täpsed. Kui võrgu- või poekanalis toodetele loodud tehingud ei ole veel headquartersi serveri ja andmebaasiga sünkroonitud, ei pruugi headquartersi vabade varude lehed näidata nende toodete täpset reaalajas varude väärtust. Ja vastupidi, kui konfigureerisite oma ettevõtte nii, et headquartersi või teiste integreeritud rakenduste kasutajad saavad müüa, võtta vastu, tagastada või muul viisil poest või veebilaost väljas olevaid varusid, ei pruugi kassa ega võrgukanal omada teavet, mis on vajalik täpse reaalajas kaupade väärtuse kuvamiseks.

On oluline, et mõistaksite, et kõiki tööpäevadel esitatavaid vabade varude saadavuse andmeid loetakse hinnangulisteks väärtuseks. Seega kui proovite võrrelda rakenduse pakutavat vabade varude teavet tegelike riiulitel olevate füüsiliste varudega või kui proovite võrrelda vabasid varusid, mis on kassas näidatud, vabade varude andmetega, mille leiate sama lao jaoks headquartersis, võivad väärtused erineda. See tööpäeval esinev erinevus on eeldatav ja seda ei peaks lugema probleemiks. Kui soovite andmeid auditeerida ja veenduda, et varude saadavuse POS-is, API-des ja headquartersis esitatud väärtused vastaksid tegelikele füüsilistele üksustele, mille poe või lao riiulitelt leiate, on selle tegemiseks parim aeg pärast kanali tööde selleks päevaks lõppemist ja kui kõik tehingud on headquartersi ja kanalite vahel õigesti sünkroonitud.

## <a name="channel-side-inventory-calculation"></a>Kanalipoolse lao arvutamine

Kanalipoolsete laovarude arvutamine on mehhanism, mis võtab Commerce Headquartersis viimased teadaolevad kanali laoandmed alusvarudena, ja seejärel tegurid täiendavates varude muutustes, mis toimusid kanali poolel, mida ei kaasata alusvarudesse hinnangulise reaalajas vabade kaubavarude arvutamiseks. 

Järgmisi varude muudatusi võetakse praegu kanalipoolses varude arvutamise loogikas arvesse.

- Kaupluses sularaha ja kaubaga seotud tellimuste kaudu müüdud varud
- Kaupluse või poest või internetist saadud klienditellimuste kaudu müüdud varud
- Kauplustesse tagastatud inventar
- Kaupluse laost täidetud inventar (komplekteeritud, pakkimine, lähetamine)

Kanalipoolse laoarvutuse kasutamiseks eeltingimusena tuleb tööga **Toote saadavus** loodud peakontori varude andmete perioodiline hetktõmmis saata kanali andmebaasidesse. Hetktõmmis sisaldab teavet, mida headquarters omab konkreetse toote või tootevariandi ja lao kombinatsiooni jaoks varude saadavuse kohta. See sisaldab ainult laokandeid, mis olid hetketõmmise tegemisel peakontoris töödeldud ja sisestatud ja see ei pruugi olla reaalajas 100 protsenti täpne, kuna jaotatud serverites toimub kogu aeg müügitöötlus.

- Kui toote varu müüdi poe laost kassarakenduses sularahakande või asünkroonse klienditellimuse müügitehingu kaudu, ei oma headquarters kohe müügiga seotud lao väljamineku kande kohta teavet. Headquarters annab poe müügi seda tüüpi varude kohta teavet ainul pärast seda, kui P-töö laeb seotud kande kaupluse kanali andmebaasist headquartersisse ja seotud müügitellimused luuakse väljavõtte sisestuse või vähehaaval toimuva sisestusprotsessi kaudu. Tellimuste loomise protsess headquartersis loob seostuvad varude kanded. 
- E-Commerce’i kanali tellimuste kohta sisaldab headquarters teavet varude kannete kohta alles pärast seda, kui kanded on saadetud P-töö kaudu headquartersisse ja tellimuse sünkroonimisprotsess on lõpule viidud.

Commerce Headquartersis varude hetktõmmise tegemiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Tooted ja varud \> Toote saadavus**.
1. Valige **OK**, et käitada **toote saadavuse** töö. Saate selle töö ajastada ka partiina käitatavaks.

Pärast seda, kui **toote saadavuse** töö käitamine on lõpetatud, tuleb jäädvustatud andmed tõugata kanali andmebaasidesse, et vabade varude hinnangu arvutamisel arvestada uusima headquartersi varude hetktõmmisega.

Hetkeseisu andmete sünkroonimiseks peakontorist kanali andmebaasidesse järgige järgmisi samme.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Käivitage töö **1130** (**Toote saadavus**), et sünkroonida hetktõmmise andmed, mille **toote saadavuse** töö headquartersis lõi, oma kanali andmebaasidega.

## <a name="inventory-availability-apis-for-e-commerce"></a>Varude saadavuse API-d e-kaubanduse jaoks

Commerce pakub toote varude saadavuse päringute päringuks e-kaubanduse stsenaariumite jaoks järgmisi API-sid.

- **GetEstimatedAvailability** – kasutage seda API-d, et teha päringuid toote või tootevariandi kohta võrgukanali lao või ladude kohta, mis on seotud võrgukanali täitmisgrupiga.
- **GetEstimatedProductWarehouseAvailability** – Kasutage seda API-d konkreetsest laost toote või tootevariandi kaubavaru küsimiseks.

> [!NOTE]
> Need apid asendavad APIsid **GetProductAvailabilities** ja **GetAvailableInventoryNearby** kommertsversioons 10.0.7 ja vanemates versioonides.

Mõlemad API-d kasutavad sisemiselt kanalipoolset arvutusloogikat ja tagastavad hinnangulise **füüsilise saadaoleva** koguse, **kogu saadaoleva koguse**, **mõõtühiku (UoM)** **ja varude taseme** nõutud toote ja lao jaoks. Soovi korral saab tagastatud väärtused kuvada teie e-Commerce’i saidil või neid saab kasutada teie e-Commerce’i saidil teiste äriloogikate käivitamiseks. Näiteks saate takistada toodete ostmist, millele on märgitud varude tasemeks "laost väljas".

Kuigi teised Commerce’i serveris saadaolevad API-d saavad toodete vabade koguste hankimiseks minna otse komponenti Headquarters, me ei soovita, et neid kasutataks e-Commerce’i keskkonnas võimalike jõudlusprobleemide ja seotud mõju tõttu, mida need sagedased taotlused võivad teie Headquartersi serveritele avaldada. Lisaks võivad kaks ülalmainitud API-d kanalipoolse arvutusega anda täpsema hinnangu toote saadavuse kohta, võttes arvesse kanalis loodud kandeid, mis ei ole veel peakontorile teada.

Enne eelnevalt mainitud API-de kasutamist, peate lubama Headquartersi tööruumi **Funktsioonihaldus** kaudu funktsiooni **Optimeeritud toote saadavuse arvutamine**. Kui teie võrgu- ja kauplusekanalid kasutavad samu täitmisladusid, peate lubama ka **täiustatud e-äri kanalipoolse varude arvutamise loogika** funktsiooni, et kanali poole arvutusloogikat kahe API-s teguriks tegur sisestamata kannetes (sularaha ja kandmine, kliendi tellimused, tagastused) loodaks kaupluse kanalis. Pärast nende funktsioonide lubamist peate käivitama **1070-töö** **(kanali konfiguratsioon)**.

Et määrata, kuidas tootekogus API väljundis tagastatakse, järgige neid samme.

1. Valige suvandid **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**.
1. Valige vahekaart **Varud** ja seejärel konfigureerige **e-commerce'i kiirkaardi varude saadavuse API-s** **koguse väärtust API väljundi** sättes.
1. Sätte muutuse sünkroonimiseks kanalites käivitage töö **1070** (**Kanali konfiguratsioon**).

Sätte **API väljundi kogus** jaoks on kolm võimalust:

- **Tagastatud laokogus** – füüsiliselt saadav kogus ja nõutud toote kogu saadetav kogus tagastatakse API väljundis.
- **Tagastatud laokogus miinus laopuhver** – API toodangus tagastatud kogust korrigeeritakse, lahutades laopuhvri väärtuse. Lisateavet laopuhvri kohta vt jaotisest[Laopuhvrite ja laotasemete konfigureerimine](inventory-buffers-levels.md).
- **Ära tagasta varude kogust** – API väljundis tagastatakse ainult varude tase. Lisateavet laotasemete kohta vt jaotisest [Laopuhvrite ja laotasemete konfigureerimine](inventory-buffers-levels.md).

Saate kasutada `QuantityUnitTypeValue` API parameetrit ühiku tüübi määramiseks, milles soovite API-d koguse tagastada. See parameeter toetab **laoühikut** (vaikimisi), **ostuüksust** ja **müügiüksuse** valikuid. Tagastatud kogus ümardatakse peakontoris vastava mõõtühiku (UOM) kohta määratud täpsusele.

**GetEstimatedAvailability** API pakub erinevate päringustsenaariumide toetamiseks järgmisi sisendparameetreid.

- `DefaultWarehouseOnly` – selle parameetri abil saate teha päringuid võrgukanali vaikelaos kasutatava toote varude kohta. 
- `FilterByChannelFulfillmentGroup` ja `SearchArea` - kasutage neid kahte parameetrit, et teha päringuid toote varudele kõikidelt pealelaadimisasukohtadelt konkreetses otsingualas, mille aluseks on `longitude`, `latitude` ja `radius`. 
- `FilterByChannelFulfillmentGroup` ja `DeliveryModeTypeFilterValue` - kasutage neid kahte parameetrit, et teha päringuid konkreetsetest ladudest pärit toote varudele, mis on seotud võrgukanali täitmisgrupiga ja mis on konfigureeritud toetama teatud tarneviise. Parameeter `DeliveryModeTypeFilterValue` toetab suvandeid **kõik** (vaikimisi), **saatmine** ja **pealevõtmine**. Näiteks stsenaariumis, kus võrgutellimust saab täita mitmest saatmislaost, saate kasutada neid kahte parameetrit toote varude saadavuse kohta kõigis neid saatmisladudes. Sellisel juhul tagastab API toote vaba koguse ja laovarude taseme igas saatmislaos, lisaks liitkoguse ja koondvarude taseme päringuulatuse kõikidest lähetatavatest ladudest.
 
Ostuboks, kauplusevalija, soovinimekirja, ostukorvi ja ostukorvi ikooni moodulid tarbivad ülalmainitud API-sid ja parameetreid, et kuvada laotaseme teateid üle e-ärisaidi. Ärisaidi koostaja pakub toote- ja ostukäitumise juhtimiseks erinevaid laosätteid. Lisateavet vt teemast [Varude sätete rakendamine](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>Müügikoha varude otsing kanalipoolse arvutusega

Kommertsversioonis 10.0.9 ja varasemates kasutas kassa toiming **Varude otsing** reaalajas teenuse kutsumist Headquartersist, et hankida valitud toote varude kohta teavet nii kasutaja praeguse poe ja mis tahes teise poe jaoks, mis olid täitmisgrupi jaoks poe kanali konfigureerimise osana konfigureeritud. Rakenduse kommertsversiooni 10.0.10 ja uuemate versioonide puhul saate reaalajas teenuse kõned peakontorisse välja lülitada ning kasutada hoopis kanalipoolset kalkulatsiooni Commerce serveris, et määrata, milline on kauplusele füüsiliselt saadaval ja mis tahes muud täitmisgrupis määratletud asukohad. See kanali arvutatud varude konfiguratsioon on samuti kasulik asukohtade jaoks, kus internetiühendus ei ole usaldusväärne, kuna te ei pea olema võrgus, et hankida Headquartersist varude otsinguid.

Kui kanalipoolne arvutus on õigesti konfigureeritud ja hallatud, võib see pakkuda praeguse poe varude kohta palju usaldusväärsemat hinnangut, kuna see kasutab Commerce’i kanali andmebaasis olevaid kande andmeid, kuid mille kohta Headquarters ei pruugi veel teavet omada. Näiteks, kui kasutate kassa varude otsinguteks olemasolevat reaalajas teenuse kutset, siis Headquartersil ei ole tõenäoliselt veel teavet sularahamüügi kohta, mis toote jaoks just aset leidis. Seega ületab Headquartersi tagastatav vabade varude väärtus selle toote jaoks tõenäoliselt poe tegelikku vabasid varusid ühe üksuse võrra. Samas kui kasutate kanalipoolset arvutust, siis sularahamüügi saab arvutusele liita ja lahutada näidatud laoväärtusest. Olgugi nii kanalipoolse arvutuse kui ka reaalajas teenuse kutse edastatavad väärtused on vaid vabade varude hinnang, siis kanalipoole arvutuse väärtus on suurema tõenäosusega selle poe jaoks täpne.

Müügikoha **lao otsingutoimingu** konfigureerimiseks peakontoris, kasutamaks kanalipoolset arvutusloogikat ning lülitamaks välja reaalajas teenuse kutset, järgige neid samme.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**.
1. Valige Funktsiooniprofiil.
1. Kiirkaardil **Funktsioonid** jaotises **Inventuuri saadavuse arvutamine** muutke välja **Inventuuri saadavuse arvutamise režiim** väärtus **Reaalajas teenus** väärtusele **Kanal**. Vaikimisi kasutavad kõik funktsiooniprofiilid reaalajas teenuse kutseid. Kui soovite kasutada kanalipoolse arvutuse loogikat, peate muutma selle välja väärtust. See muudatus mõjutab kõiki jaekaupluseid, mis on valitud funktsiooniprofiiliga ühendatud.

Seejärel peate sünkroonima kanalite muudatused jaotusgraafiku protsessi kaudu headquartersis, tehes järgmised toimingud.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Käivitage töö **1070** (**Kanali konfigureerimine**).

Pärast konfiguratsiooni lõpetamist ei kasuta füüsiliselt saadaolevate varude kohta esitatud teave enam reaalajas teenuse kutset, kui kasutaja kassarakenduses kasutab toimingut **Varude otsing** (standard- ja maatriksvaated). Selle asemel arvutatakse praeguse poe ja kõikide täitmisgrupi poodide füüsiliselt saadaolevad varud viimase teadaoleva hetktõmmise alusel, mis Commerce Headquartersist kanali andmebaasile edastati. Hetktõmmise väärtust täpsustatakse kanalipoolse arvutuse poolt veelgi, et korrigeerida füüsiliselt saadaolevat väärtust täiendava müügi või tagastustehingute alusel, mis valitud toote jaoks kanali andmebaasis leiduvad, mida töö 1130 viimati sünkroonitud hetktõmmisesse ei kaasatud. Kui kanali andmebaas ei sisalda ühegi täitmisgrupi lao või poe tehinguandmeid, ei sisalda see ühtegi täiendavat tehingut, mille saaks väärtuse uuesti arvutamisele lisada. Seega on vabade varude parim hinnang, mille saab nende ladude või poodide jaoks kuvada, on viimase teadaoleva Commerce Headquartersi hetktõmmise andmed.

Kassa kuvad **Tellimuse täitmine** kasutavad samuti kanalipoolset arvutust, et näidata kaupade vabasid varusid, kui valitud on tellimuse täitmise rida ja kasutaja kuvab valitud üksuse vabade varude paneeli **Üksikasjad**.

## <a name="optimize-your-inventory-data"></a>Varude andmete optimeerimine

Varude parima võimaliku hinnangu tagamiseks on oluline, et kasutaksite järgmisi Commerce’i pakett-töösid ja käitaksite neid sageli.

- **P-töö** – P-töö asub lehel **Jaotusgraafikud** ja seda tuleb sageli käitada. See töö toob kanali andmebaasidest Commerce Headquartersisse e-Commerce’i tellimusi, kassa loodavaid asünkroonseid klienditellimusi ja kassa loodavaid sularahamüügi tellimusi, et neid edasi töödelda. Kuni need andmed sünkroonitakse kanalist Commerce Headquartersisse, puudub Commerce Headquartersil teave nende kannete tulemusena ladudes olevate toodete varude korrigeerimiste kohta.
- **Tellimuste sünkroonimine** – see töö töötleb Commerce Headquartersis P-töö edastatavaid kande toorandmeid ja teisendab Commerce Headquartersis e-Commerce’i ja asünkroonsed kliendi tellimuse kanded müügitellimusteks. Kuni see töö töödeldakse ja luuakse müügitellimused, siis seni ei looda varude kandeid. Seega Commerce Headquartersi vabad varud kandeid arvesse ei võta.
- **Kandeväljavõtete arvutamine partiina** – poes loodud sularahakannete puhul tagab vähehaaval toimuv sisestamine, et müügitehingutega seotud varud uuendatakse tõhusalt. Sularahamüügi tellimuste varude kannete kõige tõhusamaks töötlemiseks veenduge, et konfigureeriksite oma süsteemi kasutama [vähehaaval toimuvat sisestamist](./trickle-feed.md).
- **Kandeväljavõtete sisestamine partiina** – see töö on samuti vähehaaval toimuvaks sisestamiseks vajalik. See järgib tööd **Kandeväljavõtete arvutamine partiina**. See töö postitab süstemaatiliselt arvutatud väljavõtted, nii et kassamüügi müügitellimused luuakse Commerce Headquartersis ja Commerce Headquarters kajastab täpsemalt teie poe varusid.
- **Toote saadavus** – see töö loob Commerce Headquartersis varude hetktõmmise.
- **1130 (toote saadavus)** – see töö asub lehel **Jaotusgraafikud** ja tuleks käitada kohe pärast tööd **Toote saadavus**. See töö transpordib varude hetktõmmise andmed Commerce Headquartersist kanali andmebaasidesse.

> [!NOTE]
> - Üldiselt on hea tava käitada  **toote saadavuse** ja **1130** töid kord tunnis ning ajastada P-töid, sünkroonida tellimusi ja teha vähehaaval toimuvaid sisestamisega seotud töid sama või suurema sagedusega.
> - Jõudluse huvides, kui kanalipoolse varude saaadvuse arvutusi kasutatakse e-Commerce’i API-sid või kassa kanalipoolset varude loogikat kasutades varude saadavuse taotluse tegemiseks, kasutab arvutus vahemälu, et teha kindlaks, kas arvutuse loogika uuesti käitamise õigustamiseks on möödas piisavalt aega. Vaikimisi vahemäluks on määratud 60 sekundit. Näiteks lülitasite oma poe jaoks sisse kanalipoolse arvutuse ja vaatasite toote vabasid varusid lehel **Varude otsing**. Kui seejärel müüakse üks toote ühik, ei näita leht **Varude otsing** vähendatud varusid enne, kui vahemälu on tühjendatud. Pärast seda, kui kasutajad sisestavad kanded kassas, peaksid nad ootama 60 sekundit enne, kui kontrollivad, kas vabad varud on vähendatud.

Kui teie ettevõtte stsenaarium nõuab väiksemat vahemälu aega, pöörduge abi saamiseks oma tootetoe esindaja poole.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
