---
title: Tagasimaksete protsess, ülevaatamine ja sisestamine
description: See teema kirjeldab, kuidas töödelda tagasimaksehalduse tehinguid, arvutada nende allahindlusi, vaadata üle loodud kanded, sisestada kandeid ja vaadata sisestusi üle.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 82b8a4e6ba7ebea7df9f5dad5abc3dfc3ce2687d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270757"
---
# <a name="process-review-and-post-rebates"></a>Tagasimaksete protsess, ülevaatamine ja sisestamine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas töödelda tagasimaksehalduse tehinguid, arvutada nende allahindlusi, vaadata üle loodud kanded, sisestada kandeid ja vaadata sisestusi üle.

## <a name="change-the-status-of-a-deal"></a>Pakkumise oleku muutmine

Saate igale tehingule selle jälgimiseks määrata oleku. Sellel olekul on ainult informatiivne eesmärk.

1. Valige tehing (näiteks [lehel **Kõik tagasimaksehalduse tehingud**](rebate-management-deals.md)).
1. Valige toimingupaani vahekaardil **Tagasimaksehalguse tehingud** grupis **Halda** suvand **Muuda staatust**.
1. Dialoogiboksis **Oleku muutmine** määrake väljal **Tagasimakse olek** uus olek.
1. Valige nupp **OK**.

## <a name="calculate-fifo-purchase-prices"></a>FiFO ostuhindade arvutamine

**FiFO ostuhinna** perioodilise ülesande arvutamine peab olema käitatud, et arvutada tagasimaksed [tehingute](rebate-management-deals.md) puhul, kus väli **Hinna alus** väärtuseks on seatud *FIFO*. Süsteem kasutab esimena sisse, esimesena välja (FIFO) reeglit, et arvutada müüdud laoväärtus. Seda väärtust kasutatakse seejärel müüja tagasimaksete arvutamiseks.

Mine **Tagasimaksete haldus \> Perioodilised ülesanded \>FIFO ostuhinna arvutamine**. Kuvatavas dialoogiboksis valige arvutuse käivitamiseks **OK**.

## <a name="process-rebate-management-deals"></a>Tagasimaksehalduse tehingute töötlemine

Tehingu töötlemise ajal arvutab süsteem kõik asjakohased tagasimaksed ja autoritasud, mis on seadistatud. Töödeldakse ainult valitud tehinguid, mille arvutamisperioodid on arvutamiseks valmis ja mille olekuks on *Aktiivne*. Pärast töötlemise lõpetamist loob süsteem kannete komplekti, mille saate üle vaadata ja seejärel sisestada.

> [!NOTE]
> Kõigil juhtudel töödeldakse tagasimakseid tasemel, mis on määratud iga tehingu sättega **Vastavusseviimine** (*Tehing* või *Rida*). Üherealisi arvutusi saate teha ainult nende tehinguid puhul, kus välja **Vastavusseviimine** väärtuseks on seatud *Rida*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Töödelge kõikide tehingute ridu

1. Avage sobiv [tagasimakse tehingud loendileht](rebate-management-deals.md) tehingu tüübi jaoks, mida soovite kasutada.
1. Valige rida igale tehingule, mida soovite töödelda (või avage tehing, mida soovite töödelda).
1. Tegevuspaani vahekaardil **Tagasimaksehalduse tehingud** valige grupi **Loo** jaoks üks järgmistest käskudest:

    - **Protsessi \> Ettevalmistamine** – tehke iga asjakohase tagasimakse tehingu puhul tekkepõhine ettevalmistus, kuid ärge neid sisestage. See menüükäsk ei ole saadaval tehingutele, kus välja **Tagasimakse väljund** väärtuseks on seatud *Kaup*.
    - **Töötlemine \> Tagasimakse haldus** – töötlege kannete seeriat, mis annab tagasimakse väärtuse igale tehingule.
    - **Protsess \>Mahakandmine** - tagasimakse tehingu ja määratud perioodi iga lähtekande puhul töödelge hälbeid eraldise jaoks sisestatud summade ja tagasimaksehalduse vahel. See menüükäsk ei ole saadaval tehingutele, kus välja **Tagasimakse väljund** väärtuseks on seatud *Kaup*.

