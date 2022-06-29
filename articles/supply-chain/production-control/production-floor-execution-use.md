---
title: Kuidas töötajad kasutavad tootmisosakonna käivitusliidest
description: See artikkel kirjeldab, kuidas kasutada tootmispinna käivitamise liidest töötaja vaatepunktist.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 2ee316a3e6a6baef7aa8b5d46b04a2d1bb07a641
ms.sourcegitcommit: d770f0e6a012675a3027641704be804beb99754b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/16/2022
ms.locfileid: "9022500"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Kuidas töötajad kasutavad tootmisosakonna käivitusliidest

[!include [banner](../includes/banner.md)]

Tootmisosakonna käivitusliides on optimeeritud puudutusega suhtluseks. Selle kujundus annab visuaalse kontrasti, mis vastab tootmisjaoskonna juurdepääsetavuse nõuetele. See pakub samasuguseid funktsionaalseid võimalusi, nagu töökaardi seade. Kuid see võimaldab ka mitme töö paralleelset alustamist tööde loendis. (See võimalus on tuntud ka kui *töödekogum*.) Lisaks saavad töötajad avada tööde loendist avada juhendi, mis loodi Microsoft Dynamics 365 juhendis. Sedasi saavad nad visuaalseid HoloLensi juhiseid.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Tootmisosakonna käivitusliidesesse kasutajana sisselogimine

Enne kui töötajad võivad hakata seadet kasutama, peab järelevaataja või tehniline personal selle ette valmistama ja avama õige lehekülje Dynamics 365 Supply Chain Managementis. Lisateavet seadme seadistamise kohta leiate teemast [Seadme seadistamine tootmisosakonna käivitusliidese käitamiseks](production-floor-execution-setup.md).

Kui seade on ette valmistatud, kuvatakse sellel sisselogimisleht. Sellel lehel kuvatakse teave kohaliku tööraku tööde oleku kohta. Seda teavet uuendatakse regulaarselt. Lehel kasutavad töötajad oma pääsme ID-sid allkirjastamiseks. Kuigi töötajatel ei pea olema Supply Chain Managementi kasutajakontot, peab neil olema *ajaliselt registreeritud töötaja* konto, mida nad saavad kasutada sisselogimisel.

![Tootmisosakonna käivitusliidese sisselogimisleht.](media/pfei-sign-in-page.png "Tootmisosakonna käivitusliidese sisselogimisleht")

Selle artikli ülejäänud jaotised kirjeldavad, kuidas töötajad liidesega suhtlevad.

## <a name="all-jobs-tab"></a>Vahekaart Kõik tööd

Vahekaardil **Kõik tööd** kuvatakse tööde loend, kus on kõik tootmistööd, mille olek on *Pole alustatud*, *Peatatud* või *Käivitatud*. (Selle vahekaardi nimi on kohandatav ja võib süsteemi jaoks erineda.)

![Vahekaart Kõik tööd.](media/pfei-all-jobs-tab.png "Vahekaart Kõik tööd")

Tööde loendis on järgmised veerud. Numbrid vastavad eelmisel joonisel kujutatud numbritele.

1. **Valimise veerg** – kõige vasakpoolsem veerg kasutab märkeid, mis viitavad töödele, mille töötaja on valinud. Töötajad saavad loendist valida korraga mitu tööd. Kõigi loendis olevate tööde valimiseks märkige veerupäises ruut. Kui valitud on üks töö, kuvatakse selle töö üksikasjad lehe alumises osas.
1. **Töö oleku veerg** – see veerg kasutab iga töö oleku kuvamiseks sümboleid. Tööde, millel pole selles veerus sümbolit, olek on *Pole alustatud*. Roheline kolmnurk tähistab töid, mille olek on *Alustatud*. Kaks kollast vertikaalset rida tähistavad töid, mille olek on *Peatatud*.
1. **Kõrge prioriteedi veerg** – see veerg kasutab hüüumärke, et tähistada kõrge prioriteediga töid.
1. **Tellimus** – selles veerus kuvatakse töö tootmistellimuse number.
1. **Kirjeldus** – selles veerus kuvatakse toimingu kirjeldus, mille osa see töö on.
1. **Taotletud** – selles veerus kuvatakse kogus, mida töö plaanib toota.
1. **Alustatud** – selles veerus kuvatakse kogus, mis on selle töö jaoks juba alustatud.
1. **Lõpetatud** – selles veerus kuvatakse kogus, mis on selle töö jaoks juba lõpetatud.
1. **Maha kantud** – selles veerus kuvatakse kogus, mis on selle töö jaoks juba maha kantud.
1. **Järelejäänud** – selles veerus kuvatakse selle töö veel lõpetamata kogus.

