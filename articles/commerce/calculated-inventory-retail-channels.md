---
title: Jaemüügikanalite varude saadavuse arvutamine
description: Selles teemas kirjeldatakse valikuid, mis on poe- ja võrgukanalite vabade varude näitamiseks saadaval.
author: hhainesms
ms.date: 08/13/2020
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
ms.openlocfilehash: 29efccab017d9dff98872871bfe953fba19d2c30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799681"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Varude saadavuse arvutamine jaemüügikanalite jaoks

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas ettevõte saab kasutada rakendust Microsoft Dynamics 365 Commerce, et vaadata toodete võrgu- ja poekanalite hinnangulist toodete vaba varu.

## <a name="accuracy-of-calculation"></a>Arvutuse täpsus

Commerce kasutab skaleeritavuse ja jõudluse tagamiseks mitmeid servereid ja andmebaase. Seetõttu on oluline, et mõistaksite, et kassarakenduse, e-Commerce’i varude saadavuse rakenduse programmeerimisliideste (API-d) ja Commerce Headquartersi vabade varude lehtede kaudu esitatavad varude väärtused ei pruugi olla reaalajas 100% täpsed. Kui võrgu- või poekanalis toodetele loodud tehingud ei ole veel Commerce Headquartersi serveri ja andmebaasiga sünkroonitud, ei pruugi Commerce Headquartersi vabade varude lehed näidata nende toodete täpset reaalajas varude väärtust. Ja vastupidi, kui konfigureerisite oma ettevõtte nii, et Commerce Headquartersi või teiste integreeritud rakenduste kasutajad saavad müüa, võtta vastu, tagastada või muul viisil poest või veebilaost väljas olevaid varusid, ei pruugi kassa ega võrgukanal omada teavet, mis on vajalik täpse reaalajas kaupade vabade varude väärtuse kuvamiseks.

Selles teemas selgitatakse andmete sünkroonimise protsesse, mida saab sageli käitada, et aidata piirata andmete latentsust rakenduste või kanalite vahel. Samas on oluline, et mõistaksite, et kõiki tööpäevadel esitatavaid vabade varude saadavuse andmeid loetakse hinnangulisteks väärtuseks. Seega kui proovite võrrelda rakenduse pakutavat vabade varude teavet tegelike riiulitel olevate füüsiliste varudega või kui proovite võrrelda vabasid varusid, mis on kassas näidatud, vabade varude andmetega, mille leiate sama lao jaoks Commerce Headquartersis, võivad väärtused erineda. See tööpäeval esinev erinevus on eeldatav ja seda ei peaks lugema probleemiks. Kui soovite andmeid auditeerida ja veenduda, et varude saadavuse API-des ja Commerce Headquartersis esitatud väärtused vastaksid tegelikele füüsilistele üksustele, mille poe või lao riiulitelt leiate, on selle tegemiseks parim aeg pärast kanali tööde selleks päevaks lõppemist ja kui kõik tehingud on Commerce Headquartersi ja kanali vahel õigesti sünkroonitud.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>Varu otsingu API-de kasutamine e-Commerce’i varu saadavuse taotluste jaoks

Klientide e-Commerce’i saidil ostlemisel toote varu saadavuse kuvamiseks saate kasutada järgmisi API-sid.

- **GetEstimatedAvailability** – kasutage seda API-d, et hankida kaubavarude saadavus e-kaubanduse kanali laos või kõikides ladudes, mis on seotud e-kaubanduse kanali täitmisgrupi konfiguratsiooniga. Seda API-d saab kasutada kindlal otsingualal või raadiuses ka ladude jaoks, mis põhineb pikkuskraadi ja laiuskraadi andmetel.
- **GetEstimatedProductWarehouseAvailability** – Kasutage seda API-d konkreetses laos toote kaubavaru küsimiseks. Näiteks saate seda kasutada varu saadavuse kuvamiseks tellimuse pealevõtmist sisaldavates stsenaariumides.

