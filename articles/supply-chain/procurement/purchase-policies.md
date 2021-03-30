---
title: Ostupoliitikate ülevaade
description: Selles artiklis antakse teavet ostupoliitikate kohta. Ostupoliitika on reeglite kogum, mis juhib taotluse protsessi. Ostupoliitikad aitavad hankeadministraatoritel hankestrateegiat juurutada, luues poliitikastruktuuri, mis on vastavuses organisatsiooni strateegiliste ostunõuetega.
author: RichardLuan
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage, PurchReqControlRule, RequisitionReplenishCatAccessPolicyRule, PurchReApprovalPolicyRule, RequisitionReplenishControlRule, PurchReqControlRFQRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11614
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8c8fa3e4b59cdb013c1c524e06085b06905715e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215885"
---
# <a name="purchasing-policies-overview"></a>Ostupoliitikate ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet ostupoliitikate kohta. Ostupoliitika on reeglite kogum, mis juhib taotluse protsessi. Ostupoliitikad aitavad hankeadministraatoritel hankestrateegiat juurutada, luues poliitikastruktuuri, mis on vastavuses organisatsiooni strateegiliste ostunõuetega.

Ostupoliitika koosneb poliitikareeglite kogumist. Poliitikareegli määratlemisel valite esmalt reegli tüübi. Seejärel loote reegli tüübi reegli, määratledes reegli sätted, alguskuupäeva ja lõppkuupäeva.  

Näiteks loob administraator poliitika, valib **kataloogi poliitika** reegli tüübi ja lisab siis poliitikale kataloogi poliitika reegli. Kataloogi poliitika reegel määrab, et sisemise hanke puhul tuleb kasutada kataloogi Adventure. Kui ostupoliitika on seostatud konkreetse organisatsiooniga, näevad selle organisatsiooni töötajad taotluste loomisel kataloogi Adventure.

## <a name="assigning-policies-to-organizations"></a>Organisatsioonidele poliitikate määramine
Poliitika jõustumiseks peab see olema organisatsiooniga seostatud. Ostupoliitikad seostatakse **hanke sisejuhtimise** hierarhia eesmärgiga. Seetõttu kehtivad ostupoliitikad ainult organisatsioonidele, mis on hierarhiates, mille hierarhia eesmärk on **hanke sisejuhtimine**. Organisatsioone saate valida ka tabeli CompanyInfo juriidiliste isikute lamedast loendist. Need juriidilised isikud on määratud poliitika raamistikus kui „Ettevõtted”.

## <a name="determining-which-rule-to-apply"></a>Reegli rakendamise määramine
Ostupoliitikate konfigureerimisest olenevalt võivad organisatsiooni kasutajaid mõjutada mitmed reeglid. Järgmised näited illustreerivad erinevaid viise, kuidas konfigureerida ostupoliitikaid ja määrata, kuidas poliitikaid kande tegemisel rakendatakse.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Näide 1: lihtsa ostupoliitika konfigureerimine

Väiksemad ja vähem keerukad organisatsioonid saavad seadistada ostupoliitikaid juriidilise isiku järgi ja kasutada ainult ettevõtete organisatsiooni hierarhiat.  

Väikeettevõtte Fabrikami puhul erinevad ostunõuded kogu organisatsioonis väga vähe. Ostureeglid erinevad ainult organisatsiooni juriidiliste isikute seas. Näiteks ostavad Kanada Fabrikami ja USA Fabrikami töötajad kaupu ja teenuseid erinevatest kataloogidest ja eri hankijatelt. Seetõttu seadistab Fabrikam oma ostupoliitikad juriidilise isiku tasemel.  

Fabrikam loob kaks ostupoliitikat. Poliitika A rakendub selle USA juriidilisele isikule 1111. Poliitika B rakendub Kanada juriidilisele isikule 2222. Kui juriidilise isiku 1111 töötaja loob ostutaotluse, tuletatakse poliitika reeglid poliitikast A. Näiteks on tootekataloog, mida töötaja näeb, määratud poliitika A kataloogipoliitika reeglis.  

