---
title: Üleviimistellimuste loomine laorakenduses
description: Selles teemas kirjeldatakse, kuidas luua ja töödelda mobiilirakenduses Warehouse Management üleviimistellimusi
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d8bab58727a7031f122864cb7465d9bc5983b467
ms.sourcegitcommit: 1f2394be857afaefa8749f607cda62dfa00ba2c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/02/2021
ms.locfileid: "6164842"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Üleviimistellimuste loomine laorakenduses

[!include [banner](../includes/banner.md)]

See funktsioon laseb laotöötajatel luua ja töödelda üleviimistellimusi otse mobiilirakenduses Warehouse Management. Esiteks peab töötaja valima sihtlao ja seejärel saavad nad skannida rakenduse abil ühe või mitu litsentsiplaati, et lisada litsentsiplaadid üleviimistellimusele. Kui laotöötaja valib suvandi **Lõpeta tellimus**, loob pakett-töö litsentsiplaatide jaoks registreeritud vaba kaubavaru alusel vajaliku üleviimistellimuse ja tellimuse read.

## <a name="enable-the-create-transfer-orders-from-the-warehouse-app-feature"></a><a name="enable-create-transfer-order-from-warehouse-app"></a>Funktsiooni „Üleviimistellimuste loomine laorakenduses” lubamine

Enne selle funktsiooni kasutamist tuleb teie süsteemis lubada nii see ise kui ka selle eeltingimused. Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et kontrollida funktsiooni olekut ja vajaduse korral see lubada.

1. Esmalt lubage funktsioon [Laorakenduse sündmuste töötlemine](warehouse-app-events.md), mis on loetletud [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) järgmiselt.
    - **Moodul** – laohaldus
    - **Funktsiooni nimi** – laorakenduse sündmuste töötlemine
1. Seejärel lubage funktsioon *Üleviimistellimuste loomine laorakenduses*, mis on loetletud järgmiselt.
    - **Moodul** – laohaldus
    - **Funktsiooni nimi** – üleviimistellimuste loomine ja töötlemine laorakenduses
1. Väljaminevate saadetiste töötlemise automatiseerimiseks peate lubama ka funktsiooni [Väljaminevate saadetiste kinnitamine pakett-töödes](confirm-outbound-shipments-from-batch-jobs.md). Funktsioon on loetletud järgmiselt.
    - **Moodul** – laohaldus
    - **Funktsiooni nimi** – väljaminevate saadetiste kinnitamine pakett-töödes

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Mobiilse seadme menüükäsu seadistamine üleviimistellimuste loomiseks

Siin on toodud üldised juhised selle kohta, kuidas seadistada mobiilses seadmes menüükäsku üleviimistellimuse loomiseks. Sõltuvalt teie ärinõuetest, mis on seotud automatiseerimise tasemega, mis tuleb määrata, kui kasutajad loovad laos üleviimistellimusi, lubatakse eri konfiguratsioonid. Selles dokumendis toodud olukorras kirjeldatakse üht sellist konfiguratsiooni.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Valige uue menüükäsu lisamiseks **Uus**. Seejärel määrake alustamiseks järgmised sätted.

    - **Menüükäsu nimi** – määrake nimi kujul, mil see peaks rakenduses Supply Chain Management ilmuma.
    - **Pealkiri** – määrake menüü nimi nii, nagu see peaks töötajatele mobiilirakenduses Warehouse Management kuvatama.
    - **Režiim** – määrake väärtuseks *Kaudne* (see menüü üksus ei loo tööd).
    - **Tegevuse kood** – seadke väärtuseks *Üleviimistellimuse loomine litsentsiplaatide põhjal*, et võimaldada laotöötajatel luua üleviimistellimus ühe või mitme skannitud litsentsiplaadi põhjal.

