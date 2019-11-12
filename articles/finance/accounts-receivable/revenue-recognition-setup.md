---
title: Tulu tuvastamise seadistus
description: Selles teemas kirjeldatakse tulude tuvastamise seadistamise suvandeid ja nende mõjusid.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 73acfc92777b8fe07b89bea782e13213d38000cd
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570329"
---
# <a name="revenue-recognition-setup"></a>Tulu tuvastamise seadistus
[!include [banner](../includes/banner.md)]

Lisatud on moodul **Tulu tuvastamine**, mis sisaldab kõiki seadistamiseks vajalikke menüü-üksusi. Selles teemas kirjeldatakse seadistamise suvandeid ja nende mõjusid.

> [!NOTE]
> Tulu tuvastamise funktsiooni ei saa funktsioonihalduse kaudu sisse lülitada. Praegu peate selle sisselülitamiseks kasutama konfiguratsioonivõtmeid.

Moodulil **Tulu tuvastamine** on järgmised seadistussuvandid.

- Tulu tuvastamise töölehed
- Tulu tuvastamise parameetrid
- Tulugraafikud 
- Varude seadistamine

    - Kaubagrupid ja väljastatud tooted
    - Tulugraafiku määratlemine
    - Tulu hinna määratlemine

        - Sisestusreeglid
        - Kogumid

    - Kogumi komponendid
    - Kogumi kaup

- Projekti seadistus

## <a name="revenue-recognition-journals"></a>Tulu tuvastamise töölehed

Tulu tuvastamisele on lisatud uus töölehe tüüp. Tööleht on vajalik ja seda kasutatakse kahes stsenaariumis.

Esimene stsenaarium leiab aset pärast kõigi lepinguliste kohustuste täitmist, kui tuvastatakse edasilükkunud tulu, luues tulu tuvastamise töölehe, mis põhineb tulugraafiku üksikasjadel. Tööleht sisaldab raamatupidamise kirjet, mis teisaldab saldo edasilükkunud tulu pearaamatukontolt tulu pearaamatukontole.

Teine stsenaarium leiab aset siis, kui pärast ümberjaotamist luuakse tööleht. Ümberjaotamine toimub siis, kui müügitellimuse rida lisatakse eelnevalt arveldatud müügitellimusele või kui luuakse uus müügitellimus, mis sisaldab rida, mis on algse lepingu osa. Kui arve sisestati enne uue müügitellimuse rea lisamist, tuleb sisestatud kliendiarvele luua korrigeeriv raamatupidamise kirje.

Tööleht seadistatakse lehel **Töölehe nimed** (**Tulu tuvastamise \> Seadistus \> Töölehe nimed**). Töölehe tüübiks peab olema määratud **Tulu tuvastamine**. Tulu tuvastamise töölehel saate valida sisestamiskihi, kuhu sisestada.

## <a name="parameters-for-revenue-recognition"></a>Tulu tuvastamise parameetrid

Tulu tuvastamise sätted konfigureeritakse lehe **Pearaamatu parameetrid** vahekaardil **Tulu tuvastamine** (**Tulu tuvastamine \> Seadistus \> Pearaamatu parameetrid**). Saadaval on järgmised sätted.