Kui juriidilise isiku 2222 töötaja loob ostutaotluse, tuletatakse poliitika reeglid poliitikast B.  

**Märkus.** Kui juriidilise isiku 1111 töötaja ostab kauba juriidilise isiku 2222 töötaja nimel, rakenduvad juriidilisele isikule 2222 määratud poliitika reeglid (st poliitika reeglid poliitikast B).

### <a name="example-2-complex-purchasing-policy-configuration"></a>Näide 2: keerulise ostupoliitika konfigureerimine

Eelmises näites määratleti kõik ostureeglid ühes organisatsiooni hierarhias, ettevõtete organisatsiooni hierarhias. Siiski võib keerukas organisatsioon määratleda poliitikaid mitme organisatsiooni hierarhia jaoks.  


Contoso on suur ettevõte, mis nõuab keerukaid ostureegleid taotlusprotsessi juhtimiseks. Contoso on määratletud reeglid kahele erinevale organisatsiooni hierarhiale: osakonna ja globaalsele ostujuhtimisele.  

Poliitika 123 on määratletud Suurbritannia müügi müügisosakonna osakonna organisatsiooni hierarhiale. Poliitika 123 puhul määrab ostutaotluse kontrollreegel, et piirangud tuleb kehtestada minimaalsetele tellimiskogustele. Selle reegli puhul valitakse suvand **Jõusta minimaalse tellimuskoguse piirangud**.  

Poliitika 456 on määratletud müügi- ja turundusosakonna globaalse ostujuhtimise organisatsiooni hierarhiale. Poliitika 456 puhul ei määra ostutaotluse kontrollreegel, et piirangud tuleb kehtestada minimaalsetele tellimiskogustele. Selle reegli puhul ei valita suvandit **Jõusta minimaalse tellimuskoguse piirangud**.  

Sam töötab Contoso Ühendkuningriigi kontori Ühendkuningriigi müügi müügiosakonnas. Tema osakonnale rakenduvad nii osakonna kui ka globaalse ostujuhtimise organisatsiooni hierarhiad. Kui Sam loob ostutaotluse, peab süsteem määrama, millist poliitikat rakendada. Süsteemiadministraator seadistab ostupoliitika parameetrid määratlemaks, et ostupoliitikaid tuleb rakendada järgmises eelisjärjestuses.

1.  Globaalne ostujuhtimine
2.  Osakond
3.  Ettevõtted

Seetõttu rakendatakse Sami loodud ostutaotlusele poliitikat 456 ja ostutaotluse puhul ei ole nõutav tellimuse miinimumkogus.

## <a name="policy-rules"></a>Poliitika reeglid
### <a name="catalog-policy-rule"></a>Kataloogi poliitikareegel

Kataloogi poliitikareegel määrab, millised hankekataloogi kasutajad näevad ostutaotluste loomist. Kui kasutajale on antud õigus toodete tellimiseks teise kasutaja nimel, kasutab tellimus kataloogi poliitika reeglit, mis on määratletud taotleja juriidilise isiku ja tootmisüksuse jaoks, et määrata, millist kataloogi kuvada. Enne kui saate määratleda kataloogi poliitika reegli, peate looma hankekataloogi ja selle avaldama.

### <a name="category-access-policy-rule"></a>Kategooriale juurdepääsu poliitikareegel

Kategooria juurdepääsupoliitika reegel määrab, millistele kategooriatele on kasutajatel juurdepääs ostutaotluste loomisel. Kui ühtegi reeglit pole määratud, saab ostutaotlusele lisada kõik hankekategooriad.

1.  Valige suvand **Kaasa emareegel**, et rakendada kategooriale emaorganisatsiooni kategooria juurdepääsupoliitika reegel.
2.  Valige paanil **Saadaolevad kategooriad** kategooriad, millele reegel rakendub. Kui valite kategooria, lisatakse loendisse **Valitud kategooriad** ka kõik kategooriad, mis on hierarhias kõrgemal.
3.  Valige suvand **Kaasa alamkategooriad**, et rakendada reeglit kõikidele valitud kategooria alamkategooriatele.

