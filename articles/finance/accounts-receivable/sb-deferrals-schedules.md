---
title: Viitvõlagraafikud tulu- ja kulu viitvõlgades
description: Selles teemas kirjeldatakse tulu ja kulu viitvõlgade viitvõlagraafikuid.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 953347500f83a4a16f43331b572d2029027a5f59
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557969"
---
# <a name="deferral-schedules"></a>Edasilükkamise graafikud

Viitvõlagraafikud luuakse pärast kande sisestamist.

Viitvõlagraafikute **üksikasjade ülevaatamiseks** **saate** kasutada lehte Kõik viitvõlagraafikud või aktiivsed viitvõlagraafikud. Kuvatav teave sõltub viitvõlagraafiku tüübist (lineaalne või sündmusepõhine) ja kande tüübist. See sisaldab viitvõlagraafiku ridu ja viitvõlagraafiku kogusummasid. Lehekülge saate kasutada viitvõlagraafiku muutmiseks.

## <a name="recognize-revenue"></a>Tulu tuvastamine

> [!NOTE]
> - Ühe viitvõlagraafiku tulu äratundmiseks alustage sammust 1.
> - Mitme graafiku tulu äratundmiseks alustage sammust 2.

1. Leheküljel Kõik **viitvõlagraafikud valige** **graafiku ridade ruudustikus** read, mida soovite ära tunda ja seejärel valige **äratuntav**.
2. Seadke tuvastamistoimingu väli Tuvastamistöölehe **loomiseks** **·**.**·**
3. Valige äralõigamiskuupäeva **väljal** Äralõigamiskuupäev. Töötlemine hõlmab ainult ridu, mille lõppkuupäev on valitud äralõigamiskuupäevast varasem või sellega sama.
4. Valige **filter** ja lisage andmefiltrid nii, et loendis kuvatakse ainult soovitud kirjete vahemik.
5. Ridade **kuvamiseks** valige kuva eelvaade.
6. Valige ridade loendist mis tahes read, mida te ei soovi töödelda, ja valige käsk **Eemalda**.
7. Valige, kas soovite summeerida tuvastamise töölehe sisestuse.
8. **Jaotises Kande** kuupäev saate kande töötlemiseks kande kuupäeva muuta. Kande kuupäeva saab määrata suletud perioodideks.
9. Kui soovite töötlemist partii osana teha, valige suvand **Partii**. Dialoogiboksis Pakktöötlus **seadke** partii parameetrid ja seejärel valige OK **,** et naasta tuvastamise töötlemise **lehele**. Tulu tuvastamise tuvastustöötletakse partii töötlemisel hiljem.
10. Valige **protsess**. Kui te ei suutnud kannet partiisse lisada, töödeldakse kõik read kohe. Vastasel juhul töödeldakse ridu partii töötlemisel.

## <a name="modify-a-schedule"></a>Graafiku muutmine

Viitvõlagraafiku muutmiseks järgige neid samme.

1. Leheküljel Kõik **viitvõlagraafikud** valige viitvõlagraafik ja seejärel valige **graafik Raamatupidamise \> muutmine**.
2. Redigeerige **lehel** Ajakava muutmine suvandeid, mida soovite muuta. Sõltuvalt viitvõlagraafikust ei saa te kõiki valikuid redigeerida.
3. Viitvõlagraafiku **muudatuste** läbivaatamiseks valige eelvaade.
4. Valige nupp **OK**.

### <a name="straight-line-deferral-schedules"></a>Lineaalsed viitvõlagraafikud

Kui viitvõlagraafikus pole tuvastatud ega väliselt sisestatud ridu, saate muuta kogu viitvõlagraafikut, kaasa arvatud alguskuupäeva.

Kui viitvõlagraafikus on tuvastatud või väliselt sisestatud ridu ja te muudate viitvõlagraafikut, sõltub viitvõlagraafiku tulenev käitumine ümberarvutamiskuupäevast ja tuvastatud ridade viitvõla lõppkuupäevast. Vaikimisi määrab esimene tuvastamata periood viitvõla lõppkuupäeva.

Tuvastamise kuupäeva kasutamiseks valige graafiku alguse väljal **üks järgmistest väärtustest**: 
- **Järele järele** – summa pärast kõigi tuvastatud ridade ümberarvumist.
- **Storneerimine** : kõik pärast ümberarvutuse kuupäeva read tühistatakse, kasutades selleks määratud töölehe nime ja sisestuskuupäeva. Ümberarvutuskuupäevale järgmine summa arvutatakse seejärel uuesti.