## <a name="active-jobs-tab"></a>Vahekaart Aktiivsed tööd

**Aktiivsete tööde** vahekaardid kuvavad kõikide tööde loendi, mida sisse logitud töötaja on juba alustanud. (Selle vahekaardi nimi on kohandatav ja võib süsteemi jaoks erineda.)

![Vahekaart Aktiivsed tööd.](media/pfei-active-jobs-tab.png "Vahekaart Aktiivsed tööd")

Aktiivsete tööde loendis on järgmised veerud.

- **Valimise veerg** – kõige vasakpoolsem veerg kasutab märkeid, mis viitavad töödele, mille töötaja on valinud. Töötajad saavad loendist valida korraga mitu tööd. Kõigi loendis olevate tööde valimiseks märkige veerupäises ruut. Kui valitud on üks töö, kuvatakse selle töö üksikasjad lehe alumises osas.
- **Tellimus** – selles veerus kuvatakse töö tootmistellimuse number.
- **Kirjeldus** – selles veerus kuvatakse toimingu kirjeldus, mille osa see töö on.
- **Taotletud** – selles veerus kuvatakse kogus, mida töö plaanib toota.
- **Alustatud** – selles veerus kuvatakse kogus, mis on selle töö jaoks juba alustatud.
- **Lõpetatud** – selles veerus kuvatakse kogus, mis on selle töö jaoks juba lõpetatud.
- **Maha kantud** – selles veerus kuvatakse kogus, mis on selle töö jaoks juba maha kantud.
- **Järelejäänud** – selles veerus kuvatakse selle töö veel lõpetamata kogus.

## <a name="my-jobs-tab"></a>Vahekaart Minu tööd

Vahekaart **Minu** tööd lubab töötajatel hõlpsasti vaadata kõiki just neile määratud lugemata ja lõpetamata töid. See on kasulik ettevõtetele, kus tööd on mõnikord või alati määratud teatud töötajatele (inimressurssidele), mitte teist tüüpi ressurssidele (nt masinatele).

Planeerimissüsteem määrab iga tootmistöö automaatselt kindlale ressursikirjele ja igal ressursikirjel on tüüp (nt masin või inimene). Kui seadistate töötaja tootmistöötajana, saate seostada töötaja konto kordumatu inimressursside kirjega.

Vahekaardil **Minu** tööd loetletakse kõik sisselogitud töötaja inimressursside kirjele määratud lugemata ja lõpetamata tööd, kui mõni töötaja on sisse logitud. See ei loetle kunagi töid, mis on määratud masinasse või muud tüüpi ressursile, isegi kui sisse logitud töötaja on alustanud tööd.

Kõikide sisse logitud töötaja alustatud tööde vaatamiseks, olenemata ressursi tüübist, millele iga töö on määratud, kasutage **vahekaarti Aktiivsed** tööd. Kõigi lõpetamata tööde vaatamiseks, mis vastavad kohaliku töö filtri konfiguratsioonile, sõltumata töötajast või olekust, kasutage **vahekaarti Kõik** tööd.

![Vahekaart Minu tööd.](media/pfei-my-jobs-tab.png "Vahekaart Minu tööd")

## <a name="my-machine-tab"></a>Vahekaart Minu masin

Vahekaart **Minu masin** lubab töötajatel valida vara, mis on ühendatud masina ressursiga vahekaardil **Kõik tööd** seatud filtri sees. Siis saab töötaja vaadata valitud vara olekut ja seisundit, lugedes kuni nelja valitud loenduri ning viimaste hooldustaotluste ja registreeritud ületunnitöö väärtused. Töötaja saab nõuda ka valitud vara hooldust ning registreerida ja redigeerida masina töötunde. (Selle vahekaardi nimi on kohandatav ja võib süsteemi jaoks erineda.)

![Vahekaart Minu masin.](media/pfei-my-machine-tab.png "Vahekaart Minu masin")

Vahekaardil **Minu masin** on järgmised veerud. Numbrid vastavad eelmisel joonisel kujutatud numbritele.

1. **Masina vara** – valige masina vara, mida soovite jälgida. Alustage nime tippimist, et valida ühtivate varade loendist, või valige tööloendi filtris olevatest ressurssidest kõigi varade loendist valimiseks suurendav ikoon.

    > [!NOTE]
    > Supply Chain Managementi kasutajad saavad määrata ressursi igale varale vastavalt vajadusele, kasutades lehekülge **Kõik varad** (vahekaardil **Põhivara**, kasutades ripploendit **Ressurss**). Lisateavet leiate teemast [Vara loomine](../asset-management/objects/create-an-object.md).

