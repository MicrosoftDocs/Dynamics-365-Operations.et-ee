---
title: Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)
description: See teema selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide genereerimiseks OPENXML-vormingus.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf909efbac5dce8e22d9713ad2e694ce624ffeb0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681897"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)

[!include [banner](../../includes/banner.md)]

See teema selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide genereerimiseks OPENXML-vormingus. Seda konfiguratsiooni kasutatakse hankija maksete töötlemiseks.

Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha ka GBSI ettevõttes.

Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid. Samuti peab teil olema Exceli fail, mis imporditakse malli loomisel. Sellele failile pääseb juurde [Maksearuande mallist](https://go.microsoft.com/fwlink/?linkid=862266).


## <a name="upload-the-payments-data-model-configuration"></a>Makse andmemudeli konfiguratsiooni üleslaadimine
1. Navigeerimispaanil avage **Moodulid > Organisatsiooni haldus > Tööruumid > Elektrooniline aruandlus**.
2. Märkige loendis näidisettevõtte seadistuse pakkujaks Litware, Inc. Kui seda seadistuse pakkujat pole näha, peate esmalt lõpetama etapid teemas [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).
3. Valige **Määra aktiivseks**.
4. Valige **Osad**. Valige võimaluse korral tüübi Operationsi ressursid jaoks hoidla. Kui see on saadaval, jätke uue hoidla loomise järgmised etapid vahele.  
5. Klõpsake valikut **Lisa** rippdialoogi avamiseks.
6. Väljas **Seadistuse osa tüüp** sisestage `Operations resourcesdd`.
7. Valige käsk **Loo hoidla**.
8. Valige nupp **OK**.
9. Valige **Avamine**.
10. Valige puult suvand **Maksemudel**.
11. Valige **Impordi**. Importige see andmemudel. Seda kasutatakse andmeallikana uues vormingu konfiguratsioonis. Jätke see etapp vahele, kui see konfiguratsioon on juba imporditud.  
12. Valige **Jah**.
13. Sulgege lehed kuni naasete lehele „Elektrooniline aruandlus“.

## <a name="create-a-new-format-configuration"></a>Uue vormingu konfiguratsiooni loomine
1. Valige **Aruandluse konfiguratsioonid**.
2. Valige puult suvand **Maksemudel**.
3. Rippdialoogi avamiseks valige käsk **Loo konfiguratsioon**.
4. Väljas **Uus** sisestage `Format based on data model PaymentModel`. Looge vorming, mis põhineb andmemudelil PaymentModel.
5. Kirjutage välja **Nimi** järgmist: `Sample worksheet report`. Töölehe aruande näide  
6. Kirjutage välja **Kirjeldus** järgmist: `Sample worksheet report for vendors' payments`. Töölehe aruande näide hankijate maksete jaoks.  
7. Sisestage või valige väärtus väljal **Andmemudeli definitsioon**. Valige määratlus **CustomerCreditTransferInitiation**.  
8. Valige **Konfiguratsiooni loomine**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Uue dokumendi koostamine töölehe vormingus OPENXML
1. Valige puult suvand **Maksemudel\Töölehe näidisaruanne**.
2. Valige **Kujundaja**.
3. Toimingupaanil valige **Impordi**.
4. Valige **Excelist importimine**.
5. Valige suvand **Manused**. Manustage olemasolev Exceli dokument mallina.  
6. Valige suvand **Uus**.
7. Valige **Fail**. Osutage olemasolevale Exceli failile.  
8. Sulgege leht.
9. Väljas **Mall** sisestage või valige väärtus. Valige manustatud Exceli fail, mida kasutada mallina.  
10. Valige nupp **OK**. Pange tähele, et ER-i vormingu komponendid on loodud kujundamisvormingus viitava MS Exceli dokumendi struktuuri alusel (nimega vahemikud).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Uue andmeallika loomine kogusummade arvutamises valuutakoodide järgi
1. Valige **Vastendamine** vahekaart.
2. Rippdialoogi avamiseks valige käsk **Lisage põhinõue**.
3. Valige puult suvand **Funktsioonid\Rühmitusalus**.
4. Kirjutage välja **Nimi** järgmist: `PaymentByCurrency`.
5. Valige **Rühma muutmisalus**.
6. Valige puult **mudel**, seejärel suvand **mudel\Maksed**.
7. Valige **Lisa väli kohta**.
8. Valige **Mida rühmitada**.
9. Valige puult **mudel\Maksed**, seejärel suvand **mudel\Maksed\Valuuta**.
10. Valige **Lisa väli kohta**.
11. Valige **Rühmitatud väljad**.
12. Valige puult suvand **mudel\Maksed\Etteantud summa(InstructedAmount)**.
13. Valige **Lisage väli kohta**, seejärel valige **Koondamisväljad**.
14. Tehke väljas **Meetod** valik. Valige funktsioon **SUMMA koondamine**.  
15. Kirjutage välja **Nimi** järgmist: `TotalInstructuredAmount`.
16. Valige käsk **Salvesta**.
17. Sulgege leht.
18. Valige nupp **OK**.

## <a name="map-format-components-to-data-sources"></a>Vormingu komponentide vastendamine andmeallikatega
1. Valige puul **mudel\Maksed\Algatav osapool(InitiatingParty)\Nimi** ja **Excel\Aruandepäis\Ettevõttenimi**.
2. Valige **Seo**.
3. Valige puul **mudel\Maksed\Võlausaldaja\Tuvastamine\Allika ID (SourceID)** ja **Excel\Makseread\Pakkujakontonimi**.
4. Valige **Seo**.
5. Valige puul **mudel\Maksed\Võlausaldaja\Nimi** ja **Excel\Makseread\Pakkujanimi**.
6. Valige **Seo**.
7. Valige puul **mudel\Maksed\Võlausaldaja agentuur(CreditorAgent)\Nimi** ja **Excel\Makseread\Pank**.
8. Valige **Seo**.
9. Valige puul **mudel\Maksed\Võlausaldaja agentuur(CreditorAgent)\Suunamisnumber(RoutingNumber)** ja **Excel\Makseread\Suunamisnumber**.
10. Valige **Seo**.
11. Valige puul **mudel\Maksed\Võlausaldaja konto(CreditorAccount)\Tuvastamine\Number** ja **Excel\Makseread\Kontonumber**.
12. Valige **Seo**.
13. Valige puul **mudel\Maksed\Etteantud summa(InstructedAmount)** ja **Excel\Makseread\Võlad**.
14. Valige **Seo**.
15. Valige puul **mudel\Maksed\Valuuta** ja **Excel\Makseread\Valuuta**.
16. Valige **Seo**.
17. Valige puul **Maksevaluutajärgi\rühmitatud\Valuuta** ja **Excel\Kokkuvõtteread\Kokkuvõttevaluuta**.
18. Valige **Seo**.
19. Valige puul **Maksevaluutajärgi\rühmitatud\Etteantudkogusumma** ja **Excel\Kokkuvõtteread\Kokkuvõttesumma**.
20. Valige **Seo**.
21. Valige puul **Maksevaluutajärgi** ja **Excel\Kokkuvõtteread**.
22. Valige **Seo**.
23. Valige puul **mudel\Maksed** ja **Excel\Makseread**.
24. Valige **Seo**.
25. Valige **Salvesta**, seejärel sulgege leht.

## <a name="use-the-created-configuration-for-payments-processing"></a>Loodud konfiguratsiooni kasutamine maksete töötlemiseks
1. Valige käsk **Muuda olekut**.
2. Valige **Lõpeta**.
3. Valige nupp **OK**.
4. Navigeerimispaanil avage **Moodulid > Makstaolevad arved > Maksete seadistamine > Makseviisid**.
5. Väljal **Makseviis** väärtusega **Elektrooniline** filtreerimiseks kasutage kiirfiltrit.
6. Valige suvand **Redigeeri**.
7. Laiendage jaotis **Failivormingud**.
8. Valige väljas **Elektrooniline üldaruanne** valik **Jah**.
9. Väljas **Ekspordi vormingu seadistus** sisestage või valige väärtus. Valige seadistus **Töölehe näidisaruanne**.  
10. Valige käsk **Salvesta**.
11. Sulgege leht.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Loodud konfiguratsiooni kasutamine makse töölehtede töötlemise testimiseks
1. Navigeerimispaanil avage **Moodulid > Makstaolevad arved > Maksed > Maksepäevik**.
2. Uue maksepäeviku loomiseks valige **Uus**.
3. Kirjutage välja **Nimi** järgmist: **Pakkujamakse**.
4. Valige **Read**.
5. Väljal **Konto** kirjutage väärtused `GB_SI_000001`.
6. Määra **Võlg** väärtuseks `1000`.
7. Valige suvand **Uus**.
8. Väljal **Konto** kirjutage väärtused `GB_SI_000005`.
9. Määra **Võlg** väärtuseks `2000`.
10. Kirjutage välja **Valuuta** järgmist: `EUR`.
11. Väljal **Nihke konto** kirjutage väärtused `GBSI OPER`.
12. Kirjutage välja **Makseviis** järgmist: `Electronic`.
13. Valige käsk **Salvesta**.
14. Valige **Loo maksed**.
15. Kirjutage välja **Makseviis** järgmist: `Electronic`.
16. Kirjutage välja **Faili nimi** järgmist: `Payments`.
17. Kirjutage välja **Pangakonto** järgmist: `GBSI OPER`.
18. Valige **OK** ja seejärel taas **OK**. Vaadake loodud tööleht üle, sh makseridade üksikasjad kui ka selles makseteates kasutatud iga valuutakoodi summad.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]