Malli kasutamisel ignoreeritakse vahelejäetud perioode ja malli kasutatakse ainult lõppkuupäeva arvutamiseks.

### <a name="event-based-deferral-schedules"></a>Sündmusepõhised viitvõlagraafikud

Sündmusel põhineva viitvõlagraafiku puhul saate muuta kõiki tuvastamata ridu.

Kui viitvõlagraafikus on tuvastatud või väliselt sisestatud ridu, ei saa te viitvõlagraafiku malli ega eraldustüüpi muuta. Olemasoleva viitvõlagraafiku muutmisel ei saa välja **Loo eraldi sündmused väärtust muuta**.

Kui rida tuvastatakse või sisestatakse väliselt, on **märgitud** ruut Tuvastatud.

## <a name="modify-a-deferral-or-recognition-account"></a>Viitvõla- või tunnustuskonto muutmine

Viitvõlagraafiku viitvõla- või tunnustuskonto muutmiseks järgige neid samme.

1. Leheküljel Kõik **viitvõlagraafikud** valige viitvõlagraafik ja seejärel valige konto **Muutmine \>**.
2. Valige leheküljel **Konto** muutmine konto, mida soovite muuta (viitvõlg, lühiajaline või tunnustus).
3. **Valige uus konto** väljal Uus konto.
4. Valige, kas konto muudatused loovad korrigeerimist töölehe sisestusi.
5. Kui eelmises sammus on **seadistatud** valik Jah, **valige töölehe nimi väljal Töölehe** **nimi ja määrake kande kuupäev väljal Kande** kuupäev.
6. Valige nupp **OK**.

## <a name="put-a-deferral-schedule-on-hold"></a>Viitvõlagraafiku ootele panemine

Viitvõlagraafiku ootele panemiseks järgige neid samme.

1. Leheküljel Kõik **viitvõlagraafikud** valige viitvõla graafik ja seejärel valige Ootekoha **ooteltus \>**.
2. Lehel Ootel **olemine** valige, kas soovite saldo üle kanda viitvõlakontolt või ooteltuskontolt.
3. Kui valisite saldo ülekandmise, **valige** töölehe nimi väljal Töölehe nimi, **valige ootel konto väljal Ootel** **konto ja määrake kande kuupäev väljal Kande** kuupäev.
4. Valige nupp **OK**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Ooteltuse eemaldamine viitvõlagraafikust

Viitvõlagraafiku eemaldamiseks ootelt järgige neid samme.

1. Valige loendis **Kõik viitvõlagraafikud** viitvõlagraafik ja seejärel **\> valige ooteltuse eemaldamine**.
2. **Valige töölehe nimi** väljal Töölehe nimi.
3. **Määrake kande kuupäev** väljal Kande kuupäev.
4. Valige nupp **OK**.

## <a name="cancel-unrecognized-amounts"></a>Tundmatute summade tühistamine

> [!NOTE]
> Kõik juba tuvastatud või väliselt sisestatud read jäetakse sellest protsessist välja.

Tuvastamata summade tühistamiseks viitvõlagraafikus järgige neid samme.

1. **Leheküljel Kõik viitvõlagraafikud** valige viitvõlagraafik ja seejärel valige **\> Tühista tuvastamata summad**.
2. **Lehel Tundmatu summa tühistamine valige**, kas soovite luua tühistamiskirjeid.
3. Kui valisite tühistamiskirjete loomise, **valige** töölehe nimi väljal Töölehe nimi, **·** **valige tühistamiskonto väljal Tühistuskonto ja määrake kande kuupäev väljal Kande** kuupäev.
4. Valige nupp **OK**.

## <a name="cancel-a-completed-schedule"></a>Lõpetatud graafiku tühistamine

Kasutage lehte **Kõik viitvõlagraafikud**, et tühistada mis tahes tuvastatud või väliselt sisestatud summad ja tühistada viitvõla graafik, et edasist tuvastamist vältida.

Kogu viitvõlagraafiku tühistamiseks järgige neid samme.

