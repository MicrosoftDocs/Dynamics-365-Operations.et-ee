---
title: Garantiikirja kanne
description: See protseduur selgitab garantiikirja töötlemist.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 089515287fc5706983b10614f69b4b1cd90178c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834712"
---
# <a name="letter-of-guarantee-transaction"></a>Garantiikirja kanne

[!include [banner](../../includes/banner.md)]

See protseduur selgitab garantiikirja töötlemist.



Enne selle toimingu tegemist peavad olema tehtud järgmised toimingud.

- Pangateenuste ja garantiikirjade sisestusreeglite häälestamine.

- Garantiikirja jaoks panga süsteemiteenuse leppe loomine.



See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Garantiikirjaga müügitellimuse loomine
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
4. Laiendage jaotist Üldine.
5. Sisestage või valige väärtus väljal Koht.
6. Klõpsake loendis valitud real olevat linki.
7. Sisestage või valige väärtus väljal Ladu.
8. Klõpsake loendis valitud real olevat linki.
9. Valige väljal Pangadokumendi tüüp suvand Garantiikiri.
10. Klõpsake nuppu OK.
11. Sisestage või valige väärtus väljal Kaubakood.
12. Sisestage arv väljale Ühiku hind.
13. Laiendage jaotis Rea üksikasjad.
14. Klõpsake vahekaarti Tarne.
    * Märkus. Valige suvandi Tarnekuupäeva kontroll sätteks Puudub  
15. Sisestage kuupäev väljale Nõutav lähetuskuupäev.
16. Sisestage kuupäev väljale Kinnitatud lähetuskuupäev.

## <a name="process-letter-of-guarantee_request"></a>Garantiikirja protsess Taotlemine
1. Klõpsake tegumiribal valikut Haldamine.
2. Klõpsake suvandit Garantiikiri.
3. Klõpsake tegevuspaanil suvandit Garantiikiri.
4. Klõpsake suvandit Taotlus rippdialoogi avamiseks.
5. Sisestage või valige väärtus väljal Tüüp.
6. Klõpsake loendis valitud real olevat linki.
7. Sisestage number väljale Väärtus.
8. Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.
9. Klõpsake nuppu OK.
10. Sulgege leht.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Garantiikirja protsess Edasta panka
1. Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake suvandit Edasta panka, et avada rippdialoog.
4. Sisestage väärtus väljale Pangakonto või valige see.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake nuppu OK.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Garantiikirja Protsess Võta pangalt vastu
1. Klõpsake suvandit Võta pangalt vastu, et avada rippdialoog.
2. Sisestage väärtus väljale Panga number.
    * Kontrollige arvutatud väärtusi väljadel Marginaal ja Kulu.  
3. Klõpsake nuppu OK.
4. Laiendage jaotist Tegevused.
    * Kontrollige kirjet Võta pangalt vastu.  
5. Klõpsake linki väljal Töölehe partiinumber.
6. Klõpsake valikut Read.
    * Kontrollige töölehekannete sisestamist.  
7. Sulgege leht.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Garantiikirja protsess Anna kasusaajale
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake loendis valitud real olevat linki.
3. Klõpsake tegumiribal valikut Haldamine.
4. Klõpsake suvandit Garantiikiri.
5. Klõpsake tegevuspaanil suvandit Garantiikiri.
6. Klõpsake suvandit Anna kasusaajale, et avada rippdialoog.
7. Klõpsake nuppu OK.
8. Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake suvandit Anna kasusaajale, et avada rippdialoog.
11. Klõpsake nuppu OK.
12. Laiendage jaotist Tegevused.
    * Kinnitage kirje Anna kasusaajale.  

## <a name="process-letter-of-guarantee_increase-value"></a>Garantiikirja protsess Suurenda väärtust
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake loendis valitud real olevat linki.
3. Klõpsake tegumiribal valikut Haldamine.
4. Klõpsake suvandit Garantiikiri.
5. Klõpsake tegevuspaanil suvandit Garantiikiri.
6. Klõpsake suvandit suurenda väärtust rippdialoogi avamiseks.
7. Sisestage arv väljale Lisatav väärtus.
8. Klõpsake nuppu OK.
9. Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.
10. Otsige loendist ja valige soovitud kirje.
11. Klõpsake suvandit suurenda väärtust rippdialoogi avamiseks.
12. Klõpsake nuppu OK.
13. Laiendage jaotist Tegevused.
    * Kontrollige kirjet Suurenda väärtust.  
14. Otsige loendist ja valige soovitud kirje.
15. Klõpsake linki väljal Töölehe partiinumber.
16. Klõpsake valikut Read.
    * Kontrollige sisestatud töölehekandeid.  

## <a name="process-letter-of-guarantee_liquidate"></a>Garantiikirja protsess Likvideeri
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake loendis valitud real olevat linki.
3. Klõpsake tegumiribal valikut Haldamine.
4. Klõpsake suvandit Garantiikiri.
5. Klõpsake tegevuspaanil suvandit Garantiikiri.
6. Klõpsake suvandit Likvideeri, et avada rippdialoog.
7. Klõpsake nuppu OK.
8. Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake suvandit Likvideeri, et avada rippdialoog.
11. Klõpsake nuppu OK.
12. Laiendage jaotist Tegevused.
    * Kontrollige kirjet Likvideeri.  
13. Otsige loendist ja valige soovitud kirje.
14. Klõpsake linki väljal Töölehe partiinumber.
15. Klõpsake valikut Read.
    * Kontrollige sisestatud töölehekandeid.  
16. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]