> [!NOTE]
> Need API-d asendavad API-d **GetProductAvailabilities** ja **GetAvailableInventoryNearby** rakenduse Dynamics 365 Retail versioonides 10.0.7 ja varasemad.

Mõlemad API-d hangivad andmeid Commerce’i serverist ja esitavad konkreetse toote või tootevariandi ja lao kombinatsiooni vabade varude hinnangu. Kuigi teised Commerce’i serveris saadaolevad API-d saavad toodete vabade koguste hankimiseks minna otse komponenti Commerce Headquarters, me ei soovita, et neid kasutataks e-Commerce’i keskkonnas võimalike jõudlusprobleemide ja seotud mõju tõttu, mida need sagedased taotlused võivad teie Commerce Headquartersi serveritele avaldada. Lisaks sellele, kui vaba varu arvutatakse Commerce’i serveri kaudu, siis on tõenäolisem, et arvutus kaasab varud, mis hiljutiste e-Commerce’i tehingutega müüdi, mis pole veel komponendiga Commerce Headquarters sünkroonitud. Kuigi Commerce Headquarters ei pruugi nende kannete kohta teavet omada, on Commerce’i serveris ja kanali andmebaasis need andmed olemas. Seega andmetega arvestatakse ja see võib aidata pakkuda toote saadaolevate varude palju täpsemat hinnangut.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>E-Commerce’i arvutatud varude saadavuse kasutamise alustamine

Enne eelnevalt mainitud API-de kasutamist, peate lubama Commerce'i peakontori tööruumi **Funktsioonihaldus** kaudu funktsiooni **Optimeeritud toote saadavuse arvutamine**.

Enne kui API-d saavad arvutada kauba varude saadavuse parima hinnangu, tuleb Commerce Headquartersi varude saadavuse perioodilist hetktõmmist töödelda ja saata kanali andmebaasi, mida kasutab e-Commerce’i Commerce Scale Unit. Hetktõmmis sisaldab teavet, mida Commerce Headquarters omab konkreetse toote või tootevariandi ja lao kombinatsiooni jaoks varude saadavuse kohta. See võib hõlmata varude korrigeerimisi või liikumisi, mille on põhjustanud varude saamine või saadetised või teised protsessid, mida teostatakse Commerce Headquartersis, ja millist teavet e-Commerce’i kanal ainult sünkroonimisprotsessi tõttu omab.

Andmebaasi hetktõmmis, mille **toote saadavuse** töö loob, arvutab ainult varude kanded, mis töödeldi ja sisestati Commerce Headquartersisse hetktõmmise tegemise ajal. Kui toote varu müüdi poe laost kassarakenduses sularahakande või asünkroonse klienditellimuse müügitehingu kaudu, ei oma Commerce Headquarters kohe müügiga seotud lao väljamineku kande kohta teavet. See annab poe müügi seda tüüpi varude kohta teavet ainul pärast seda, kui P-töö laadib seotud kande kaupluse kanali andmebaasist Commerce Headquartersisse ja seotud müügitellimus luuakse väljavõtte sisestuse või vähehaaval toimuva sisestusprotsessi kaudu. Tellimuse loomise protsess Commerce Headquartersis loob seostuvad varude kanded. E-Commerce’i kanali tellimuste kohta sisaldab Commerce Headquarters teavet varude kannete kohta alles pärast seda, kui kanded on saadetud P-töö kaudu Commerce Headquartersisse ja tellimuse sünkroonimisprotsess on lõpule viidud. Seega on oluline, et te mõistaksite, et **toote saadavuse** töös edastatav varude hetktõmmise väärtus ei pruugi olla reaalajas 100% täpne pideva müügi töötlemise tõttu, mis jaotatud serverite üleselt aset leiab.