1. Kuvatavas dialoogiboksis määrake väljad **Alates** ja **Kuni** kuupäevani, et määrata kalkulatsiooni kuupäevavahemik.
1. Kalkulatsiooni käivitamiseks valige **OK**.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Ühe või mitme valitud tehingu rea töötlemine

1. Avage sobiv [tagasimakse tehingud loendileht](rebate-management-deals.md) tehingu tüübi jaoks, mida soovite kasutada.
1. Avage tehing, millelt soovite rida töödelda.
1. Valige ülemises parempoolses nurgas vahekaart **Read**.
1. Valige kiirkaardil **Tagasimakse haldus** rida iga tehingurea puhul, mida soovite töödelda.
1. Valige kiirkaardi **Tagasimakse haldus** tööriistaribal üks järgmistest käskudest. (Need käsud on saadaval ainult tehingute puhul, kus välja **Vastavusseviimine** väärtuseks on seadtud *Rida*.)

    - **Töötlemine \> Ettevalmistamine** – tehke iga asjakohase tehingu rea puhul tekkepõhine ettevalmistus, kuid ärge neid sisestage. See menüükäsk ei ole saadaval tehingutele, kus välja **Tagasimakse väljund** väärtuseks on seatud *Kaup*.
    - **Töötlemine \> Tagasimakse haldus** – töötlege kannete seeriat, mis annab tagasimakse väärtuse igale reale.
    - **Protsess \>Mahakandmine** - tagasimakse tehingu ja määratud perioodi iga lähtekande puhul töödelge hälbeid eraldise jaoks sisestatud summade ja tagasimaksehalduse vahel. See menüükäsk ei ole saadaval tehingutele, kus välja **Tagasimakse väljund** väärtuseks on seatud *Kaup*. 

1. Kuvatavas dialoogiboksis määrake väljad **Alates** ja **Kuni** kuupäevani, et määrata kalkulatsiooni kuupäevavahemik.
1. Kalkulatsiooni käivitamiseks valige **OK**.

### <a name="process-deals-using-a-batch-job"></a>Töötle tehinguid, kasutades partiitööd

Kindlate tehingu või tehingu ridade töötlemise asemel võite käivitada partiitöö mitme tehingu samaaegseks töötlemiseks. Võite valikuliselt rakendada kirjefiltreid ja/või seadistada korduva graafiku. Tehingute töötlemiseks partiitöö abil järgige järgmisi samme.

1. Järgige üht neist sammudest.

    - Minge **Tagasimaksehaldus \> Perioodilised ülesanded \> Töötlemine \> Ettevalmistamine**, et anda iga asjakohase tehingu jaoks tekkepõhiste kannete kogum, kuid ilma neid sisestamata.
    - Minge **Tagasimakse haldus \> Perioodilised ülesanded \> Töötlemine \> Tagasimakse haldus**, et töödelda kannete seeriat, mis annab tagasimakse väärtuse igale tehingule.
    - Minge **Tagasimakse haldus \> Perioodilised ülesanded \> Töötlemine \> Mahakandmine**, et tühistada varem sisestatud kanded, et need maha kanda, nii et saaks arvutada uusi tagasimakse tehingukandeid.

1. Seadke jaotise **Periood** kiirkaardil **Parameetrid** kuvatavas dialoogiboksis väljad **Alates kuupäevast** ja **Kuni kuupäevani**, et määrata kalkulatsiooni kannete kuupäevavahemik.
1. Kuvatavas jaotises **Garantiiperiood** määrake väljad **Alates kuupäevast** ja **Kuni kuupäevani**, et määrata kalkulatsiooni garantiivahemik.
1. Kiirkaardil **Kirjeid, mida kaasata** saate seadistada filtreid, ,mis piiravad partiitöö töödeldavaid tehinguid. Need sätted töötavad samamoodi, nagu need töötavad teist tüüpi partiitööde puhul.
1. Vajadusel saate seadistada partiitööde töötlemise ja plaanilimise suvandid kiirkaardil **Taustal käitamine**. Need sätted töötavad samamoodi, nagu need töötavad teist tüüpi partiitööde puhul.
1. Kalkulatsiooni käivitamiseks ja/või plaanimiseks valige **OK**.

## <a name="view-and-edit-rebate-management-transactions"></a>Tagasimaksehalduse kannete kuvamine ja redigeerimine

