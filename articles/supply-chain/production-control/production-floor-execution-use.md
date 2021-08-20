---
title: Kuidas töötajad kasutavad tootmisosakonna käivitusliidest
description: Selles teemas kirjeldatakse, kuidas kasutada tootmisosakonna käivitusliidest töötaja vaatepunktist.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c2215ae4162616fec892a8bce6cff5d5f68e5aa1457b41d86bb540bdcff87197
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747861"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Kuidas töötajad kasutavad tootmisosakonna käivitusliidest

[!include [banner](../includes/banner.md)]

Tootmisosakonna käivitusliides on optimeeritud puudutusega suhtluseks. Selle kujundus annab visuaalse kontrasti, mis vastab tootmisjaoskonna juurdepääsetavuse nõuetele. See pakub samasuguseid funktsionaalseid võimalusi, nagu töökaardi seade. Kuid see võimaldab ka mitme töö paralleelset alustamist tööde loendis. (See võimalus on tuntud ka kui *töödekogum*.) Lisaks saavad töötajad avada tööde loendist avada juhendi, mis loodi Microsoft Dynamics 365 juhendis. Sedasi saavad nad visuaalseid HoloLensi juhiseid.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Tootmisosakonna käivitusliidesesse kasutajana sisselogimine

Enne kui töötajad võivad hakata seadet kasutama, peab järelevaataja või tehniline personal selle ette valmistama ja avama õige lehekülje Dynamics 365 Supply Chain Managementis. Lisateavet seadme seadistamise kohta leiate teemast [Seadme seadistamine tootmisosakonna käivitusliidese käitamiseks](production-floor-execution-setup.md).

Kui seade on ette valmistatud, kuvatakse sellel sisselogimisleht. Sellel lehel kuvatakse teave kohaliku tööraku tööde oleku kohta. Seda teavet uuendatakse regulaarselt. Lehel kasutavad töötajad oma pääsme ID-sid allkirjastamiseks. Kuigi töötajatel ei pea olema Supply Chain Managementi kasutajakontot, peab neil olema *ajaliselt registreeritud töötaja* konto, mida nad saavad kasutada sisselogimisel.

![Tootmisosakonna käivitusliidese sisselogimisleht.](media/pfei-sign-in-page.png "Tootmisosakonna käivitusliidese sisselogimisleht")

Selle teema järgnevates jaotistes kirjeldatakse, kuidas töötajad liidesega suhtlevad.

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

## <a name="reporting-scrap"></a>Maha kantud koguse esitamine

Kui töötaja lõpetab või osaliselt lõpetab töö, saab ta teatada maha kantud koguse, valides töö vahekaardil **Aktiivsed tööd** ja valides seejärel **Maha kantud koguse esitamine**. Seejärel sisestab töötaja dialoogiboksis **Maha kantud koguse esitamine** maha kantud koguse numbriklahvistiku abil. Töötaja valib ka põhjuse (*Puudub*, *Masin*, *Operaator* või *Materjal*).

![Dialoogiboks Maha kantud koguse esitamine.](media/pfei-report-scrap-dialog.png "Dialoogiboks Maha kantud koguse esitamine")

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