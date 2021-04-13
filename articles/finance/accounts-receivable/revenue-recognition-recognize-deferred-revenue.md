---
title: Edasilükkunud tulu tuvastamine
description: Sellest teemast leiate teavet tulu tuvastamise kohta tulu tuvastamise funktsiooni abil.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8d9b5e1248497ec74e1c7125b2395c0ed4c825c2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820517"
---
# <a name="recognize-deferred-revenue"></a>Edasilükkunud tulu tuvastamine

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tulu tuvastamise funktsiooni ei saa funktsioonihalduse kaudu sisse lülitada. Praegu peate selle sisselülitamiseks kasutama konfiguratsioonivõtmeid.

Selles teemas kirjeldatakse tulu tuvastamise protsessi tulu tuvastamise graafikuga. Pärast müügitellimuse arve sisestamist luuakse iga tulugraafikuga müügitellimuse rea jaoks tulu tuvastamise graafik. Real olevat tulugraafikut kasutatakse selleks, et määrata, kas rea tulu tuleks edasi lükata.

## <a name="view-revenue-recognition-schedule-details"></a>Tulu tuvastamise graafiku üksikasjade kuvamine

Tulu tuvastamise graafiku üksikasjade vaatamiseks on kaks võimalust.

- Saate avada tulu tuvastamise graafiku otse arveldatud müügitellimusest. Sel juhul filtreeritakse tulugraafikus olev teave nii, et kuvatakse ainult valitud müügitellimuse üksikasjad. See variant on kasulik müügitellimuse graafiku üksikasjade kontrollimiseks.
- Saate avada tulu tuvastamise graafiku lehelt **Tulu tuvastamine \> Perioodilised ülesanded**. Seda varianti kasutatakse sageli siis, kui tulu tuvastatakse perioodi lõpus. Lehe esmakordsel avamisel teavet ei kuvata. Kasutage ruudustiku kohal olevaid filtreid, et määratleda graafiku kuvatavate üksikasjade kriteeriumid. Saate filtreerida arve kuupäevade alusel, sisestades kuupäevavahemiku, müügitellimuse, kliendi, projekti ID või oleku.

[![Tulugraafikute lehe illustratsioon](./media/revenue-recognition-schedule-page.png)](./media/revenue-recognition-schedule-page.png)

Ruudustiku all olev kiirkaart **Finantsdimensioon** kuvab müügitellimuse rea finantsdimensiooni. Neid dimensioone arvestati edasilükatud tulu sisestamisel. Neid arvestatakse ka tulu tuvastamisel. Kasutatavad dimensiooniväärtused sõltuvad tulu ja edasilükatud tulu põhikontodele omistatud konto struktuurist.

## <a name="recognize-revenue"></a>Tulu tuvastamine

Tulu tuvastamiseks käitatakse lehel **Tulu tuvastamine** protsess **Töölehe loomine**. Selle lehe saate avada kas müügitellimusest või lehelt **Perioodilised ülesanded**. Kui protsess käitatakse müügitellimusest, tuvastab see ainult valitud müügitellimuse tulu. Tavaliselt käivitatakse protsess lehel **Perioodilised ülesanded**, et tuvastada kõigi sisestatud müügitellimuste arvete tulu.

Tulu valimise ja sisestamise kriteeriumite määratlemiseks valige **Töölehe loomine**, et avada dialoogiboks **Loo tööleht**.

