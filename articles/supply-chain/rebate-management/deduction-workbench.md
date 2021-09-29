---
title: Mahaarvamise töölaual mahaarvamiste haldamine
description: Selles teemas kirjeldatakse mahaarvamise töölaua kasutamist mahaarvamisi sisaldavate kliendimaksete töötlemiseks.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: bf98529176fbed368708ea925f542a70f2936037
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500398"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Mahaarvamise töölaual mahaarvamiste haldamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse mahaarvamise töölaua kasutamist mahaarvamisi sisaldavate kliendimaksete töötlemiseks.

Klient, kellel on saada tagasimakse, võib otsustada tagasimakse väljamaksmist mitte oodata. Selle asemel võib klient saata makse, mis sisaldab mahaarvamist tagasimakse summa ulatuses. Seda tüüpi kannete käsitlemiseks saate kasutada mahaarvamise töölauda, et vastendada mahaarvamisi kreeditkannete avamiseks, mahaarvamiste tükeldamiseks, mahaarvamistest keeldumiseks ja nende mahakandmiseks.

> [!NOTE]
> Mahaarvamise töölaud on olnud pikk aeg Microsoft Dynamics 365 Supply Chain Management müügi ja turunduse funktsiooni osa. Nüüd on seda siiski täiustatud, nii et see töötab ka uuema **tagasimaksehalduse** mooduliga. See teema kirjeldab, kuidas kasutada mahaarvamise töölaual nii vanemaid funktsioone kui ka tagasimaksehalduse funktsioone. Kui te pole siiski [oma süsteemi jaoks **tagasimakse halduse** moodulit sisse lülitanud](rebate-management-enable.md), ei ole mõned siin kirjeldatud funktsioonid teile saadaval.

## <a name="prerequisites"></a>Eeltingimused

### <a name="set-up-the-old-deduction-management-system"></a>Saate häälestada vana mahaarvamiste haldussüsteemi

Võite kasutada mahaarvamise töölaua koos Supply Chain Management rakenduse vanade mahaarvamishalduse võimalustega, isegi kui te ei kasuta **Tagasimaksehaldus** moodulit. Peate siiski oma süsteemi selles jaotises kirjeldatud viisil ette valmistama.

Enne mahaarvamiste töölaua kasutamist peate sooritama teemas [Tagasihalduse seadistamine](/dynamicsax-2012/appuser-itpro/set-up-deduction-management) kirjeldatud seadistamistoimingud. Peale selle peab teil olema kliendile seadistatud mõnd tüüpi tagasimakselepe: kas kliendi tagasimakse, mida kirjeldatakse teemas [Kliendi tagasimaksete seadistamine ja haldamine](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates), või kaubandushüvitise tagasimakse.

Kui rakendate mahaarvamist kliendi tagasimaksele, peate lõpetama järgmised punktid.