### <a name="category-policy-rule"></a>Kategooria poliitikareegel

Kategooria poliitika reegel määratleb, kuidas kasutajad saavad valida igale kategooriale hankijad. See määratleb ka nõuded vastuvõtmise ja arveldusprotsessidele.

### <a name="re-approval-rule-for-purchase-orders"></a>Ostutellimuste eelkinnituse reegel

Eelkinnituse reegel on valikuline reegel, mis määratleb eelkinnituse nõudmise kriteeriumi, kui ostutellimust muudetakse. Valitud välju hinnatakse ostutellimuse töövoos, kui töövoos on seadistatud tingimus „Ostutellimuse eelkinnitamine on nõutud”.

> [!NOTE]
> Arvestuse jaotus lähtestatakse alati, kui mudetakse kinnitatud ostutellimust, millel on aktiivne muudatusehaldus. Seega tuleks arvestada, et kui soovite vältida ostutellimuse uut kinnitamist teatud väljade muutmisel, EI TOHIKS uuesti kinnitamisel kaasata valitud väljana välja Accounting distribution.changed. 

### <a name="purchase-requisition-rfq-rule"></a>Ostutaotluse pakkumiskutse reegel

Ostutaotluse pakkumiskutse reegel määratleb ostutaotluse rea jaoks pakkumiskutset nõudvad kriteeriumid. Kui rida vastab tingimustele, ilmub pakkumise reale tempel „mitteametlik pakkumiskutse” või „ametlik pakkumiskutse”.

### <a name="purchase-requisition-control-rule"></a>Ostutaotluse juhtimisreegel

Ostutaotluse juhtimisreegel on valikuline taotluste puhul, mille tüüp on **tarbimine**. Seda tüüpi reeglite loomisel saate seada suvandeid erinevatele vahekaartidele.

-   Vahekaardil **Töövoo esitamine** saate konfigureerida väljad, mis tuleb täita taotluse real taotluse esitamiseks kinnitamise eesmärgil.
-   Vahekaardil **Tellimuse kogused** saate konfigureerida väljad, mis on ostutellimusel nõutavad teatud tingimustel. Saate rakendada ka tellimuse koguseid.
-   Vahekaardil **Kuupäevad** saate konfigureerida, kas aruandluskuupäev on sama mis nõudekuupäev
-   Vahekaardil **Aadress** saate määratleda, kas kasutajal lubatakse ostutaotlusele rakendamiseks luua süsteemis uusi aadresse.

### <a name="requisition-purpose-rule"></a>Taotluse eesmärgi reegel

Taotluse eesmärgi reegel on valikuline reegel, mis määrab konkreetsele juriidilisele isikule lubatud taotluse eesmärgi tüübi. Kui selle reegli puhul ei ole muud eesmärki märgitud, siis on taotluse eesmärk loomisel automaatselt **tarbimine**.

### <a name="replenishment-category-access-policy-rule"></a>Täiendamise kategooria juurdepääsupoliitika reegel

Täiendamise kategooria juurdepääsupoliitika reegel on valikuline reegel, mis määrab konkreetse juriidilise isiku taotluse nõude täitmiseks saadaolevad tooted, kui taotluse eesmärk on **täiendamine**.

### <a name="replenishment-control-rule"></a>Täiendamise kontrollreegel

Täiendamise kontrollreegel on valikuline reegel, mis määratleb väljad, mis tuleb taotluse real täita taotluse esitamisel kinnitamiseks, kui taotluse eesmärk on **täiendamine**.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Ostutellimuse loomise ja nõudluse konsolideerimise reegel

Ostutellimuse loomise ja nõude konsolideerimise reegel määratleb poliitikareeglid, mida kasutada siis, kui ostutellimus on loodud kinnitatud ostutaotlusest. Seda tüüpi reeglite loomisel saate seada suvandeid erinevatele vahekaartidele.