- **Tulu tuvastamise töölehe nimi** – valige tööleht, mis loodi tulu tuvastamiseks. Tööleht on vajalik siis, kui tulu tuvastatakse tulugraafikust või kui teete juba arveldatud müügitellimuse ümberjaotamise.
- **Luba allahindluse eraldamise meetod** – määrake selle suvandi olekuks **Jah**, et määratleda tulu hind iga väljastatud toote tulu hinnas määratud õiglase turuväärtuse eraldamise alusel. See eraldamine hõlmab rea allahindluste eraldamist kaupade lõikes. Kui selle suvandi olekuks on määratud **Ei**, kasutab süsteem iga väljastatud toote tulu hinnas määratletud keskmist hinda. Kui selle suvandi olekuks on määratud **Ei**, kuid väljastatud toodetele ei ole keskmist hinda määratud, siis tulu hinna eraldamist ei toimu.
- **Kaasa päise allahindlused** – määrake see suvand olekusse **Jah**, et määratleda tulu hind, eraldades päise allahindlused toodete lõikes. Kui see suvand on määratud olekusse **Ei**, siis ei kaasata päise allahindlust tulu hinna eraldamisse.
- **Keela lepingutingimused** – määrake see suvand olekusse **Jah**, kui tooted, millel on tulu tüüp **Lepingujärgne tugi**, saab väljastada ka siis, kui neile poole määratud lepingu algus- ja lõppkuupäevi. Tavaliselt on lepingu algus- ja lõppkuupäevad tulu tüübiga **Lepingujärgne tugi** kaupade korral nõutavad. Kui lepingu algus- ja lõppkuupäev ei ole määratud, arvutatakse tulugraafiku üksikasjad sisestamisel juhtumite arvu ja arve kuupäeva põhjal.
- **Arvete korrigeerimiste sisestamine müügireskontrole ümberjaotamisel** – kui teete juba sisestatud arvete ümberjaotamist, tuleb sisestatud arve raamatupidamise kirjet korrigeerida. Kasutage seda suvandit korrigeerimisviisi määramiseks.

    - Määrake see suvand olekusse **Ei**, et piirata korrigeeriva kande sisestamist pearaamatusse. Kui see suvand on määratud olekusse **Ei**, siis ei looda raamatupidamise sisekorrektsiooniks müügireskontros täiendavaid dokumente. Arve tasumisel kasutab tasakaalustusprotsess vana raamatupidamise kirjet, et sisestada kõik skontod või realiseeritud kasumid või kahjumid.
    - Määrake see suvand olekusse **Jah**, et luua müügireskontros korrigeerimiskande jaoks automaatselt stornodokument ja uus arve. Kuna see korrigeerimine on raamatupidamise sisekorrektsioon, siis uusi dokumente ei saadeta ega edastata kliendile. Stornodokument tasakaalustatakse algse arvega ja klient tasub uue korrigeeritud arve. Arvestage, et kõik kolm dokumenti kuvatakse aruannetes, nt kliendi väljavõttel.

