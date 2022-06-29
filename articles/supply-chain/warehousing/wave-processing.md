---
title: Voo loomine ja töötlemine
description: See artikkel kirjeldab, kuidas luua, töödelda ja vabastada laine, et luua komplekteerimistöö koorma, saadetise, tootmistellimuse või kanban-tellimuse jaoks.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 60bf4ab6944bd982e022ead6431adae417ddfb43
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014615"
---
# <a name="wave-creation-and-processing"></a>Voo loomine ja töötlemine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas luua, töödelda ja vabastada laine, et luua komplekteerimistöö koorma, saadetise, tootmistellimuse või kanban-tellimuse jaoks. Võite luua järgmiste tellimustüüpide voogusid.

- **Müügitellimused** – kasutage müügitellimuste ridade kaasamiseks tarnevooge. Müügitellimuse väljastamisel lattu saab müügitellimuse ridu voogu kaasata.
- **Tootmistellimused** – kasutage tootmisvooge toote koosluse ridade lisamiseks.
- **Kanban-tellimused** – Kanban-vood sisaldavad kanban-tellimuste komplekteerimislehe ridu.

Müügitellimuste ja kanban-tellimuste puhul tuleb varud reserveerida enne tellimuse väljastamist lattu. Vastasel korral ei saa kaupu ega eraldamisridu voos töödelda. Tootmistellimused on siiski veidi paindlikumad. Tootmistellimuste puhul saate valida ühe järgmistest valikutest.

- Nõudke kõikide materjalide reserveerimist enne tellimuse lattu väljastamist.
- Lubage tootmistellimuste väljastamine lattu, kuigi kõiki materjale ei saa reserveerida. Kui valite selle suvandi, peate lattu väljastamise protsessi käsitsi kordama, kui täiendavad materjalid kättesaadavaks muutuvad. Näiteks on see kasulik, kui teil on olemas tootmise alustamiseks vajalikud materjalid ja on võimalik oodata, kuni täiendavad materjalid kättesaadavaks muutuvad.