-   Vahekaardil **Ostutellimuse tükeldamine** saate määratleda ostutaotluse ridade eraldi ostutellimusteks tükeldamise kriteeriumi.
-   Vahekaardil **Hinna/allahindluse ülekanne** saate määratleda, millal arvutada ümber hinnalepe, kui loodud onostutellimus.
    -   **Ainult kaubandusleppe puudumisel**: hinnad ja allahindlused kantakse ostutaotluselt üle vaid juhul, kui kehtiv kaubanduslepe või baashind puudub. Kui kauba või hankija kaubanduslepe või baashind on olemas, arvutatakse hinnad ja allahindlused ümber kaubandusleppe või baashinna alusel ning rakendatakse ostutellimusele. Kui pole sätestatud teisiti, siis on see vaikekäitumine.
    -   **Alati**: hinnad ja allahindlused kantakse alati ostutaotlusest üle.

    Samuti saate anda nõude esitajale loa muuta hinna ja allahindluse ülekandmise viisi üksikute ostutaotluse ridade puhul Valige suvand **Luba ostutaotluse ridadel manuaalne alistamine** selle võimaluse aktiveerimiseks.
-   Vahekaardil **Kauba kirjelduse kanne** saate kauba kirjelduse taotluselt üle kanda, kui see pärineb pakkumiskutselt.
-   Vahekaardil **Hinnakõikumine** saate määratleda reeglid kinnitatud ostutaotluste ülevaatusprotsessi kaudu tagasi marsruutimiseks, kui hankekataloogi kauba hind tõuseb. Määrake maksimaalne summa, mida ostutaotluse rea kauba netosumma saab suurendada ostutaotluse kinnitamise ja ostutellimuse loomise aja vahel. Netosumma arvutatakse järgmise valemi järgi: (\[kogus × (ühiku hind – allahindlus) ÷ hinnaühik\] + ostu lisakulud) × (100 – allahindluse protsent) ÷ 100 Ostutaotluse ridu, mis ületavad teie määratud hinnakõikumise, säilitatakse käsitsi töötlemiseks. Vahekaardil **Tõrgete töötlemine** konfigureeritavad reeglid määravad, kuidas ostutaotluse ridu töödeldakse.
-   Vahekaardil **Tõrgete töötlemine** saate konfigureerida töötlemisreegli, mis rakendub ostutaotlusele, kui selle kontrollimine nurjub ostutellimuse loomise käigus hankija või hinnakõikumise vea tõttu. Tehke üks järgmistest valikutest:
    -   **Tegevuseta** – ostutaotluse read jäävad lehele **Kinnitatud ostutaotluste vabastamine**. Ostutaotluse ridade olekuks jääb **Kinnitatud**. Samas peab vead lahendama enne, kui ostutellimust saab ostutaotluse ridade jaoks luua.
    -   **Tühista ostutaotluse rida** – ostutaotluse read tühistatakse. Nõude esitaja saab tühistatud ridadele luua uue ostutaotluse, kui ta soovib rea kaupu taotleda.
    -   **Loo uus ostutaotluse rida** – ostutaotluse read tühistatakse. Seejärel luuakse uued ostutaotlused, mis sisaldavad ainult kontrollimisel nurjunud ostutaotluse ridu. Uute ostutaotluste loomisel on nende olekuks **Mustand**. Need ostutaotlused saab pärast kontrollimisvigade lahendamist ülevaatamiseks uuesti esitada. Ostutaotluse ridade ettevalmistajat teavitatakse ridade tühistamisest ja et nurjunud ostutaotluse ridade jaoks loodi uued ostutaotlused.