Commerce Headquartersis varude hetktõmmise tegemiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Tooted ja varud \> Toote saadavus**.
1. Valige **OK**, et käitada **toote saadavuse** töö. Saate selle töö ajastada ka nii, et see käitatakse partiina.

Pärast seda, kui **toote saadavuse** töö käitamine on lõpetatud, tuleb jäädvustatud andmed tõugata e-Commerce’i kanali andmebaasidesse, et vabade varude hinnangu arvutamisel arvestada uusima Commerce Headquartersi varude hetktõmmisega.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Käivitage töö **1130** (**Toote saadavus**), et sünkroonida hetktõmmise andmed, mille **toote saadavuse** töö Commerce Headquartersis lõi, oma kanali andmebaasidega.

Kui varude saadavust taotletakse API-lt **GetEstimatedAvailability** või **GetEstimatedProductWarehouseAvailability**, käivitatakse arvutus, et proovida hankida toote varude parim võimalik hinnang. Arvutus viitab kõigile e-Commerce’i klienditellimustele, mis on kanali andmebaasis, kuid mida ei kaasatud hetktõmmise andmetes, mille töö 1130 esitas. See loogika teostatakse, jälgides Commerce Headquartersi viimast töödeldud laokannet ja võrreldes seda kanali andmebaasi kannetega. See annab kanalipoolse arvutusloogika jaoks võrdlusaluse, nii et täiendavad varude liikumised, mis e-Commerce’i kanali andmebaasides klienditellimuse müügitehingute jaoks aset leidsid, saab liita API edastatava hinnanguliste varude väärtusele.

Kanalipoolse arvutuse loogika tagastab taotletud toote ja lao jaoks hinnangulise füüsiliselt saadaoleva väärtuse ja saadaoleva koguväärtuse. Soovi korral saab väärtused kuvada teie e-Commerce’i saidil või neid saab kasutada teie e-Commerce’i saidil teiste äriloogikate käivitamiseks. Näiteks saate kuvada API edastatud tegeliku vabade varude arvu asemel teate „Laost otsas”.

Arvutuse loogika, mida kanalipoolsed e-Commerce’i API-d varude väärtuse hindamiseks kasutavad, saavad hinnata varusid ainult klienditellimuste alusel, mis on kanali andmebaasis loodud, kuid mis pole veel Commerce Headquartersiga sünkroonitud ega seal postitatud. Kui teie kanali andmebaas sisaldab ka poepõhiste ladude sularahamüügi kannete andmeid, siis sularahamüüki ei liideta nende ladude kanalipoolse e-Commerce’i arvutustesse.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Kassa kanali varude otsingu toimingu konfigureerimine

Retaili versioonis 10.0.9 ja varasemates kasutas kassa toiming **Varude otsing** reaalajas teenuse kutsumist Commerce Headquartersist, et jankida valitud toote varude kohta teavet nii kasutaja praeguse poe ja mis tahes teise poe jaoks, mis olid täitmisgrupi jaoks poe kanali konfigureerimise osana konfigureeritud. Rakenduse Commerce versioonis 10.0.10 ja uuemates saate Commerce Headquartersi reaalajas teenuse kutsumised välja lülitada. Selle asemel saate kasutada Commerce’i serveri kanalipoolset arvutust, et teha kindaks vabad varud, mis on poe jaoks ja mis tahes teise asukoha jaoks, mis on täitmisgrupis määratletud, füüsiliselt saadaval. See kanali arvutatud varude konfiguratsioon on samuti kasulik asukohtade jaoks, kus internetiühendus ei ole usaldusväärne, kuna te ei pea olema võrgus, et hankida Commerce Headquartersist varude otsinguid.