- [Seadistage oma kliendi tagasimaksed](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- Kinnitage ja töödelge tagasimakse enne kui saate mahaarvamise töölauda kasutada.

Kui rakendate mahaarvamist kaubandustoetuse tagasimaksele, peate lõpetama järgmised punktid.

- Seadistage tagasimakse.
- Rakendage tagasimakse.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Moodulite Müügireskontro ja mahaarvamised

Süsteem salvestab kõik mahaarvamissündmused nõuete päevikusse. Seetõttu peab teie süsteem sisaldama päevikut, mida saab sel eesmärgil kasutada. Kui teil ei ole veel nõude töölehte, seadistage see nüüd. See päevik on vajalik mahaarvamiste tegemiseks otse mahaarvamise töölauale, kliendi arveldusele või kliendilehele.

Mahaarvamiste jaoks uue nõudepäeviku seadistamiseks toimige järgmiselt.

1. Avage **Pearaamat \> Töölehe seadistamine \> Töölehtede nimed**.
1. Valige **Uus** ja määrake uuele töölehe nimele järgmised väljad.

    - **Nimi**- siia saate sisestada nõude töölehe kordumatu nime.
    - **Kirjeldus** – sisestage uue töölehe kirjeldus.
    - **Töölehe tüüp** - valige *Päevane*.
    - **Kandeseeria** – määrake olemasolev numbriseeria. Teise võimalusena looge uus numbrijada, millel on ettevõtte ulatus, ja määrake see uuele töölehe nimele.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
1. Seadke vahekaardi **Mahaarvamised** kiirkaardil **Üldine** **Nõude töölehe nime** väljale äsja loodud töölehe nimi.
1. Seadistage kiirkaardil **Tagastustellimus** järgmised väljad.

    - **Loo tagastustellimus** – märkige see valik, et määrata, mida süsteem peaks kogusepõhise nõude heakskiidul tegema:

        - *Jah* - loo tagastustellimus.
        - *Ei* – loo negatiivne müügitellimus.

    - **Loomine ilma seotud arveta** – valige väärtus, et määrata, mida süsteem peaks tegema, kui kogusepõhine nõue kinnitatakse, kuid arvet pole lisatud:

        - *Kinnita* - tagastustellimuse loomine.
        - *Hoiatus* - tagastustellimus luuakse, kuid kuvatakse järgmine hoiatusteade: "Nõue pole arvega seotud."
        - *Tõrge* - tagastustellimust ei looda ja kuvatakse järgmine tõrketeade: "Nõue pole arvega seotud." Uuendus on tühistatud."

    - **Loo tagastustellimus enne mahaarvamise kinnitamist** – määrake selleks valikuks *Jah*, kui tagastustellimusi saab luua enne nõude kinnitamist. See säte kehtib ainult kogusepõhistele nõuetele, mille puhul suvand **Loo tagastustellimus** on seatud väärtusele *Jah*.

### <a name="configure-general-ledger-parameters"></a>Pearaamatu parameetrite konfigureerimine

Kui süsteem loob nõudepäeviku uueks mahaarvamiseks, loob see ka kaks uut klienditehingut: ühe nõude summa tasaarvestamiseks algse arvega ja teise, et registreerida kliendi võlg nõude summale (kuna nõue ei ole pole veel heaks kiidetud). Seetõttu peate seadistama oma süsteemi nii, et ühel kandel võib olla mitu kliendirida.

Ühele kandele mitme kliendirea lubamiseks järgige neid samme.

1. Avage **Pearaamat \> Pearaamatu seadistamine \> Pearaamatu parameetrid**.
1. Määrake kiirkaardi **Üldine** vahekaardil **Pearaamat** suvandi **Luba mitu kannet ühe kande sees** suvandile *Jah*.
1. Kui saate hoiatusteate, valige muudatuse aktsepteerimiseks suvand **Sule**.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Mahaarvamise põhjuste loomine

Süsteem nõuab, et kasutajad täpsustavad põhjuse igale mahaarvamisele, mille nad sisestavad otse mahaarvamise töölauale, kliendi tasaarvelduse või kliendi lehele. See põhjus määratleb, kuidas mahaarvamist kinnitatakse.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste põhjused**.
1. Valige **Uus**, et lisada ruudustikku rida, ja seejärel määrake järgmised väljad.

    - **Nõude põhjus**- sisestage põhjuse unikaalne nimi.
    - **Kirjeldus** : sisestage põhjuse kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.
    - **Nõude alus** – valige nõude põhjus:

        - *Hinnapõhine* – saate kinnitamisel luua vabas vormis krediidi.
        - *Kogusel põhinev* – looge kinnitamisel negatiivne müügi- või tagastustellimus.

    - **Tagastuspõhjuse kood** – valige tagastuspõhjuse kood, mida rakendada tagastustellimuse **tagastuspõhjuse koodi** väärtusena.
    - **Tüüp** – valige mahaarvamise tüüp. Valitud tüübi **mahaarvamise vastaskonto** väärtust kasutatakse mahaarvamise või nõude loomisel **mahaarvamise vastaskonto** välja häälestamiseks. Mahaarvamise tüübid määratakse lehel **Mahaarvamise tüübid** (**Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamise tüübid**).
    - **Nõude sisestuskonto** – see väli on saadaval ainult siis, kui **nõude aluse** välja väärtuseks on seatud *Hinnapõhine*. Kui hinnapõhine nõue kinnitatakse, määrab süsteem siin valitud pearaamatukonto vabas vormis kreeditarve **põhikonto** väärtuseks.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Saate häälestada kinnitatud mahaarvamiste tasakaalustamiseks perioodilist ülesannet

Mahaarvamiste jaoks, mis luuakse mahaarvamise töölaual, kliendiarveldusel või kliendilehel käsu **Uus mahaarvamine** abil, saate seadistada *Arveldatud mahaarvamiste lahendamise* perioodilise ülesande, et automaatselt sobitada mahaarvamised ja krediidid, millel on vastav **Mahaarvamise ID** väärtused ja summad.

Selle ülesande plaanimiseks minge **Müükide turundus \> Perioodilised ülesanded \> Tasakaalustage kinnitatud mahaarvamised** ja seadistage suvandid, filtrid ja plaan, samuti nagu muude perioodiliste ülesannete tüüpide puhul.

> [!NOTE]
> Kui **Müügireskontro parameetrite** lehe (**Müügireskontro \> Seadistus \> Müügireskontro parameetrid**) vahekaardil **Tasakaalustus** on suvand **Automaatne tasakaalustamine** seatud väärtusele *Jah*, siis ei saa kinnitatud *Mahaarvamiste tasakaalustamine* perioodilises ülesandes midagi teha, sest kreedit tasakaalustatakse automaatselt.

## <a name="create-a-deduction"></a>Mahaarvamise loomine

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Looge mahaarvamispäeviku kirje kliendimaksepäeviku abil

Mahaarvamise töölehe sisestuse loomiseks toimige järgmiselt.

1. Avage **Müügireskontro \> Maksed \> Kliendi makse tööleht**.
1. Rea lisamiseks tabelisse klõpsake valikut **Uus**.
1. Valige uue rea nimi väljal **Nimi** töölehe nimi.
1. Toimingupaanil valige nupp **Alused**.
1. Saate sisestada kuupäeva, ettevõttekonto ja kliendikonto numbri.
1. Valige väljal **Arve**, millega mahaarvamine on seotud.
1. Sisestage väljale **Kreedit** kliendi makstud summa.
1. Valige **OK** kinnitamaks, et summa on väiksem kui märgitud kande kogusumma.
1. Valige vastaskonto tüüp ja vastaskonto.
1. Tööriistaribal ruudustiku kohal valige **Mahaarvamised**.
1. Valige tegevuspaanil suvand **Uus**, et lisada rida jaotise **Mahaarvamine** tabelisse. Uue rea **Mahaarvamise ID** väli seatakse automaatselt.
1. Valige **Tüüp** väljal mahaarvamise tüüp.
1. Sisestage väljale **Summa** summa, mis kuvatakse mahaarvamisloendi all oleval väljal **Saldo**. See summa kujutab kliendi maksest mahaarvatud summat.
1. Sulgege leht **Mahaarvamine**. Te tagastatakse **Kliendi maksete** lehele, mis näitab nüüd mahaarvamise uut rida.
1. Valige toimingupaanil **Valideeri \> Valideeri**. Peaksite nägema järgmist sõnumit: „Tööleht on korras”.
1. Tehke toimingupaanil valik **Väljastamine**.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Looge mahaarvamine töölaua abil

Looge mahaarvamise töölauale uus mahaarvamine, järgige neid samme.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Toimingupaanil valige **Halda \> Uus mahaarvamine**.

    **Uus mahaarvamine** dialoogiboksis on **mahaarvamise ID** väli seatud **mahaarvamise ID** numbriseeria põhjal, mis on määratud **Kaubandushüvitise halduse parameetrid** lehel (**Müük ja turundus \> Häälestamine \>Kaubandushüvitised \> Kaubandushüvitiste halduse parameetrid**).

1. Seadistage järgmised väljad.

    - **Kliendi konto** - valige kliendi konto, mille suhtes mahaarvamist rakendatakse.
    - **Välise nõude number** – sisestage kliendi nõude viide.
    - **Nõude summa** – sisestage maksustatav nõude summa. Välja väärtus peab olema positiivne.
    - **Valuuta** – valige mahaarvamise valuuta. Vaikeväärtus on valitud kliendikontole määratud valuuta.
    - **Nõude alus** – valige nõude alus. Nõude alus määratleb pärast mahaarvamist või nõuet kinnitatud krediidikande tüübi.

        - *Hinnapõhine* – luuakse mustandi vabas vormis arve.
        - *Kogusel põhinev* – luuakse negatiivne müügi- või tagastamistellimus.

    - **Nõude kuupäev** – valige nõude kuupäev. Praegune kuupäev on vaikeväärtus.
    - **Nõude põhjus** – valige praeguse mahaarvamisega seotud põhjusekood. Teie valitud nõude alus mõjutab valikuid, mida rakendada. Lisateavet selle kohta, kuidas luua ja konfigureerida valikuks saadaolevaid nõude põhjusi, vt selle teema varasemast jaotisest [Mahaarvamise põhjuste loomine](#deduction-reasons).
    - **Märkused** – saate lisada mis tahes rakenduvad märkused. Kui nõue kinnitatakse, saab kinnitaja nõude märkusi redigeerida või lisada.
    - **Loo nõude tööleh** t – määrake see suvand, et määrata, kas nõude töölehe peaks looma nõude või mahaarvamise loomisel.

        - *Jah* – süsteem loob ja sisestab üldise töölehe, kasutades nõude töölehte, mis on seadistatud **Müügireskontro parameetrid** lehel. (Lisateavet vt teemast sellest teemast varasemalt toodud [Konfigureerige müügireskontro ja mahaarvamised](#accounts-receivable-deductions).) Kui nõudega on seotud arve, kasutatakse rakendatava arve saldo vähendamiseks nõude töölehte. Kui nõue hiljem tagasi lükatakse, tühistatakse nõude tööleht ja tasakaalustused (kui arve lisati).
        - *Ei* – praegu ei looda nõude töölehte. See luuakse nõude heakskiidul. Arve saab siiski uue nõudega siduda, isegi kui nõude töölehte ei looda. Tasakaalustust ei saa siiski ilma nõude tööleheta teha.

1. Valige nupp **OK**.

    Luuakse uus mahaarvamine. Kui seate valiku **Nõude töölehe loomine** väärtusele *Jah*, sisestatakse järgmised kanded.

    - **Kaks uut kliendikannet** – üks kanne tasakaalustab nõude summa algse arvega. Teine kanne registreerib kliendi võla nõude summale, kuna nõuet pole veel kinnitanud. Algse arve kanne ja tasakaalustav nõudekanne märgitakse automaatselt tasakaalustamiseks, kui lisate arve, valides tegevuspaanil **Halda \> Lisa arve**.
    - **Kaks vastaskonto kannet** – need kanded sisestatakse **mahaarvamise vastaskonto** pearaamatukontole.
    - **Nõude tööleht** – mahaarvamise töölaual kuvatava iga mahaarvamise nõude töölehe vaatamiseks valige vahekaart **Viited**. Nõude tööleht kuvatakse **töölehe partiinumbri** väljal. Saate vaadata ka nõude töölehte vahekaardil **Mahaarvamissündmused**. Seal on **uuendamise tüübi** väärtus *Vaste*.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Mahaarvamise loomine kliendi tasakaalustuselt

Kliendi tasakaalustustest mahaarvamise loomise protsess sarnaneb mahaarvamise töölaua kaudu mahaarvamise loomise protsessiga. Kliendi ja arve valuuta seadistatakse automaatselt ning arve lisatakse. Kui loote nõude või mahaarvamise kliendi tasakaalustuse lehe kaudu, ei pea te tegevuspaanil valima käsku **Halda \> Lisa arve**.

1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Valige klient, kellele mahaarvamine luua.
1. Paani Tegumiriba vahekaardil **Kogu** grupis **Sea** valige suvand **Kannete seadmine**.
1. Valige dialoogiboksi **Kannete seadmine** vahekaardil **Ülevaade** arve, mille kohta mahaarvamist luua.
1. Valige tööriistaribal **Mahaarvamised \> Uus mahaarvamine**.

    **Uus mahaarvamine** dialoogiboksis on **mahaarvamise ID** väli seatud **mahaarvamise ID** numbriseeria põhjal, mis on määratud **Kaubandushüvitise halduse parameetrid** lehel (**Müük ja turundus \> Häälestamine \>Kaubandushüvitised \> Kaubandushüvitiste halduse parameetrid**). **Kliendi konto** väli määratakse kliendi kontole, mille suhtes mahaarvamist rakendatakse.

1. Seadistage järgmised väljad.

    - **Välise nõude number** – sisestage kliendi nõude viide.
    - **Nõude summa** – sisestage maksustatav nõude summa. Välja väärtus peab olema positiivne.
    - **Valuuta** – valige mahaarvamise valuuta. Vaikeväärtus on valitud kliendikontole määratud valuuta.
    - **Nõude alus** – valige nõude alus. Nõude alus määratleb pärast mahaarvamist või nõuet kinnitatud krediidikande tüübi.

        - *Hinnapõhine* – luuakse mustandi vabas vormis arve.
        - *Kogusel põhinev* – luuakse negatiivne müügi- või tagastamistellimus.

    - **Nõude kuupäev** – valige nõude kuupäev. Praegune kuupäev on vaikeväärtus.
    - **Nõude põhjus** – valige praeguse mahaarvamisega seotud põhjusekood. Teie valitud nõude alus mõjutab valikuid, mida rakendada. Lisateavet selle kohta, kuidas luua ja konfigureerida valikuks saadaolevaid nõude põhjusi, vt selle teema varasemast jaotisest [Mahaarvamise põhjuste loomine](#deduction-reasons).
    - **Märkused** – saate lisada mis tahes rakenduvad märkused. Kui nõue kinnitatakse, saab kinnitaja nõude märkusi redigeerida või lisada.
    - **Loo nõude tööleh** t – määrake see suvand, et määrata, kas nõude töölehe peaks looma nõude või mahaarvamise loomisel.

        - *Jah* – süsteem loob ja sisestab üldise töölehe, kasutades nõude töölehte, mis on seadistatud **Müügireskontro parameetrid** lehel. (Lisateavet vt teemast sellest teemast varasemalt toodud [Konfigureerige müügireskontro ja mahaarvamised](#accounts-receivable-deductions).) Kui nõudega on seotud arve, kasutatakse rakendatava arve saldo vähendamiseks nõude töölehte. Kui nõue hiljem tagasi lükatakse, tühistatakse nõude tööleht ja tasakaalustused (kui arve lisati).
        - *Ei* – praegu ei looda nõude töölehte. See luuakse nõude heakskiidul. Arve saab siiski uue nõudega siduda, isegi kui nõude töölehte ei looda. Tasakaalustust ei saa siiski ilma nõude tööleheta teha.

1. Valige nupp **OK**.

    Luuakse uus mahaarvamine. Kui seate valiku **Nõude töölehe loomine** väärtusele *Jah*, sisestatakse järgmised kanded.

    - **Kaks uut kliendikannet** – üks kanne tasakaalustab nõude summa algse arvega. Teine kanne registreerib kliendi võla nõude summale, kuna nõuet pole veel kinnitanud. Algse arve kanne ja tasakaalustav nõudekanne märgitakse automaatselt tasakaalustamiseks, kui lisate arve, valides tegevuspaanil **Halda \> Lisa arve**.
    - **Kaks vastaskonto kannet** – need kanded sisestatakse **mahaarvamise vastaskonto** pearaamatukontole.
    - **Nõude tööleht** – mahaarvamise töölaual kuvatava iga mahaarvamise nõude töölehe vaatamiseks valige vahekaart **Viited**. Nõude tööleht kuvatakse **töölehe partiinumbri** väljal. Saate vaadata ka nõude töölehte vahekaardil **Mahaarvamissündmused**. Seal on **uuendamise tüübi** väärtus *Vaste*.

    Olete tagasi lehel **Kannete seadmine**, mis näitab nüüd valitud arve märkimist. Nupp **Sisesta** on saadaval ainult siis, kui seate valiku **Loo nõude tööleht** valikule *Jah*. Kui see on saadaval, valige käsk **Sisesta**, et vähendada arve saldot **nõude summa** väärtuse alusel.

### <a name="create-a-deduction-from-a-customer-page"></a>Mahaarvamise loomine kliendi lehelt

Kliendi lehe mahaarvamise loomise protsess sarnaneb mahaarvamise töölaua kaudu mahaarvamise loomise protsessiga. Klient seadistatakse automaatselt.

1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Valige klient, kellele mahaarvamine luua.
1. Valige toimingupaani vahekaardil **Kogu** rühmas **Mahaarvamised** valik **Loo mahaarvamised**.

    **Uus mahaarvamine** dialoogiboksis on **mahaarvamise ID** väli seatud **mahaarvamise ID** numbriseeria põhjal, mis on määratud **Kaubandushüvitise halduse parameetrid** lehel (**Müük ja turundus \> Häälestamine \>Kaubandushüvitised \> Kaubandushüvitiste halduse parameetrid**). **Kliendi konto** väli määratakse kliendi kontole, mille suhtes mahaarvamist rakendatakse.

1. Seadistage järgmised väljad.

    - **Välise nõude number** – sisestage kliendi nõude viide.
    - **Nõude summa** – sisestage maksustatav nõude summa. Välja väärtus peab olema positiivne.
    - **Valuuta** – valige mahaarvamise valuuta. Vaikeväärtus on valitud kliendikontole määratud valuuta.
    - **Nõude alus** – valige nõude alus. Nõude alus määratleb pärast mahaarvamist või nõuet kinnitatud krediidikande tüübi.

        - *Hinnapõhine* – luuakse mustandi vabas vormis arve.
        - *Kogusel põhinev* – luuakse negatiivne müügi- või tagastamistellimus.

    - **Nõude kuupäev** – valige nõude kuupäev. Praegune kuupäev on vaikeväärtus.
    - **Nõude põhjus** – valige praeguse mahaarvamisega seotud põhjusekood. Teie valitud nõude alus mõjutab valikuid, mida rakendada. Lisateavet selle kohta, kuidas luua ja konfigureerida valikuks saadaolevaid nõude põhjusi, vt selle teema varasemast jaotisest [Mahaarvamise põhjuste loomine](#deduction-reasons).
    - **Märkused** – saate lisada mis tahes rakenduvad märkused. Kui nõue kinnitatakse, saab kinnitaja nõude märkusi redigeerida või lisada.
    - **Loo nõude tööleh** t – määrake see suvand, et määrata, kas nõude töölehe peaks looma nõude või mahaarvamise loomisel.

        - *Jah* – süsteem loob ja sisestab üldise töölehe, kasutades nõude töölehte, mis on seadistatud **Müügireskontro parameetrid** lehel. (Lisateavet vt teemast sellest teemast varasemalt toodud [Konfigureerige müügireskontro ja mahaarvamised](#accounts-receivable-deductions).) Kui nõudega on seotud arve, kasutatakse rakendatava arve saldo vähendamiseks nõude töölehte. Kui nõue hiljem tagasi lükatakse, tühistatakse nõude tööleht ja tasakaalustused (kui arve lisati).
        - *Ei* – praegu ei looda nõude töölehte. See luuakse nõude heakskiidul. Arve saab siiski uue nõudega siduda, isegi kui nõude töölehte ei looda. Tasakaalustust ei saa siiski ilma nõude tööleheta teha.

1. Valige nupp **OK**.

    Luuakse uus mahaarvamine. Kui seate valiku **Nõude töölehe loomine** väärtusele *Jah*, sisestatakse järgmised kanded.

    - **Kaks uut kliendikannet** – üks kanne tasakaalustab nõude summa algse arvega. Teine kanne registreerib kliendi võla nõude summale, kuna nõuet pole veel kinnitanud. Algse arve kanne ja tasakaalustav nõudekanne märgitakse automaatselt tasakaalustamiseks, kui lisate arve, valides tegevuspaanil **Halda \> Lisa arve**.
    - **Kaks vastaskonto kannet** – need kanded sisestatakse **mahaarvamise vastaskonto** pearaamatukontole.
    - **Nõude tööleht** – mahaarvamise töölaual kuvatava iga mahaarvamise nõude töölehe vaatamiseks valige vahekaart **Viited**. Nõude tööleht kuvatakse **töölehe partiinumbri** väljal. Saate vaadata ka nõude töölehte vahekaardil **Mahaarvamissündmused**. Seal on **uuendamise tüübi** väärtus *Vaste*.

## <a name="create-a-credit-note-for-a-customer"></a>Kliendile kreeditarve loomine

Kui kliendi jaoks on olemas kinnitatud tagasimakse, looge kliendi kontol tagasimakset kujutav kreeditarve, nagu on vaja. Seejärel kuvatakse kreedit mahaarvamise töölaual, kus selle saab mahaarvamisega vastendada.

Kreeditarve loomiseks toimige järgmiselt.

1. Avage jaotis **Müük ja turundus \> Kliendid \> Kõik kliendid**.
1. Valige klient.
1. Paani Tegumiriba vahekaardil **Kogu** grupis **Sea** valige suvand **Kannete seadmine**.
1. Dialoogiboksis **Kannete seadmine** valige kanne, mille suhtes tagasimakse rakendati.
1. Valige tööriistariba menüü **Funktsioonid** rakenduv tagasimakseprogrammi tüüp.
1. Valige leheküljel **Tagasimakse** vahekaardil **Ülevaade** vastava tagasimakse ID kõrval **märkeruut**.
1. Tegevuspaanil valige **Funktsioonid \> Loo kreeditarve**.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Mahaarvamise töötlemine mahaarvamise töölaual

Mahaarvamise töölaual saate mahaarvamisi vastendada krediidikannete avamiseks, mahaarvamiste tükeldamiseks ja mahakandmiseks.

Olenevalt sellest, kuidas soovite mahaarvamist töödelda, viige läbi üks või mitu järgmiseid alajaotisi. Protseduure saate vajadusel kombineerida. Näiteks saate mahaarvamise tükeldada kaheks osaks ning seejärel vastendada ühe osa kreeditiga ja jätta teise osa töölauale, et see teise kreeditiga hiljem vastendada. Mahaarvamise saab vastendada ka mahaarvamise summast väiksema kreeditiga ja seejärel mahaarvamise järelejäänud saldo keelata või maha kanda.

### <a name="match-a-deduction-to-a-credit"></a>Mahaarvamise vastendamine kreeditiga

Mahaarvamise sobitamiseks kreeditiga järgige neid samme.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Jaotises **Avatud kanded** märkige mahaarvamisega vastendamiseks kreediti ruut **Märk**. Kui loendis on mitu kreeditit, saate mahaarvamisega vastendamiseks valida neist rohkem kui ühe. Kui soovite, et süsteem valiks automaatselt mahaarvamise summale vastavad kreeditid, valige tööriistaribal sobiv suvand menüüs **Vali mahaarvamissumma**.
1. Klõpsake tegumiribal suvandeid **Haldamine \> Vastenda**. Süsteem vastendab mahaarvamise kreeditile. Kui saldo jääb mahaarvamisse, kuvatakse see vahekaardi **Mahaarvamised** väljal **Jääksumma**.

    > [!NOTE]
    > Mahaarvamiste puhul, mis loodi mahaarvamise töölaual **Uus mahaarvamine** käsuga, kliendi tasakaalustuse või kliendi lehega, on käsk **Halda \> Vastenda** saadaval ainult siis, kui **Nõude olek** väli on seatud väärtusele *Aktsepteeritud*. Seda käsku saab kasutada hinna- või kogusepõhise kande käsitsi vastendamiseks seostatud kreeditiga jaotises **Avatud kanded**. See kreedit luuakse kas siis, kui mahaarvamine on kinnitatud (kasutades käsku **Halda \> Kinnita mahaarvamine**) või kui see on lisatud olemasolevale krediidile, nagu on kirjeldatud teemas [Väljaspool mahaarvamisprotsessi kinnitamist loodud kreedit](#credits-outside-approval). *Kinnitatud mahaarvamiste* perioodilise tasakaalustamise ülesannet (**Müügi turundus \> Perioodilised ülesanded \> Sea kinnitatud mahaarvamised**) saab kasutada ka mahaarvamiste ja kreeditide automaatseks vastendamiseks, kus on vastendatud **mahaarvamise ID** väärtused ja summad.

### <a name="split-a-deduction"></a>Mahaarvamise tükeldamine

Mahaarvamise tükeldamiseks tehke järgmist.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Klõpsake tegumiribal suvandeid **Haldamine \> Tükelda**.
1. Sisestage dialoogiboksi **Tükeldatud summa** väljale **Tükelda** summa, mida põhivähenduses tükeldada. Seejärel valige **OK**.
1. Pange vahekaardil **Mahaarvamised** tähele, et tükeldatud summa kohta kuvatakse uus kirje. Algse mahaarvamise kirje sisaldab mahaarvamise saldo jääki. Nüüd saate algse tagasimakse kaht osa eraldi hallata.
1. Valige algne mahaarvamise kirje ja seejärel valige vahekaart **Viited**. **Tükeldatud summa** väljal kuvatakse summa, mis jaotati algsest summast.

### <a name="attach-an-invoice-to-a-deduction"></a>Arve seostamine mahaarvamisega

Arve saate mahaarvamisele lisada, kui mahaarvamine loodi mahaarvamise töölaua, kliendi tasakaalustuse või kliendi lehe käsuga **Uus mahaarvamine** ja kui sellega pole praegu seotud ühtegi arvet (st veerg **Arve** on tühi).

Arve lisamiseks mahaarvamisele järgige neid samme.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Toimingupaanil valige **Halda \>Kinnita arve**.
1. Valige arve dialoogiaknas **Arve lisamine** ja seejärel valige **OK**.
1. Dialoogiboksis **Kannete tasakaalustamine** järgige üht neist sammudest, sõltuvalt sellest, kas nõude tööleht sisestati mahaarvamise loomisel.

    - Kui nõude tööleht sisestati, kuvatakse teie valitud arvel ja nõudetöölehe kliendi krediidikandel märge veerus **Märk**. Valige **Sisesta**. Seotud arve ülejäänud saldot vähendatakse nõude summa võrra.
    - Kui nõude töölehte ei sisestatud, ei ole veerus **Märk** märgitud ühtki kannet. Kuna te ei saa nõude töölehega tasakaalustada enne, kui mahaarvamine on kinnitatud, valige käsk **Tühista**.

### <a name="detach-an-invoice-from-a-deduction"></a>Eraldage arve mahaarvamisest

Saate arve mahaarvamisest lahutada, kui mahaarvamine loodi mahaarvamise töölaual, kliendi arvelduslehel või kliendilehel oleva käsu **Uus mahaarvamine** abil, kui arve on sellele lisatud (st veerg **Arve** näitab arve numbrit) ja kui väli **Nõude olek** on seatud väärtusele *Avatud*. Võite selle ülesande lõpule viia, sest sellele oli lisatud vale arve. Arve eemaldatakse mahaarvamisest ja selle järelejäänud saldo uuendatakse, kui seda vähendati arvega seotud ajal.

Arve eraldamiseks toimige järgmiselt.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Toimingupaanil valige **Halda \> Eemalda arve**.

### <a name="approve-a-deduction"></a>Mahaarvamise kinnitamine

Saate kinnitada mahaarvamisi, mis loodi, kasutades mahaarvamise töölaual, kliendi tasakaalustuses või kliendi lehel käsku **Uus mahaarvamine**. Kuid saate kinnitada ainult mahaarvamisi, kus **Nõude olekuks** on määratud *Avatud*.

Mahaarvamise kinnitamiseks tehke järgmist.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Toimingupaanil valige **Halda \> Mahaarvamise kinnitamine**.
1. Dialoogiboksis **Mahaarvamise kinnitamine** redigeerige või lisage vajalik teave **Märkus** väärtusele.
1. Kui mahaarvamine on hinnapõhine ja arve ei ole sellega seotud, valige kauba käibemaksugrupp. Tavaliselt seadistatakse kauba käibemaksugrupp arvel. Seetõttu peab maksu kaubakood olema määratud, kui see pole arvega seotud.
1. Valige nupp **OK**.

    Seejärel ei saa mahaarvamist enam muuta. Kui valiku **Loo nõude tööleht** väärtuseks oli mahaarvamise loomisel määratud *Ei*, luuakse ja sisestatakse nõude tööleht mahaarvamise heakskiidul. Kui mahaarvamine on kinnitatud, luuakse ja avatakse krediit automaatselt. Tüüp sõltub mahaarvamise **nõude baas** väärtusest:

    - *Hinnapõhine* – kui mahaarvamine on hinnapõhine, luuakse kliendikonto jaoks vabas vormis arve. Saate lisada kirjelduse ja sisestada krediidi. Mahaarvamised täidetakse mustandi loomisel järgmiste väljadega:

        - **Mahaarvamise ID** – see väli lisatakse päisele, et lubada jälitatavus mahaarvamisel jälle.
        - **Põhikonto** – väärtus määratletakse mahaarvamisele määratud mahaarvamise põhjusel sätestatud **nõude sisestuskonto** väärtusega.
        - **Kauba käibemaksugrupp** – väärtus määratletakse seotud arvega või mahaarvamise heakskiidul valitud väärtusega.
        - **Ühiku hind** – väärtus on mahaarvamise nõude summa kreedit.
        - **Arve tekst** – vaikimisi on see väli seadistatud mahaarvamise **Märkused** väärtusele.

    - *Kogusel põhinev* – kui mahaarvamine on kogusepõhine, luuakse avatud müügi- või tagastustellimus. Säte **Loo tagastustellimus** **[Müügireskontro parameetrid](#accounts-receivable-deductions)** lehel määratleb, kas müügi- või tagastustellimus luuakse mahaarvamise heakskiidul. Kuvatakse leht **Tellimuste kopeerimine** ja filtreeritakse nii, et kuvatakse read, kus **Arve konto** väli on seatud mahaarvamise kliendikontole. Tehke järgmist.

        1. Jaotis **Arved** kiirkaardil **Päised** kuvatakse müügiarved, kus **Arve konto** väärtus vastab mahaarvamise kliendi kontole. Valige rakendatav müügiarve.
        1. Jaotises **Read** kuvatakse valitud müügiarve read. Märkige ruut **Märgi** iga rea kohta, mille soovite kopeerida. Kõigi ridade valimiseks märkige jaotises **Päised** ka müügitellimuse ruut **Vali kõik**.
        1. Korrigeerige ühe või mitme rea **Kogus** väärtust vastavalt vajadusele.

            Kõik seni valitud read on loetletud kiirkaardi **Kopeerimiseks valitud read või päis**.

        1. Korrake eelmiseid kahte sammu vastavalt vajadusele, kuni kiirkaardi **Kopeerimiseks on valitud read või päis** loendis kõik vajalikud read loetletud.
        1. Valige nupp **OK**.

            Avatakse uus tagastustellimus ja järgmised väljad seatakse automaatselt.

            - **Mahaarvamise ID** – see väli lisatakse päisele, et lubada jälitatavus mahaarvamisel jälle.
            - **Tagastuspõhjuse kood** – vaikimisi on see väli seatud mahaarvamisele määratud mahaarvamise põhjusele määratud **tagastuspõhjuse koodi** väärtusele.

Kui kreedit on arveldatud, kuvatakse see mahaarvamise töölaua **avatud kannete** jaotises rakendatava **Mahaarvamise ID** väärtuse suhtes ja selle **Nõude tüüp** väli on seatud väärtusele *Muud krediidid*. Kreedit on saadaval seni, kuni see tasakaalustatakse mahaarvamisega ühel järgmistest viisidest:

- Selle saate käsitsi tasakaalustada, valides tegevuspaanil väärtuse **Halda \> Sobita**.
- See tasakaalustatakse automaatselt *tasakaalustatud kinnitatud nõuete* perioodilise tööga (**Müük ja turundus \> Perioodilised ülesanded \> Tasakaalusta kinnitatud nõuded**).
- See tasakaalustatakse automaatselt, kuna lehe **Müügireskontro parameetrid** vahekaardi **Tasakaalustus** suvand **Automaatne tasakaalustamine** on seatud väärtusele *Jah*.

Mahaarvamise heakskiidul loodud kreediti vaatamiseks saate kasutada ka mahaarvamise töölaua **Avatud kanded** jaotises nuppu **Avatud kreedit**.

### <a name="create-a-return-order"></a>Tagastustellimuse loomine

Saate luua mahaarvamiste tagastustellimuse, mis loodi, kasutades mahaarvamise töölaual, kliendi tasakaalustuses või kliendi lehel käsku **Uus mahaarvamine**. Siiski peavad kõik järgmised tingimused olema täidetud:

- **Nõude aluse** välja väärtuseks on seatud *Kogusepõhine*.
- **Nõude olek** välja väärtuseks on seatud *Ava*.
- Suvand **Loo tagastustellimus** vahekaardil **Mahaarvamised** lehel **[Müügireskontro parameetrid](#accounts-receivable-deductions)** on seatud väärtusele *Jah*.
- Suvand **Loo tagastustellimus enne mahakandmise kinnitamist** vahekaardil **Mahaarvamised** lehel **[Müügireskontro parameetrid](#accounts-receivable-deductions)** on seatud väärtusele *Jah*.

Tagastustellimuse loomiseks järgige järgmisi samme.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Valige toimingupaanil **Halda \> Loo tagastustellimus**.
1. Dialoogiboksis **Mahaarvamise kinnitamine** redigeerige või lisage vajalik teave olemasolevale **Märkused** väärtusele ja vajutage seejärel **OK**.
1. Dialoogikaknas **Kopeeri tellimused** kiirkaardil **Arved** jaotises **Päised** kuvatakse müügiarved, kus **Arve konto** väärtus vastab mahaarvamise kliendi kontole. Valige rakendatav müügiarve.
1. Jaotises **Read** kuvatakse valitud müügiarve read. Märkige ruut **Märgi** iga rea kohta, mille soovite kopeerida. Kõigi ridade valimiseks märkige jaotises **Päised** ka müügitellimuse ruut **Vali kõik**.
1. Korrigeerige ühe või mitme rea **Kogus** väärtust vastavalt vajadusele.

    Kõik seni valitud read on loetletud kiirkaardi **Kopeerimiseks valitud read või päis**.

1. Korrake eelmiseid kahte sammu vastavalt vajadusele, kuni kiirkaardi **Kopeerimiseks on valitud read või päis** loendis kõik vajalikud read loetletud.
1. Valige nupp **OK**.

    Avatakse uus tagastustellimus ja järgmised väljad seatakse automaatselt.

    - **Mahaarvamise ID** – see väli lisatakse päisele, et lubada jälitatavus mahaarvamisel jälle.
    - **Tagastuspõhjuse kood** – vaikimisi on see väli seatud mahaarvamisele määratud mahaarvamise põhjusele määratud **tagastuspõhjuse koodi** väärtusele.

### <a name="deny-a-deduction"></a>Mahaarvamise keelamine

Mahaarvamise keelamiseks tehke järgmist.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Klõpsake tegumiribal suvandeid **Haldamine \> Keela**.
1. Valige dialoogiboksis **Keelamine** keelamise põhjusekood ja seejärel valige **OK**.
1. Valige toimingupaani all oleval väljal **Näita** suvand *Suletud*.

    Vahekaardil **Mahaarvamised** kuvatakse mahaarvamisest keeldumine ja mahaarvamise väli **Järelejäänud summa** on määratud *0,00*.

    Mahaarvamiste puhul, mis loodi, kasutades mahaarvamise töölaual, kliendi tasakaalustuses või kliendi lehel käsku **Uus mahaarvamine** järgmiste sündmuste abil.

    - Vahekaardil **Viited** uuendatakse jaotise **Keelamine** väljad.
    - Kui valisite nõudepäeviku loomise mahaarvamise loomisel ja kui mahaarvamisele on lisatud arve, mis vähendas arve saldot, eraldatakse arve ja varem manustatud arve ülejäänud saldo suureneb tagasilükatud nõude summa.
    - Mahaarvamise **Olek** välja väärtuseks on seatud *Suletud*.
    - Mahaarvamise **Nõude olek** välja väärtuseks on seatud *Tagasi lükatud*.

Keeldumise tagasipööramiseks toimige järgmiselt.

1. Valige vahekaardil **Mahaarvamised** tagasi lükatud mahaarvamine.
1. Valige toimingupaanil **Tagasi lükkamise tagasipööramine**.

    Mahaarvamiste puhul, mis loodi, kasutades mahaarvamise töölaual, kliendi tasakaalustuses või kliendi lehel käsku **Uus mahaarvamine** järgmiste sündmuste abil.

    - Vahekaardil **Viited** uuendatakse jaotise **Keelamine** väljad.
    - Mahaarvamise **Olek** välja väärtuseks on seatud *Avatud*.
    - Mahaarvamise **Nõude olek** välja väärtuseks on seatud *Avatud*.

### <a name="write-off-a-deduction"></a>Mahaarvamise mahakandmine

Mahaarvamise mahakandmiseks tehke järgmist.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Klõpsake tegumiribal suvandeid **Haldamine \> Mahakandmine**.
1. Valige dialoogiboksis **Mahakandmine** mahakandmise põhjusekood ja seejärel valige **OK**.
1. Valige väljal **Kuva** suvand *Suletud*.

    Vahekaardil **Mahaarvamised** kuvatakse mahaarvamisest mahakandmine ja mahaarvamise väli **Järelejäänud summa** on määratud *0,00*.

    Mahaarvamiste puhul, mis loodi, kasutades mahaarvamise töölaual, kliendi tasakaalustuses või kliendi lehel käsku **Uus mahaarvamine** järgmiste sündmuste abil.

    - Vahekaardil **Viited** uuendatakse jaotise **Mahakandmine** väljad.
    - Kui lõite nõude töölehe mahaarvamise loomisel, sisestatakse nõude tööleht mahaarvamise mahakandmispõhjuse koodile. Seda kirjet saate vaadata vahekaardil **Mahaarvamise sündmused**, kus selle **uuendustüübi** väärtus on *Mahakandmine*.
    - Mahaarvamise **Olek** välja väärtuseks on seatud *Suletud*
    - Mahaarvamise **Nõude olek** välja väärtuseks on seatud *Mahakandmine*.

Mahakandmise tagasipööramiseks tehke järgmist.

1. Valige vahekaardil **Mahaarvamised** tagasi lükatud mahaarvamine.
1. Klõpsake tegumiribal suvandit **Pööra mahakandmine tagasi**.

    Mahaarvamiste puhul, mis loodi, kasutades mahaarvamise töölaual, kliendi tasakaalustuses või kliendi lehel käsku **Uus mahaarvamine** järgmiste sündmuste abil.

    - Vahekaardil **Viited** uuendatakse jaotise **Mahakandmine** väljad.
    - Kui lõite nõude töölehe mahaarvamise loomisel, sisestatakse nõude tööleht mahaarvamise mahakandmispõhjuse koodile. Seda kirjet saate vaadata vahekaardil **Mahaarvamise sündmused**, kus selle **uuendustüübi** väärtus on *Mahakandmise tagasipööramine*.
    - Mahaarvamise **Olek** välja väärtuseks on seatud *Avatud*.
    - Mahaarvamise **Nõude olek** välja väärtuseks on seatud *Avatud*.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Väljaspool mahaarvamisprotsessi loodud kreedit

See jaotis rakendub mahaarvamistele, mis loodi, kasutades mahaarvamise töölaual, kliendi tasakaalustuses või kliendi lehel käsku **Uus mahaarvamine**.

Erinevad kasutajad on võib-olla juba loonud vabas vormis arve, tagastustellimuse või negatiivse müügitellimuse kliendi nõudele väljaspool **Kinnita mahaarvamine** protsessi. Kui mahaarvamise töölaual olemasolev mahaarvamine kinnitatakse, loob süsteem automaatselt teise vabas vormis arve, tagastustellimuse või negatiivse müügitellimuse. See jaotis kirjeldab, kuidas siduda olemasolevad kreeditid mahaarvamisega enne mahaarvamise kinnitamist, et vältida duplikaatkrediite.

### <a name="attach-a-credit-to-deduction"></a>Lisage mahaarvamisele krediit

Selles jaotises kirjeldatakse kreediti seostamist kreediti mahaarvamisega.

Kui mahaarvamisele on lisatud krediit, saate seda vaadata, kasutades mahaarvamise töölaua jaotise **Avatud tehingud** tööriistariba nuppu **Ava krediit**.

Kui kreedit on arveldatu ja mahaarvamine on kinnitatud, kuvatakse see mahaarvamise töölaua **avatud kannete** jaotises rakendatava **Mahaarvamise ID** väärtuse suhtes ja selle **Nõude tüüp** väli on seatud väärtusele *Muud krediidid*.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Vabatekstilise arve seostamine mahaarvamisega

Vabatekstilise arve lisamiseks mahaarvamisele järgige neid samme.

1. Avage **Müügireskontro \> Arved \> Kõik vabas vormis arved**.
1. Valige sobiv arve.
1. Toimingupaanil vahekaardil **Arve** valige suvand **Lisa kreedit mahaarvamisele**. See nupp on saadaval ainult juhul, kui on vabatekstilise arve väli **Mahaarvamise ID** on tühi. Tühi väli näitab, et vabas vormis arve pole veel mahaarvamisega seotud.
1. Lehel **Lisa kreedit mahaarvamisele** saate valida *ühe* mahaarvamise. Valiku jaoks on saadaval ainult avatud *hinnapõhised* mahaarvamised.
1. Valige nupp **OK**. **Mahaarvamise ID** väli on seadistatud vabastekstilise arve päisele.

#### <a name="attach-a-return-order-to-a-deduction"></a>Tagastustellimuse seostamine mahaarvamisega

Tagastustellimuse lisamiseks mahaarvamisele järgige neid samme.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik tagastustellimused**.
1. Valige rakendatav vastuvõetud või avatud tagastuse kauba autoriseerimise (RMA) number.
1. Toimingupaanil vahekaardil **Tagastustellimus** valige suvand **Lisa kreedit mahaarvamisele**. See nupp on saadaval ainult juhul, kui on tagastustellimuse väli **Mahaarvamise ID** on tühi. Tühi väli näitab, et tagastustellimus pole veel mahaarvamisega seotud.
1. Lehel **Lisa kreedit mahaarvamisele** saate valida *ühe* mahaarvamise. Valiku jaoks on saadaval ainult avatud *kogusepõhised* mahaarvamised.
1. Valige nupp **OK**. **Mahaarvamise ID** väli on seadistatud tagastustellimuse arve päisele.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Müügitellimuse seostamine mahaarvamisega

Müügitellimuse lisamiseks mahaarvamisele järgige neid samme.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused**.
1. Valige rakendatav avatud, tarnitud või arveldatud müügitellimus.
1. Toimingupaanil vahekaardil **Arve** valige suvand **Lisa kreedit mahaarvamisele**. See nupp on saadaval ainult juhul, kui on müügitellimuse väli **Mahaarvamise ID** on tühi. Tühi väli näitab, et müügitellimus pole veel mahaarvamisega seotud.
1. Lehel **Lisa mahaarvamine** saate valida *ühe* mahaarvamise. Valiku jaoks on saadaval ainult avatud *kogusepõhised* mahaarvamised.
1. Valige nupp **OK**. **Mahaarvamise ID** väli on seadistatud müügitellimuse arve päisele.

#### <a name="detach-a-deduction-from-a-credit"></a>Mahaarvamise eemaldamine krediidist

Kui on lisatud vale mahaarvamine, saate selle krediidist eemaldada. Siiski peavad kõik järgmised tingimused olema täidetud:

- Mahaarvamisega on seotud kreedit.
- **Nõude olek** välja väärtuseks on seatud *Ava*.

Mahaarvamise lahutamiseks kreeditilt järgige üht järgmistest sammudest, sõltuvalt kreediti tüübist:

- **Vabas vormis arved**: valige arve leheküljel **Kõik vabas vormis arved**. Siis toimingupaanil vahekaardil **Arve** valige suvand **Eemalda kreedit mahaarvamisest**.
- **Tagastustellimused**: valige soovitud tellimus lehel **Kõik tagastustellimused**. Siis toimingupaanil vahekaardil **Tagastustellimus** valige suvand **Eemalda kreedit mahaarvamisest**.
- **Müügitellimused**: valige soovitud tellimus lehel **Kõik müügitellimused**. Siis toimingupaanil vahekaardil **Arve** valige suvand **Eemalda kreedit mahaarvamisest**.

### <a name="attach-a-deduction-to-a-credit"></a>Mahaarvamise lisamine kreeditile

Selles jaotises kirjeldatakse, kuidas saate mahaarvamisest krediidile mahaarvamise lisada.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Mahaarvamise lisamine vabas vormis, tagastustellimusele või müügitellimuse krediidile

Vabale tekstile, tagastustellimusele või müügitellimuse krediidile mahaarvamise lisamiseks toimige järgmiselt.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige sobiv avatud mahaarvamine.
1. Toimingupaanil valige **Halda \> Mahaarvamise lisamine kreeditile**. See nupp on saadaval ainult siis, kui **Nõude olek** välja väärtuseks on seatud *Avatud*.
1. Lehel **Lisa kreedit** saate valida *ühe* kreediti. Näidatav kreeditsumma sõltub mahaarvamise **nõude baas** väärtusest:

    - *Hinnapõhine* – lehel kuvatakse kliendikonto vabas vormis arved, kus **Mahaarvamise ID** väli on tühi. Kuvatakse ka kliendi ostutellimused, kuna vabas vormis arve võib olla sisestamata. Seega ei pruugi sellel olla numbrit, mida saab viidata.
    - *Kogusepõhine* – näidatav kreediti tüüp sõltub **Tagastustellimuse loomine** suvandi sättest lehel **[Müügireskontro parameetrid](#accounts-receivable-deductions)**.

        - *Jah* – lehel kuvatakse kliendikonto tagastustellimused, kus **Mahaarvamise ID** väli on tühi.
        - *Ei* – lehel kuvatakse kliendikonto müügitellimused, kus **Mahaarvamise ID** väli on tühi.

1. Valige nupp **OK**. **Mahaarvamise ID** väli on seadistatud kreediti päisele.

Kui mahaarvamisele on lisatud krediit, saate seda vaadata, kasutades mahaarvamise töölaua jaotise **Avatud tehingud** tööriistariba nuppu **Ava krediit**.

Kui kreedit on arveldatu ja mahaarvamine on kinnitatud, kuvatakse see mahaarvamise töölaua **avatud kannete** jaotises rakendatava **Mahaarvamise ID** väärtuse suhtes ja selle **Nõude tüüp** väli on seatud väärtusele *Muud krediidid*.

#### <a name="detach-a-credit-from-the-deduction"></a>Eraldage krediit mahaarvamisest

Kui vale krediit on lisatud, saate selle mahaarvamisest lahutada. Toimingupaanil grupis **Halda** valige suvand **Eemalda kreedit mahaarvamisest**. **Mahaarvamise ID** väärtus eemaldatakse krediidist.

**Mahaarvamise eemaldamine kreeditist** nupp on saadaval ainult juhul, kui täidetud on järgmised tingimused:

- Mahaarvamisega on seotud kreedit.
- **Nõude olek** välja väärtuseks on seatud *Ava*.

## <a name="create-a-one-time-promotion"></a>Looge ühekordne reklaam

Mõnikord ei pruugi teil olla kinnitatud tagasimakset, mille saate mahaarvamisega vastendada. Sel juhul saate kasutada funktsiooni *ühekordne kampaania*, et vastendada mahaarvamine kliendiga seostatud kaubandushüvitisega. Funktsioon *ühekordne kampaania* loob uue kaubandushüvitise leppe ja tervikväljamaksega tootesündmuse. See vastendab tervikväljamakse mahaarvamisega ja teeb mahaarvamise sulgemiseks vajalikud sisestused.

See funktsioon on kasulik, kui kasutate kaubandushüvitisi. Kaubandushüvitiste kohta lisateabe saamiseks vt [Kaubandushüvitise haldus](../sales-marketing/trade-allowance.md).

Esmalt peate seadistama malli, mille abil luua uus kaubandushüvitise lepe. Malli seadistamiseks toimige järgmiselt.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mallid**.
1. Valige toimingupaanil nupp **Uus**.
1. Täitke väljad teabega, mis peaks ilmuma selle malli põhjal loodud lepetes.
1. Valige kiirkaardi **Kliendid** väljal **Hierarhia** hierarhiatase.
1. Valige hierarhialoendist klient, kellele pole vastendatud mahaarvamist, ja seejärel valige paremnooleklahv (**\>**). Klient lisatakse **Kaubandushüvitise lepingu kliendid** loendisse.
1. Seadke ülejäänud väljad vastavalt vajadusele ja sulgege leht.
1. Minge **Müük ja turundus \> Häälestus \> Kaubandushüvitis \> Kaubandushüvitise halduse parameetrid**.
1. Valige vahekaardi **Ülevaade** väljal **Ühekordse kampaania mall**, mida kasutada ühekordse kampaaniahinna loomiseks.

Järgmisena saate mahaarvamise töölauale luua ühekordse kampaania. Ühekordse kampaania loomiseks toimige järgmiselt.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige töödeldava mahaarvamise kõrval olev **Märk** märkeruut.
1. Tegevuspaanil valige suvand **Halda \> Mahaarvamise tasakaalustamine ühekordse kampaaniana**.
1. Dialoogiboksis **Ühekordne kampaania** järgige neid samme mahaarvamise seostamiseks ühe või mitme fondiga.

    1. Klõpsake suvandit **Uus** ja seejärel valige väljal **Fondi ID** fondi ID. Korrake seda etappi vajaliku hulga fondide lisamiseks.
    1. Sisestage iga fondi ID kõrval olevale väljale **Protsent** mahaarvamise protsent fondi eraldamiseks. Väljadele **Protsent** sisestatud summad peavad andma kokku 100%.

1. Valige nupp **OK**. Süsteem loob uue kaubandusleppe hüvitise, millel on tervikväljamaksega tootesündmus, ja vastendab tervikväljamakse mahaarvamisele.

## <a name="do-a-mass-update-of-deductions"></a>Massvärskendage mahaarvamised

Kui teil on vaja mitmele mahaarvamisele teha sama muudatus, saate need mahaarvamised valida ja teha nende väljade massvärskenduse.

Massvärskenduse tegemiseks toimige järgmiselt.

1. Minge **Müük ja turundus \> Kaubandushüvitised \> Mahaarvamised \> Mahaarvamiste töölaud**.
1. Valige toimingupaani all oleval väljal **Kuva** kuvatavate mahaarvamiste tüüp.
1. Märkige iga soovitud värskendatava mahaarvamise kõrval olev märkeruut. Siis, toimingupaanil valige **Halda \> Massvärskendamine**.
1. **Massvärskendus** dialoogiaknas kuvatakse valitud mahaarvamised. Värskendage väljad vastavalt vajadusele ja seejärel valige muudatuste aktsepteerimiseks **OK**.
