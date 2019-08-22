---
title: Finantskonsolideerimised võrgus
description: Selles teemas kirjeldatakse pearaamatu finantskonsolideerimisi võrgus.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 8836e5b43498c792d214b13b2196645c4ee3ffba
ms.sourcegitcommit: 9b4c3fff2f30006b7bb491ef6ffe89d41bcbfa11
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1863796"
---
# <a name="consolidate-online"></a>Konsolideeri võrgus

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse pearaamatu finantskonsolideerimisi võrgus. Enne selle teema lugemist lugege kindlasti teemat [Finantskonsolideerimised ja valuuta teisendamine](financial-consolidations-currency-translation.md).

Kui olete seadistuse lõpetanud, sisestage konsolideerimise üksikasjad lehel **Konsolideeri (võrgus)**. Kui olete lõpetanud, klõpsake suvandit **OK** või **Partii**, et konsolideerimist töödelda.

## <a name="criteria"></a>Kriteeriumid
Vahekaardil **Kriteeriumid** lehel **Konsolideeri (võrgus)** määrake kontod, perioodid ja konsolideeritavate andmete tüüp.

![Kriteeriumite vahekaart](./media/criteria-consolidate-online.png "Kriteeriumite vahekaart")

Siin on selle vahekaardi eri väljade selgitus.

- **Kirjeldus** – sisestage konsolideeritava perioodi täpne kirjeldus.
- **Põhikonto** – kasutage selle jaotise välju töödeldavate põhikontode määramiseks.

    - **Alates** ja **Kuni** – määrake töödeldavate kontode vahemik. Kui jätate need väljad tühjaks, viiakse kõikide ettevõtete kõik kontod üle konsolideeritavale ettevõttele. Seega, kui konsolideerite nelja ettevõtet ja igal ettevõttel on eraldi kontoplaan, luuakse konsolideeritavas ettevõttes kõik kontod kõigilt neljalt ettevõttelt.
    - **Konsolideerimiskonto kasutamine** – kui määrate selle suvandi valikule **Jah**, muutub kättesaadavaks väli **Vali konsolideerimiskonto asukohast**. Valige sellest väljas, kas kõik kontod tuleks konsolideerida konsolideerimiskontole, mis on määratud lehel **Põhikontod**, või kas soovite valida konto ühest konsolideerimiskonto grupist.
    - **Konsolideerimiskonto grupp** – valige grupp, mida kasutatakse konsolideerimisel põhikonto vastendamiseks.

- **Konsolideerimisperiood** – konsolideerimisperioodi määramiseks kasutage selle jaotise välju.

    - **Alates** ja **Kuni** – määrake konsolideerimise kuupäevavahemik. Kui jätate need väljad tühjaks, töödeldakse konsolideerimist kõikide perioodide kohta, mis on määratud ettevõtte pearaamatu kalendris. Me ei soovita teil neid välju tühjaks jätta.
    - **Tegelike summade kaasamine** – määrake see suvand valikule **Jah**, et konsolideerida tegelikke andmeid.
    - **Eelarvesummade kaasamine** – määrake see suvand valikule **Jah**, et konsolideerida andmeid eelarve registrist.
    - **Saldode uuesti loomine konsolideerimise käigus** – me ei soovita määrata seda suvandit valikule **Jah**. Selle asemel looge saldod uuesti eraldi pakett-tööna.

- **Eelarvemudelid** – kui olete otsustanud konsolideerida eelarveandmeid, kasutage selle jaotise välju eelarvemudelite määramiseks.

    - **Alates** ja **Kuni** – määrake kasutatavate mudelite vahemik.
    - **Eelarvekursi tüüp** – valige eelarvekursi tüüp, mida kasutatakse eelarveandmete valuuta teisendamiseks.

## <a name="financial-dimensions"></a>Finantsdimensioonid
Määrake vahekaardil **Finantsdimensioonid** dimensioonid, mis peaksid olema kaasatud konsolideeritavasse ettevõttesse. Dimensiooni valimiseks määrake väli **Täpsustus** valikule **Dimensioon** ja seejärel määrake dimensiooni järjestus konsolideeritavas ettevõttes.