Kui kanalipoolne arvutus on õigesti konfigureeritud ja hallatud, võib see pakkuda praeguse poe varude kohta palju usaldusväärsemat hinnangut, kuna see kasutab Commerce’i kanali andmebaasis olevaid kande andmeid, kuid mille kohta Commerce Headquarters ei pruugi veel teavet omada. Näiteks, kui kasutate kassa varude otsinguteks olemasolevat reaalajas teenuse kutset, siis Commerce Headquartersil ei ole tõenäoliselt veel teavet sularahamüügi kohta, mis toote jaoks just aset leidis. Seega Commerce Headquartersi tagastatav vabade varude väärtus selle toote jaoks ületab tõenäoliselt poe tegelikku vabasid varusid ühe üksuse võrra. Samas kui kasutate kanalipoolset arvutust, siis sularahamüügi saab arvutusele liita ja lahutada näidatud laoväärtusest. Olgugi nii kanalipoolse arvutuse kui ka reaalajas teenuse kutse edastatavad väärtused on vaid vabade varude hinnang, siis kanalipoole arvutuse väärtus on suurema tõenäosusega selle poe jaoks täpne.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Kassa kanali pool arvutatud varude saadavuse kasutamise alustamine

Kanalipoolse arvutusloogika kasutamiseks ja reaalajas teenuse kutsete väljalülitamiseks kassarakenduse varude otsingu jaoks peate esmalt lubama Commerce'i peakontori tööruumi **Funktsioonihaldus** kaudu funktsiooni **Optimeeritud toote saadavuse arvutamine**. Lisaks funktsiooni lubamisele, peate tegema muudatused **Funktsiooniprofiili**.

**Funktsiooniprofiili** muutmiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**.
1. Valige Funktsiooniprofiil.
1. Kiirkaardil **Funktsioonid** jaotises **Inventuuri saadavuse arvutamine** muutke välja **Inventuuri saadavuse arvutamise režiim** väärtus **Reaalajas teenus** väärtusele **Kanal**. Vaikimisi kasutavad kõik funktsiooniprofiilid reaalajas teenuse kutseid. Seega kui soovite kasutada kanalipoolse arvutuse loogikat, peate muutma selle välja väärtust. See muudatus mõjutab kõiki jaekaupluseid, mis on valitud funktsiooniprofiiliga ühendatud.

Seejärel peate sünkroonima kanali muudatused jaotusgraafiku protsessi kaudu, tehes järgmised toimingud.

1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Käivitage töö **1070** (**Kanali konfigureerimine**).

Pärast konfiguratsiooni lõpetamist ei kasuta füüsiliselt saadaolevate varude kohta esitatud teave enam reaalajas teenuse kutset, kui kasutaja kassarakenduses kasutab toimingut **Varude otsing** (standard- ja maatriksvaated). Selle asemel arvutatakse praeguse poe ja kõikide täitmisgrupi poodide füüsiliselt saadaolevad varud viimase teadaoleva hetktõmmise alusel, mis Commerce Headquartersist kanali andmebaasile edastati. Hetktõmmise väärtust täpsustatakse kanalipoolse arvutuse poolt veelgi, et korrigeerida füüsiliselt saadaolevat väärtust täiendava müügi või tagastustehingute alusel, mis valitud toote jaoks kanali andmebaasis leiduvad, mida töö 1130 viimati sünkroonitud hetktõmmisesse ei kaasatud. Kui kanali andmebaas ei sisalda ühegi täitmisgrupi lao või poe tehinguandmeid, ei sisalda see ühtegi täiendavat tehingut, mille saaks väärtuse uuesti arvutamisele lisada. Seega on vabade varude parim hinnang, mille saab nende ladude või poodide jaoks kuvada, on viimase teadaoleva Commerce Headquartersi hetktõmmise andmed.

Kassa kuvad **Tellimuse täitmine** kasutavad samuti kanalipoolset arvutust, et näidata kaupade vabasid varusid, kui valitud on tellimuse täitmise rida ja kasutaja kuvab valitud üksuse vabade varude paneeli **Üksikasjad**.

## <a name="optimize-your-inventory-data"></a>Varude andmete optimeerimine

