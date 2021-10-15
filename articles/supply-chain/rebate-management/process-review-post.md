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
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 803b4d8b287f2b0dc523654e3e1852209f4ea039
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573533"
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

## <a name="create-source-transactions"></a>Lähtekannete loomine

Saate luua müügi- või ostutellimusi, millel on lähtetehingud kas enne või pärast rakendatava tagasimaksehalduse tehingu loomist.

Iga tehingurea saate seadistada nii, et see loob automaatselt tagasimaksepakkumise, konteerides müügitellimuse või ostutellimuse tarne või arve. Seadke tehingurea välja **Tehingu liik** väärtuseks *Tarne* või *Arve* ja seadke suvandi **Protsess sisestamisel** väärtuseks *Jah*. Kui välja **Tehingu liik** väärtuseks on seatud *Tellimus*, on töötlemine sisestamisel keelatud. Lähtetehingute puhul, mis loodi pärast tehingu aktiveerimist, saate siiski seda sätet töödelda, nagu on kirjeldatud selle teema jaotises [Protsessi tagasimaksehalduse tehingud](#process-deals).

### <a name="enable-price-details"></a>Hinna üksikasjade lubamine

Enne lähtekannete loomist peate lubama müügireskontro **Hinna üksikasjade lubamine** suvandi.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
1. Määrake vahekaardil **Hinnad** kiirkaardil **Hinna üksikasjad** suvandi **Luba hinna üksikasjad** väärtuseks *Jah*.

### <a name="create-a-source-transaction"></a>Lähtekande loomine

Lähtekande loomiseks toimige järgmiselt.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige suvand **Uus**.

    Tagasimaksenõuete loomise viisi matkimiseks peate looma müügitellimuse, kus toode ja kogus kvalifitseerivad kõnealuse kliendi tagasimakse saamiseks.

1. Sisestage või valige väljale **Kliendikonto** klient, kes vastab tagasimaksetehingu tingimustele.
1. Müügitellimuse loomiseks valige **OK**.
1. Lisage kiirkaardil **Müügitellimuse read** järgmiste väljadega rida.

    - **Kaubakood** – määrake kaup, mis vastab tagasimakse tingimustele.
    - **Kogus** – määrake kogus, mis vastab tagasimaksetehingu tingimustele, mis sisaldab rida, mille välja **Alus** väärtuseks on seatud *Kogus*.
    - **Ühiku hind** – määrake kogus, mis vastab tagasimaksetehingu tingimustele, mis sisaldab rida, mille välja **Alus** väärtuseks on seatud *Väärtus*.
    - **Sait** – valige sait, kus toode on saadaval ja mis vastab tagasimaksetehingu tingimustele.
    - **Ladu** – valige ladu, kus toode on saadaval ja mis vastab tagasimaksetehingu tingimustele.

1. Tööriistaribal **müügitellimuse ridade** kiirkaardil valige **Müügitellimuse rida \> Hinna üksikasjad**. See käsk on saadaval ainult siis, kui lubasite hinna üksikasjad, nagu on kirjeldatud eelmises jaotises.
1. Valige lehelt **Hinna üksikasjad** kiirkaart **Tagasimaksehaldus**. Sellel kiirkaardil on toodud kõik tagasimaksehalduse tehingud, mis kehtivad praeguse tellimuserea puhul, ja hinnanguline tagasimaksesumma tellimuse valuutas. Pange tähele, et summad on ainult tulevaste tagasimaksenõuete hinnangud. Tegelikud tagasimaksesummad võivad erineda. Siin on mõned tegurid, mis võivad mõjutada tegelikke summasid:

    - Müügi kogumaht, mille klient saavutas perioodilise tagasimakselepingu alusel.
    - Kas klient tagastas kõik kogused või osalised kogused.
    - Kas rakendatav müügitellimus saavutas kandetüübi (*Tellimus, Tarne* või *Arve*), mis on määratletud tagasimakse haldustehingu jaoks.
    - Tehingu **väljund** väärtus. Tühi tagasimaksesumma kuvatakse tehingute puhul, mille välja **Väljund** väärtuseks on seatud *Kaup*.

1. Pange tähele, et kiirkaardil **Üksikasjad** sisaldab **veerise hindamise** jaotis järgmisi välju. Need väljad lisatakse tagasimaksehalduse abil. Kõik need näitavad väärtusi ühiku kohta (kiirkaardi **Tagasimaksehaldus** väljadel kuvatakse rea koguväärtused).

    - **Tagasimaksehalduse tagasimakse summa** (ainult müügitellimused)
    - **Tagasimakse haldamise autoritasu summa** (ainult müügitellimused)
    - **Tagasimaksehalduse müüja tagasimakse summa** (müügi- ja ostutellimused)

1. Sulgege leht **Hinna üksikasjad**.
1. Kui müügitellimus ei vasta äsja vaadatud allahindlustele, tehke allahindluste välistamiseks neid samme. (Kuid tavaliselt ei välista te allahindlusi.)

    1. Valige kiirkaardil **Müügitellimuse read** asjakohane rida.
    1. Seadke kiirkaardi **Rea üksikasjad** vahekaardil **Hind ja allahindlus** suvandi **Välista tagasimaksehaldusest** väärtuseks *Jah*. See valik ei rakendu ostutellimustele. Lisaks jäetakse välja ainult kliendi mahaarvestused, kui selle suvandi väärtuseks on seatud *Jah*. Kliendi litsentsitasude tagasimaksed ja müüja tagasimaksed kehtivad endiselt.

1. Valige toimingupaani vahekaardi **Korje ja pakendamine** grupis **Loo** väärtus **Sisesta saateleht**.
1. Kiirkaardi **Parameetrid** väljal **Kogus** valige *Kõik*.
1. Valige nupp **OK**.
1. Kui teil palutakse töö kinnitada, klõpsake valikut **OK**.
1. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
1. Kiirkaardi **Parameetrid** väljal **Kogus** valige *Kõik* või *Pakendi silt*.
1. Valige nupp **OK**.
1. Kui teil palutakse töö kinnitada, klõpsake valikut **OK**.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>Tagasimaksehalduse tehingute töötlemine

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

### <a name="process-deals-by-using-the-rebate-workbench"></a>Tehingute töötlemine tagasimakse tööpingi abil

Kindlate tehingu või tehingu ridade töötlemise asemel võite mitme samaaegse tehingu töötlemiseks kasutada *tagasimakse töölauda*. Võite valikuliselt rakendada kirjefiltreid ja/või seadistada korduva graafiku. Te ei pea ridu valima. Süsteem töötleb kõiki ridu, mis vastavad teie seadistatud kuupäeva- ja filtrinõuetele.

Pakkumiste töötlemiseks tagasimakse töölaua abil tehke järgmist.

1. Minge **Tagasimaksehaldus \> Tagasimaksete haldusse tehingud \> Tagasimakse töölaud**.
1. Tegevuspaani vahekaardil **Tagasimakse töölaud** valige grupi **Töötlemine** jaoks üks järgmistest käskudest:

    - **Töötlemine \> Ettevalmistamine** – tehke iga asjakohase tehingu rea puhul tekkepõhine ettevalmistus, kuid ärge sisestage kogunenud summasid.
    - **Töötlemine \> Tagasimakse haldus** – töötlege kannete seeriat, mis annab tagasimakse väärtuse igale reale.
    - **Protsess \>Mahakandmine** - töödelge eraldiste ja allahindluste haldamise erinevused, mis postitatakse iga allikatehingu kohta allahindlustehingu ja määratud perioodi kohta.

1. Dialoogiaknas **Tagasimaksehaldus** jaotises **Periood** kuvatavas dialoogiboksis väljad **Alates kuupäevast** ja **Kuni kuupäevani**, et määrata kalkulatsiooni kuupäevavahemik.
1. Kuvatavas jaotises **Garantiiperiood** määrake väljad **Alates kuupäevast** ja **Kuni kuupäevani**, et määrata kalkulatsiooni garantiivahemik.
1. Kiirkaardil **Kirjeid, mida kaasata** saate seadistada filtreid, ,mis piiravad partiitöö töödeldavaid tehinguid. Need sätted töötavad samamoodi, nagu need töötavad teist tüüpi partiitööde puhul.
1. Vajadusel saate seadistada partiitööde töötlemise ja plaanilimise suvandid kiirkaardil **Taustal käitamine**. Need sätted töötavad samamoodi, nagu need töötavad teist tüüpi partiitööde puhul.
1. Kalkulatsiooni käivitamiseks ja/või plaanimiseks valige **OK**.

## <a name="view-and-edit-rebate-management-transactions"></a>Tagasimaksehalduse kannete kuvamine ja redigeerimine

Ühe või mitme tehingu töötlemise ajal loob süsteem kanded, mida saate vaadata ja võib-olla redigeerida enne nende sisestamist.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>Tagasimaksehalduse kannete kuvamine ja redigeerimine tagasimaksetehingute loendilehe abil

Tagasimaksete haldamise tehingute vaatamiseks ja muutmiseks allahindlustehingute loendi lehe kaudu tehke järgmist.

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

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>Tagasimaksehalduse kannete kuvamine ja redigeerimine tagasimakse töölaua abil

Tagasimaksete haldamise tehingute vaatamiseks ja muutmiseks allahindlustöölaua kaudu tehke järgmist.

1. Minge **Tagasimaksehaldus \> Tagasimaksete haldusse tehingud \> Tagasimakse töölaud**.
1. Seadke välja **Näita** väärtuseks *Sisestamata*.
1. **Tagasimakse tööpingi** lehel kuvatakse kannete loend. Iga tehing sisaldab asjakohaseid üksikasju. Need üksikasjad varieeruvad sõltuvalt kande tüübist. Sellel lehel saate teha järgmisi toiminguid.

    - Mis tahes kande kohta lisateabe vaatamiseks valige see ja seejärel valige vahekaart **Üldine**, **Finantsdimensioon** või **Dimensioon**.
    - Kui kasutate nõuete protsessi, saate kanded märkida kas taotletud või taotlemata tehinguteks. Valige asjakohased read ja siis minge tegevuspaani vahekaardile **Tagasimakse töölaud** ja valige üks järgmistest käskudest. (Nõudeprotsesse saab lubada lehel [**Tagasimaksehalduse parameetrid**](rebate-management-parameters.md).)

        - **Märgi tehtuks** – märkige valitud kanded tehtuks.
        - **Märgi tegemata** – märkige valitud kanded staatusesse tegemata.

    - Ühe või mitme rea nõude sisestamiseks valige vastavad read. Seejärel toimingupaanil vahekaardil **Tagasimakse töölaud** valige suvand **Sisesta**. Nupp **Sisesta** on saadaval ettevalmistus-, tagasimakse- ja mahakandmiskannete jaoks. Dialoogiaknas **Sisesta** määratakse automaatselt väljad **Alates** ja **Kuni**. Määrake **Sisestamise kuupäeva** väli ja valige seejärel **OK**.
    - Avatud või sisestamata kande puhul kuvatava summa korrigeerimiseks valige kanne ja järgige seejärel toimige järgmiselt.

        - Redigeerige väärtust väljal **Parandatud summa**.
        - Toimingupaanil vahekaardil **Tagasimakse töölaud** valige suvand **Määra parandus**. Seejärel sisestage väärtus ripploendisse, mis kuvatakse väljal **Parandatud summa**.

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

### <a name="post-transactions-by-using-the-rebate-workbench"></a>Sisestage tehingud allahindluse töölaua abil

Pärast kannete töötlemist, tagasimakset või mahakandmist järgige neid samme tagasimakse töölaua kasutamiseks, et üle vaadata ja sisestada ühe või mitme konkreetse kanderead kõigi tehingute jaoks.

1. Minge **Tagasimaksehaldus \> Tagasimaksete haldusse tehingud \> Tagasimakse töölaud**.
1. Valige ruudustikus rida iga tehingurea jaoks, mille soovite postitada. Saate valida sisestamata sätted, tagasimakse ja/või mahakandmiskanded. Kehtivad järgnevad reeglid.

    - Süsteem sisestab ka kõik read, mille **tagasimakse kande numbri** väärtus on sama kui ridadel, mille valite.
    - Süsteem ei sisesta ühtegi *tagasimakse* kande tüüpi rida, mis pole märgitud nõudeks.
    - Kui valite juba sisestatud read, jätab süsteem sisestatud read vahele.
    - Nupp **Sisesta** on saadaval ainult siis, kui valite vähemalt ühe sisestamata rea.

1. Tehke toimingupaani vahekaardil **Tagasimakse töölaud** grupis **Töötlemine** valik **Sisesta**.
1. Määrake väli **Sisestamise kuupäev** **Sisesta** dialoogiboksis. Väljad **Alates** ja **Kuni** seatakse automaatselt, mis põhineb valitud ridade varaseimal **alates** ja viimasel väärtusel **Kuni**.
1. Klõpsake kannete sisestamiseks nuppu **OK**.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>Tagasimakse halduse töölehtede ülevaade

Pärast kannete sisestamist saate üle vaadata tulemuseks saadud töölehed, dokumendid või üksused. Tagasimaksete ja tagasimaksete sihtkanded põhinevad sisestusprofiilis määratud maksetüübil ja tagasimakse väljundi tüübil. Näiteks, kui tagasimakse väljamineku väärtuseks on seatud *Kaup*, luuakse müügitellimus kliendi tagasimakse jaoks ja ostutellimus luuakse hankija tagasimakse jaoks. Neid tellimusi saab vaadata sihtkannete kaudu. Teise võimalusena, kui makse on seatud võlgnevuse kasutamiseks, luuakse kliendi jaoks seadistatud müüja arve kliendi tagasimaksete jaoks.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>Vaadake töölehti allahindlustehingute loendi lehe kaudu

Tagasimaksehalduse tehinguga seotud töölehe sisestuste ülevaatamiseks toimige järgmiselt.

1. Avage sobiv [tagasimakse tehingud loendileht](rebate-management-deals.md) tehingu tüübi jaoks, mida soovite kasutada.
1. Valige tehing, mille kohta kontrollida töölehe sisestusi.
1. Tegevuspaani vahekaardil **Tagasimaksehalduse tehingud** grupis **Kanded** valige kas **Kanded** või **Garanteeritud kanded**, sõltuvalt kannete tüübist, mida soovite vaadata.
1. Seadke välja **Näita** väärtuseks *Kõik* või *Sisestatud*.
1. Otsige ja valige kandekogum, mida soovite kontrollida ning seejärel valige tegumiribal üks järgmistest nuppudest. (Need nupud on saadaval ainult siis, kui valitud tehingute kogu jaoks on olemas asjakohased sisestused.)

    - **Sihtkanded** – vaadake üle asjakohased töölehed ja muud tüüpi dokumendid, mis valitud tehing genereeris.
    - **Kaubad** – vaadake üle vastavad müügi- või ostutellimused, mis loodi valitud tehinguga.

1. Kuvatakse vastavate töölehtede, dokumentide või üksuste loend. Mis tahes töölehe, dokumendi või üksuse kohta lisateabe saamiseks valige selle rida ja seejärel valige toimingupaanil suvand **Kuva üksikasjad**.

### <a name="review-journals-by-using-the-rebate-workbench"></a>Töölehtede ülevaatus tagasimakse tööpingi abil

Töölehtede ülevaatamiseks tagasimakse töölaua abil tehke järgmist.

1. Minge **Tagasimaksehaldus \> Tagasimaksete haldusse tehingud \> Tagasimakse töölaud**.
1. Seadke välja **Näita** väärtuseks _Kõik_ või _Sisestatud_.
1. Leidke ja valige rida, mida soovite kontrollida. Seejärel tehke tegumiriba vahekaardil **Allahindluse tööleht** grupis **Kuva** valik **Sihtkanded**. See nupp on saadaval ainult siis, kui valitud rea kohta on asjakohased postitused.
1. Kuvatakse vastavate töölehtede, dokumentide või üksuste loend. Mis tahes töölehe, dokumendi või üksuse kohta lisateabe saamiseks valige selle rida ja seejärel valige toimingupaanil suvand **Kuva üksikasjad**.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Tagasimaksehalduse kanded mahaarvamise töölaual

Kui sisestate tagasimaksehalduse kande, mil on üks järgmistest **makse tüübi** väärtustest, loob süsteem kliendi mahaarvamise töölehe või vabas vormis arve vastavale kliendi kontole:

- Kliendi mahaarvamised
- Maksuarve kliendi mahaarvamised
- Kaubanduskulud
- Aruandlus

Pärast sihtkande loomist ja sisestamist on see saadaval avatud kandena **Mahaarvamise töölaua** lehel (**Müük ja turundus \>Kaubandushüvitis \> Mahaarvamised \> Mahaarvamise töölaud**). Avatud kannete **nõudetüübi** väärtus on *Tagasimakse haldus* ja jälituse lubamiseks on saadaval **tagasimakse kandenumbri** väärtus. Kuupäev on määratud tagasimaksehalduse sihtkande sisestuskuupäevale. Mahaarvamise töölaua kasutamiseks avatud kannete tasakaalustamiseks olemasolevate mahaarvamistega sama kliendi konto puhul valige tegevuspaanil suvand **Säilita \> Vastanda**.

Lisateavet vt jaotisest [Mahaarvamiste haldamine mahaarvamise töölaual](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Sisestamata kannete likvideerimine

Pärast kannete töötlemist, tagasimakset või mahakandmist järgige neid samme valitud sisestamata kannete likvideerimiseks.

1. Minge **Tagasimaksehaldus \> Tagasimaksete haldusse tehingud \> Tagasimakse töölaud**.
2. Seadke välja **Näita** väärtuseks *Sisestamata*.
3. Saate otsida ja valida kustutavad kanded. Siis tehke toimingupaani vahekaardil **Tagasimakse töölaud** grupis **Töötlemine** valik **Eemalda**.
4. Sisestamata kannete kustutamiseks klõpsake nuppu **OK**.

## <a name="cancel-a-posted-provision"></a>Sisestatud eraldise tühistamine

Pärast eraldise töötlemist ja sisestamist järgige neid samme sisestatud eraldiskannete tühistamiseks.

1. Minge **Tagasimaksehaldus \> Tagasimaksete haldusse tehingud \> Tagasimakse töölaud**.
2. Seadke välja **Näita** väärtuseks *Sisestatud*.
3. Leidke ja valige tühistamistehingud. Siis tehke toimingupaani vahekaardil **Tagasimakse töölaud** grupis **Töötlemine** valik **Tühista eraldis**.
4. Klõpsake kannete tagasipööramiseks nuppu **OK**.

Need allahindluse tagasipööramised on nähtavad ka vastavatel [tagasimaksehalduse töölehtedel](#review-journals).
