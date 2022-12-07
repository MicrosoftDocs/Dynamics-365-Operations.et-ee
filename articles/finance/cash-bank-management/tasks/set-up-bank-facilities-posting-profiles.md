---
title: Pangateenuste ja garantiikirjade sisestusreeglite seadistamine
description: Selle ülesandega luuakse panga süsteemiteenus ja sisestusreegel, mis on vajalik garantiikirja töötlemiseks.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0987ae1e9cfbb1e2d2a957a5fd1ad82257292c0a
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804097"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Pangateenuste ja garantiikirjade sisestusreeglite seadistamine

[!include [banner](../../includes/banner.md)]

Selle ülesandega luuakse panga süsteemiteenus ja sisestusreegel, mis on vajalik garantiikirja töötlemiseks.



See ülesanne kasutab demoettevõtte USMF andmeid. 




## <a name="general-ledger-parameter"></a>Pearaamatu parameeter
1. Avage sularaha **- ja > halduse > parameetrid**.
2. Laiendage jaotist **Pank** .
3. Valige suvand **Garantiikirja** lubamine.
4.  **Otsingu avamiseks** klõpsake kande töölehe väljal ripploendit.
5. Otsige loendist ja valige soovitud kirje.
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake vahekaardil **Numbriseeriad** .
    * Numbriseeria määratlemine garantiikirja numbri ja garantiikirja kandeviidete jaoks  
8. Klõpsake nuppu **Salvesta**.
9. Sulgege leht.

## <a name="create-bank-facility"></a>Panga süsteemiteenuse loomine
1. Avage sularaha **- ja pangahalduse > seadistus > panga vahendid**.
2. Klõpsake valikut **Uus**.
3. Väljale Süsteemiteenuse **grupp** sisestage panga süsteemiteenuse grupi nimi garantiikirja kande jaoks.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Klõpsake nuppu **Salvesta**.
6. Klõpsake vahekaardil Süsteemiteenuse **tüübid**.
7. Klõpsake valikut **Uus**.
8. Väljale Süsteemiteenuse **tüüp** sisestage panga süsteemiteenuse tüübi nimi, mis on seotud panga süsteemiteenuse lepinguga.
9. Sisestage väärtus väljale **Kirjeldus**.
10.  **Otsingu avamiseks** klõpsake väljal Süsteemiteenuse grupp ripploendit.
11. Otsige loendist ja valige soovitud kirje.
12. Klõpsake loendis valitud real olevat linki.
13. Valige väljal **Süsteemiteenuse** olemus suvand.
14. Klõpsake nuppu **Salvesta**.
15. Sulgege leht.

## <a name="bank-posting-profile"></a>Panga sisestusreegel
1. Avage sularaha **- ja pangahalduse > seadistus > pangadokumentide sisestusreeglid**.
2. Klõpsake valikut **Uus**.
3.  **Otsingu avamiseks** klõpsake väljal Konto/grupi number ripploendit.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6.  **Väljal Tasakaalusta konto** valige tasakaalustamiseks põhikonto.
7.  **Valige kulukannete** konto väljal Kulude konto.
8.  **Marginaali konto** väljal valige marginaalkande konto.
9.  **Valige garantiikirja** kande likvideerimiskonto väljal Likvideerimiskonto. 
10. Klõpsake nuppu **Salvesta**.
11. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
