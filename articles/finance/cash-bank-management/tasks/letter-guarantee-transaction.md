---
title: Garantiikirja kanne
description: See protseduur selgitab garantiikirja töötlemist.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30e21c11b067f6def127f3eab026d7255ab1ca29
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779930"
---
# <a name="letter-of-guarantee-transaction"></a>Garantiikirja kanne

[!include [banner](../../includes/banner.md)]

See protseduur selgitab garantiikirja töötlemist.



Enne selle toimingu tegemist peavad olema tehtud järgmised toimingud.

- Pangateenuste ja garantiikirjade sisestusreeglite häälestamine.

- Garantiikirja jaoks panga süsteemiteenuse leppe loomine.



See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Garantiikirjaga müügitellimuse loomine
1. Minge kõigi **> müügireskontro > müügireskontrosse**.
2. Klõpsake valikut **Uus**.
3. Väljale **Kliendi konto** sisestage või valige väärtus.
4. Laiendage jaotist Üldine.
5. Sisestage või valige väärtus väljale **Sait**.
6. Klõpsake loendis valitud real olevat linki.
7. Sisestage või valige väärtus väljale **Ladu**.
8. Klõpsake loendis valitud real olevat linki.
9. **Väljal Pangadokumendi tüüp** valige **garantiikiri**.
10. Klõpsake valikut **OK**.
11. Sisestage või valige väärtus väljale **Kauba kood**.
12. Sisestage arv väljale **Ühiku hind**.
13. Laiendage jaotis Rea üksikasjad.
14. Klõpsake vahekaarti Tarne.
    * Märkus. Valige suvandi Tarnekuupäeva kontroll sätteks Puudub  
15. Sisestage **väljale Nõutav** lähetuskuupäev kuupäev.
16. Sisestage **kinnitatud** lähetuskuupäeva väljale kuupäev.

## <a name="process-letter-of-guarantee_request"></a>Garantiikirja protsess Taotlemine
1. Tegevuspaanil klõpsake nuppu **Haldamine**.
2. Klõpsake **garantiikirjal**.
3. Tegevuspaanil klõpsake **garantiikirja**.
4. Dialoogiakna **avamiseks** klõpsake nuppu Taotlus.
5. Sisestage **või** valige väärtus väljal Tüüp.
6. Klõpsake loendis valitud real olevat linki.
7. Sisestage arv väljale **Väärtus**.
8. Sisestage **aegumiskuupäeva** väljale kuupäev ja kellaaeg.
9. Klõpsake valikut **OK**.
10. Sulgege leht.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Garantiikirja protsess Edasta panka
1. Avage sularaha **ja panga > ja > garantiikirjad**.
2. Otsige loendist ja valige soovitud kirje.
3. Dialoogiakna **avamiseks klõpsake** nuppu Edasta panka.
4. Sisestage või valige väärtus väljal **Pangakonto**.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake valikut **OK**.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Garantiikirja Protsess Võta pangalt vastu
1. Klõpsake **nuppu Võta pangast vastu**, et avada dialoogiaken.
2. **Tippige väärtus** väljale Panga number.
    * Kontrollige arvutatud marginaali ja **kulu** väljade **väärtusi**.  
3. Klõpsake valikut **OK**.
4. Laiendage jaotist Tegevused.
    * Kontrollige kirjet Võta pangalt vastu.  
5. Klõpsake, et järgida linki töölehe **partiinumbri väljal**.
6. Klõpsake **Read**.
    * Kontrollige töölehekannete sisestamist.  
7. Sulgege leht.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Garantiikirja protsess Anna kasusaajale
1. Minge kõigi **> müügireskontro > müügireskontrosse**.
2. Klõpsake loendis valitud real olevat linki.
3. Tegevuspaanil klõpsake nuppu **Haldamine**.
4. Klõpsake **garantiikirjal**.
5. Tegevuspaanil klõpsake **garantiikirja**.
6. Dialoogi **avamiseks klõpsake nuppu** Anna kasusaajale.
7. Klõpsake valikut **OK**.
8. Avage sularaha **ja panga > ja > garantiikirjad**.
9. Otsige loendist ja valige soovitud kirje.
10. Dialoogi **avamiseks klõpsake nuppu** Anna kasusaajale.
11. Klõpsake valikut **OK**.
12. Laiendage jaotist Tegevused.
    * Kinnitage kirje Anna kasusaajale.  

## <a name="process-letter-of-guarantee_increase-value"></a>Garantiikirja protsess Suurenda väärtust
1. Minge kõigi **> müügireskontro > müügireskontrosse**.
2. Klõpsake loendis valitud real olevat linki.
3. Tegevuspaanil klõpsake nuppu **Haldamine**.
4. Klõpsake **garantiikirjal**.
5. Tegevuspaanil klõpsake **garantiikirja**.
6. Dialoogiakna **avamiseks** klõpsake nuppu Suurenda väärtust.
7. **Sisestage number väljale** Lisa väärtus.
8. Klõpsake valikut **OK**.
9. Avage sularaha **ja panga > ja > garantiikirjad**.
10. Otsige loendist ja valige soovitud kirje.
11. Dialoogiakna **avamiseks** klõpsake nuppu Suurenda väärtust.
12. Klõpsake valikut **OK**.
13. Laiendage jaotist Tegevused.
    * Kontrollige kirjet Suurenda väärtust.  
14. Otsige loendist ja valige soovitud kirje.
15. Klõpsake, et järgida linki töölehe **partiinumbri väljal**.
16. Klõpsake **Read**.
    * Kontrollige sisestatud töölehekandeid.  

## <a name="process-letter-of-guarantee_liquidate"></a>Garantiikirja protsess Likvideeri
1. Minge kõigi **> müügireskontro > müügireskontrosse**.
2. Klõpsake loendis valitud real olevat linki.
3. Tegevuspaanil klõpsake nuppu **Haldamine**.
4. Klõpsake **garantiikirjal**.
5. Tegevuspaanil klõpsake **garantiikirja**.
6. Dialoogiakna **käivitamiseks** klõpsake nuppu Likvideeri.
7. Klõpsake valikut **OK**.
8. Avage sularaha **ja panga > ja > garantiikirjad**.
9. Otsige loendist ja valige soovitud kirje.
10. Dialoogiakna **käivitamiseks** klõpsake nuppu Likvideeri.
11. Klõpsake valikut **OK**.
12. Laiendage jaotist Tegevused.
    * Kontrollige kirjet Likvideeri.  
13. Otsige loendist ja valige soovitud kirje.
14. Klõpsake, et järgida linki töölehe **partiinumbri väljal**.
15. Klõpsake **Read**.
    * Kontrollige sisestatud töölehekandeid.  
16. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
