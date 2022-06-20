---
title: Viitvõlakanded kordustellimuse arvelduses
description: See artikkel kirjeldab erinevaid kandeid, mida saab kasutada viitvõlakannetes tulu ja kulu viitvõlgade osana kordustellimuse arvelduses.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c3862f1a250bf8e56303975b5c6a3560cd84c1e7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872582"
---
# <a name="deferral-default-transactions"></a>Edasilükkamise vaiketehingud

Selles artiklis kirjeldatakse kandeid, mis lubavad tulu- ja kulu viitvõlgu. Viitvõlgade graafikud põhinevad alati algsel dokumendil või arveldusgraafikul ja sõltuvad sellest. Viitvõlagraafikud luuakse vaikesätete alusel ja neid ei saa eraldi sisestada ega luua.

## <a name="sales-order-transaction-deferral"></a>Müügitellimuse kande viitvõlg

Kasutage lehte **Viitvõlad** või **Kreeditarve loomine**, et sisestada või redigeerida müügitellimuse rea viitvõla parameetreid.

> [!NOTE]
> Kui müügitellimus luuakse arveldusgraafikust, on **·** **kõik** viitvõlgade või kreeditarve loomise lehe väärtused kirjutuskaitstud ja viitvõla parameetreid ei saa redigeerida. Väärtuste redigeerimiseks kasutage lehte **Muuda ajakava**.

### <a name="edit-deferral-options"></a>Viitvõla suvandite redigeerimine

Rea viitvõla valikute redigeerimiseks järgige neid samme.

1. Looge müügitellimuse kanne.
2. Valige rida ja seejärel **viitvõlad**.
3. Leheküljel Kande **viitvõlg** peab edasilükatud **suvand** olema seatud väärtusele **Jah**. Redigeerige muid vajaminevad väljad.
4. Viitvõlagraafiku eelvaateks valige **eelvaade**.
5. Kui olete kande viitvõlga mis tahes muudatusi teinud, valige **OK** ja minge tagasi kandelehele.
6. Kinnitage ja sisestage kanne.

Pärast kande sisestamist avage leht Kõik **viitvõlagraafikud**, et vaadata viitvõlagraafikut.

### <a name="create-a-credit-note"></a>Kreeditarve loomine

Kreeditarve loomiseks toimige järgmiselt.

1. Looge müügitellimuse kanne.
2. **Jaotises Müügitellimuse read** valige kaup, mille jaoks soovite luua kreeditarve.
3. Valige **müügitellimuse rida Uus** \> **ja** seejärel **kreeditarve.**
4. Valige **viitvõlad**.
5. **Seadke müügitellimuse kande viitvõla lehel** kaubale **suvand Kohanda** olemasolevat graafikut **väärtusele** Jah.
6. Valige väljal **Korrigeeritud** graafik viitvõlagraafik, millele soovite kreeditarvet rakendada.
7. Värskendage **vajaduse korral ümberarvutamiskuupäeva** **ja** lõppkuupäeva välju.
8. Valige nupp **OK**.
9. Lõpetage müügitellimuse kande sisestamine.

### <a name="purchase-orders-and-purchase-invoices"></a>Ostutellimused ja ostuarved

Kui soovite ostutellimuse puhul kasutada viitvõla funktsiooni, looge esmalt arve. Seejärel kasutage lehte **Ootel hankija arved**, et redigeerida või lisada viitvõla kaupu. Viitvõlgu ei saa otse ostutellimusele redigeerida ega lisada.

1. Kasutage hankija **arve sisestamiseks lehte** Ootel hankija arved.

    Rea sisestamisel määratakse teie valitud kauba või hankekategooria viitvõlg automaatselt. See viitvõlg põhineb viitvõla seadistusel viitvõla **vaikesätete** lehel. Viitvõlgu saab jaotuse tasemel redigeerida või lisada.

3. Ostureal valige suvand Finantside **jaotamissummad \>**.
4. Valige iga jaotussumma jaoks **viitvõlad**. Kui arve on sisestatud, luuakse viitvõlagraafik iga jaotuse kohta, mille jaoks viitvõlg on seatud.