1. **Sätted** – valige hammasrattaikoon, et avada dialoogiboks, kus saate valida, milliseid loendureid valitud masina vara puhul vaadata. Nende loendurite väärtused kuvatakse vahekaardil **Varahaldus**. Menüü **Sätted** (kuvatakse järgmisel kuvatõmmisel) võimaldab teil lubada kuni neli loendurit. Iga lubatava loenduri puhul kasutage loenduri valimiseks paani ülaosas otsinguvälja. Otsinguväljal loetletakse kõik lehe **Varahaldus** ülaosas valitud varaga seotud loendurid. Määrake iga loendur nii, et see jälgiks kas **koondväärtust** või loenduri viimast **tegelikku** väärtust. Näiteks kui seadistate loenduri, mis jälgib, kui palju tunde on masin töötanud, peaksite selle seadistama väärtusele **Liidetud**. Kui määrate loenduri viimati uuendatud temperatuuri või rühu mõõtmiseks, peaksite selle häälestama väärtusele **Tegelik**. Valige **OK**, et salvestada oma sätted ja sulgeda dialoogiboks.

    ![Vahekaardi Minu masin sätted.](media/pfei-my-machine-tab-settings.png "Vahekaarsi Minu masin sätted")

1. **Hooldustaotlus** – valige see nupp dialoogiboksi avamiseks, kus saate luua hooldusnõude. Saate sisestada kirjelduse ja märkuse. Supply Chain Managementi kasutaja tähelepanu juhitakse sellele, kes siis saab seejärel teisendada hooldusnõude hooldustöötellimuseks.
1. **Seisaku registreerimine** – valige see nupp, et avada dialoogiboks, kus saate registreerida masina seisuaja. Saate valida põhjuse koodi ja sisestada seisakule kuupäeva/ajavahemiku. Masina seisuaja registreerimist kasutatakse masina vara tõhususe arvutamiseks.
1. **Vaatamine või redigeerimine** – valige see nupp, et avada dialoogiboks, kus saate redigeerida või vaadata olemasolevaid seisuaja kirjeid.

## <a name="starting-and-completing-production-jobs"></a>Tootmistööde alustamine ja lõpetamine

Töötajad alustavad tootmistööd, valides töö vahekaardilt **Kõik tööd** ja valides seejärel suvandi **Käivita töö** dialoogiboksi **Alusta tööd** avamiseks.

![Dialoogiboks Alusta tööd.](media/pfei-start-job-dialog.png "Dialoogiboks Alusta tööd")

Töötajad kasutavad dialoogiboksi **Alusta tööd**, et kinnitada tootmiskogus ja seejärel alustada tööd. Töötajad saavad kogust kohandada, valides välja **Kogus** ja kasutades seejärel kuvatavat numbriklahvistikku. Seejärel valivad töötajad töö alustamiseks **Alusta**. Dialoogiboks **Alusta tööd** suletakse ja töö lisatakse vahekaardile **Aktiivsed tööd**.

Töötajad saavad alustada tööd, mis on mis tahes olekus. Kui töötaja alustab tööd, mille olek on *Alustamata*, kuvatakse dialoogiboksi **Alusta tööd** väljal **Kogus** algselt kogu kogus. Kui töötaja alustab tööd, mille olek on *Alustatud* või *Peatatud*, kuvatakse väljal **Kogus** algselt järelejäänud kogus.

## <a name="reporting-good-quantities"></a>Õigete koguste aruandlus

Kui töötaja lõpetab või osaliselt lõpetab töö, saab ta teatada õige toodetud koguse, valides töö vahekaardil **Aktiivsed tööd** ja valides seejärel **Edenemisteabe esitamine**. Seejärel sisestab töötaja dialoogiboksis **Edenemisteabe esitamine** õige koguse numbriklahvistiku abil. Kogus on vaikimisi tühi. Pärast koguse sisestamist saab töötaja uuendada töö olekuks *Käimas*, *Peatatud* või *Lõpetatud*.

![Dialoogiboks Edenemisteabe esitamine.](media/pfei-report-progress-dialog.png "Dialoogiboks Edenemisteabe esitamine")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Headest kogustest teatamine partiitellimuste puhul, millel on kaas- ja kõrvalsaadused

Töötajad saavad kasutada partiitellimuste edenemisest teatamiseks tootmispõranda täitmisliidest. See aruandlus hõlmab kaas- ja kõrvalsaaduste aruandlust.