-   Vahekaardil **Ostutellimuse käsitsi loomine** saate määratleda parameetrid, mis määravad, kas ostutaotlust tuleb töödelda käsitsi või kas seda saab automaatselt ostutellimuseks teisendada. Parameetrid võivad kehtida sisekataloogi kaupadele, väliskataloogi kaupadele ja mittekataloogi kaupadele. Tehke üks järgmistest valikutest:
    -   **Loo ostutellimused käsitsi** – looge kõikide ostutaotluste puhul ostutellimused käsitsi.
    -   **Loo ostutellimused automaatselt** – looge kõikide kinnitatud ostutaotluste ostutellimused automaatselt. Käsitsi ostutellimuse loomiseks ei säilitata ühtki ostutaotlust.
    -   **Loo ostutellimusi automaatselt, v.a nendel tingimustel** – looge ostutellimused käsitsi ostutaotlustele, mis vastavad teie määratletud kriteeriumile. Kõik muud kinnitatud ostutaotlused teisendatakse automaatselt ostutellimusteks. Kui teete valiku **Loo ostutellimusi automaatselt, v.a nendel tingimustel**, saate lisada hankekategooriad ja hankijad määramaks, millised kinnitatud ostutaotluse read säilitatakse käsitsi töötlemiseks. See suvand võib kehtida sisekataloogi kaupadele, väliskataloogi kaupadele ja mittekataloogi kaupadele. Hankekategooria valimisel valitakse ka kõik hankekategooria alamkategooriad. Valige suvand **Kõik** teatud tüüpi ostutaotluse rea puhul, et säilitada käsitsi töötlemiseks kõik seda tüüpi read.

    Kui soovite, et ostutellimused loodaks ostutellimuse loomise pakett-töö käivitamisel kinnitatud ostutaotlustest automaatselt, valige suvand **Ostutellimuse automaatse loomise käivitamine pakett-tööna**. See suvand kehtib ainult ostutaotlustele, mis ei nõua käsitsi töötlemist. Automaatse ostutellimuse loomise käivitamisel pakett-tööna saate plaanida selle tegevuse ajal, kui ressursid on vähem piiratud. Kui ostutaotluse ridadel on valitud suvand **Nõutav ettemakse**, valige suvand **Kui taotlus on ettemakse jaoks häälestatud**, et säilitada kinnitatud ostutaotlused käsitsi töötlemiseks. Käsitsi töötlemiseks säilitatavaid ostutaotlusi saab filtreerida nii, et saate vaadata ainult neid ostutaotluse ridu, mis nõuavad ettemakset.
-   Vahekaardil **Nõudluse konsolideerimine** saate määratleda parameetrid, mis määravad, kas käsitsi töödeldud ostutaotlusi saab kaasata ostutaotluse konsolideerimisse. Parameetrid võivad kehtida sisekataloogi kaupadele, väliskataloogi kaupadele ja mittekataloogi kaupadele. Tehke üks järgmistest valikutest:
    -   **Ära luba nõudluskonsolideerimist** – nõudluskonsolideerimise puhul ei ole sobilikke kinnitatud ostutellimuse ridu. See suvand on vaikimisi valitud ja kehtib ainult ostutaotluse ridadele, mis nõuavad ostutellimuse loomisel käsitsi töötlemist.
    -   **Luba alati nõudluskonsolideerimine** – nõudluskonsolideerimise puhul on sobilikud kõik kinnitatud ostutellimuse read. **Märkus.** Kui valite vahekaardil **Nõudluskonsolideerimine** suvandi **Luba alati nõudluskonsolideerimine**, kuid valite vahekaardil **Ostutellimuse käsitsi loomine** suvandi **Loo ostutellimused automaatselt**, säilitatakse kõik ostutaotlused käsitsi töötlemiseks.
    -   **Luba nõudluskonsolideerimine nendel tingimustel** – määrake kriteerium, mis määrab, kas kinnitatud ostutaotluse read on nõudluskonsolideerimise puhul sobilikud. Iga ostutaotluse rea tüübi puhul saate määrata kriteeriumid hankekategooria ja hankija alusel. Kui teete valiku **Luba nõudluskonsolideerimine nendel tingimustel**, saate iga ostutaotluse rea tüübi puhul määrata kriteeriumid hankekategooria ja hankija alusel. Hankekategooria valimisel valitakse ka kõik hankekategooria alamkategooriad. Kui valite suvandi **Kõik** konkreetse rea tüübi puhul, sobivad kõik seda tüüpi ostutaotluse read nõudluskonsolideerimiseks.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]