[![Töölehe loomise parameetrite suvandid](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

Dialoogiboksis kasutage väljagrupi **Töötlemise kuupäev** suvandeid, et määratleda tulu tuvastamisel kasutatav sisestuskuupäev. Kui valite **Valitud kuupäev**, saate sisestada sisestuskuupäeva väljale **Kande kuupäev**. Kui valite **Tulugraafiku kuupäev**, ei kasutata kande kuupäeva. Selle asemel kasutatakse sisestuskuupäevana graafiku iga rea välja **Tuvastamise kuupäev** väärtust.

Järgmiseks sisestage väljal **Alates kuupäevast** tulu tuvastamise "alates"-kuupäev. Kõik graafiku read, millel tuvastamise kuupäev on "alates"-kuupäevaga võrdne või sellest varasem, tuvastatakse, eeldusel, et nad ei ole ootel.

Kui olete kuupäevade määratlemise lõpetanud, klõpsake töölehe loomiseks dialoogiboksis nuppu **OK**. Saate teate, mis näitab loodud kannete arvu ja töölehte, kus need loodi. Töölehte ei sisestata automaatselt. Seetõttu on tulu tuvastamise halduril aega, et kontrollida, milliseid graafiku ridu tuvastatakse.

Pärast protsessi käitamist märgitakse töölehele üle kantud read olekusse **Töödeldud**. Lipp **Töödeldud** näitab, et read on üle kantud töölehele, kuid neid saab sisestada või jätta sisestamata. Pärast tulu tuvastamise töölehe sisestamist jääb lipp **Töödeldud** alles. Kui tulu tuvastamise tööleht kustutatakse või kui rida kustutatakse, eemaldatakse lipp **Töödeldud**. Sel viisil saab rida tuvastada, kui protsess **Loo tööleht** uuesti käitatakse.

[![Tulu tuvastamise graafikute leht](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Lehel **Tulu tuvastamise tööleht** (**Tulu tuvastamine \> Töölehe sisestused \> Tulu tuvastamise tööleht**) avage **Read**, et vaadata tuvastamise üksikasju. Graafiku iga tuvastatud rea kohta luuakse alati eraldi kanne, isegi kui kõik read on sisestatud samal kuupäeval ja kasutades samu pearaamatukontosid.

[![Töölehe kande leht](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

Veerus **Konto** kuvatakse edasilükkunud tulu pearaamatukonto. Pearaamatukontot ei saa redigeerida. See piirang aitab tagada, et väljastatakse õige edasilükkunud tulu pearaamatukonto. Seda pearaamatukontot ei kontrollita konto struktuuri suhtes, kuna see võib olla alates viidatud tulu pearaamatukontole sisestamisest muutunud.

Veerus **Vastaskonto** kuvatakse tulu pearaamatukonto. Vaikimisi võetakse tulu pearaamatukonto varude sisestusprofiilidest ja finantsdimensioonid võetakse müügitellimuse realt. Seda pearaamatukontot kontrollitakse praeguse konto struktuuri suhtes. Kuid seda saab redigeerida, kui konto struktuur on muutunud ja nõuab täiendavaid finantsdimensioone.

Vaikimisi summa on võetud graafiku vastavalt realt ja seda ei saa muuta.

Kui müügitellimus on mitme valuuta müügitellimus, siis määratakse vahetuskursiks vaikimisi arve vahetuskurss. Selline käitumismudel aitab tagada, et arvestusvaluuta ja aruandlusvaluuta summad vabastatakse täielikult. Ümardamise tõttu võib graafiku viimase rea vahetuskurss veidi erineda arve vahetuskursist.

Pärast tulu tuvastamise töölehe sisestamist sisestatakse kanne graafikule. Kui graafiku sama rea kohta on rohkem kui üks kanne, kuvatakse real tärn (\*). Selle rea jaoks sisestatud kannete vaatamiseks valige **Kande kanded**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Tulu tuvastamise graafiku üksikasjade muutmine

Enamikku tulugraafiku andmetest ei saa redigeerida. Graafikule ei saa lisada uusi ridu ja olemasolevaid ridu ei saa kustutada. Iga müügitellimuse rea tulugraafiku üksikasju tuleb säilitada, et aidata tagada, et edaspidi tuvastaks organisatsioon sama summa, mis oli edasi lükatud.

### <a name="edit-schedule-lines"></a>Graafiku ridade redigeerimine

Graafiku ridadel on lubatud mõned redigeerimised. Ridadel saab muuta järgmisi välju.

- **Ootel** – selle lipu saab enne rea töötlemist määrata või eemaldada. Lipu eemaldamiseks valige rida ja seejärel käsk **Eemalda ootelolek**. Ootel olevatel ridadel ei saa tulu tuvastada. Ridu saab automaatselt ootele panna, kui tulugraafikul on automaatsed ootelepanekud seadistatud.

    [![Tulugraafikud – graafiku ridade redigeerimine](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Tuvastamise kuupäev** – tuvastamise kuupäeva saab enne rea töötlemist muuta. Kui käitatakse protsess, mis loob tulu tuvastamiseks töölehe, sisestatakse kuupäev väljale **Tulu tuvastamine alates kuupäevast**. Seda kuupäeva võrreldakse väljal **Tuvastamise kuupäev** oleva kuupäevaga, et määrata, milliseid ridu tuleks tuvastada.
- **Vabastatav summa** – enne rea töötlemist saab vabastatavat summat muuta. Tuvastatud tulu summat saate vähendada, kuid mitte suurendada. See väli võimaldab organisatsioonil tuvastada osa tulust tuvastamise kuupäeval. Kui summat muudetakse, näitab summa väljal **Ülejäänud summa**, kui palju tulu tuleb veel tuvastada.
- **Väljastatav kogus** – kui tulugraafik on seadistatud ühe korra või ühe kuu kohta, näidatakse väljal **Väljastatav kogus** müügitellimuse rea kogust. Seda välja saab samuti redigeerida ja see annab teise võimaluse tulu osa tuvastamiseks. Näiteks kui real olev kogus on 5, saate koguse alistada nii, et see on väiksem kui 5. Summat väljal **Vabastatav summa** uuendatakse proportsionaalselt.

### <a name="update-contract-terms"></a>Lepingutingimuste uuendamine

Tulugraafiku üksikasjad luuakse arve sisestamisel müügitellimuse reale määratud tulugraafiku alusel. Kui müügitellimuse rea tulugraafik on vale, ei saa seda müügitellimusel pärast müügitellimuse arveldamist muuta. Selle asemel peate tulugraafiku muutmiseks kasutama nuppu **Lepingutingimuste uuendamine**. Tulugraafikut saab muuta kas enne või pärast tulu tuvastamist.

Graafiku muutmiseks valige muudetava üksuse mis tahes graafiku rida. Järgmisel joonisel on valitud 12-kuulise tulugraafikuga postitatud üksuse S0008 rida. Kui valite **Lepingutingimuste uuendamine**, kuvatakse dialoogiboksis lepingu algus- ja lõppkuupäevad ning tulugraafik.

[![Lepingu algus- ja lõppkuupäevad](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Muutke lepingu algus- ja lõppkuupäeva nii, et need kajastaksid õiget kuupäevavahemikku. Kuupäevavahemiku muutmisel peab välja **Juhtumite arv** väärtus kattuma süsteemis määratletud tulugraafikuga. Selles näites, kuna leping muudeti 24-kuuliseks lepinguks, tuleb seadistada 24-kuuline tulugraafik. Kuna 24-kuuline tulugraafik on olemas, sisestatakse see vaikimisi ja lepingut saab muuta. Kui kattuva juhtumite arvuga tulugraafikut pole olemas, ei saa lepingut muuta. Kui olete lepingutingimuste ja tulugraafiku uuendamise lõpetanud, valige muudatuste salvestamiseks dialoogiboksis nupp **OK**.

[![Uuendatud lepingu kuupäevavahemik](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Lepingu muudatused mõjutavad tulugraafiku üksikasju järgmiselt.

- Kui toote kohta ei ole tulu tuvastatud, eemaldatakse kõik eelmise graafiku üksikasjad ja asendatakse uute tulugraafiku üksikasjadega. Näiteks oli üksuse S0008 graafiku üksikasjades algselt 12 rida. Need 12 rida eemaldatakse ja asendatakse uue tulugraafiku 24 reaga.
- Kui toote kohta on tulu tuvastatud, siis tuvastati osa tulu valesti, sest tuvastamine põhines valel tulugraafikul. Need read tuleb tühistada ja uue graafiku alusel uuesti tuvastada. Selle stsenaariumi korral luuakse uued tulugraafiku read, millel on negatiivne summa algsel tuvastamise kuupäeval. Seejärel luuakse uued read, et tuvastada summad uue tulugraafiku alusel. Näiteks tuvastasite 8. augustil 2019 tulu 10,53 $. 8. septembril 2019 tuvastasite tulu 13,16 $. Seetõttu luuakse samade kuupäevadega kaks uut rida. Üks rida on -10,53 $ ja teine rida on -13,16 $ jaoks. Seejärel luuakse kakskümmend neli uut rida ja neile eraldatakse kogu edasilükatud tulu 160,61 $. Tühistamise ridu saate sisestada, käivitades protsessi **Loo tööleht**.

[![Tulu tuvastamise graafik](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]