Mõned tootjad, eriti töötlevas tööstuses, kasutavad oma tootmisprotsesside haldamiseks partiitellimusi. Partiitellimused luuakse valemitest ja neid valemeid saab määratleda nii, et nende väljundiks on kaas- ja kõrvalsaadused. Kui nende partiitellimuste kohta antakse tagasisidet, tuleb toodangu kogus registreerida valemiartiklile ning ka kaas- ja kõrvalsaadustele.

Kui töötaja lõpetab partiitellimuse töö või lõpetab selle osaliselt, saab ta teatada kauba või praagi kogused iga toote kohta, mis on määratletud tellimuse väljundina. Tooted, mis on määratletud partiitellimuse väljundina, võivad olla *Valem*, *Kaastoode* või *Kõrvaltoode* tüüpi.

Toodete headest kogustest teatamiseks valib töötaja vahekaardil **Aktiivsed tööd** töö ja seejärel **Edenemisteabe esitamine**.

Seejärel saab töötaja dialoogiboksis **Edenemisteabe esitamine** valida toodete hulgast, mis on määratletud aruande esitamise partiitellimuse väljundina. Töötaja saab valida loendist ühe või mitu toodet ja seejärel valida **Edenemisteabe esitamine**. Iga toote puhul on kogus vaikimisi 0 ja töötaja saab koguse sisestamiseks kasutada numbriklaviatuuri. Kui toodete vahel liikumiseks saab töötaja valide nuppude **Eelmine** ja **Järgmine** vahel. Pärast iga toote koguse sisestamist saab töötaja uuendada töö olekuks *Käimas*, *Peatatud* või *Lõpetatud*.

![Kaastoodete ja kõrvalsaaduste aruandlus.](media/report-co-by-products.png "Kaastoodete ja kõrvalsaaduste aruandlus")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Aruandlus kaupade planeerimise partiitellimuste kohta

Kui töötaja lõpetab planeeritava kauba partiitellimuse töö, esitab ta kogused ainult kaas- ja kõrvalsaaduste kohta, kuna planeerimisartiklid ei sisalda *Valem* tüüpi üksust.

### <a name="reporting-co-product-variation"></a>Kaastoote variatsioonist teatamine

Kui partiitellimus luuakse valemiversioonist, kus suvand **Kaastoodete variatsioonid** on seatud väärtusele *Jah*, saab töötaja esitada aruande kaastoodete kohta, mis ei kuulu partiitellimuste määratlusesse. Seda funktsiooni kasutatakse stsenaariumide korral, kus tootmisprotsessis võib tekkida ootamatu tooteväljund.

Sel juhul saab töötaja määrata aruandluse aluseks oleva kaastoote ja koguse, valides aruande edenemise dialoogiboksis **Kaastoodete variatsioonid**. Seejärel saab töötaja valida kõigi välja antud toodete hulgast, mis on määratletud kaastoodetena.

### <a name="reporting-catch-weight-items"></a>Tegeliku kaaluga kaupade aruandlus

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Töötajad saavad kasutada tootmispinna käivitamise liidest tegeliku kaalu kaupade jaoks loodud partiitellimuste edenemise aruandeks. Partiitellimused luuakse valemitest, mille puhul saab määrata tegeliku kaalu kaubad valemiüksustena, kaastoodetena ja kaastoodetena. Valemit saab määratleda ka nii, et valemiread peaksid olema määratletud tegeliku kaalu jaoks määratletud koostisainete jaoks. Tegeliku kaalu kaubad kasutavad varude jälgimiseks kahte mõõtühiku ühikut: tegeliku kaalu kogus ja varude kogus. Näiteks võib toiduainetetööstuses määratleda karbistatud liha tegeliku kaalu kaubana, kus tegeliku kaalu kogust kasutatakse kastide arvu jälgimiseks ja varude kogust kasutatakse väljade kaalu jälgimiseks.

## <a name="reporting-scrap"></a>Maha kantud koguse esitamine

Kui töötaja lõpetab või osaliselt lõpetab töö, saab ta teatada maha kantud koguse, valides töö vahekaardil **Aktiivsed tööd** ja valides seejärel **Maha kantud koguse esitamine**. Seejärel sisestab töötaja dialoogiboksis **Maha kantud koguse esitamine** maha kantud koguse numbriklahvistiku abil. Töötaja valib ka põhjuse (*Puudub*, *Masin*, *Operaator* või *Materjal*).