Saate määrata, milliseid neist tootmistellimuste valikutest vaikimisi kasutada, kasutades välja **Materjalireserveeringu vajadus** lehel **Tootmise juhtimise parameetrid**. Konkreetse tootmistellimuse seadistust saab siiski alati muuta vastavalt vajadusele. Lisateavet vt [Voo töötlemise laoparameetrid](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Voo loomine ja töötlemine

Järgnev diagramm näitab voogu selle kohta, kuidas saatmisvood luuakse, töödeldakse ja vabastatakse. Numbrid vastavad selle jaotise hilisematele osadele.

![Voo loomise protsess.](media/wave-processing-diagram.png "Voo loomise protsess")

### <a name="prerequisites"></a>Eeltingimused

Enne käivitamist peab voomall olema saadaval voo tüübi jaoks, mida soovite luua (saatmine, tootmine või kanban). Voomall määrab mitu seadistust voo loomise ja töötlemise kohta, sh millised sammud tuleb teha käsitsi ja mida tehakse automaatselt. Lisateabe saamiseks vaadake jaotist [Voomallid](wave-templates.md).

### <a name="create-a-wave"></a>Loo voog

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Loo vood automaatselt lao ja tellimuse tüübi alusel

Voo automaatseks loomiseks seadistage [Voomallid](wave-templates.md), mis kehtivad iga asjakohane tellimuse tüübi ja lao puhul. Veenduge, et igal mallil on suvand **Automatiseeri voo loomine** seatud väärtusele *Jah*.

#### <a name="manually-create-waves"></a>Käsitsi voogude loomine

Voo käsitsi loomiseks tehke järgmist.

1. Veenduge, et vastavad [voomallid](wave-templates.md) ei oleks seadistatud looma lao ja tellimuse tüüpide jaoks automaatselt voogu, kohas kus soovite seda teha käsitsi.
1. Sõltuvalt loodava voo tüübist tehke ühte järgmistest.

    - Mine laohalduse **väljaminevate** \> **lainete saadetise lainetesse** \> **Kõik** \> **lained.** Valige toimingupaanil nupp **Voog**.
    - Minge laohalduse **väljaminevatele** \> **lainetele Tootmisvood** \> **Kõik** \> **tootmisvood.** Valige toimingupaanil nupp **Tootmisvoog**.
    - Minge laohalduse **väljaminevate lainete** \> **kanbani** \> **vood Kõik** \> **kanbani vood.** Valige toimingupaanil nupp **Loo voog**.

1. Sisestage väljale **Kirjeldus** voo lühikirjeldus. See peaks näitama, mida voos töötlete.

1. Valige väljal **Voomalli nimi** loodava voo tüübi jaoks voo mall. Voo mall sisaldab voo meetodeid, mis teevad voos toiminguid, nt loovad töö. Näiteks voogude lähetamiseks kasutatav voo mall võib sisaldada koormate loomise, voogudesse ridade eraldamise, täiendamise ja voo jaoks komplekteerimistöö loomise meetodeid.

1. Kui soovite kasutada voo puhul täiendavate päringukriteeriumidena voo atribuute, valige atribuudid väljadelt **Vooatribuudid**.

### <a name="specify-what-to-include-in-a-wave"></a>Täpsustage, mida voogu lisada

Pärast voo loomist olete valmis sellele sisu lisama.

> [!NOTE]
> Vajadusel saate voogu ridu lisada isegi pärast selle töötlemist seni, kuni see pole välja antud.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Automaatselt täpsustage, mida voogu lisada

Voo automaatseks loomiseks seadistage [Voomallid](wave-templates.md), mis kehtivad iga asjakohane tellimuse tüübi ja lao puhul. Veenduge, et igal mallil on suvand **Automatiseeri voo loomine** seatud väärtusele *Jah*. Kui suvand **Määra avatud voogudesse** on seatud väärtusele *Jah*, saab teie mall read automaatselt määrata mis tahes kvalifitseeruvale avatud voole.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Käsitsi täpsustage, mida voogu lisada

Kui voog on loodud, kuid pole veel välja antud, saate käsitsi määrata, mida kaasata. Ridade käsitsi voosse lisamiseks.

1. Sõltuvalt voo tüübist, millele ridu lisada, tehke ühte järgmisest.

    - Mine laohalduse **väljaminevate** \> **lainete saadetise lainetesse** \> **Kõik** \> **lained.** Valige toimingupaanil nupp **Voog**.
    - Minge laohalduse **väljaminevatele** \> **lainetele Tootmisvood** \> **Kõik** \> **tootmisvood.** Valige toimingupaanil nupp **Tootmisvoog**.
    - Minge laohalduse **väljaminevate lainete** \> **kanbani** \> **vood Kõik** \> **kanbani vood.** Valige toimingupaanil nupp **Loo voog**.

1. Valige voog. Klõpsake tegumiribal ühte järgmistest valikutest.

      - **Saadetiste haldamine**
      - **Tootmiste haldamine**
      - **Kanban-töö komplekteerimislehtede haldamine**

1. Valige akna ülaosas voogu lisatav laine ja seejärel klõpsake käsku **Lisa voogu**. Rida teisaldatakse kiirkaardile **Vooread**.

    Korrake seda sammu iga lisatava rea puhul. Kõigi ridade lisamiseks valige käsk **Lisa kõik**.

    > [!TIP]
    > Saadetise voogude puhul leiate konkreetse tellimuse kiiresti, valides väljalt **Voofiltri kood** kohandatud filtri. Laine filtri koodid sisaldavad vormil **Voofiltrid** loodud saadetiste päringukriteeriume. See väli pole tootmisvoogude või kanban-voogude puhul saadaval.
    > Roheline märge veerus **Vool** näitab, et saadetis on voogu lisatud.

### <a name="process-the-wave-to-create-the-picking-work"></a>Voo töötlemine komplekteerimistöö loomiseks

Kui voogon loodud ja sisaldab kõiki selle nõutavaid ridu, olete valmis seda töötlema, et luua vastav korjamistöö.

#### <a name="automatically-process-a-wave"></a>Voo automaatne töötlemine

Voo automaatseks töötlemiseks seadistage vastavad [voomallid ](wave-templates.md) koos vajalike automaatse töötlemise valikutega.

#### <a name="manually-process-a-wave"></a>Voo manuaalne töötlemine

Saate töödelda voogu ainult siis, kui **Voo olek** on *Loodud*. Pärast voo töötlemist muudetakse **voo olek** olekuks *Hoitud*.

Kogu vajaliku sisuga voo käsitsi töötlemiseks järgige järgmisi samme.

1. Sõltuvalt töödeldava voo tüübist tehke ühte järgmist.

    - Valige laohalduse **väljaminevad** \> **lained Saadetise** \> **lained Kõik** \> **lained.** Valige toimingupaanil nupp **Voog**.
    - Valige laohalduse **väljaminevad** \> **vood Tootmisvood** \> **·** \> **Kõik tootmisvood.** Valige toimingupaanil nupp **Tootmisvoog**.
    - Valige laohalduse **väljaminevad** \> **vood Kanbani** \> **vood Kõik** \> **kanbani vood.** Valige toimingupaanil nupp **Loo voog**.

1. Valige töödeldav voog. Klõpsake toimingupaanil suvandit **Töötlemine**.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Väljastage voog lattu komplekteerimise ja pakkimise alustamiseks

Enne väljastamist tuleb voogu töödelda. Voo väljastamisel on komplekteerimistöö laos saadaval. Pärast väljastamist saate voo tühistada ja ridu lisada, kuid te ei saa ridu muuta.

#### <a name="automatically-release-a-wave"></a>Voo automaatne väljaandmine

Voo automaatseks töötlemiseks seadistage vastavad [voomallid ](wave-templates.md) koos vajalike automaatse töötlemise valikutega.

#### <a name="manually-release-a-wave"></a>Voo manuaalne väljaandmine

Voo käsitsi väljastamiseks tehke järgmist.

1. Sõltuvalt väljaantava voo tüübist tehke ühte järgmist.

      - Valige laohalduse **väljaminevad** \> **lained Saadetise** \> **lained Kõik** \> **lained.** Valige toimingupaanil nupp **Voog**.
      - Valige laohalduse **väljaminevad** \> **vood Tootmisvood** \> **·** \> **Kõik tootmisvood.** Valige toimingupaanil nupp **Tootmisvoog**.
      - Valige laohalduse **väljaminevad** \> **vood Kanbani** \> **vood Kõik** \> **kanbani vood.** Valige toimingupaanil nupp **Loo voog**.

1. Valige väljastatav voog. Valige toimingupaanil nupp **Anna voog välja**.

## <a name="containerize-a-wave"></a>Voo konteinerisse pakendamine

Automaatne konteinerite koostamine loob saadetiste jaoks konteinerid ja komplekteerimistööd pärast voo töötlemist. Lisateavet häälestamise kohta vt [Konteinerisse pakendamine](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Plaanitud töö loomine

Kui funktsioon *Töö loomise plaanimine* on lubatud, loob voo töötlemine plaanitud töö, mida kasutatakse lõpuks uue töö loomisprotsessi poolt. Töö loomise ajal töö blokeeritakse, kasutades funktsiooni *Organisatsiooniülene töö blokeerimine*. Lisateavet vt [Voo ajal töö loomise plaanimine](configure-wave-schedule-work-creation.md).

Järgmine vooskeem näitab, kuidas plaanitud tööd laine töötlemise ajal luuakse.

![Töö loomise graafik.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Plaanitud töö

Leht **Plaanitud töö üksikasjad** (**Laohaldus \> Töö \> Plaanitud töö üksikasjad**) näitab teavet plaanitud töö kohta, mis voo töötlemise ajal algselt luuakse. Saadaval on järgmised suvandi **Protsessi olek** väärtused.

- **Järjekorras** – plaanitud töö on töö loomiseks kasutamiseks ootel.
- **Lõpetatud** – plaanitud töä on töö loomiseks kasutatud.
- **Nurjus** – voo töötlemine nurjus. Pange tähele, et plaanitud töö võib olla olekus **Nurjunud** koos või ilma seotud tegeliku tööta. Kui tegeliku töö loomise protsess nurjub, jääb tegelik töö olekusse *Tühistatud*.

### <a name="batch-job-for-the-work-creation-process"></a>Töö loomisprotsessi pakett-töö

Töötlemise voogude pakett-tööde vaatamiseks valige tegevuspaanil **Pakett-tööd** lehel **Kõik vood**.

Siit saate vaadata iga pakett-töö ID kohta kõiki partii ülesande üksikasju.

## <a name="cancel-a-wave"></a>Voo tühistamine

Vajaduse korral saate töödeldud voo tühistada. Loodud voo ja komplekteerimistöö tühistamiseks tehke järgmist.

1. Sõltuvalt tühistatava voo tüübist tehke ühte järgmist.

      - Mine laohalduse **väljaminevate** \> **lainete saadetise lainetesse** \> **Kõik** \> **lained.**
      - Minge laohalduse **väljaminevatele** \> **lainetele Tootmisvood** \> **Kõik** \> **tootmisvood.**
      - Minge laohalduse **väljaminevate lainete** \> **kanbani** \> **vood Kõik** \> **kanbani vood.**

1. Valige tühistamiseks voog. Toiminguriba vahekaardil **Töö** valige suvand **Tühista**.

## <a name="review-wave-batch-job-details"></a>Voo partiitöö üksikasjade ülevaade

Kasutage lehte **voo partiitöö üksikasjad**, et kontrollida partiitöid ja mis tahes vooga seostatud ülesandeid. Sellest on kasu eelkõige nurjunud voo tõrkeotsingul. Ilma selle funktsioonita on partiitöö üksikasjadele tavaliselt juurdepääs ainult administraatoritel. Lehe **Voo partiitöö üksikasjad** saab teha kättesaadavaks mittehaldusega kasutajatele ning pakub partiitööde ja seotud ülesannete kirjutuskaitstud vaadet.

### <a name="turn-the-wave-batch-job-details-page-on-or-off"></a>Voo pakett-töö üksikasjade lehe sisse- või väljalülitamine

Tarneahela halduse versiooni 10.0.25 **puhul** lülitatakse voo pakett-töö üksikasjade leht vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse *tööruumist* voo pakett-töö [üksikasju](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="use-the-wave-batch-job-details-page"></a>Voo partiitöö üksikasjade lehe kasutamine

Leht **Voo partiitöö üksikasjad** koondab partiitööd ja nende ülesanded, mis võimaldab teil uurida kõiki voo samme ilma, et peate navigeerima edasi-tagasi ühe partiitöö ja partiitööde loendi vahel. Lehekülg annab ka juurdepääsu partiilogile ja kui teil on vajalikud õigused, siis ka link **partiitööde** lehele.

Selle lehe avamiseks valige voog mis tahes erinevate voogude lehel ja seejärel valige tegevuspaanilt **Voo partiitöö üksikasjad**.

## <a name="review-load-validation-and-error-messages"></a>Vaadake üle laadimise valideerimise ja tõrketeated

Voo töötlemise ajal kontrollib süsteem ja kuvab voo iga koormarea oleku. Kui hoiatusi ei toimu, jätkab see järgmist voo etappi. Hoiatuste ilmnemisel kuvatakse siin pärast kogu voo lõpetamist järgmine tõrge.

> Voost leiti kehtetud koormaread. Palun eemaldage kehtetud koormaread.

Seejärel saate enne uuesti proovimist üle vaadata voo iga koormarea lõpliku oleku ja parandada kõik hoiatused. See võimaldab teil käsitleda kõiki hoiatusi kohe enne voo taastöötlemist. (Eelmistes väljaannetes lõpetas süsteem voo töötlemise pärast esimest hoiatust, nii et saate hoiatusi parandada ainult ükshaaval.)

Viis, kuidas süsteem kuvab voo töötlemise olekuteateid, sõltub sellest, kuidas olete lehel **Laohalduse parameetrid** seadistanud suvandi **Loo voo töötluse ajaloo logi**.

- Kui **Voo töötluse ajaloo logi** loomise väärtuseks on seatud *Ei*, kuvatakse **teabelogis** koormarea olekuteated.
- Kui **Voo töötluse ajaloo logi** loomise väärtuseks on seatud *Jah*, kuvatakse lehel **Voo töötlemise ajaloo logi** koormarea olekuteated. Logi vaatamiseks minge **Laohaldus \> Väljaminevate vood \> Voo töötluse ajaloo logi**.

## <a name="additional-resources"></a>Lisaressursid

- [Vootöötluse näite konfigureerimine](tasks/configure-wave-processing.md)
- [Voomallid](wave-templates.md)
- [Konteinerisse määramine](wave-containerization.md)