1. Leheküljel Kõik **viitvõlagraafikud** valige viitvõla graafik ja seejärel valige Tühista **\> lõpetatud graafik**.
2. Valige leheküljel **Täieliku graafiku** tühistamine, kas soovite luua tühistamiskirjeid.
3. Kui valisite tühistamiskirjete loomise, **valige** töölehe nimi väljal Töölehe nimi, **valige konto väljal Tühistuskonto** **ja määrake kande kuupäev väljal Kande** kuupäev.
4. Valige nupp **OK**.

## <a name="reverse-transactions"></a>Kannete storneerimine

> [!NOTE]
> - Ühe viitvõlagraafiku tulu tuvastamise tühistamiseks alustage sammust 1.
> - Mitme graafiku tulu tuvastamise tühistamiseks alustage sammust 2.

1. Leheküljel Kõik **viitvõlagraafikud valige** **graafiku ridade ruudustikus** read, mille soovite tagasipööramine tühistada, ja seejärel valige tühista **.**
2. Seadke tuvastamistoimingu väli tuvastamistöölehele **vastupidiseks** **·**.**·**
3. Valige äralõigamiskuupäeva **väljal** Äralõigamiskuupäev. Töötlemine hõlmab ainult ridu, mille lõppkuupäev on määratud äralõigamiskuupäevast varasem või sellega sama.
4. Valige **filter** ja lisage andmefiltrid nii, et loendis kuvatakse ainult soovitud kirjete vahemik.
5. Ridade **kuvamiseks** valige kuva eelvaade.
6. Valige ridade loendist mis tahes read, mida te ei soovi töödelda, ja valige käsk **Eemalda**.
7. Väljad **Nimi** **ja** Kirjeldus uuendatakse automaatselt töölehe vaikenime ja kirjeldusega. Väärtusi saate vajaduse korral muuta. Samuti saate valida, kas soovite tuvastustöölehe sisestuse summeerida.
8. **Jaotises Kande** kuupäev saate kande töötlemiseks kande kuupäeva muuta. Kande kuupäeva saab määrata suletud perioodideks.
9. Kui soovite töötlemist partii osana teha, valige suvand **Partii**. Dialoogiboksis Pakktöötlus **seadke** partii parameetrid ja seejärel valige OK **,** et naasta tuvastamise töötlemise **lehele**. Tühistatud tulu tuvastamist töödeldakse partii töötlemisel hiljem.
10. Valige nupp **OK**. Kui te ei suutnud kannet partiisse lisada, töödeldakse kõik read kohe. Vastasel juhul töödeldakse ridu partii töötlemisel.

## <a name="apply-or-unapply-a-credit-note"></a>Kreeditarve sidumine või sellelt tühistamine

Kreeditarve rakendamiseks järgige neid samme.

> [!NOTE]
> Kui loote **müügitellimuse** **·** **kande viitvõlalehelt kreeditarve ja seate suvandi Olemasoleva graafiku kohandamise väärtuseks Jah**, rakendatakse kreeditarve graafikule kreeditarve sisestamisel automaatselt.

1. **Leheküljel Kõik viitvõlagraafikud** valige viitvõla graafik.
2. Valige loendist **Kreediti** korrigeerimised rida ja seejärel rakenda **.**
3. **Määrake lehel Kreeditarve (viitvõlgade)** **ümberarvutuse kuupäev väljal Ümberarvutuse** **kuupäev** ja lõppkuupäev väljal Lõppkuupäev.
4. Valige päiseloendist **müügitellimus** **, mis** sisaldab kreeditarveid.
5. **Valige rida** loendist Read.
6. Valige nupp **OK**.
7. Valige **Jah**.

> [!NOTE]
> Kreeditarve rakendamiseks erinevate arvete mitme üksiku kauba puhul tuleb neid samme korrata.

Kreeditarve mittesidumiseks järgige neid samme.

1. **Leheküljel Kõik viitvõlagraafikud** valige viitvõla graafik.
2. Valige loendist **Kreediti** korrigeerimised arve ja seejärel valige **Tühista sidumine**.
3. Valige **Jah**.

## <a name="fields"></a>Väljad

Lehel **Kõik viitvõlagraafikud** on järgmised väljad.