![Dialoogiboks Maha kantud koguse esitamine.](media/pfei-report-scrap-dialog.png "Dialoogiboks Maha kantud koguse esitamine")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Korrigeerige materjali tarbimist ja tehke materjali reserveeringuid

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Töötajad saavad korrigeerida materjali tarbimist iga tootmistöö puhul. Seda funktsiooni kasutatakse stsenaariumide puhul, kus tootmistöö tarbitud materjalide tegelik kogus oli planeeritud kogusest suurem või väiksem. Seetõttu tuleb seda korrigeerida, et hoida kaubavaru tasemeid aktiivsena.

Töötajad saavad reserveerida ka materjalide partii- ja seerianumbreid. Seda funktsiooni kasutatakse stsenaariumides, kus töötaja peab materjali jälgimisnõuete täitmiseks käsitsi määratlema, milline materjalipartii või seerianumbrid tarbiti.

Töötajad saavad määrata korrigeeritava koguse, valides suvandi Korrigeeri **materjali**. See nupp on saadaval järgmistes asukohtades:

- Dialoogiaknas **Praagi** aruanne
- Dialoogiaknas **Edenemise** aruanne
- Tööriistaribal paremal

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Materjalitarbimise korrigeerimine dialoogiboksides Praak ja Aruanne edenemise kohta

Kui töötaja on sisestanud koguse aruande edenemise **või** praagi **aruande** dialoogiboksi, **muutub nupp Materjali korrigeerimine** kättesaadavaks. Kui kasutaja selle nupu valib, kuvatakse dialoogiboks **Materjali** korrigeerimine. Selles dialoogiboksis loetletakse kaubad, mida plaanitakse tarbida, kui tööle esitatakse hea või praagitud kogus.

Dialoogiboksis kuvatavas loendis kuvatakse järgmine teave:

- **Tootenumber** – tootee master ja tootevariant.
- **Toote nimi** – toote nimi.
- **Soovitus** – töö jaoks määratud koguse jooksul edenemise või praagi puhul tarbitava materjali hinnanguline kogus.
- **Tarbimine** – töö jaoks määratud koguse jooksul edenemise või praagi puhul tarbitava materjali tegelik kogus.
- **reserveeritud** – laos füüsiliselt reserveeritud materjali kogus;
- **Ühik** – koosluse ühik.

Dialoogiakna paremal pool kuvatakse järgmine teave:

- **Tootenumber** – tootee master ja tootevariant.
- **Hinnanguline** – hinnanguline tarbitav kogus.
- **alustatud** – tootmistööga alustatud kogus;
- **Järelejääv** kogus – hinnangulise koguse kogus, mis jääb tarbima.
- **Väljastatud** kogus – tarbitud kogus.

Sooritada saab järgmisi toiminguid:

- Töötaja saab määrata materjalile kohandatava koguse, valides suvandi Kohanda **tarbimist**. Pärast koguse kinnitamist uuendatakse kogus veerus **Tarbimine** korrigeeritud kogusega.
- Kui töötaja valib materjali **korrigeerimise**, luuakse tootmise komplekteerimislehe tööleht. See tööleht sisaldab samu kaupu ja koguseid nagu loend Materjali **korrigeerimine**.
- Kui töötaja korrigeerib kogust **dialoogiboksis** Materjali korrigeerimine, **uuendatakse** vastava töölehe rea välja Soovitus sama kogusega. Kui töötaja valite **dialoogiboksis** Materjali korrigeerimine **valiku** Tühista, siis komplekteerimisleht kustutatakse.
- Kui töötaja valib **OK**, siis komplekteerimislehte ei kustutata. See sisestatakse, kui töö aruanne on aruandes praagist või **edenemise** **aruande dialoogiboksis**.
- Kui töötaja valib dialoogiaknas **Aruande** edenemine **või** Praagi **aruanne** valiku Tühista, siis komplekteerimisleht kustutatakse.

### <a name="adjust-material-from-the-primary-or-secondary-toolbar"></a>Materjali korrigeerimine esmaselt või teiseselt tööriistaribalt