1. Kasutage sätet **Üleviimistellimuse rea loomise poliitika**, et kontrollida, kuidas üleviimistellimuse ridasid selle menüükäsu kaudu luuakse. Read luuakse/värskendatakse skannitud litsentsiplaatide jaoks registreeritud vaba kaubavaru alusel. Valige üks järgmistest väärtustest.

    - **Reserveeringuteta** – üleviimistellimuse ridu ei reserveerita.
    - **Litsentsiplaadi põhjal juhitav strateegia koos ridade reserveerimisega** – üleviimistellimuse ridasid reserveeritakse ning kasutatakse litsentsiplaadi põhjal juhitava strateegia suvandit, mis talletab tellimuse ridadega seotud asjakohased litsentsiplaadi ID-d. Leitud litsentsiplaadi ID väärtuseid saab seetõttu kasutada üleviimistellimuse ridade jaoks tööde loomise protsessi osana.

1. Kasutage sätet **Väljamineva saadetise poliitika**, et automatiseerida väljamineva üleviimistellimuse saadetise protsessi vajaduse korral veelgi. Kui töötaja valib nupu **Lõpeta tellimus**, loob rakendus laorakenduse sündmuse *Tellimuse lõpetamine*, mis salvestab siin valitud väärtuse praeguse üleviimistellimuse iga rea väljale **Väljamineva saadetise poliitika**. Hiljem, kui pakett-töö käigus töödeldakse üleviimistellimuse loomiseks järjekorras olevaid sündmusi, saab pakett-töö sellele väljale talletatud väärtust lugeda ja seetõttu kontrollida, kuidas töö igat rida töötleb. Valige üks järgmistest:

    - **Puudub** – automatiseeritud töötlust ei toimu.
    - **Lattu väljastamine** – automatiseerib lattu väljastamise protsessi.
    - **Saadetise kinnitamine** – automatiseerib saadetise kinnitamise protsessi.
    - **Väljastamine ja saadetise kinnitamine** – automatiseerib nii lattu väljastamise kui ka saadetise kinnitamise protsessid.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Mobiilse seadme menüükäsu lisamine menüüsse

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**
1. Valige suvand **Redigeeri**.
1. Valige olemasolev menüü pärast uue menüükäsu valimist jaotisest **Saadaolevad menüüd ja menüükäsud**. Lisage menüükäsk paremnoole nupu valimise kaudu.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Üleviimistellimuse loomine litsentsiplaatide põhjal

Mobiilirakenduses Warehouse Management on saadaval lihtne protsess üleviimistellimuste loomiseks litsentsiplaatide põhjal. Selleks peab töötaja tegema mobiilirakenduses Warehouse Management järgmist.

1. Looge üleviimistellimus ja määrake sihtladu.
1. Määrake kindlaks iga lähetatav litsentsiplaat.
1. Valige **Lõpeta tellimus**.