[![Seadistusteave](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Tulugraafikud

Tulugraafik tuleb luua igal juhtumil, mil tulu saab edasi lükata. Näiteks, kui teie organisatsioon pakub tuge 6-, 12-, 18- ja 24-kuuliste perioodidega, peate looma iga perioodi jaoks tulugraafiku. Tulugraafiku seadistus määratleb, kuidas eraldatakse tulu hind valitud perioodide arvu lõikes. Samuti määratleb see vaikekuupäevad, mis sisestatakse arve sisestamisel loodavasse tulugraafikusse.

Kui tuvastate tulu vahe-eesmärkide järgi, soovitame teil luua vahe-eesmärkidele tulu tuvastamise graafikud, sõltumata tuvastamiskuupäevadest. Pärast graafikute loomist saate neid redigeerida nii, et need kajastaksid eeldatavaid vahe-eesmärkide kuupäevi. Need kirjed saab panna ootele, kuniks olete saanud teate vahe-eesmärgi täitmisest ja tulu saab tuvastada.

Tulugraafikud luuakse lehel **Tulugraafikud** (**Tulu tuvastamine \> Seadistus \> Tulugraafikud**).

[![Tulugraafikud](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Sisestage kirjeldavad väärtused väljadesse **Tulugraafik** ja **Kirjeldus**. Järgmisi lisasätteid kasutatakse tulugraafiku loomiseks arve sisestamisel.

- **Esinemised** – sisestage tulu edasilükkamise kuude või esinemiste arv.
- **Automaatne ootelepanek** – märkige see ruut, kui arve sisestamisel tuleks kõik tulugraafiku read automaatselt ootele panna. Enne rea edasilükatud tulu tuvastamist tuleb ootelepanek graafiku igalt realt käsitsi eemaldada.
- **Automaatsed lepingutingimused** – märkige see ruut, kui lepingu algus- ja lõppkuupäevad tuleks määrata automaatselt. Need kuupäevad määratakse automaatselt ainult tulu tüübiga **Lepingujärgne tugi** väljastatud toodetele. Lepingu alguskuupäevaks määratakse automaatselt müügitellimuse rea nõutud lähetuskuupäev ja lepingu lõppkuupäevaks määratakse automaatselt kuupäev, mis saadakse, kui alguskuupäevale liidetakse tulugraafiku seadistamisel määratletud kuude või esinemiste arv. Näiteks müügitellimuse real oleval tootel on üheaastane garantii. Vaikimisi on tulugraafik **12 k** (12 kuud) ja selle tulugraafiku märkeruut **Automaatsed lepingutingimused** on valitud. Kui müügitellimuse real on nõutav lähetuskuupäev 16. detsember 2019, siis vaikimisi on lepingu alguskuupäev on 16. detsember 2019 ja lepingu lõppkuupäev 15. detsember 2020.
- **Tuvastamise alus** – tuvastamise alus määratleb, kuidas tulu hind esinemiste lõikes eraldatakse.

    - **Igakuiselt kuupäevade järgi** – summa eraldatakse iga kuu tegelike päevade alusel.
    - **Igakuiselt** – summa eraldatakse võrdselt esinemistes määratletud kuude arvu lõikes.
    - **Esinemised** – summa eraldatakse võrdselt esinemiste lõikes, kuid see võib hõlmata lisaperioodi, kui valite tuvastamisreegliks **Tegelik alguskuupäev**.

- **Tuvastamisreegel** – tuvastamisreegel määratleb arvele tulugraafikus määratavad vaikekuupäevad.

    - **Tegelik alguskuupäev** – graafiku loomisel kasutatakse kas lepingu alguskuupäeva (lepingujärgse toe \[TK\] kaupade korral) või arve kuupäeva (oluliste ja ebaoluliste kaupade korral).
    - **Kuu esimene** – lepingu alguskuupäevaks (või arve kuupäevaks) on graafiku esimese rea kuupäev. Kuid kõigi järgnevate graafikute read luuakse kuu esimese jaoks.
    - **Tükeldamine kuu keskel** – graafiku esimese rea kuupäev sõltub arve kuupäevast. Kui arve sisestatakse esimesest kuni viieteistkümnenda kuupäevani, luuakse tulugraafik kuu esimese päeva alusel. Kui arve sisestatakse alates kuueteistkümnendast kuupäevast, luuakse tulugraafik järgmise kuu esimese päeva alusel.
    - **Järgmise kuu esimene** – graafiku kuupäevaks on järgmise kuu esimene päev.

Klõpsake nuppu **Tulugraafiku üksikasjad**, et vaadata üldisi perioode ja igas perioodis tuvastatud protsente. Vaikimisi on **Tuvastamise protsendi** väärtus jaotatud perioodide arvu lõikes võrdselt. Kui tuvastamise aluseks on kas **Igakuine** või **Esinemised**, saab tuvastamise protsenti muuta. Tuvastamise protsendi muutmisel teavitab hoiatusteade teid, et koguväärtus ei võrdu 100 protsendiga. Kui saate teate, saate jätkata ridade redigeerimist. Kuid enne lehe sulgemist peab koguväärtus võrduma 100 protsendiga.

[![Tulugraafiku andmed](./media/revenue-recognition-revenue-schedule-details.png)](./media/revenue-recognition-revenue-schedule-details.png)

## <a name="inventory-setup"></a>Varude seadistamine

Saate tuvastada müügitellimustes väljastatud toodete tulu, kuid mitte müügitellimuste müügikategooriates või vabas vormis arvetes, kui dokumenti ei ole kaasatud kaupu. Väljastatud toodete seadistamisel tehtavad valikud määravad, kuidas kauba tulu tuvastatakse. Näiteks määratlevad valikud, kas tulu hind eraldatakse ja kas tulu lükatakse tulugraafikut kasutades edasi.

Seadistamist saab alustada lehe **Kaubagrupp** kiirkaardil **Tulu tuvastamine** (**Tulu tuvastamine \> Seadistus \> Varude ja toote seadistus \> Kaubagrupp**). Lehel on mitu seadistusvälja. Neid välju kasutatakse vaikeväärtuste määramiseks ainult süsteemis loodavatele uutele väljastatud toodetele. Uute toodete loomisel sisestatakse siin määratud väärtused kaubagrupi jaoks vaikimisi. Väljastatud toodete vaikeväärtused saate alistada lehel **Väljastatud tooted** (**Tulu tuvastamine \> Seadistus \> Varude ja toote seadistus \> Väljastatud tooted**). Väljastatud toodete jaoks määratatud vaikeväärtused kantakse seejärel müügitellimusele edasi.

## <a name="item-groups-and-released-products"></a>Kaubagrupid ja väljastatud tooted

### <a name="define-the-revenue-schedule"></a>Tulugraafiku määratlemine

Müügitellimuse rea tulu lükatakse edasi, kui väljastatud toote jaoks on määratud tulugraafik ja seda kasutatakse vaikimisi müügitellimuse real. Kui seda sätet tuleks kasutada tootel vaikimisi, saate lehe **Kaubagrupp** kiirkaardil **Tulu tuvastamine** määratleda tulugraafiku (**Tulu tuvastamine \> Seadistus \> Varude ja toote seadistus \>Kaubagrupp**). Lehe **Väljastatud tooted** kiirkaardil **Tulu tuvastamine** saate määratleda ka väljastatud toote sätte (**Tulu tuvastamine \> Seadistus \> Varude seadistus \> Väljastatud tooted**).

Väljal **Tulugraafik** valige tulugraafik, mis tähistab perioodi, millele tulu tuleb edasi lükata. Tulugraafik sisestatakse automaatselt müügitellimuse reale ja müügitellimuse arve sisestamisel luuakse graafiku üksikasjad.

### <a name="define-the-revenue-price"></a>Tulu hinna määratlemine

Kaubagrupid ja väljastatud tooted saab seadistada kas keskmise hinna meetodil või allahindluse eraldamise meetodil. Mõlema meetodi korral tuleb lehel **Väljastatud tooted** määrata mitmesuguseid sätteid.

- **Kas tulu eraldamine on aktiivne** – määrake see suvand olekusse **Jah**, et kaasata väljastatud toode tulu eraldamise arvutamisse. Kui selle suvandi olekuks on määratud **Ei**, kasutab väljastatud toode keskmise hinna meetodit, kui keskmine hind on määratletud. Kui keskmine hind ei ole määratletud, kasutatakse tulu või edasilükkunud tulu sisestamiseks müügitellimuse rea ühikuhinda.
- **Tulu tüüp** – valige tulu tüüp, mis määratleb väljastatud toote.

    - **Oluline** – kaup on organisatsiooni tulu esmane allikas. See on väärtus on vaikesäte.
    - **Ebaoluline** – kaup ei ole organisatsiooni tulu esmane allikas. Kui kasutatakse keskmise hinna sätteid, siis lõigatakse hind välja keskmise hinnani ja seejärel eraldatakse. Näiteks on olulisel kaubal fikseeritud hind, mis tuleb tuluna tuvastada. Kui on olemas allahindlus, võidakse allahindlus olulise kauba tulust välja lõigata, kuid **ainult** kuni fikseeritud hinna summani. Ülejäänud allahindlus võetakse välja ebaoluliste kaupade tulust. Teise võimalusena ei pruugita allahindlust olulise kauba tulust välja lõigata.
    - **Lepingujärgne tugi** – kaup toetab muid kliendile müügis sisalduvaid elemente. Tulu hind jaotatakse müügis sisalduvate oluliste ja ebaoluliste toodete lõikes. Sõltuvalt seadistusest ei pruugi TK-kaubad nõuda müügitellimuse real lepingu algus- ja lõppkuupäeva määratlemist.

- **Välista väljalõikest** – määrake see suvand olekusse **Jah**, et näidata, et kauba keskmist hinda ei saa korrigeerida madalamaks määratletud miinimumprotsendist või kõrgemaks maksimumprotsendist. Mis tahes tulu hind tuletatakse müügitellimusse kaasatud mõne teise väljastatud toote tulu hinnast. Kui see suvand on määratud olekusse **Ei**, saab kauba keskmist hinda korrigeerida või välja lõigata. Arvestage, et kui te müüte rohkem kui ühte kaupa, mis on seadistatud keskmise hinnana, tuleb vähemalt üks väljastatud toode seadistada nii, et selle suvand **Välista väljalõikest** on määratud olekusse **Ei**. Sel viisil on olemas vähemalt üks kaup, millele saab eraldada tulu hinna erinevusi.
- **Keskmine hind** – määrake see suvand olekusse **Jah**, et näidata, et kauba tulu hinda tuleks korrigeerida nii, et see võrdub keskmise hinnaga, kui see on väiksem teie määratletud miinimumhälbest või suurem maksimumhälbest, ning et väljalõigatud summa tuleks eraldada ridadele, millel on tooted, mille suvand **Välista väljalõikest** on määratud olekusse **Ei**.

    - **Maksimumhälve** – sisestage lubatud protsent üle keskmise hinna.
    - **Miinimumhälve** – sisestage lubatud protsent alla keskmise hinna.

Kui olete väljastatud toote sätete konfigureerimise lõpetanud, peate käsitsi määratlema tulu hinna, sisestades õiglase väärtuse hinna või keskmise hinna (kui kasutate keskmise hinna meetodit) lehel **Tulu hinnad** (avage **Tulu tuvastamine \> Seadistus \> Varude seadistus \> Väljastatud tooted** ning seejärel valige tegumiribal vahekaardil **Müük** grupis **Tulu tuvastamine** suvand **Tulu hinnad**).

[![Tulu hinnad](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Sellel lehel käsitsi määratud tulu hinda kasutatakse iga müügitellimuse tulu hinna eraldamise määratlemiseks määratud kriteeriumite alusel. Iga kriteerium vastendatakse müügitellimuse reaga, et määrata tulu hind, mida tuleks eraldamise protsessis kasutada.

- **Kauba kood** ja **Kauba seos** – tulu hinna saab määrata üksikule tootele või tootegrupile. Kui valite väljal **Kauba kood** üksuse **Tabel**, valige väljal **Kauba seos** väljastatud toode. Kui valite väljal **Kauba kood** üksuse **Grupp**, valige väljal **Kauba seos** kaubagrupp.
- **Konto kood** ja **Konto/grupi number** – tulu hinna saab määrata kõigile klientidele, üksikule kliendile või klientide grupile. Kui valite väljal **Konto kood** üksuse **Kõik**, kasutatakse hinda kõigil klientidel. Kui valite väljal **Konto kood** üksuse **Tabel**, valige väljal **Konto/grupi number** klient. Kui valite väljal **Konto kood** üksuse **Grupp**, valige väljal **Konto/grupi number** kliendigrupp.
- **Valuuta** – peate sisestama eraldi tulu hinna iga valuuta kohta, mille müügitellimusse sisestate. Näiteks kui müüte praegu USA dollarites, Kanada dollarites ja eurodes, peate määratlema tulu hinna kõigis kolmes valuutas. Tulu hinda ei teisendata ühest valuutast, nt arvestusvaluutast, teistele kasutatavatele tehingu valuutadele.
- **Summa või protsent hinnakirjast** – määrake, kas tulu hind on seadistatud summana või protsendina hinnakirja hinnast. Kui valite **Protsent hinnakirjast**, saavad kasutajad summa asemel sisestada keskmise hinna protsendina hinnakirja hinnast. Väärtust **Protsent hinnakirjast** kasutatakse ainult TK-kaubana seadistatud väljastatud toodetel.
- **Tulu eraldamise hind** – sõltuvalt väljal **Summa või protsent hinnakirjast** valitud väärtusest sisestage kas summa või protsent, et tähistada tulu hinda, mida kasutatakse tulude eraldamiseks müügitellimuse elementide lõikes.
- **Alguskuupäev** ja **Lõppkuupäev** – sisestage kuupäevavahemik, mille vältel on tulu hind aktiivne. Need väljad pole kohustuslikud.

Kui lehel **Pearaamatu parameetrid** on suvand **Luba allahindluse eraldamise meetod** määratud olekusse **Jah** ning väljastatud toote **Tulu tüüp** on määratud olekusse **Lepingujärgne tugi**, peate määrama ka kaubad, mida väljastatud toode toetab. See seadistus tehakse lehel **Seadistuse alus** (avage **Tulu tuvastamine \> Seadistus \> Varude seadistus \> Väljastatud tooted** ning seejärel valige tegumiribal vahekaardil **Müük** grupis **Tulu tuvastamine** üksus **Seadistuse alus**).

Lehel **Seadistuse alus** lisage kirje iga kaubagrupi kohta, mida kaup toetab. Kui tulu eraldamine toimub, jaotatakse tulu hind TK-kauba oluliste ja ebaoluliste osade lõikes.

### <a name="posting-profiles"></a>Sisestusreeglid

Tulu edasilükkamise võimalust toetavad kolm täiendavat sisestustüüpi. Need sisestustüübid seadistatakse lehe **Sisestamine** vahekaardil **Müügitellimus** (**Tulu tuvastamine \> Seadistus \> Varude ja toote seadistus \> Sisestamine**).

- **Edasilükatud tulu** – sisestage põhikonto tulu hinnale, mis sisestatakse edasilükatud tulule (tulu asemel). Tulu hind lükatakse edasi, kui müügitellimuse real on tulugraafik.
- **Edasilükatud tuletusreegel** – sisestage põhikonto tuletusreegli summale, mis sisestatakse edasilükatud tuletusreeglile, kui tulu on samuti edasi lükatud.
- **Osaline arve tulu kliiring** – sisestage põhikonto kliiringukontole, mida kasutatakse kas müügitellimuse osalisel arveldamisel või ümberjaotamise toimumisel. Selle konto saldo naaseb väärtusele 0 (null), kui müügitellimused on täielikult arveldatud.

### <a name="bundles"></a>Kogumid

Kogumi kaubad on unikaalsed väljastatud tooted, mis on seadistatud nii, et need sisaldavad komponente. Seadistus tehakse koosluse (BOM) funktsiooni abil. Kui müügitellimusele sisestatakse kogumi kaup, kasutatakse tulu hindade ja tulugraafikute määramiseks üksikuid komponente. Kuid kliendi prinditud dokumendid, nt müügitellimus ja arve, kajastavad siiski kogumi kaupa.

#### <a name="bundle-components"></a>Kogumi komponendid

Kogumisse kaasatud komponendid tuleb seadistada lehel **Väljastatud tooted** (**Tulu tuvastamine \> Seadistus \> Varude ja toote seadistus \> Väljastatud tooted**). Need komponendid on väljastatud tooted ja need tuleb seadistada samal viisil kui kooslusesse kaasatud tooted. Näiteks võib väljastatud toode olla tüübi **Kaup** või tüübi **Teenus** kaup, kuid see tuleb määrata kauba mudeli gruppi, kus suvand **Ladustatav toode** on määratud olekusse **Jah**. Lisateabe saamiseks vt koosluse kaupade seadistamise dokumentatsiooni.

Komponendid tuleb seadistada ka tulu tuvastamiseks, nagu oleksid need tooted, mida saab müüa müügitellimuses ükshaaval. Näiteks veenduge, et iga komponendi jaoks oleks määratletud õige tulu hind ja et TK-kaupadele oleks seadistatud hinna alus.

#### <a name="bundle-items"></a>Kogumi kaubad

Kogumi kauba seadistamisel tuleb lehel **Väljastatud tooted** määrata kaks välja (**Tulu tuvastamine \> Seadistus \> Varude ja toote seadistus \> Väljastatud tooted**).

- Kiirkaardil **Projekteeri** väljal **Tootmise tüüp** peab kaup olema seadistatud kui koosluse kaup.
- Kiirkaardil **Üldine** väljal **Kogum** peab kaup olema märgitud kogumi kaubana.

Seejärel tuleb komponendid lehel **Koosluse versioonid** määrata kogumi/koosluse emakaubale (avage **Tulu tuvastamine \> Seadistus \> Varude ja toote seadistus \> Väljastatud tooted** ning seejärel valige tegumiribal vahekaardil **Projekteeri** grupis **Kooslus** üksus **Koosluse versioonid**). Lisateabe saamiseks vt koosluste seadistamise dokumentatsiooni.

[![Väljastatud tooted, koosluse graafikud](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Kui kogumi emakaup ja kogumi komponendid on määratud eraldama, jaotatakse kogumi tulu hind komponentidele nende tulupanuse protsendi alusel.

## <a name="project-setup"></a>Projekti seadistus

Tulu tuvastamist saab kasutada ka müügitellimustel, mis luuakse aja- ja materjalikulu projekti kaudu. Projektidest pärinevate müügitellimuste korral tuleb teil lihtsalt määratleda projekti sisestusprofiilides põhikontod, mida kasutatakse projekti arvete sisestamiseks. Põhikontod määratletakse lehel **Pearaamatu sisestamise seadistus** (**Tulu tuvastamine \> Seadistus \> Projekti seadistus \> Pearaamatu sisestamise seadistus**).

- **Edasilükatud arve tulu** (**Tulukontod** all) – sisestage põhikonto tulu hinnale, mis sisestatakse edasilükatud tulule (tulu asemel). Tulu hind lükatakse edasi, kui müügitellimuse real on tulugraafik.
- **Edasilükatud tulu** (**Kulukontod** all) – sisestage põhikonto tuletusreegli summale, mis sisestatakse edasilükatud tuletusreeglile, kui tulu on samuti edasi lükatud.