![Finantsdimensioonide vahekaart](./media/financial-dimensions-cons.png "Finantsdimensioonide vahekaart")

Olenemata määratud järjestusest on esimene segment alati **Põhikonto**.

## <a name="legal-entities"></a>Juriidilised isikud
Määrake vahekaardil **Juriidilised isikud** ettevõtted, mis peaksid olema kaasatud konsolideeritavasse ettevõttesse. Määrake ka nende ettevõtete omandiõiguse protsent. Kui määrate omandiõiguseks vähem kui 100 protsenti, võetakse määratud protsent konsolideeritavas ettevõttes kokku. Teisenduserinevuste korral kasutatakse välja **Teisenduserinevuste konto tüüp** põhikonto valimiseks seadistuses lehel **Automaatsete kannete kontod**.

![Juriidiliste isikute vaheleht](./media/legal-entities-cons.png "Juriidiliste isikute vaheleht")

![Automaatsete kannete kontode leht](./media/accounts-for-automatic-cons.png "Automaatsete kannete kontode leht")

## <a name="elimination"></a>Eemaldamine
Vahekaardil **Eemaldamine** on teil kolm võimalust eemalduste töötlemiseks:

- Valige eemaldamisreegel ja seejärel valige väljalt **Soovituse valikud** suvand **Ainult soovitus**. See suvand töötleb eemaldust konsolideerimisprotsessi käigus, aga ei sisesta kõike korraga. Võite sisestada töölehe hiljem.
- Valige eemaldamisreegel ja seejärel valige väljalt **Soovituse valikud** suvand **Ainult sisesta**. See suvand töötleb eemaldust konsolideerimisprotsessi käigus ja sisestab kõik korraga.
- Käitage eemaldamissoovitus konsolideerimise protsessist eraldi, kasutades eemaldamise töölehte.

![Eemaldamise vahekaart](./media/elimination-cons-onl.png "Eemaldamise vahekaart")

Lisateavet eemaldamiste kohta vt teemast [Eemaldamisreeglid](./elimination-rules.md).

## <a name="currency-translation"></a>Valuuta tõlge
Vahekaardil **Valuuta teisendamine** määrate juriidilise isiku, konto ja vahetuskursi tüübi ning määra. Väljal **Rakenda vahetuskurssi väljalt** on saadaval kolm suvandit:

- **Konsolideerimise kuupäev** – konsolideerimise kuupäeva kasutatakse vahetuskursi saamiseks. See kurss vastab punkti- või kuu lõpu kursile. Näete kursi eelvaadet, aga ei saa seda redigeerida.
- **Kande kuupäev** – iga kande kuupäeva kasutatakse vahetuskursi valimiseks. Seda suvandit kasutatakse kõige rohkem põhivaradel ja seda nimetatakse sageli ajalooliseks kursiks. Te ei näe kursi eelvaadet, kuna konto vahemikus on eri kannete jaoks palju kursse.
- **Kasutaja määratud kurss** – pärast selle suvandi valimist võite sisestada teile sobiva vahetuskursi. See suvand on kasulik keskmiste vahetuskursside korral või kui konsolideerite fikseeritud vahetuskursside suhtes.

![Valuuta teisendamise vahekaart](./media/currency-translation-cons-online.png "Valuuta teisendamise vahekaart")

## <a name="additional-resources"></a>Lisaressursid

Lisateavet konsolideerimise ja valuuta teisendamise kohta vaadake selle teema ülemteemast [Finantskonsolideerimised ja valuuta teisendamine](./financial-consolidations-currency-translation.md).

Lisateavet stsenaariumide kohta, kus võite luua konsolideeritud finantsaruandeid, vt teemast [Konsolideeritud finantsaruannete loomine](./generating-consolidated-financial-statements.md).