>[!NOTE]
> Üleviimistellimuse jaoks mõeldud litsentsiplaate saavad määrata ka mitu töötajat, kasutades selleks nuppu **Vali üleviimistellimus**, et valida laorakenduses järjekorras olevatest sündmustest olemasolev töötlemata üleviimistellimuse number. Lisateavet üleviimistellimuse numbri väärtuste leidmise kohta leiate teemast [Laorakenduse sündmuste päring](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Näidisstsenaarium

Selles stsenaariumis antakse ülevaade üleviimistellimuste loomisest ja automaatsest töötlemisest valitud litsentsiplaatides registreeritud vaba kaubavaru põhjal.

Selleks, et läbida stsenaarium soovitatud väärtuste abil, peate töötama süsteemis, kuhu on installitud demoandmed, ja valima enne alustamist juriidilise isiku *USMF*.

Selles stsenaariumis eeldatakse, et olete juba lubanud nii funktsiooni [Üleviimistellimuste loomine ja töötlemine laorakenduses](#enable-create-transfer-order-from-warehouse-app) kui ka [laorakenduse sündmuste töötlemise](warehouse-app-events.md) võimaluse.

Lisaks üleviimistellimuse loomise seadistamisele mobiilse seadme menüükäskudes tuleb seadistada ja lubada ka täiendavad mallid, asukohakorraldused ning pakett-tööd.

### <a name="example-scenario-blueprint"></a>Näidisstsenaariumi plaan

Olete jaemüüja ja teil on mitu litsentsiplaati, millest igaüks sisaldab ühes teie ladudes (*ladu 51*) kindlasse kohta paigutatud mitmesuguseid kaupu. Soovite lubada protsessi, mis võimaldab töötajatel luua mitme skannitud litsentsiplaadi teise lattu (*ladu 61*) üleviimise tellimus. Te lähetate üleviimistellimuse ja värskendate seda kohe, kui tellimuse viimane litsentsiplaat on kindlaks määratud.

![Automatiseeritud üleviimistellimuse protsessi näide](media/create-transfer-order-from-app-example.png "Automatiseeritud üleviimistellimuse protsessi näide")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Mobiilse seadme menüükäsu loomine üleviimistellimuste loomiseks

Selles jaotises selgitatakse, kuidas luua uus mobiilse seadme menüükäsk üleviimistellimuste loomiseks. Seadke suvandi **Režiim** väärtuseks *Kaudne* ja suvandi **Tegevuse kood** väärtuseks *Üleviimistellimuse loomine litsentsiplaatide põhjal*.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Valige suvand **Uus**.
1. Sisestage väljale **Menüükäsu nimi** väärtus *Loo ÜT*.
1. Sisestage väljale **Pealkiri** kirjeldus *ÜT loomine*.
1. Valige väljal **Režiim** suvand *Kaudne*.
1. Valige väljal **Tegevuse kood** suvand *Üleviimistellimuse loomine litsentsiplaatide põhjal*
1. Valige väljal **Tellimuse rea loomise poliitika** suvand *Litsentsiplaadi põhjal juhitav strateegia koos ridade reserveerimisega*.
1. Valige väljal **Väljamineva saadetise poliitika** suvand *Väljastamine ja saadetise kinnitamine*.
1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige suvand **Redigeeri**.
1. Valige olemasolev menüü **Varud** ja seejärel uus menüükäsk jaotisest **Saadaolevad menüüd ja menüükäsud**. Lisage menüükäsk menüüsse **Varud** paremnoole nupu valimise kaudu.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Töömallide seadistamine automaatseks töötlemiseks ja töö lõpetamiseks leitud litsentsiplaadi järgi

Selles jaotises selgitatakse, kuidas lubada töömall malli loodud töö automaatseks töötlemiseks voo väljastamise korral.

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Valige väljal **Töökäsu tüüp** suvand *Üleviimise väljaminek*.
1. Valige uue töömalli loomiseks **Uus**.
1. Sisestage väljale **Töömall** väärtus *51 automaatselt töödeldud LP-d*.
1. Sisestage väljale **Töömalli kirjeldus** väärtus *51 automaatselt töödeldud LP-d*.
1. Valige märkeruut **Töötle automaatselt**. See peab olema valitud, et automatiseerimine üldse toimuda saaks.
1. Demoandmetes on juba olemas töömall *51 üleviimine*; redigeerige välja **Järjekorranumber** nii, et uuel töömallil oleks väiksem järjekorranumber kui olemasoleval töömallil *51 üleviimine*.
1. Valige tööriistaribal **Salvesta**, et lubada kiirkaart **Töömalli üksikasjad**.
1. Valige kiirkaardil **Töömalli üksikasjad** tööribalt suvand **Uus**. Lisate kaks rida.
1. Tehke väljal **Töö tüüp** valik *Komplekteerimine*.
1. Valige väljal **Töö klassi ID** väärtus *TransfOut*.
1. Valige tööriistaribal **Töömalli üksikasjad** suvand **Uus**.
1. Väljal **Töö tüüp** valige *Ladustamine*.
1. Valige väljal **Töö klassi ID** väärtus *TransfOut*.
1. Valige **Salvesta**, et lubada väli **Korralduse kood**.
1. Määrake suvandi **Töö tüüp** real *Ladustamine* suvandi **Korralduse kood** väärtuseks *Laouks*. Veenduge, et sellel uuel töömallil oleks kõige väiksem **Järjekorranumber**.
1. Valige päringuredaktori avamiseks tööriistaribalt **Redigeeri päringut**.
1. Valige vahekaardil **Vahemik** suvand **Lisa**.
1. Valige lisatud rea **väljal** suvand *Ladu*.
1. Valige väljal **Kriteeriumid** väärtus *51*.
1. Valige vahekaart **Sortimine**.
1. Valige **Lisa** ja seadke suvandi **Väli** väärtuseks *Leitud litsentsiplaadi ID*. Selle välja valimisel lubatakse tööriistariba nupp **Tööpäise piirid**.
1. Valige **OK** ja seejärel **Jah**, et lähtestada rühmitus ja naasta lehele **Töömallid**.
1. Valige **Tööpäise piirid** ja lubage suvandi **Leitud litsentsiplaadi ID** jaoks valik **Rühmita selle välja põhjal** ning sulgege.

> [!NOTE]
> Kõiki seadistusi ei saa automaatselt töödelda, näiteks tegeliku kaaluga kaupu ja eri jälgimisdimensioonide kasutamist.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Asukohakorralduse seadistamine litsentsiplaadi põhjal juhitava strateegia jaoks

Selles jaotises selgitatakse, kuidas seadistada asukohakorralduse komplekteerimisprotsessi, et kasutada **litsentsiplaadi põhjal juhitavat** strateegiat.

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Valige suvand **Redigeeri**.
1. Valige navigeerimisloendi päises **töökäsu tüüp** *Üleviimise väljaminek*.
1. Valige navigeerimisloendis olemasolev asukohakorraldus **51 ÜT komplekteerimine**.
1. Märkige kiirkaardil **Read** märkeruut **Luba tükeldamine**.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada uus tegevuserida.
1. Sisestage väljale **Nimi** suvand *LP põhjal juhitud*.
1. Valige väljal **Strateegia** väärtus *Litsentsiplaadi põhjal juhitud*. See tegevus vajab vähimat järjekorranumbrit.
1. Valige tööriistaribal **Salvesta**.
1. Valige tööriistaribal lehe **värskendamise** ikoon.
1. Valige kiirkaardil **Asukohakorralduse tegevused** rida *ÜT komplekteerimine*.
1. Valige tööriistaribal **Asukohakorralduste tegevused** suvand **Nihuta alla**, et muuta järjekorranumber suuremaks kui äsja loodud tegevuse *LP põhjal juhitud* järjekorranumber.

> [!NOTE]
> Litsentsiplaadi põhjal juhitud strateegia üritab reserveerida ja luua komplekteerimistööd nende asukohtade põhjal, milles asuvad üleviimistellimuse ridadega seotud nõutud litsentsiplaadid. Kuid kui see ei ole võimalik ja te soovite ikka luua komplekteerimistööd, peaksite valima mõne muu asukohakorralduse tegevuse strateegia ja võib-olla otsima varusid lao muust kohas sõltuvalt teie äriprotsessi vajadustest.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Pakett-töö seadistamine laorakenduse sündmuste töötlemiseks

Selles jaotises selgitatakse, kuidas seadistada ajastatud pakett-tööd laorakenduse sündmuste töötlemiseks.

1. Avage **Laohaldus \> Perioodilised ülesanded \> Laorakenduse sündmuste töötlemine**.
2. Lubage dialoogiboksis jaotises **Taustal käivitamine** suvand **Pakktöötlus**.
3. Valige **Kordumine** ja seadistage töötlemise pakett-töö oma ettevõtte jaoks vajaliku intervalli põhjal.
4. Põhidialoogi naasmiseks valige **OK**.
5. Valige põhidialoogis **OK**, et lisada töö pakktöötluse järjekorda.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Pakett-töö seadistamine üleviimistellimuste automaatseks väljastamiseks

Selles jaotises selgitatakse, kuidas seadistada ajastatud pakett-tööd, et väljastada üleviimistellimused, mis on märgitud kui „valmis väljastamiseks”.

1. Avage jaotis **Laohaldus \> Lattu väljastamine \> Üleviimistellimuste automaatne väljastamine**.
1. Laiendage dialoogiboksis jaotis **Kaasatavad kirjed**.
1. Valige jaotisest **Kaasatavad kirjed** suvand **Filter**.
1. Valige päringulehel **WHSTransferAutoRTWQuery** vahekaardil **Vahemik** suvand **Lisa**, et lisada päringusse uus rida.
1. Väljal uue rea väljal **Tabel** rippmenüü ja valige tabel **Üleviimistellimuse rea väljastamine lattu**.
1. Valige rippmenüüst **Väli** suvand **Väljamineva saadetise poliitika**.
1. Valige väljal **Kriteeriumid** suvand **Väljastamine ja saadetise kinnitamine**.
1. Valige real, kus suvandi **Väli** väärtuseks on seatud *Laost*, väljal **Kriteeriumid** suvand *51*.
1. Põhidialoogiboksi naasmiseks valige **OK**.
1. Laiendage jaotis **Taustal käivitamine**, et seadistada pakktöötlus.
1. Lubage jaotises **Taustal käivitamine** suvand **Pakktöötlus**.
1. Valige **Kordumine** ja seadistage töötlemise pakett-töö oma ettevõtte jaoks vajaliku intervalli põhjal.
1. Põhidialoogi naasmiseks valige **OK**.
1. Valige põhidialoogis **OK**, et töö lisataks pakktöötluse järjekorda.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>Pakett-töö „Väljamineva saadetise töötlemine” seadistamine

Selles jaotises selgitatakse, kuidas seadistada ajastatud pakett-tööd, et käitada väljamineva saadetise kinnitamine lähetamiseks valmis koormate puhul, mis on seotud „lähetamiseks valmis” üleviimistellimuse ridadega.

1. Avage **Laohaldus \> Perioodilised ülesanded \> Väljaminevate saadetiste töötlemine**.
1. Jaotise kaasamiseks laiendage valikut **Kirjed**.
1. Valige **Filter**.
1. Valige päringus **WHSLoadShipConfirm** vahekaart **Liitmised**.
1. Laiendage tabelihierarhiat nii, et laiendatud oleksid **Koormad** ja **Koorma üksikasjad**.
1. Valige tabel **Koorma üksikasjad**.
1. Valige nupp **Lisa tabeli liitmine**.
1. Tabeliseoste loendis filtreerige või leidke veerus **Seos** väärtus *Üleviimistellimuse read (viide)*.
1. Valige loendis olev tabeliseos ja seejärel vajutage nuppu **Vali**.
1. Valige tabel **Üleviimistellimuse read**.
1. Valige nupp **Lisa tabeli liitmine**.
1. Tabeliseoste loendis filtreerige või leidke veerus **Seos** väärtus *Varude üleviimise lisaväljad (kirje ID)*.
1. Valige loendis olev tabeliseos ja seejärel vajutage nuppu **Vali**.
1. Valige vahekaart **Vahemik**.
1. Vahekaardi **Vahemik** päringutabelites seadistate te kolm päringukriteeriumide vahemikku. Rea lisamiseks valige nupp **Lisa**.
1. Lisage vahemik tabelile **Koormad**. Seadke suvandi **Väli** väärtuseks *Koorma olek* ja suvandi **Kriteeriumid** väärtuseks *Laaditud*.
1. Lisage tabelile **Varude üleviimise lisaväljad** veel üks vahemik. Seadke suvandi **Väli** väärtuseks *Väljamineva saadetise poliitika* ja suvandi **Kriteeriumid** väärtuseks *Väljastamine ja saadetise kinnitamine*.
1. Lisage tabelile **Koorma üksikasjad** veel üks vahemik. Seadke suvandi **Väli** väärtuseks *Viide* ning suvandi **Kriteeriumid** väärtuseks *Üleviimistellimuse saadetis*.
1. Põhidialoogiboksi naasmiseks valige **OK**.
1. Laiendage jaotist **Käivita taustal**.
1. Lubage **Pakktöötlus**.
1. Valige **Kordumine** ja seadistage töötlemise pakett-töö oma ettevõtte jaoks vajaliku intervalli põhjal.
1. Põhidialoogi naasmiseks valige **OK**.
1. Valige põhidialoogis **OK**, et töö lisataks pakktöötluse järjekorda.

> [!NOTE]
> Lisateavet leiate teemast [Väljaminevate saadetiste kinnitamine pakett-töödes](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>Funktsiooni „Üleviimistellimuse loomine laorakenduses” näidise töötlemine

### <a name="add-on-hand-on-a-license-plate"></a>Vaba kaubavaru lisamine litsentsiplaati

Selle stsenaariumi alustamisel peab teil olema litsentsiplaat, mis sisaldab füüsiliselt saadaolevat vabu kaubavaru.

| Kaup | Ladu | Lao olek | Koht | Litsentsiplaat | Kogus |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Saadaval | LP-010 | LP10 | 1 |
| A0002 | 51 | Saadaval | LP-010 | LP10 | 2 |

Lisage füüsilise vaba kaubavaru kogused, kasutades järgmisi väärtusi.

> [!NOTE]
> Peate looma litsentsiplaadi ja kasutama asukohti, mis võimaldavad teil kasutada mitmesuguseid kaupu, nagu LP-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Laorakenduses ülekandetellimuste loomine ja töötlemine

1. Avage rakendus ja logige sisse kasutajana *51*. Praeguse kasutaja ladu on 51.
1. Valige menüükäsk **Loo ÜT** menüüasukohast, kuhu te selle seadistuse ajal lisasite.
1. Alustage üleviimistellimuse loomist, sisestades väljale **Ladu** sihtlao („lattu”), s.t sisestage *61*. Uus üleviimistellimus läheb praegusest laost 51 („laost”) sihtlattu *61*.
1. Valige nupp **OK**.
1. Skannige litsentsiplaadi ID väljal **Litsentsiplaat**. Sisestage varasemas etapis lisatud varude litsentsiplaat, s.t *LP10*.
1. Valige nupp **OK**.
1. Valige menüünupp ja seejärel valige **Lõpeta tellimus**, et lõpetada laorakenduses üleviimistellimuse loomine.

Nimetatud näite puhul kasutatakse kaht **laorakenduse sündmust** (*Üleviimistellimuse loomine* ja *Üleviimistellimuse lõpetamine*).

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Laorakenduse sündmuste päring

Saate vaadata sündmuste järjekorda ja mobiilirakenduse Warehouse Management loodud sündmuseteateid, avades **Laohaldus \> Päringud ja aruanded \> Mobiilse seadme logid \> Laorakenduse sündmused**.

Sündmuse *Üleviimistellimuse loomine* teadete olekuks määratakse *Ootel*, mis tähendab, et pakett-töö **Laorakenduse sündmuste töötlemine** ei võta ega töötle sündmuseteateid. Kohe kui sündmuseteate olekuks määratakse *Järjekorras*, töötleb pakett-töö sündmusi. See toimub samal ajal kui sündmuse *Üleviimistellimuse lõpetamine* loomine (kui töötaja valib mobiilirakenduses Warehouse Management nupu **Lõpeta tellimus**). Kui sündmuse *Üleviimistellimuse loomine* teated on töödeldud, määratakse olekuks *Lõpetatud* või *Nurjus*. Kui sündmuse *Üleviimistellimuse lõpetamine* olekuks määratakse *Lõpetatud*, kustutatakse kõik seotud sündmused järjekorrast.

Kuna üleviimistellimuse andmete loomise jaoks mõeldud **laorakenduse sündmusi** ei töötle pakett-töö enne, kui teadete olekuks on määratud *Järjekorras*, peate leidma üles nõutavad üleviimistellimuse numbrid, mis leiduvad väljal **Identifikaator**. Väli **Identifikaator** asub lehe **Laorakenduse sündmused** päises.

Laosündmuse töötlemise osana võib üleviimistellimuse rea loomine nurjuda. Sel juhul määratakse sündmuseteate olekuks *Nurjus* ja te saate kasutada **pakett-töö logi** teavet, et saada teada põhjused ja parandada probleemid.

Tavalised probleemid võivad olla seotud protsessi puuduva seadistusega, nt sündmusest *Üleviimistellimuse loomine* puuduva transiitlaoga. Sel juhul lisaksite te transiitlao lähetuslaole ja kasutaksite suvandit **Lähtesta**, et muuta kõigi laorakenduse sündmuste teadete olek olekust *Nurjus* olekusse *Järjekorras*, mis tähendab, et pakett-töö töötleb pärast seadistusandmete parandamist uuesti sündmuseteateid.

Tootmiskeskkondades oleksid erandid seotud rohkem protsessiga, nagu näiteks vajaliku litsentsiplaadi olemasolu, mis on pakett-töö töötlemise ajal tühi ja seega ei looda üleviimistellimuse ridu. Nurjunud sündmuse teadet saab eemaldada, kasutades suvandit **Kustuta** või lisades litsentsiplaadile vajaliku füüsilise vaba kaubavaru ja kasutades suvandit **Lähtesta** kõigi seotud sündmuseteadete puhul.

Lisateavet leiate teemast [Laorakenduse sündmuse töötlemine](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Näidisstsenaariumi töötlemise järeltegevus

Selle stsenaariumi jooksul toimus järgmine.

1. Mobiilirakendust Warehouse Management kasutades valisite te menüükäsu, mis kasutab tegevuse koodi **Üleviimistellimuse loomine litsentsiplaatide põhjal**.
1. Rakenduses paluti teil valida üleviimistellimuse jaoks sihtladu. Lähteladu on alati see, milles te olete praegu töötajana sisse logitud.
1. Sihtlao valimisel reserveeris süsteem eelseisva üleviimistellimuse ID-numbri (teie süsteemis määratletud üleviimistellimuse numbriseeria põhjal), kuid ei loonud veel üleviimistellimust.
1. Kui skannisite litsentsiplaati *LP10*, mis sisaldab vaba kaubavaru, mis tuleks uude lattu teisaldada, lisati **laorakenduse sündmus** hiljem töötlemiseks sündmuste järjekorda. Laosündmus sisaldas teate üksikasju skannimise kohta, sh plaanitud üleviimistellimuse numbrit.
1. Kui mobiilirakenduses Warehouse Management valitakse nupp **Lõpeta tellimus**, luuakse uus sündmus **Üleviimistellimuse lõpetamine** ja seotud olemasoleva sündmuse **Üleviimistellimuse loomine** olekuks määratakse **Järjekorras**.
1. Teie eest peidetuna valis **laorakenduse sündmuste töötlemise pakett-töö** **järjekorras** sündmuse ja kogus kokku skannitud litsentsiplaadiga seotud vaba kaubavaru. Vaba kaubavaru põhjal loodi tegelik üleviimistellimuse kirje ja seotud read. Töö täitis ka üleviimistellimuse välja **Väljamineva saadetise poliitika** väärtusega, mis põhineb konfigureeritud suvandil *Väljastamine ja saadetise kinnitamine*, ning sidus litsentsiplaadi strateegia **Litsentsiplaadi põhjal juhitud** ridadega.
1. Üleviimistellimuse rea välja **Väljamineva saadetise poliitika** väärtuse alusel viis **üleviimistellimuste automaatse väljastamise pakett-töö** nüüd üleviimistellimuse väljastamiseni lähetuslattu. Ning **voomalli**, **töömalli** ja **asukohakorralduste** seadistuse tõttu töödeldi töö automaatselt, mistõttu muudeti suvandi **Koorma olek** väärtuseks *Laaditud*.
1. Koorma puhul käivitatakse **väljamineva saadetise töötlemise pakett-töö**, mille tulemusena lähetatakse üleviimistellimus ja luuakse saadetise eelteatis (ASN).
1. Kõigi nende sündmuste ajastus sõltub loodud pakett-tööde suvandi **Kordumine** sätetest.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="mobile-device-menu-item-setup"></a>Mobiilse seadme menüükäsu seadistamine

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Miks ma ei näe menüükäsu töö tegevuste ripploendis suvandit „Üleviimistellimuse loomine litsentsiplaatide põhjal”?

Funktsioon *Üleviimistellimuste loomine ja töötlemine laorakenduses* peab olema lubatud. Lisateavet leiate teemast [Üleviimistellimuste loomise lubamine laorakenduses](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-management-mobile-app-processes"></a>Laohalduse mobiilirakenduse protsessid

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Miks ma ei näe menüünuppu „Lõpeta tellimus”?

Üleviimistellimusele peab olema määratud vähemalt üks litsentsiplaat.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Kas samasse üleviimistellimusse saavad lisada litsentsiplaate samal ajal mitu mobiilirakenduse Warehouse Management kasutajat?

Jah, mitu laotöötajat saavad skannida litsentsiplaate samasse üleviimistellimusse.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Kas sama litsentsiplaati on võimalik lisada erinevatele üleviimistellimustele?

Ei, litsentsiplaati saab lisada ainult ühele üleviimistellimusele korraga.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Kui ma olen valinud nupu „Lõpeta tellimus”, kas ma saan sellesse üleviimistellimusse veel litsentsiplaate lisada?

Ei, te ei saa lisada rohkem litsentsiplaate üleviimistellimusse, millel on laorakenduse sündmus **Üleviimistellimuse lõpetamine**.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Kuidas saan leida olemasolevaid üleviimistellimusi, mida kasutada mobiilirakenduse Warehouse Management nupu „Vali üleviimistellimus” kaudu, kui tagasüsteem pole veel tellimust loonud?

Praegu ei saa te rakenduses üleviimistellimusi otsida, kuid leiate üleviimistellimuse numbrid lehelt **Laorakenduse sündmused**. Lisateavet leiate teemast [Laorakenduse sündmuste päring](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>Kas saan mobiilirakenduses Warehouse Management kasutatava üleviimistellimuse numbri käsitsi valida?

Toetatakse ainult numbriseeriate kaudu automaatselt loodud üleviimistellimuse numbreid.

### <a name="background-processing"></a>Taustal töötlemine

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Kuidas puhastada kirjeid laorakenduse sündmuste järjekorra teatetabelitest?

Seda saate vaadata ja hallata lehel **Laorakenduse sündmused**. Lisateavet leiate teemast [Laorakenduse sündmuste päring](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Miks ei värskendata üleviimistellimuse vastuvõtukuupäeva vastavalt tarnekuupäeva kontrollimise seadistusele?

Üleviimistellimused luuakse ilma **tarnekuupäeva kontrollimise** võimalusteta.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Kas ma saan kasutada litsentsiplaati, millel on füüsiline negatiivne vaba kaubavaru?

See funktsioon toetab litsentsiplaadi tasemel ainult positiivseid füüsilisi vaba kaubavaru koguseid, kuid teil võib olla füüsiline negatiivne vaba kaubavaru kõrgemas laos ja laooleku tasemetel, kui määrate litsentsiplaadid üleviimistellimustele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]