Varude parima võimaliku hinnangu tagamiseks on oluline, et kasutaksite järgmisi Commerce’i pakett-töösid ja käitaksite neid sageli.

- **P-töö** – P-töö asub lehel **Jaotusgraafikud** ja seda tuleb sageli käitada. See töö toob kanali andmebaasidest Commerce Headquartersisse e-Commerce’i tellimusi, kassa loodavaid asünkroonseid klienditellimusi ja kassa loodavaid sularahamüügi tellimusi, et neid edasi töödelda. Kuni need andmed sünkroonitakse kanalist Commerce Headquartersisse, puudub Commerce Headquartersil teave nende kannete tulemusena ladudes olevate toodete varude korrigeerimiste kohta.
- **Tellimuste sünkroonimine** – see töö töötleb Commerce Headquartersis P-töö edastatavaid kande toorandmeid ja teisendab Commerce Headquartersis e-Commerce’i ja asünkroonsed kliendi tellimuse kanded müügitellimusteks. Kuni see töö töödeldakse ja luuakse müügitellimused, siis seni ei looda varude kandeid. Seega Commerce Headquartersi vabad varud kandeid arvesse ei võta.
- **Kandeväljavõtete arvutamine partiina** – poes loodud sularahakannete puhul tagab vähehaaval toimuv sisestamine, et müügitehingutega seotud varud uuendatakse tõhusalt. Sularahamüügi tellimuste varude kannete kõige tõhusamaks töötlemiseks veenduge, et konfigureeriksite oma süsteemi kasutama [vähehaaval toimuvat sisestamist](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Kandeväljavõtete sisestamine partiina** – see töö on samuti vähehaaval toimuvaks sisestamiseks vajalik. See järgib tööd **Kandeväljavõtete arvutamine partiina**. See töö postitab süstemaatiliselt arvutatud väljavõtted, nii et kassamüügi müügitellimused luuakse Commerce Headquartersis ja Commerce Headquarters kajastab täpsemalt teie poe varusid.
- **Toote saadavus** – see töö loob Commerce Headquartersis varude hetktõmmise.
- **1130 (toote saadavus)** – see töö asub lehel **Jaotusgraafikud** ja tuleks käitada kohe pärast tööd **Toote saadavus**. See töö transpordib varude hetktõmmise andmed Commerce Headquartersist kanali andmebaasidesse.

On soovitatav, et te ei käitaks neid pakett-töid liiga sageli (iga paari minuti tagant). Sagedased tööd koormavad Commerce'i peakontori (HQ) üle ja võivad mõjutada jõudlust. Üldiselt on hea tava käitada toote saadavuse ja 1130 töid kord tunnis ning ajastada P-töid, sünkroonida tellimusi ja teha vähehaaval toimuvaid sisestamisega seotud töid sama või suurema sagedusega.

> [!NOTE]
> Jõudluse huvides, kui kanalipoolse varude saadvuse arvutusi kasutatakse e-Commerce’i API-sid või uut kassa kanalipoolset varude loogikat kasutades varude saadavuse taotluse tegemiseks, kasutab arvutus vahemälu, et teha kindlaks, kas arvutuse loogika uuesti käitamise õigustamiseks on möödas piisavalt aega. Vaikimisi vahemäluks on määratud 60 sekundit. Näiteks lülitasite oma poe jaoks sisse kanalipoolse arvutuse ja vaatasite toote vabasid varusid lehel **Varude otsing**. Kui seejärel müüakse üks toote ühik, ei näita leht **Varude otsing** vähendatud varusid enne, kui vahemälu on tühjendatud. Pärast seda, kui kasutajad sisestavad kanded kassas, peaksid nad ootama 60 sekundit enne, kui kontrollivad, kas vabad varud on vähendatud.

Kui teie ettevõtte stsenaarium nõuab väiksemat vahemälu aega, pöörduge abi saamiseks oma tootetoe esindaja poole.


[!INCLUDE[footer-include](../includes/footer-banner.md)]