Materjali **korrigeerimise nuppu** saab konfigureerida nii, et see ilmub esmasel või teisese tööriistaribal. (Lisateavet vt teemast [Kujundage tootmispinna täitmisliides](production-floor-execution-tabs.md).) Töötaja saab valida **korrigeerida materjali** pooleli toodangu jaoks. Sel juhul kuvatakse dialoogiboks **Materjali korrigeerimine**, kus töötaja saab teha soovitud korrigeerimisi. Kui dialoogiboks on avatud, luuakse tootmistellimusele tootmise komplekteerimisleht, mis sisaldab korrigeeritud koguste ridu. Kui töötaja valib suvandi **Sisesta kohe**, kinnitatakse korrigeerimine ja komplekteerimisleht sisestatakse. Kui töötaja valib suvandi **Tühista**, kustutatakse komplekteerimisleht ja korrigeerimist ei tehakse.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Korrigeeri tegeliku kaaluga kaupade materjali tarbimist

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Töötajad saavad korrigeerida tegeliku kaalu kaupade materjali tarbimist. Seda funktsiooni kasutatakse stsenaariumide puhul, kus tootmistöö tarbitud tegeliku kaalu materjali tegelik kogus oli planeeritud kogusest suurem või väiksem. Seetõttu tuleb seda korrigeerida, et hoida kaubavaru tasemeid aktiivsena. Kui töötaja korrigeerib tegeliku kaalu kauba tarbimist, saab ta korrigeerida nii tegeliku kaalu kogust kui ka varude kogust. Näiteks kui tootmistöö plaanitakse tarbida viit kasti, mille eeldatav kaal on 2 kg kasti kohta, saab töötaja korrigeerida nii tarbitava kasti arvu kui ka kastide kaalu. Süsteem kontrollib, et väljade määratud kaal jääb väljastatud tootele määratud miinimum- ja maksimumläve piiresse.

### <a name="reserve-materials"></a>Materjalide reserveerimine

Dialoogiboksis Materjali **korrigeerimine** saab töötaja materjali reserveeringuid teha ja korrigeerida, valides suvandi **Reserveeri materjal**. Materjalide **reserveerimise** dialoogiboks, mis kuvatakse kauba füüsiliselt saadaolevad varud iga ladustamis- ja jälgimisdimensiooni kohta.

Kui täpsemate laoprotsesside jaoks on materjal lubatud, kuvatakse loendis ainult füüsiliselt saadav laovaru materjali toodangu sisestuskohas. Toodangu sisendasukoht määratletakse ressursil, kus tootmistööd planeeritakse. Kui kaubakoodi kontrollitakse partii- või seerianumbrit, kuvatakse füüsiliselt saadaval olevate partii- ja seerianumbrite täielik loend. Reserveeritava koguse määramiseks saab töötaja valida reserveeritava **materjali**. Olemasoleva reserveeringu eemaldamiseks saab töötaja valida suvandi Eemalda **reserveering**.