| Väljad | Kirjeldus |
|--------|-------------|
| **Päis** | |
| **Ajastamine** | |
| Eraldamise tüüp | Eraldamise tüüp sündmusepõhiste viitvõlgade puhul: protsent **või** **summa**. |
| Ümberklassifitseerimise kuupäev | <p>Viimane kuupäev, mil viitvõlagraafiku lühiajalist ümberklassifitseerimist töödeldakse. Seda kuupäeva uuendatakse iga kord, kui **sündmuse lühiajalist ümberklassifitseerimist** kasutatakse viitvõlagraafikus.</p>See väli on saadaval ainult siis, kui kasutatakse jooksvaid perioode või fikseeritud lühiajalise viitvõla meetodit. |
| **Konto** | |
| Edasilükkamise konto | Viitvõlasumma puhul kasutatav konto. |
| Kajastamise konto | Konto, mida kasutatakse tunnustussumma puhul. |
| Kajastamise tüüp | Tuvastamise tüüp. |
| Jaotustüüp | Jaotuse tüüp. |
| **Kanne** | |
| Loomise allikas | Kande loomise allikas. |
| Kande tüüp | Kande tüüp. |
| Müügitellimus | Müügitellimuse number. |
| Arve | Arve number. |
| Kaup | Kaubakood. |
| **Arveldusgraafik** | |
| Arveldusgraafiku number | Vastava arveldusgraafiku number. |
| Arveldamise rea olek | Vastava arveldusgraafiku rea üksuse olek. |
| Välised viited | Teave väliste viidete kohta arveldusgraafikust: **väline** ja **rea number**. |
| Kogusummad | <p>Viitvõlagraafiku kogusummad:</p><ul><li>**Pikaajaline –** pikaajaliste edasilükatud summade summa. See väärtus on **saadaval** **ainult** siis, kui lühiajalise viitvõla meetodi välja väärtuseks on lehel Tulu ja kulu viitvõlgade parameetrid seatud väärtusele Pole või kui lühiajaline summa on **suurem** kui 0 (null).</li><li>**Lühiajaline** – lühiajaliste edasilükatud summade summa. See väärtus on **saadaval** **ainult** siis, kui lühiajalise viitvõla meetodi välja väärtuseks on lehel Tulu ja kulu viitvõlgade parameetrid seatud väärtusele Pole või kui lühiajaline summa on **suurem** kui 0 (null).</li><li>**Tundmatu – tuvastamata** summade summa kõigi ridade kohta.</li><li>**Jäära –** kõigi ridade väliselt sisestatud summade summa.</li><li>**Tuvastatud** – kõigi ridade tuvastatud summade summa.</li><li>**Väliselt sisestatud ja tuvastatud** – kõigi ridade väliselt sisestatud ja tuvastatud summade summa.</li><li>**kogusumma** – kõigi ridade summade summa.</li></ul> |
| **Graafiku read** | |
| Rida | Rea seerianumber. |
| Edasilükkamise alguskuupäev | Viitvõlagraafiku alguskuupäev. |
| Edasilükkamise lõpukuupäev | Viitvõlagraafiku lõppkuupäev. |
| Summa | Viitvõla summa. |
| Väliselt sisestatud | Väärtus, mis näitab, kas rida on väliselt sisestatud. |
| Kajastatud | Väärtus, mis näitab, kas rida on tuvastatud. |
| Töölehe partiinumber | Partii number, mille järgi summa tuvastati. |
| Sündmuse kirjeldus | Sündmuse kirjeldus. See väli on saadaval ainult sündmusepõhiste viitvõlagraafikute puhul. |
| **Krediidi korrigeerimised** | |
| Arve | <p>Arve number.</p><p>Väärtus näitab kreeditarve korrigeerimise arvet, mida on juba viitvõlagraafikule rakendatud.</p> |
| Rakendatud summa | Kreediti korrigeerimise summa, mis on viitvõlagraafikule juba rakendatud. |
| Rakendamise kuupäev | Kreediti korrigeerimise rakendamise kuupäev. |
| **Korrigeerimine** | Korrigeerimisväärtused kuvatakse ainult siis, kui viitvõlagraafiku jaoks on töödeldud krediiditeatis. Kui kreeditarvet ei töödeldud, on need väärtused peidetud. |
| Korrigeerimissumma | Korrigeerimise kogusumma, mis on arvutatud *algsummana* – graafiku *summa*. |
| Algne lõppkuupäev | Viitvõlagraafiku algne lõppkuupäev. |
| Algne graafiku summa | Algse viitvõlagraafiku kogusumma. |
