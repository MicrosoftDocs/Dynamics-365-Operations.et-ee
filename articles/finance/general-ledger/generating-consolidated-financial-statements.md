---
title: Konsolideeritud finantsaruannete loomine
description: See artikkel kirjeldab erinevaid stsenaariume, kus võite luua konsolideeritud finantsaruandeid.
author: aprilolson
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: c6a132b742414a3dab635634c7bb5ba0dbea527d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846795"
---
# <a name="generate-consolidated-financial-statements"></a>Konsolideeritud finantsaruannete loomine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab erinevaid stsenaariume, kus võite luua konsolideeritud finantsaruandeid.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Ühe- ja mitmetasemelised konsolideerimised juriidilistele isikutele
Kõige lihtsam meetod konsolideerimiseks finantsaruandlust kasutades on kasutada aruandluspuud andmete koondamiseks kõigis ettevõtetes, millel on samad kontoplaanid ja rahandusperioodid. Siin on aruandluspuuga konsolideerimise kõrgetasemelised etapid.

1. Looge readefinitsioon ja veenduge, et ridadele oleks kaasatud kõikide ettevõtete kõik asjakohased kontod.
2. Looge veerudefinitsioon, mis sisaldab kõiki veerge, mis on vajalikud loodava aruande jaoks.
3. Looge aruandluspuu, mis sisaldab aruandlussõlme iga ettevõtte kohta, mida kasutatud konsolideeritud aruannetes.

> [!TIP]
> Lisateavet rea- ja veerudefinitsioonide ning aruandluspuude loomise ja haldamise kohta vt teemast [Finantsaruande komponendid](../../fin-ops-core/dev-itpro/analytics/financial-report-components.md).

Järgmisel joonisel on näha, kuidas saate kasutada finantsaruandluses aruandluspuu definitsiooni iga konsolideeritava ettevõtte tuvastamiseks.

![Aruandluspuu definitsioon.](./media/reporting-tree-definition.png "Aruandluspuu definitsioon")

Nagu konsolideeritud aruandes järgmisel joonisel on näha, saate aruandluspuu kasutamisel koos aruande definitsooniga vaadata iga ettevõtet eraldi. Konsolideeritud summad on näha koondtasandil.

![Kkoondtasandi konsolideeritud summa.](./media/consolidate-amount-summary-level.png "Konsolideeritud summa koondtasand")

Saate ka luua mitmetasemelise aruandluspuu, mis hõlmab nii palju tasemeid, kui teil on vaja. Järgmisel joonisel on näha mitmetasemeline aruandluspuu definitsioon, millel on kokkuvõtted üleilmse piirkonna järgi.