### <a name="tax"></a>Maks

Mõnel juhul võib maksusumma olla täielikult või osaliselt taastamatu. Kui viitvõlgades rea maksusumma sisaldab taastamatut summat, kaasatakse tagastamatu maksusumma viitvõlgades graafiku summasse arve sisestamisel.

### <a name="variance"></a>Hälve

Kui hankija arve rea summa erineb ostutellimuse rea summast, luuakse hälbe jaotused. Kui rida edasi lükatakse, seadistatakse nende jaotuste pearaamatukonto viitvõlakontole ja summad kaasatakse arve sisestamisel viitvõlagraafiku summasse. Nende jaotuste nimeks on **Hinnahälve** ja **Kulu hälve**.

### <a name="general-journals-and-invoice-journals"></a>Üldised töölehed ja arve töölehed

Kasutage lehte **Viitvõlad** töölehe kanderea viitvõlaparameetrite sisestamiseks. Samuti saate rea viitvõlgade viitvõlagraafiku eelvaadet vaadata. Rea sisestamisel määratakse viitvõlg automaatselt **, võttes aluseks viitvõlakontode seadistuse viitvõla vaikelehel**. Iga rea viitvõla suvandeid saate käsitsi muuta. Kui töölehe kanne on sisestatud, luuakse viitvõla graafik.

#### <a name="post-and-transfer"></a>Sisesta ja kanna üle

Töölehekande sisestamiseks kasutage käsku Sisesta **ja kanna** üle. Viitvõlavalikud järgivad rida, mille suhtes kanne kehtib. Vigadeta kannete puhul luuakse viitvõlagraafik, kui see on edasi lükatud. Veaga kande puhul, mis kantakse üle, kantakse koos sellega üle kõik viitvõlavalikud.

#### <a name="tax"></a>Maks

Mõnel juhul võib maksusumma olla täielikult või osaliselt taastamatu. Kui viitvõlgades rea maksusumma sisaldab taastamatut summat, kaasatakse tagastamatu maksusumma viitvõlgades graafiku summasse arve sisestamisel.

## <a name="free-text-invoice-transaction-deferral"></a>Vabas vormis arvekande viitvõlg

Kasutage lehekülge **Viitvõlad**, et sisestada vabas vormis arverea jaotuse viitvõlaparameetrid. Jaotuse sisestamisel määratakse viitvõlg automaatselt **, võttes aluseks viitvõla vaikelehe viitvõlasätted**.

## <a name="fields"></a>Väljad

Kande **viitvõla lehekülg** sisaldab järgmisi välju.