Ühe või mitme tehingu töötlemise ajal loob süsteem kanded, mida saate vaadata ja võib-olla redigeerida enne nende sisestamist.

1. Järgige üht neist sammudest.

    - Valige tehing, mille kandeid vaadata (nt lehel [**Kõik tagasimaksehalduse tehingud**](rebate-management-deals.md)). Tegevuspaani vahekaardil **Tagasimaksehalduse tehingud** grupis **Kanded** valige **Kanded** või **Garantiikanded**, sõltuvalt kande tüübist, mida soovite vaadata.
    - Tehingu üksikasjade vaatamiseks avage see (nt lehel [**Kõik tagasimaksehalduse tehingud**](rebate-management-deals.md)). Valige kiirkaardil **Tagasimaksehaldus** tehingu rida, mille kandeid soovite vaadata. Seejärel valige tööriistaribal **Kanded** või **Garantiikanded** sõltuvalt kande tüübist, mida soovite vaadata. (Need nupud on saadaval ainult tehingute puhul, kus välja **Vastavusseviimine** väärtuseks on seatud *Rida*.)

1. Kuvatakse leht **Tagasimaksehalduse kuupäeva kanded** või **Tagasimaksehalduse garantiikanded**. See sisaldab ruudustikku, kus iga rida esindab kannete kogumit üksikust tagasimakse- või garantiiperioodist. Valige ruudustiku rida ja seejärel valige tegevuspaanil **Lähtekanded**, et vaadata sellele reale kuuluvaid kandeid.
1. Kuvav lehekülg kuvab valitud tüüpi kannete loendi, mis kuulub valitud reale. Iga kanne kuvab kande tüübist sõltuvalt asjakohaseid üksikasju. Garantiikannete puhul saate vaadata ainult loendit. Teist tüüpi kannete jaoks saate sellel leheküljel teha järgmisi toiminguid.

    - Kõigi lehel esitatud kannete koguväärtuse kontrollimiseks vaadake välja **Nõudetav summa**.
    - Mis tahes kande kohta lisateabe vaatamiseks valige see ja seejärel valige vahekaart **Üldine**, **Finantsdimensioon** või **Dimensioon**.
    - Mis tahes rakenduva vähenduste vaatamiseks valige tegevuspaanil **Vähendamiskanded**. Lisateavet vt [Tagasimakse vähendamise põhimõtted](rebate-reduction-principle.md).
    - Kannete tehtuks või tegemata märkimiseks, kui kasutate nõuete protsessi, valige vastavad read ja seejärel valige tegevuspaanil üks järgmistest käskudest. (Nõudeprotsesse saab lubada [lehel **Tagasimaksehalduse parameetrid**](rebate-management-parameters.md).)

        - **Märgi tehtuks \> Kõik** – märkige kõik kanded tehtuks.
        - **Märgi tehtuks \> Valitud** – märkige valitud kanded tehtuks.
        - **Märgi tegemata \> Kõik** – märkige kõik kanded tegemata.
        - **Märgi tegemata \> Valitud** – märkige valitud kanded tegemata.

    - Kõigi asjakohaste ridade nõude sisestamiseks valige tegevuspaanil käsk **Sisesta**. Kui kasutate nõuete protsessi (kui lehel **Tagasimakse halduse parameetrid** on lubatud suvand **Kasuta nõude protsessi**), sisestatakse ainult need read, mis on märgitud kui **Saadud**. Vastasel juhul sisestatakse kõik valitud tagasimaksekande lähtekanded. Nupp **Sisesta** on saadaval ainult tagasimakse kannete puhul. See ei ole saadaval eraldise ja mahakandmiskannete jaoks. Dialoogiaknas **Sisesta** määratakse automaatselt väljad **Alates** ja **Kuni**. Määrake **Sisestamise kuupäeva** väli ja valige seejärel **OK**.
    - Avatud või sisestamata kande puhul kuvatava summa korrigeerimiseks valige kanne ja järgige seejärel toimige järgmiselt.

        - Redigeerige väärtust väljal **Parandatud summa**.
        - Valige toimingupaanil suvand **Paranduse häälestamine**. Seejärel sisestage väärtus ripploendisse, mis kuvatakse väljal **Parandatud summa**.