![Mitmetasemeline aruandluspuu definitsioon kokkuvõtetega piirkonna järgi.](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Mitmetasemeline aruandluspuu definitsioon kokkuvõtetega piirkonna järgi")

Järgmisel joonisel on näha mitmetasemeline aruandluspuu definitsioon, millel on kokkuvõtted funktsiooni järgi.

![Mitmetasemeline aruandluspuu definitsioon kokkuvõtetega funktsiooni järgi.](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Mitmetasemeline aruandluspuu definitsioon kokkuvõtetega funktsiooni järgi")

### <a name="viewing-companies-side-by-side"></a>Ettevõtete vaatamine kõrvuti
Paljud kliendid eelistavad aruandeid, kus ettevõtted kuvatakse kõrvuti ja kus veerus on näha konsolideeritud kogusumma. Seda vormingut on lihtne saavutada pärast aruandluspuu loomist. Siin on kõrgetasemelised etapid ettevõtete kõrvuti vaatamiseks konsolideeritud finantsaruannetel.

1. Looge veerudefinitsioon, mis sisaldab veergu **Finantsdimensioon** iga ettevõtte kohta.
2. Kasutage välja **Aruandlusüksus** puu ja aruandlusüksuse valimiseks iga veeru jaoks.
3. Valikuline: lisage päised ja kogusumma veerud.

Järgmisel joonisel on näha veerudefinitsioon kõrvuti vormingus.

![Veeru definitsioon kõrvuti vormingus.](./media/column-definition-side-by-side-format.png "Veeru definitsioon kõrvuti vormingus")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Konsolideerimised, mis kasutavad juriidilistest isikutest loodud organisatsiooni struktuure
Organisatsiooni hierarhiad, mis sisaldavad dimensioone või juriidilisi isikuid, loovad dünaamiliselt aruandluspuu definitsioonid finantsaruandluses. Lihtne moodus konsolideerimiste sujuvamaks muutmiseks on lisada finantsaruandluses aruandele organisatsiooni hierarhia. Finantsaruandlus valib aruande kuupäeva järgi organisatsiooni hierarhia jõustumiskuupäeval või enne seda, nagu on näha järgmisel joonisel.

![Aruandluspuu definitsiooni dünaamiline loomine.](./media/dynamically-create-reporting-tree-definitions.png "Aruandluspuu definitsiooni dünaamiline loomine")

## <a name="consolidations-that-involve-eliminations"></a>Eemaldamisi sisaldavad konsolideerimised
Eemaldamiskanded on konsolideerimisprotsessi tavaline osa. Selles näites eemaldatakse konsolideerimise ajal viis kontot: 142600, 211400, 401420, 401180 ja 510820. Ettevõtted võivad oma ettevõtete vahelised kontod erinevalt seadistada. Näiteks mõni ettevõte määrab viimaseks numbriks 9, kui kontot kasutatakse ettevõtete vahelistes kannetes. Meetodist olenemata saab eemaldamise kuvada konsolideeritud finantsaruannetel, kui teate ettevõtete vahelisi kontosid.

Järgmisel joonisel on näha veerudefinitsioon konsolideeritud kasumiaruande jaoks. Iga ettevõtte jaoks määratakse kolm ettevõtete vahelist kasumi ja kahju kontot, kasutades dimensioonifiltrit. Veerud F, G ja H sisaldavad eemaldamiskontosid ainult USMF-, USRT- ja DEMF-ettevõtete jaoks. Need veerud on seadistatud nii, et neid **ei** prindita finantsaruandele.

![Veerudefinitsiooni konsolideeritud kasumiaruanne.](./media/column-definition-consolidated-income-statement.png "Veerudefinitsiooni konsolideeritud kasumiaruanne")

Kui aruanne luuakse, arvutatakse eemaldamiskontod veergudes F, G ja H ning need võetakse kokku veerus column I. Veerg J näitab konsolideeritud summasid. Need konsolideeritavad summad välistavad eemaldamised ettevõtetele USMF, USRT ja DEMF.

> [!TIP]
> Looge teine aruanne, kus on näha ainult eemaldamiskirjed, ja kasutage seda aruandegrupis, mis sisaldab teie konsolideeritud aruannet. Sedasi on teil olemas kogu vajalik teave kõikide vajalike töölehe sisestuste loomiseks.

Järgmisel joonisel on näha konsolideeritud aruanne.

![Konsolideeritud aruande kasumiaruanne.](./media/consolidated-report-income-statement.png "Konsolideeritud aruande kasumiaruanne")

Kui te kasutate kontosid, dimensioone või mõlemat, finantsaruandlus laseb teil filtreerida eemaldamiskirjeid, kasutades dimensiooni filtreerimise võimalusi.

## <a name="minority-interest"></a>Vähemusosalus
Ettevõttele võib kuuluda vaid protsent mõnest muust ettevõttest. Selles olukorras on konsolideeritud aruannet luues oluline luua see vaid selle protsendi kohta, mis ettevõttele kuulub. Finantsaruandluses on mitu võimalust vähemusosaluse kuvamiseks, olenevalt kasutaja eelistusest. Üks võimalus on kasutada aruandluspuu definitsioonis ümberarvestuse protsenti. Teine võimalus on kuvada vähemusosalus aruandes eraldi reana.

### <a name="using-the-reporting-tree-definition"></a>Aruandluspuu definitsiooni kasutamine
Sisestage aruandluspuu definitsioonis omandiõiguse protsent veergu **Ümberarvestuse %** (veerg H), nagu on näidatud järgmisel joonisel. Aruande loomisel kasutatakse seda protsenti konsolideeritud summa arvutamiseks. Selles näites kuulub Contosole ainult 80 protsenti ettevõttest Contoso Germany. Võite sisestada väärtuse **80** või **0,8** veergu **Ümberarvestuse %** ja 80 protsenti arvestatakse ümber konsolideeritud tasemele.

> [!NOTE]
> Saate seda omandiõiguse protsenti rakendada mis tahes aruandlusüksusele, mitte ainult ettevõtte tasemel. 

![Aruandluspuu definitsiooni protsendi kasutamine.](./media/Using-reporting-tree-definition-percentage.png "Aruandluspuu definitsiooni protsendi kasutamine")

Aruande loomisel kuvab Contoso Germany aruanne 100 protsenti müügisummast ning 80 protsenti summast eraldatakse ja arvestatakse ümber müügi konsolideeritud tasemele.

Kui teile kuulub ettevõttest vähem kui 1 protsent, võite valida märkeruudu **Luba alla 1% suurust ümberarvestust** vahekaardil **Lisasuvandid** lehel **Aruande sätted**, nagu on näha järgmisel joonisel. Sel juhul koheldakse aruandluspuu veeru **Ümberarvestuse %** väärtusi vähema kui 1 protsendina. Näiteks kui sisestate väärtuse **0,8**, arvestatakse konsolideeritud tasemele ümber 0,8 protsenti, mitte 80 protsenti. Teine võimalus sama tulemuse saavutamiseks on jätta märkeruut **Luba alla 1% suurust ümberarvestust** valimata ja sisestada väärtus **0,008** veergu **Ümberarvestuse %**.

![Aruandluse seadistussuvandid.](./media/reporting-setting-options.png "Aruandluse seadistussuvandid")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Omandiõiguse kuvamine eraldi reana konsolideeritud aruandel
Teine võimalus vähemusosaluse korral on kuvada 100 protsenti tütarettevõttest iga aruande rea kohta, aga arvata mittekontrolliv intress netotulust maha.

Järgmisel joonisel on näha, et lauset **IF THEN ELSE** ja veerupiirangut readefinitsioonis võib kasutada vähemusosaluse arvutamiseks finantsaruannetel.

![Omandiõiguse kuvamine eraldi reana konsolideeritud aruandel.](./media/Showing-ownership-separate-row-consolidated-report.png "Omandiõiguse kuvamine eraldi reana konsolideeritud aruandel")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Mitu juriidiliste isikute kontoplaani
Sageli on erinevatel juriidilistel isikutel erinevad kontoplaanid, aga siiski soovitakse luua konsolideeritud finantsaruandeid. Sel juhul saab finantsaruandlust kasutada andmete konsolideerimiseks, et saaksite luua konsolideeritud finantsaruandeid. Siin on konsolideerimise kõrgetasemelised etapid, kui juriidilistes isikutes on erinevad kontoplaanid.

1. Looge readefinitsioon, millel on mitu linki finantsdimensioonidele. Iga kontoplaani kohta peab olema üks link.
2. Kasutage aruandlusüksuse piirangut veerudefinitsioonis iga ettevõtte määramiseks vastavasse veergu.


Iga eraldi ettevõtte kontoplaani kohta saab readefinitsioonis igale reale lisada finantsdimensioonidele mitu linki. Järgmisel joonisel kasutab USMF-i ettevõte kontokogumit esimeses veerus **Link finantsdimensioonidele** (veerg J) ja DEMF-i ettevõte kasutab kontosid teises veerus **Link finantsdimensioonidele** (veerg K).

> [!TIP]
> Lisateavet lahtri **Link finantsdimensioonidele** kohta vt teemast Finantsdimensioonide lahtri lingi määratlemine.

![Kontode esimese lingi finantsdimensioonidele määramine.](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Kontode esimese lingi finantsdimensioonidele määramine")

Võite kasutada aruandluspuud määramaks, millist linki finantsdimensioonidele readefinitsioonis iga ettevõtte jaoks kasutatakse. Valige readefinitsioon veerus E ja seejärel valige sobiv realink veerus F, nagu on näidatud järgmisel joonisel.

![Kasutatud finantsdimensioonide lingi readefinitsioon.](./media/link-financial-dimensions-row-definition-used.png "Kasutatud finantsdimensioonide lingi readefinitsioon")

> [!TIP]
> Kui loote lingid finantsdimensioonidele, kasutage kirjeldust, et määrata ettevõtted, millele iga link rakendub. Sedasi saate aruandluspuud luues hõlpsamini valida õige ettevõtte. Veerudefinitsioonis laseb väli **Aruandlusüksus** piirata iga veergu aruandluspuu üksusele, nii et saate andmeid vaadata kõrvuti. Kui te ei märgi veeru jaoks konkreetset ettevõtet, kuvatakse konsolideeritud andmed kõikide ettevõtete kohta.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Erinevad rahanduskalendrid mitme juriidilise isiku jaoks
Erinevatel juriidilistel isikutel võivad olla erinevad rahanduskalendrid, aga siiski võib olla vajalik luua konsolideeritud finantsaruandeid. Kui juriidilistes isikutes on erinevad rahandusperioodid, on konsolideerimiseks kaks võimalust.

- Looge veerudefinitsioon ning kasutage perioodi ja aastat, et vastendada sobivaid perioode iga ettevõtte jaoks.
- Suvanditega **Sätted** \> **Muu** \> **Lisasuvandid** valige, kas kasutada konsolideerimiseks perioodi lõppkuupäeva või perioodi numbrit.

Kui loote veerudefinitsiooni mitmele ettevõttele, millel on erinevad rahandusperioodid, on oluline kaaluda, milline ettevõte määratakse aruande definitsioonis välja **Ettevõtte nimi**. Selle ettevõtte rahanduskalendrit kasutatakse aruande definitsioonis rahanduskalendri alusena. Näiteks järgmises tabelis on näha USMF-i ja INMF-i ettevõtete jaoks seadistatud rahandusperiood. Konsolideeritud aruannete jaoks soovite kasutada rahanduskalendrit, mida kasutab USMF. Veerus Vastendamine on näha vastav periood ja aasta iga ettevõtte kohta, kui aruanne luuakse kuupäeva 30. juuni 2018 kohta.

| Ettevõte   | Finantsaasta                                  | Vastendamine                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Finantsaasta, 1. juuli kuni 30. juuni          | Periood 12, rahandusaasta 2018 | 
| INMF      | Kalendriaasta, 1. jaanuar kuni 31. detsember | Periood 6, rahandusaasta 2018  |

Järgmisel joonisel on aruande definitsioonis välja **Ettevõtte nimi** määratud USMF-i ettevõte. Seega USMF-i ettevõtte rahanduskalendrit kasutatakse rahanduskalendri alusena. Selles näites luuakse aruanne kuupäevale 30. juuni 2018 ja USMF-i ettevõte kasutab baasperioodi BASE, mis on aruande definitsioonis määratud perioodina 12. INMF-i ettevõte kasutab baasperioodi BASE–6, mis on periood 6. Mõlemad veerud hõlmavad andmeid 2018. aasta juuni kohta.

![Aruande baasperiood.](./media/report-base-period.png "Aruande baasperiood")

Järgmisel joonisel on näha aruande definitsiooni suvandid, millega saate valida, kas konsolideerimiseks kasutatakse perioodi numbrit või perioodi lõppkuupäeva.

![Aruande definitsiooni perioodi numbri suvandid.](./media/options-report-definition-period-number.png "Aruande definitsiooni perioodi numbri suvandid")

## <a name="business-unit-consolidations"></a>Äriüksuse konsolideerimised
See artikkel on keskendub aruandluspuu definitsioonide ja organisatsiooni hierarhiate kasutamisele finantsaruandluses konsolideerimise eesmärkidel. Võite aruandluspuud kasutada ka äriüksuse konsolideerimisaruannete loomiseks, näiteks aruannete loomiseks üleilmsete müükide või tootmise kohta. Need aruanded on üldine nõue. Nende loomiseks valige ettevõte ja dimensioon iga üksuse jaoks, mille põhjal soovite konsolideerida. Näiteks järgmisel joonisel on äriüksuse ümberarvestus saavutatud, korrates iga ettevõtet veerus **Ettevõte** (veerg A) ja tuvastades osakonna dimensiooni väärtuste grupi ettevõtte kohta veerus **Dimensioonid** (veerg D).

![Äriüksuse konsolideerimisaruanded.](./media/business-unit-consolidation-reports.png "Äriüksuse konsolideerimisaruanded")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Konsolideerimised, mis hõlmavad mitut aruandlusvaluutat
Finantsaruandlus pakub suuremat paindlikkust tegelike, eelarve, eelarve juhtimise ja eelarve plaanimise andmete vaatamisel mitmes valuutas. Tähtsamaid seadistusandmeid kasutades ei pea te finantsaruandluses tegema täiendavaid seadistusi, et vaadata mis tahes aruannet, mis tahes valuutas, mis tahes ajal ja mis tahes kasutaja kohta.

### <a name="prerequisites"></a>Eeltingimused
Teisendatud saldode õigesti arvutamiseks on finantsaruandlusel vaja, et kategooria **Jaotamata kasumi konto** oleks määratud jaotamata kasumi kontole loendis **Põhikonto**. Finantsaruandlus ei toeta sisestamist jaotamata kasumi kontole. Kui kanded sisestatakse jaotamata kasumi kontole, ei arvutata teisendatud saldosid õigesti. Soovitame kasutajatel seadistada täiendava jaotamata kasumi konto, et sisestada korrektsioone jaotamata kasumi kontole.

Põhikontol tuleb väljad **Finantsaruandluse vahetuskursi tüüp** ja **Valuuta teisendustüüp** kiirkaardil **Finantsaruandlus** seadistada iga konto jaoks, nagu on näha järgmisel joonisel. Seda saab teha kontode kaupa või kasutada kontomalle, et muudatusi hõlpsasti tagasi võtta.

- Valige väljas **Finantsaruandluse vahetuskursi tüüp** vahetuskursi tüüp, mis sisaldab kontole rakendatavaid valuutasid ja vahetuskursse. Seda valuutade ja vahetuskursside tabelit rakendatakse finantsaruandluses tegelikele andmetele.
- Valige väljas **Valuutateisenduse tüüp** meetod, mida kasutatakse konto vahetuskursi arvutamiseks. Seda valuuta meetodit kasutatakse finantsaruandluses nii tegelike kui ka eelarve andmete jaoks.

![Finantsaruandluse põhikontod.](./media/Financial-reporting-main-accounts.png "Finantsaruandluse põhikontod")

Eelarve, eelarve juhtimise ja eelarve plaanimise andmete jaoks määratakse vahetuskursi tüüp lehel **Pearaamat**. Seda tabelit kasutatakse vahetuskursside võtmiseks, ja kasutatakse kontole määratud valuuta teisenduse tüüpi.

### <a name="currency-translation-methods"></a>Valuuta teisendusmeetodid
Vahetuskursside arvutamiseks finantsaruandluses on neli võimalust:

- **Kaalutud keskmine** – seda meetodit kasutatakse kõige sagedamini kasumi ja kahjumi kontode jaoks. See kasutab järgmist valemit:

    (vahetuskurss × kehtivuspäevade arv) ÷ perioodi päevade arv

- **Keskmine** – see meetod on kasumi ja kahjumi kontode alternatiivmeetod. See kasutab järgmist valemit:

    Vahetuskursid kokku ÷ vahetuskursside arv

- **Praegune** – seda meetodit kasutatakse kõige sagedamini bilansikontode jaoks. Kasutatav vahetuskurss on kurss aruande kuupäeval või enne seda või finantsaruandluse veerus.
- **Kande kuupäev** – seda meetodit kasutatakse põhivara kontode jaoks. Kasutatav vahetuskurss on kurss päeval, millal vara soetati. Kui selle kuupäeva kohta pole kurssi sisestatud, kasutatakse vara soetamiskuupäevale lähimal kuupäeval sisestatud kurssi.

### <a name="report-designer-options-for-currency-translation"></a>Aruande koostaja suvandid valuuta teisendamiseks
Finantsaruandluses saab iga aruannet kuvada mis tahes arvus aruandlusvaluutades. Järgmised väljad aruande definitsioonil toetavad seda võimalust.

- Jaotis **Valuutateave** lehel **Aruande definitsioon**. Selles jaotises on näha valuuta, milles kuvatakse väärtused aruande loomisel.
- Uus märkeruut **Kaasa kõik aruandlusvaluutad**. Kui see märkeruut on valitud, lisatakse aruande järjekorda aruanne iga aruandlusvaluuta kohta pärast seda, kui on loodud aruanne, mis kasutab ettevõtte ametlikku valuutat. Kui märkeruut on tühi, saate siiski valida aruandlusvaluuta Web Viewerist. Sellisel juhul töödeldakse aruandlusvaluutat ainult siis, kui selle valite.

Aruande definitsiooni suvanditega saate hõlpsasti teisendada aruannet kõikidesse aruandlusvaluutadesse. Seega võib olla võimalik eemaldada aruannete topeltdefinitsioone, mis erinevad ainult kasutatud valuuta poolest. Kui teil on vaja aruannet, millel kuvatakse mitu valuutat kõrvuti, võite kasutada edasi välja **Valuutakuva** lehel **Veerudefinitsioon**, et teisendada ainult see aruande veerg muusse aruandlusvaluutasse.

### <a name="currency-translation-adjustment"></a>Valuuta teisendamise korrigeerimine
Valuuta teisendamise korrigeerimine (CTA) on erinevus bilansikontode arvutamiseks kasutatud kursside ja kasumiaruande kontode jaoks kasutatud kursi vahel. Erinevus viib bilansi tasakaalust välja. Saate kasutada finantsaruandlust CTA arvutamiseks kahel moel.

- Kasutage readefinitsioonis lehte **Ümardusparandused**, nagu on näha järgmisel joonisel.

    ![Valuuta teisendamise korrigeerimise ümardusparandused.](./media/Currency-translation-adjustment-rounding-adjustments.png "Valuuta teisendamise korrigeerimise ümardusparandused")

    Kui määrate rea, mis peaks kuvama ümardusparanduse (CTA), koguvarade rea, kohustuste ja omakapitali kogusumma rea ning teile sobiva läve, arvutab finantsaruandlus erinevuse ja paneb selle sobivasse ritta. Luuakse rida nimega **Ümardusparandus** ja see kuvatakse süvitsi minemisel, nagu on näha järgmisel joonisel.

    ![Ümardusparandus süvitsi.](./media/rounding-adjustment-drill-down.png "Ümardusparandus süvitsi")

- Pange kõik kontod vahemikku varadest kuludeni. Nagu järgmisel joonisel näha, on erinevus sama summa kui ümardusparandus (CTA). Seega võite seda kasutada tšeki kogusummana, et veenduda, ega ümardusparanduse leht ei hõlma vahele jäänud konto saldosid.

    ![Ümardusparandus tšekist.](./media/rounding-adjustment-form-check.png "Ümardusparandus tšekist")

### <a name="balance-calculation-approach"></a>Saldo arvutamise lähenemine
Valuutade kasutamisel õigesti teisendatud summade saamiseks kasutab finantsaruandlus saldode jaoks järgmisi arvutusmeetodeid:

- **Kaalutud keskmine ja keskmine** – iga periood arvutatakse kaalutud keskmise põhjal ja summeeritakse veergudesse nagu kvartaalne ja aasta praeguse kuupäevani.
- **Ajalooline** – iga konto, mis kasutab ajaloolise teisendamise meetodid, läheb alati tagasi kande kuupäevani. Kui kandega on seotud soetamiskuupäev, kasutatakse seda kuupäeva vahetuskursi saamiseks. Seejärel iga periood summeeritakse ja salvestatakse, et aidata parandada arvutusaega.
- **Praegune** – arvutatud ja kogusummade veerud (kvartaalne ja aasta praeguse kuupäevani) arvutatakse hetkekursi järgi, mis on määratud veerus või aruandes. Näiteks veerg **1. kvartal** kasutab 31. märtsi kurssi, kui kasutatakse kalendriaastat.

## <a name="additional-resources"></a>Lisaressursid

Lisateavet konsolideerimise ja valuutateisenduste kohta vt selle artikli emaüksusest Finantskonsolideerumine [ja valuuta teisendusülevaade](./financial-consolidations-currency-translation.md).

Lisateavet konsolideerimise üksikasjade sisestamise kohta võrgus vt teemast [Finantskonsolideerimised võrgus](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