| Väli | Kirjeldus |
|-------|-------------|
| Edasi lükatud | <p>Saate määrata, kas rida on viitvõlg:</p><ul><li>**Jah** – rida on viitvõlg.</li><li>**Ei** – rida pole viitvõlg.</li></ul><p>Kui see suvand on seatud väärtusele **Jah**, **ei ole suvand** Olemasoleva graafiku kohandamine saadaval. Kaupade ja tasude puhul, mis on juba seadistatud edasilükkumiseks, on selle valiku väärtuseks seatud **Jah**. Kaupade ja tasude puhul, mis ei ole vaikimisi seadistatud viitkuludeks, määrake selle valiku väärtuseks **Jah**.</p> |
| Olemasoleva graafiku muutmine | <p>Saate määrata, kas rida korrigeeritakse olemasolevasse viitvõlagraafikusse:</p><ul><li>**Jah** – uus müügirida on olemasoleva viitvõlagraafiku korrigeerimine. Sellisel juhul saate väljal Korrigeeritud graafik valida **viitvõlagraafiku**.</li><li>**Ei** – uus müügirida ei ole olemasoleva viitvõlagraafiku korrigeerimine.</li></ul><p>Kui see suvand on seatud väärtusele **Jah**, **pole edasilükatud** suvand saadaval.</p> |
| Muudetud graafik | <p>Valige viitvõlagraafik, mida rida korrigeeritakse. Seejärel uuendatakse kõik leheküljel olevad väärtused algse viitvõlagraafiku väärtustega. Neid väärtusi ei saa redigeerida.</p><p>See väli on saadaval ainult siis, kui suvand **Kohanda olemasolevat** graafikut on seatud väärtusele **Jah**.</p> |
| Ümberarvutamise kuupäev | <p>Määrake perioodi alguskuupäev, mille ülejäänud summa soovite ümber arvutada. Vaikekuupäev on järgmise tuvastamata perioodi kuupäev.</p><p>See väli on saadaval ainult siis, kui suvand **Kohanda olemasolevat** graafikut on seatud väärtusele **Jah**.</p> |
| Lõpukuupäev | <p>Sõltuvalt viitvõla tüübist võidakse või ei pruugita lõppkuupäeva uuendada:</p><ul><li>Lineaalse viitvõla puhul määrake graafiku uus lõppkuupäev. Viitvõlagraafiku olemasolev lõppkuupäev on vaikeväärtus.</li><li>Sündmusel põhineva viitvõla puhul määrake kreeditsündmuse rea lõppkuupäev. See kuupäev võib olla tühi.</li></ul><p>See väli on saadaval ainult siis, kui suvand **Kohanda olemasolevat** graafikut on seatud väärtusele **Jah**.</p> |
| Arveldusgraafiku number | <p>Arveldusgraafiku number.</p><p>See väli on saadaval ainult korduvate lepingu arveldusgraafikute jaoks.</p> |
| Edasilükkamise korrigeerimise meetod | <p>Edasilükatud korrigeerimismeetod. Väärtus vastab korduva lepingu arveldusgraafiku **hulgi-lõpetamise** töötlemise lehel olevale väärtusele.</p><p>See väli on saadaval ainult korduvate lepingu arveldusgraafikute jaoks.</p> |
| **Kontod - tulu** | |
| Edasilükkamise konto | <p>Viitvõlakonto, mis on müügitellimuse lehel kuvav **sisestuskonto**.</p><p>Kui rida ei edasi lükatud, on see väli tühi. Sel juhul on sisestuskonto vaikimisi tulukonto.</p> |
| Kajastamise konto | <p>Määratlege konto, mida kasutatakse viitvõla tuvastamisel. See konto peab erinema viitvõla kontost.</p><p>Kui algselt **on** valiku Edasi lükatud väärtuseks **seatud** Jah, kopeeritakse viitvõlakontol kasutatavad dimensiooniväärtused tuvastamise kontole. Kui viitvõlakonto dimensioon ei eksisteeri tuvastamise konto jaoks, siis seda ignoreeritakse.</p> |
| Esialgse kajastamise konto | <p>Valige algse tulu tuvastamise konto. Vaikeväärtus on pärit viitvõlgade **vaikelehelt**.</p><p>See väli on saadaval ainult siis **, kui viitvõla** **sisestusmeetodi** välja väärtuseks on **lehel Tulu ja kulu viitvõlgade parameetrid seatud väärtusele Tulu ja** kulu.</p> |
| Vastaskonto kajastamine | <p>Valige tulu tuvastamise konto. Vaikeväärtus on pärit viitvõlgade **vaikelehelt**.</p><p>See väli on saadaval ainult siis **, kui viitvõla** **sisestusmeetodi** välja väärtuseks on **lehel Tulu ja kulu viitvõlgade parameetrid seatud väärtusele Tulu ja** kulu.</p> |
| **Kontod - Allahindlus** | See jaotis kuvatakse ainult edasilükatud kaupade puhul. See on edasilükatud tasude jaoks peidetud. |
| Edasilükkamise konto | <p>Määrake allahindluse viitvõla konto number. Vaikeväärtus on pärit viitvõlgade **vaikelehelt**.</p><p>See väli on **saadaval** **ainult** siis, kui suvand Allahindluse viitvõlg on **lehel Tulu ja kulu viitvõlgade parameetrites** seatud eraldi allahindluse graafikuks ja reale rakendatakse allahindlus.</p> |
| Kajastamise konto | <p>Määrake allahindluse tuvastamise konto number. Vaikeväärtus on pärit viitvõlgade **vaikelehelt**.</p><p>See väli on **saadaval** **ainult** siis, kui suvand Allahindluse viitvõlg on **lehel Tulu ja kulu viitvõlgade parameetrites** seatud eraldi allahindluse graafikuks ja reale rakendatakse allahindlus.</p> |
| Esialgse kajastamise konto | <p>Valige konto allahindluse esmaseks tuvastamiseks. Vaikeväärtus on pärit viitvõlgade **vaikelehelt**.</p><p>See väli on saadaval ainult **siis** **·**, kui viitvõla sisestusmeetodi välja väärtuseks on **lehel** Tulu ja kulu viitvõlgade parameetrid seatud väärtusele Tulu ja kulu ning rea puhul rakendatakse allahindlust.</p> |
| Vastaskonto kajastamine | <p>Valige tulu tuvastamise konto. Vaikeväärtus on pärit viitvõlgade **vaikelehelt**.</p><p>See väli on saadaval ainult **siis** **·**, kui viitvõla sisestusmeetodi välja väärtuseks on **lehel** Tulu ja kulu viitvõlgade parameetrid seatud väärtusele Tulu ja kulu ning rea puhul rakendatakse allahindlust.</p> |
| **Kontod - tarbimine** | See jaotis kuvatakse ainult edasilükatud kaupade puhul. See on edasilükatud tasude jaoks peidetud. |
| Edasilükkamise konto | <p>Määrake tarbimise viitvõla konto number.</p><p>Standardtoodete puhul luuakse kaks viitvõlagraafikut:</p><ul><li>**Standardmüük** – tulugraafik, mille kreeditsaldo on. Sellisel juhul valige tarbimise viitvõlakonto.</li><li>**Tarbimine** – deebetsaldoga tarbimine \[(müüdud kaupade omahind\]) kulugraafik. Sel juhul valige tarbimise tuvastamise konto.</li></ul><p>Arve sisestamisel sisestatakse tarbimissumma määratud tarbimise viitvõla kontole. Need väljad pole teenuseüksuste puhul saadaval.</p> |
| Kajastamise konto | Määrake tarbimise tuvastamise konto number. |
| Esialgse kajastamise konto | <p>Määrake algse tarbimise tuvastamise summa konto. Vaikeväärtus on pärit viitvõlgade **vaikelehelt**.</p><p>See väli on saadaval ainult siis **, kui viitvõla** **sisestusmeetodi** välja väärtuseks on **lehel Tulu ja kulu viitvõlgade parameetrid seatud väärtusele Tulu ja** kulu.</p> |
| Vastaskonto kajastamine | <p>Määrake tarbimise tuvastamise vastaskonto. Vaikeväärtus on pärit viitvõlgade **vaikelehelt**.</p><p>See väli on saadaval ainult siis **, kui viitvõla** **sisestusmeetodi** välja väärtuseks on **lehel Tulu ja kulu viitvõlgade parameetrid seatud väärtusele Tulu ja** kulu.</p> |
| **Graafik** | |
| Graafiku tüüp | <p>Valige viitvõlagraafiku tüüp: lineaalne **(vaikimisi**) või **sündmusepõhine**.</p><p>Lehel kuvatavad suvandid põhinevad teie valitud viitvõlagraafiku tüübil.</p><p>Kui kanderea viitvõla vaikelehel on **vaikemall** määratud, põhineb viitvõlagraafiku tüüp valitud malli tüübil.</p> |
| **Graafik - Line line** | |
| Eelnevate perioodide konsolideerimine | <p>Määrake, kas soovite konsolideerida viitvõlagraafiku ridu varasemateks perioodideks:</p><ul><li>**Jah** – konsolideerige viitvõlagraafiku read varasemateks perioodideks.</li><li>**Ei** – ärge konsolideerige viitvõlagraafiku ridu varasemateks perioodideks.</li></ul><p>Vaikeväärtus on pärit leheküljelt **Tulu ja kulu viitvõla parameetrid**.</p> |
| Võrdub perioodiga | <p>Määrake, kas päevade arv igas perioodis on võrdne või erineb periooditi:</p><ul><li>**Jah** – igal perioodil on sama päevade arv.</li><li>**Ei** – perioodidel pole sama päevade arv.</li></ul><p>Kui see valik on seatud valikule **Ei**, arvestatakse perioodi päevade arvu, kui arvutatakse viitvõlagraafiku summa iga perioodi kohta.</p><p>Vaikeväärtus on pärit leheküljelt **Tulu ja kulu viitvõla parameetrid**.</p> |
| Mallist graafik | <p>Määrake, kas viitvõla graafik luuakse malli või lõppkuupäeva põhjal:</p><ul><li>**Jah** – viitvõlagraafik luuakse malli alusel.</li><li>**Ei** – viitvõlagraafik luuakse lõppkuupäeva alusel.</li></ul> |
| Mall | Valige viitvõla mall. |
| Alistamise alguskuupäev | <p>Määrake, kas soovite alguskuupäeva alistada:</p><ul><li>**Jah** – alguskuupäeva alistamine väljale Alguskuupäev sisestamise **kuupäevaga**.</li><li>**Ei** – alguskuupäev on vaikimisi **viitvõla** alguskuupäeva reegel, mis rakendatakse arve sisestamise lehel määratud arve **kuupäevale**. Reegli saab seadistada lehel **Tulu ja kulu viitvõlgade parameetrid**.</li></ul> |
| Edasilükkamise alguskuupäev | Saate määrata viitvõla alguskuupäeva. Kande kuupäev on vaikeväärtus. |
| Edasilükkamise lõpukuupäev | <p>Viitvõla lõppkuupäev.</p><p>See kuupäev arvutatakse automaatselt viitvõlamalli põhjal. Kui ühtegi malli pole valitud, peate kuupäeva käsitsi sisestama.</p> |
| **Graafik - Sündmusepõhine** | |
| Mall | <p>Valige sündmusepõhine mall. Väli on valikuline.</p><p>Kui valite malli, kirjutavad malli väärtused üle kõik sündmusepõhised andmed ja sündmuse read.</p> |
| Eraldamise tüüp | <p>Valige sündmuse ridadele eraldamistüüp:</p><ul><li>**Muutuvsummad** – igale reale sisestatakse konkreetne eraldamissumma.</li><li>**võrdsed** summad – summa eraldatakse võrdselt igale reale;</li><li>**Protsent** – summa eraldatakse igale reale sisestatud protsendiväärtuse alusel.</li><li>**Valmimisprotsent** – igale reale sisestatakse kumulatiivne lõpetamisväärtus.</li><p>**Muutuv** kogus – igale reale sisestatakse konkreetne eraldiskogus.</li></ul><p>**Märkus:** kui soovite valida **valmimisprotsendi**, peavad kuupäevad olema kasvavas järjestuses.</p> |
| **Eraldi sündmuste loomine ühiku kohta** | |
| Kirjeldus | <p>Määrake, kas soovite eraldada sündmusi ühiku kohta:</p><ul><li>**Jah** : eraldage sündmuse read nii, et koguse kohta oleks üks rida.<p>Näiteks on kolm sündmuserida ja arve kogus on neli. Sellisel juhul on tulemuseks saadud viitvõlagraafikus 12 rida.</p></li><li>**Ei** – ärge eraldage sündmuse ridu.</li></ul> |
| Aegumise konto | <p>Valige konto, mida kasutatakse tuvastatud aegunud ridade jaoks. Konto saate valida pärast viitvõlagraafiku loomist.</p><p>Kui sündmusele on seatud aegumiskuupäev, läheb tunnustussumma tuvastamisprotsessi ajal tunnustuskonto asemel aegumiskontole.</p> |
| **Graafik - Sündmusepõhised read** | |
| Kirjeldus | Sündmuse kirjeldus. |
| Edasilükkamise lõpukuupäev | <p>Valige sündmuse lõppkuupäev.</p><p>**Märkus:** kui valite lõppkuupäeva, tühjendatakse **aegumiskuupäeva** väli. Te ei saa kasutada nii lõppkuupäeva kui ka aegumiskuupäeva.</p> |
| Aegumiskuupäev | <p>Valige sündmuse aegumiskuupäev.</p><p>**Märkus:** kui valite lõppkuupäeva, tühjendatakse **aegumiskuupäeva** väli. Te ei saa kasutada nii lõppkuupäeva kui ka aegumiskuupäeva.</p> |
| Kogus | <p>Määrake eraldamiskogus. Kõigi ridade vaikeväärtus on **0** (null). Koguse uuendamisel peab kõigi ridade kogus olema müügitellimuse reakauba jaoks määratud kogusega võrdne või sellest väiksem.</p><p>See väli on saadaval ainult siis, kui välja **Eraldamise tüüp** väärtuseks on määratud **Muutuv kogus**.</p><p>Kui müügitellimuse rea kauba kogust muudetakse nii, et see oleks väiksem kui algne kogus ja arve luuakse, luuakse vähem sündmusepõhiseid ridu. Kogu eraldatud kogus ei ületa algsel müügitellimusel või arveldusgraafikul määratud kogust.</p> |
| Eraldise % | <p>Määrake eraldise protsent. Kui välja **Eraldamise tüüp** väärtuseks on seatud **Protsent** **või Valmimise** protsent, saate protsendi käsitsi sisestada. Muul juhul arvutatakse see automaatselt.</p><p>Kui välja **Eraldamise tüüp** väärtuseks on seatud **Protsent**, peab protsentide kogusumma olema 100.</p> |
| Summa | <p>Määrake eraldamissumma. Kui eraldamise **tüübi välja** väärtuseks on seatud **Muutuv** summa **või valmimisprotsent**, saate summa käsitsi sisestada.</p><p>Kui välja **Eraldustüüp** väärtuseks on **seatud** Valmimisprotsent ja te sisestate siia summa, **arvutatakse automaatselt välja Valmimise** protsent väärtus.</p><p>Ümardamise tõttu ei pruugi arvutatud summa täpselt ühtida käsitsi sisestatud summaga. Kui vajate täpset summat, määrake välja Eraldamise **tüüp väärtuseks** Muutuvsummad **·**.</p> |
| Lõpetamise protsent | <p>Saate määrata valmimisastme. Väärtus peab olema vahemikus 0 (null) kuni 100.</p><p>See väli on saadaval ainult siis, kui välja **Eraldamise** tüüp väärtuseks on **seatud Valmimisprotsent**.</p> |
| Lõpetamise summa | <p>Viitvõlagraafiku kõikide ridade arvutatud kogusumma.</p><p>Kui välja **Eraldustüüp** väärtuseks on **seatud Valmimisprotsent**, saate summa käsitsi sisestada. Sel juhul arvutatakse välja Valmimisprotsent **väärtus** teie sisestatava summa alusel.</p><p>Ümardamise tõttu ei pruugi arvutatud summa täpselt ühtida käsitsi sisestatud summaga.</p><p>See väli on saadaval ainult siis, kui välja **Eraldamise** tüüp väärtuseks on **seatud Valmimisprotsent**.</p> |
| Ära tuvasta sisestamisel | <p>Saate määrata, kas rida tuvastatakse kande sisestamisel automaatselt:</p><ul><li>**Valitud** – rida tuvastatakse automaatselt kohe pärast kande sisestamist.</li><li>**Tühjendatud** – rida ei tuvastatud kohe pärast kande sisestamist.</li></ul> |
| Kajastamise konto | <p>Saate määrata sündmuse tunnustuskonto, kui konto erineb kogu viitvõlagraafiku puhul kasutatavast kontost.</p><p>Seda välja saate kasutada seoses valikuga Tuvasta **sisestamisel**.</p> |