Lisateabe saamiseks selle kohta, kuidas seadistada toodangu sisendasukohta, vaadake järgmist sisestust: [toodangu sisendasukoha seadistamine](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> Reserveerimised, mida töötaja teeb dialoogiboksis **Materjali** reserveerimine, jäävad alles, kui töötaja valib **dialoogiaknas** **Aruanne edenemise või** praagi **aruande** valiku Tühista.
>
> Tegeliku kaalu kaupade reserveeringuid ei saa korrigeerida.

## <a name="completing-a-job-and-starting-a-new-job"></a>Töö lõpetamine ja uue töö alustamine

Tavaliselt lõpetab töötaja töö, valides vahekaardil **Aktiivsed tööd** ühe või mitu praegust tööd ja valides seejärel **Edenemisteabe esitamine**. Seejärel sisestab toodetud koguse (õige koguse) ja määrab olekuks *Lõpetatud*. Kui valitud on rohkem kui üks töö, kasutab töötaja nende vahel liikumiseks **Eelmine** ja **Järgmine**. Uue töö alustamiseks valib töötaja selle vahekaardil **Kõik tööd** ja seejärel valib **Alusta tööd**.

Töötaja saab uut tööd alustada ka siis, kui eelmine töö on veel avatud. Töötaja valib jälle uue töö vahekaardil **Kõik tööd** ja seejärel valib **Alusta tööd**. Kuid sel juhul teavitab dialoogiboks **Alusta tööd** töötajat, et praegu on üks töö juba käimas ja seetõttu peab enne uue töö alustamist selle töö peatama või lõpetama.

## <a name="working-on-multiple-jobs-in-parallel"></a>Paralleelselt mitme tööga töötamine

Üks töötaja saab töötada korraga mitme tööga (paralleelselt). Sellisel juhul nimetatakse neid töid, millega töötaja töötab, *tööde kogumiks*. Töötaja saab lisada kogumisse uusi töid või lõpetada ühe või mitu tööd kogumis. Järgmised kaks stsenaariumi näitavad, kuidas töötaja saab teha töid paralleelselt.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>1. stsenaarium: töötaja, kellel ei ole aktiivseid töid, soovib alustada kahte tööd ja töötada nendega paralleelselt

Töötaja valib kaks tööd vahekaardil **Kõik tööd** ja seejärel valib **Alusta tööd**. Dialoogiboksis **Alusta tööd** kuvatakse mõlemad valitud tööd ja töötaja saab kohandada kogust kummagi töö alustamiseks. Töötaja kinnitab seejärel dialoogiboksi ja võib alustada mõlemat tööd.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>2. stsenaarium: töötaja, kellel on pooleli kaks aktiivset tööd, soovib alustada kolmandat tööd ja töötada sellega paralleelselt teiste töödega

Töötaja valib kolmanda töö vahekaardil **Kõik tööd** ja seejärel valib suvandi **Kogum**. Dialoogiboksis **Kogum** saab töötaja kohandada kogust töö alustamiseks. Töötaja kinnitab seejärel dialoogiboksi, valides suvandi **Kogum**.

## <a name="working-on-indirect-activities"></a>Kaudsete tegevustega töötamine

Kaudsed tegevused on tegevused, mis pole tootmistellimusega otseselt seotud. Kaudseid tegevusi saab paindlikult määratleda teemas [Kaudsete tegevuste seadistamine tööaja- ja palgaarvestuse jaoks](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance) kirjeldatud juhiste järgi.

Näiteks Contoso töökoja töötaja Shannon soovib osaleda ettevõtte koosolekul ja koosolekud on kaudsed tegevused. Kehtib üks kahest järgmisest stsenaariumist.

- **Shannon töötab ühe või mitme aktiivse tööga.** Shannon valib suvandi **Tegevus**, määratleb tegevuse (koosoleku) ja kinnitab valiku. Kuvatakse teade, mis teavitab teda pooleliolevatest töödest. Shannon saab teates valida, kas lõpetada või peatada pooleliolevad tööd enne koosolekule minekut.
- **Shannonil pole aktiivseid töid.** Shannon valib suvandi **Tegevus**, määratleb tegevuse (koosoleku) ja kinnitab valiku. Nüüd on ta koosolekule registreeritud.

Mõlemal juhul läheb Shannon pärast valiku kinnitamist kas sisselogimislehele või lehele, mis ootab tema kinnitust, et ta on oma kaudselt tegevuselt naasnud. Kuvatav leht sõltub tootmisosakonna käivitusliidese konfiguratsioonist. (Lisateavet leiate teemast [Tootmisosakonna käivitusliidese konfigureerimine](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Puhkepauside registreerimine

Töötajad saavad pause registreerida. Pause saab paindlikult määratleda, nagu on kirjeldatud teemas [Tasu registreerimiste põhjal](pay-based-on-registrations.md).

Töötaja registreerib pausi, valides suvandi **Paus** ja valides seejärel kaardi, mis tähistab pausi tüüpi (nt lõunasöök). Kui töötaja kinnitab valiku, kuvab seade kas sisselogimislehe või lehe, mis ootab töötaja kinnitust, et ta on pausilt naasnud. Kuvatav leht sõltub tootmisosakonna käivitusliidese konfiguratsioonist. (Lisateavet leiate teemast [Tootmisosakonna käivitusliidese konfigureerimine](production-floor-execution-configure.md).)

## <a name="view-the-my-day-dialog"></a>Dialoogi "Minu päev" kuvamine

Dialoogiaken **Minu** päev annab töötajatele ülevaate nende registreerimistest ja saldodest. Dialoog on jagatud kolme järgmise jaotise vahel:

- Põhijaos loetletakse registreerimised, mis praegune töötaja valitud kuupäeval teeb. Avaneb praeguse päeva registreerimised ja kuvatakse kuupäeva valija, mis võimaldab töötajal teisi päevi vaadata.
- Viimane **arvutatud päevasaldo jaotis** näitab töötaja jooksvaid saldosid tasustatud aja, tasustatud ületunnitöö, puudumise ja tasustatud puudumise kohta. Need väärtused põhinevad registreerimistel, mis on kal arvutatud kinnitusprotsessi käigus.
- Jaotis **Saldod** annab ülevaate saldodest määratletud perioodi jooksul valitud registreerimiste kategooriate kohta (nt puhkus, standardaeg ja ületunnitöö). Need saldod põhinevad viisil, kuidas statistilised saldod seadistatakse Kellaaja **ja kohalviibimise moodulis**. Lisateavet selle kohta, kuidas seda seadistada, vt tootmispinna [täitmisliideses puhkusesaldode näitamist](production-floor-execution-payroll-stats.md).

Administraatorid saavad selle funktsiooni liidesele lisada, **·**[asetades nupu Minu päev tööriistaribale iga vastava vahekaardi jaoks, nagu on kirjeldatud tootmispinna käivitamise liidese kujunduses.](production-floor-execution-tabs.md)

## <a name="working-in-teams"></a>Töörühmades töötamine

Kui samale tootmistööle on määratud mitu töötajat, saavad nad moodustada meeskonna. Meeskond võib määrata ühe töötaja piloodiks. Ülejäänud töötajatest saavad seejärel automaatselt selle piloodi abilised. Tulemuseks saadud meeskonna puhul peab ainult piloot registreerima töö oleku. Ajakirjed kehtivad kõigi töörühma liikmete kohta.

### <a name="prerequisites"></a>Eeltingimused

Töörühmade kasutamiseks peab administraator lubama **tootmispinna** käivitamise **liidese vahekaardi Kõik** tööd esmase tööriistariba abilise tegevuse. Juhiseid vt tootmispinna [käivitamise liidese kujundusest](production-floor-execution-tabs.md).

### <a name="form-a-new-team-that-has-a-pilot-and-an-assistant"></a>Loo uus meeskond, omab pilooti ja abi

Töötaja saab registreeruda abilisena, valides abilise **vahekaardil** **Kõik tööd**. Seejärel saab **kuvatavas dialoogiaknas** Valige töötaja abistamiseks valida piloodi töötajate loendist, kes aktiivselt tööga töötavad. Pärast seda, kui töötaja on oma valiku kinnitanud, saavad nad valitud töötaja assistendiks, kellest saab uue meeskonna piloot.

### <a name="assign-a-new-pilot-to-an-existing-team"></a>Olemasolevale töörühmale uue piloodi määramine

Kui meeskond soovib valida uue piloodi, peab praegune piloot määrama meeskonnas uueks piloodiks teise töötaja. Uue piloodi idendimiseks valib praegune piloot vahekaardil **Kõik** **tööd assistendi**. Seejärel saab **piloot kuvatavas** dialoogiboksis Muuda pilooti valida uue piloodi juba meeskonnas olnud töötajate loendist. Kui praegune piloot on oma valiku kinnitanud, on nad meeskonnast täielikult loobutud. Kuid nad saavad meeskonda uuesti meeskonda astudes, nagu nad vajavad.

### <a name="assistant-clocks-out"></a>Abiline väljaregistreerimine

Kui töötaja, kes töötab assistendina välja, lahkub ta meeskonnast. Kui püsimeeskonnad ja Uuesti **sisseregistreerimise** **suvanditeks on seatud Jah, siis väljaregistreerinud töötaja taaskäivitub töörühma järgmisel sisseregistreerimisel automaatselt.** *·* Need suvandid leiate kellaaja **ja** kohalviibimise parameetrite **lehe vahekaardilt** Üldine.

## <a name="opening-instructions"></a>Juhiste avamine

Töötajad saavad avada tööga seotud dokumenti, valides **Juhised**. Nupp **Juhised** on saadaval ainult juhul, kui koondandmetes on dokument seostatud tööga. Näiteks dokument, mis on seotud tootega Supply Chain Managementi lehel **Väljastatud tooted**, on saadaval ka töötajatele, kes saavad saavad avada seda tootmisjaoskonna käivitusliideses.

## <a name="opening-mixed-reality-guides-for-hololens"></a>HoloLensi hübriidreaalsusjuhendite avamine

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) pakub töötajatele praktilist õpet hübriidreaalsuse abil. Saate määratleda standarditud protsesse koos etapiviisiliste juhistega, mis juhatavad teie töötajaid vajalike tööriistade ja osade juurde ning näitavad neile, kuidas neid tööriistu reaalses tööolukorras kasutada. Siin on protsessi ülevaade.

1. Iga kord, kui töötaja avab tootmisjaoskonna käivitusliidesest tööde loendi, otsib liides üles kõik asjaomased juhendid kuvatud tööde jaoks.
1. Töötaja valib juhendite loendi kuvamiseks **Juhendid**.
1. Töötaja valib loendist vastava juhendi.
1. Tootmisosakonna käivitusliides kuvab valitud juhendi QR-koodi.
1. Töötaja paneb peale HoloLensi ja vaatab QR-koodi juhendi käivitamiseks.
1. Töötaja teeb juhendi läbi, et õppida ülesannet.

Lisateavet selle kohta, kuidas luua, määrata ja kasutada HoloLensi juhendeid, vt teemast [Tootmisosakonna töötajatele mõeldud hübriidreaalsuse juhendite tegemine](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