> [!NOTE]
> Kui kasutate nõude esitamise protsessi, siis järgmise perioodi töötlemiseks sisaldab kannete loend kõiki eelmise sisestuse tagasimaksmata kandeid ja valitud perioodi uusi kandeid.

## <a name="post-rebates-transactions"></a>Tagasimakse kannete sisestamine

Töödeldud eraldise, tagasimakse haldussumma ja mahakantud väärtuse sisestamiseks peate käivitama sisestusprotsessi. Sisestusprotsess märgib sisestatud eraldise, tagasimakse halduse või mahakandmiskanded ja loob sihtkande. Kui te ei pea sihtkannet üle vaatama, saab need kanded seadistada nii, et need sisestatakse automaatselt.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Saate häälestada süsteemi kõiki sihtkandeid automaatselt sisestama

Süsteemi häälestamiseks, et sisestada kõik sihtkanded kohe pärast kannete loomist (tagasimakse, haldussumma ja mahakandmise kaudu), lülitage sisse suvand **Sisesta töölehed automaatselt** ja/või **Sisesta vabas vormis arved automaatselt** lehel **Tagasimakse halduse parameetrid**. Lisateavet vt teemast [Tagasimakse haldamise parameetrid](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Kõikide tehingute ridade kannete sisestamine

Pärast vastavate tehingute töötlemist järgige neid samme, et üle vaadata ja sisestada kõikidele ridadele genereeritud kanded ühe või mitme tehingu kohta.

1. Avage sobiv [tagasimakse tehingud loendileht](rebate-management-deals.md) tehingu tüübi jaoks, mida soovite kasutada.
1. Valige rida igale tehingule, mida soovite sisestada (või avage tehing, mida soovite sisestada).
1. Tegevuspaani vahekaardil **Tagasimaksehalduse tehingud** valige grupi **Loo** jaoks üks järgmistest käskudest:

    - **Sisesta \> Ettevalmistamine** – sisestage saadaolevad loodud tekkepõhised kanded.
    - **Sisesta \> Tagasimaksehaldus** – sisestage saadaolevad loodud tagasimakse kanded.
    - **Sisesta \> Mahakandmine** – sisestage saadaolevad loodud maha kantud kanded.

1. Määrake väli **Sisestamise kuupäev** kuvatavas dialoogiboksis. Siis määrake väljad **Alates kuupäevast** ja **Kuni kuupäevani**, et määrata sisestamist vajavate kannete vahemik.
1. Klõpsake kannete sisestamiseks nuppu **OK**.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Ühe või mitme valitud tehingu rea kannete sisestamine

Pärast vastavate tehingute töötlemist järgige neid samme, et üle vaadata ja sisestada kõikidele ridadele genereeritud kanded ühe või mitme spetsiifilise tehingurea või tehingu kohta. Seda protseduuri rakendatakse ainult tehingute puhul, kus välja **Vastavusseviimine** väärtuseks on seadtud *Rida*.

1. Avage sobiv [tagasimakse tehingud loendileht](rebate-management-deals.md) tehingu tüübi jaoks, mida soovite kasutada.
1. Avage tehing, millel on rida, millele soovite kandeid sisestada.
1. Valige ülemises parempoolses nurgas vahekaart **Read**.
1. Valige kiirkaardil **Tagasimakse haldus** rida iga tehingurea puhul, mida soovite sisestada.
1. Valige kiirkaardi **Tagasimakse haldus** tööriistaribal üks järgmistest käskudest. (Need käsud on saadaval ainult tehingute puhul, kus **Vastavusseviimine** väärtuseks on seatud *Rida*.)

    - **Sisesta \> Ettevalmistamine** – sisestage saadaolevad loodud tekkepõhised kanded.
    - **Sisesta \> Tagasimaksehaldus** – sisestage saadaolevad loodud tagasimakse kanded.
    - **Sisesta \> Mahakandmine** – sisestage saadaolevad loodud maha kantud kanded.

1. Määrake väli **Sisestamise kuupäev** kuvatavas dialoogiboksis. Siis määrake väljad **Alates kuupäevast** ja **Kuni kuupäevani**, et määrata sisestamist vajavate kannete vahemik.
1. Klõpsake kannete sisestamiseks nuppu **OK**.

### <a name="post-transactions-using-a-batch-job"></a>Kannete sisestamine partiitöö abil

Kindlate tehingu või tehingu ridade kannete sisestamise asemel võite käivitada partiitöö mitme tehingu samaaegseks kannete sisestamiseks. Võite valikuliselt rakendada kirjefiltreid ja/või seadistada korduva graafiku. Kannete sisestamiseks partiitöö abil järgige järgmisi samme.

1. Järgige üht neist sammudest.

    - Minge **Tagasimaksehalduse \> Perioodilised ülesanded \> Sisesta \> Ettevalmistamine**, et sisestada saadaolevad tekkepõhised kanded, mille olete loonud.
    - Minge **Tagasimaksehalduse \> Perioodilised ülesanded \> Sisesta \> Tagasimaksehaldus**, et sisestada saadaolevad tagasimakse kanded, mille olete loonud.
    - Minge **Tagasimaksehalduse \> Perioodilised ülesanded \> Sisesta \> Mahakandmine**, et sisestada saadaolevad mahakandmise kanded, mille olete loonud.

1. Seadke kuvatud dialoogiakna kiirkaardil **Parameetrid** jaotises **Periood** väli **Sisestuskuupäev**. Siis määrake väljad **Alates kuupäevast** ja **Kuni kuupäevani**, et määrata sisestamist vajavate kannete vahemik.
1. Kuvatavas jaotises **Garantiiperiood** määrake väljad **Alates kuupäevast** ja **Kuni kuupäevani**, et määrata garantiid, mida peab sisestama.
1. Kiirkaardil **Kirjeid, mida kaasata** saate seadistada filtreid, ,mis piiravad partiitöö töödeldavaid tehinguid. Need sätted töötavad samamoodi, nagu need töötavad teist tüüpi partiitööde puhul.
1. Vajadusel saate seadistada partiitööde töötlemise ja plaanilimise suvandid kiirkaardil **Taustal käitamine**. Need sätted töötavad samamoodi, nagu need töötavad teist tüüpi partiitööde puhul.
1. Kalkulatsiooni käivitamiseks ja/või plaanimiseks valige **OK**.

## <a name="review-rebate-management-journals"></a>Tagasimakse halduse töölehtede ülevaade

Pärast kannete sisestamist saate üle vaadata tulemuseks saadud töölehed, dokumendid või üksused. Tagasimaksete ja tagasimaksete sihtkanded põhinevad sisestusprofiilis määratud maksetüübil ja tagasimakse väljundi tüübil. Näiteks, kui tagasimakse väljamineku väärtuseks on seatud *Kaup*, luuakse müügitellimus kliendi tagasimakse jaoks ja ostutellimus luuakse hankija tagasimakse jaoks. Neid tellimusi saab vaadata sihtkannete kaudu. Teise võimalusena, kui makse on seatud võlgnevuse kasutamiseks, luuakse kliendi jaoks seadistatud müüja arve kliendi tagasimaksete jaoks.

Tagasimaksehalduse tehinguga seotud töölehe sisestuste ülevaatamiseks toimige järgmiselt.

1. Avage sobiv [tagasimakse tehingud loendileht](rebate-management-deals.md) tehingu tüübi jaoks, mida soovite kasutada.
1. Valige tehing, mille kohta kontrollida töölehe sisestusi.
1. Tegevuspaani vahekaardil **Tagasimaksehalduse tehingud** grupis **Kanded** valige kas **Kanded** või **Garanteeritud kanded**, sõltuvalt kannete tüübist, mida soovite vaadata.
1. Veenduge, et välja **Näita** väärtuseks oleks seatud *Kõik* või *Sisestatud*.
1. Otsige ja valige kandekogum, mida soovite kontrollida ning seejärel valige tegumiribal üks järgmistest nuppudest. (Need nupud on saadaval ainult siis, kui valitud tehingute kogu jaoks on olemas asjakohased sisestused.)

    - **Sihtkanded** – vaadake üle asjakohased töölehed ja muud tüüpi dokumendid, mis valitud tehing genereeris.
    - **Kaubad** – vaadake üle vastavad müügi- või ostutellimused, mis loodi valitud tehinguga.

1. Kuvatakse vastavate töölehtede, dokumentide või üksuste loend. Mis tahes töölehe, dokumendi või üksuse kohta lisateabe saamiseks valige selle rida ja seejärel valige toimingupaanil suvand **Kuva üksikasjad**.
