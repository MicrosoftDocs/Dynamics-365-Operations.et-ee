---
title: Kliendi maksetasude määramine
description: Looge kliendimaksete maksetasud.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5b94578e077834ce73c921dca18ad6e38c37659
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916296"
---
# <a name="establish-customer-payment-fees"></a>Kliendi maksetasude määramine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Looge kliendimaksete maksetasud.

See ülesanne kasutab demoettevõtte USMF andmeid.

1. **Navigeerimispaanil** avage **Moodulid > Müügireskontro > Maksete seadistamine > Makse maks**.
2. Klõpsake valikut **Uus**.
3. Sisestage väljale **Maksu ID** maksu ID. Tasu ID kuvatakse makse töölehtedel, mistõttu muutke see kirjeldavaks, et aru saada, millist tasu hinnatakse.  
4. Sisestage väljale **Nimi** makse nimi.
5. Kirjeldage makset väljal **Makse kirjeldus**.
6. Väljal **Kulu** vali, kas kulu võetakse kliendi või pearaamatu kontolt. Kui hinnatakse kliendi tasu, valige suvand Klient. Kui tasu hinnatakse teie organisatsiooni kuluna, valige Pearaamat. Selle ülesande puhul valige Klient.  
7. Valige väljas **Päeviku tüüp** seda makse maksu kasutada saav päeviku tüüp. Nende tasude kasutamisel kliendimakseteks on töölehe tüübiks tõenäoliselt Kliendimakse.  
8. Klõpsake valikut **Salvesta**.
9. Klõpsake **Makse maksu seadistamine**. Makse tasu seadistust kasutatakse kriteeriumide määratlemiseks, mil maksetasu hinnatakse.  Näiteks saate määrata, et tasu arvutatakse, kui pangakontoks on USMF OPER ja makseviisiks on tšekk.  
10. Selleks, et hinnata, millisele pangakontole see maks läheb, valige väljal **Rühmitamine** „Tabel“, „Rühm“ või „Kõik“. Kui valite suvandi Kõik, võidakse seda tasu hinnata kõigil pangakontodel.  Valides suvandi Tabel, võidakse seda tasu hinnata ainult teie valitud pangakontol. Suvandi Grupp valimisel võidakse seda tasu hinnata ainult valitud pangagrupi pangakontodel.  
11. Valige väljas **Panga seos** panga rühm või pangakonto. Suvandi Tabel valimisel kuvab otsing pangakontod. Suvandi Grupp valimisel kuvab otsing pangagrupid.  
12. Klõpsake loendis valitud real olevat linki.
13. Väljas **Makseviis** valige, millisele makseviisile see maks kehtib. Näiteks võite määrata tasu klientidele, kui nad saadavad makseid pigem tšekina kui elektroonilise maksena.  
14. Otsige loendist ja valige soovitud kirje.
15. Vajadusel sisestage välja **Makse valuuta** makse valuuta. Makse valuutat kasutatakse tasu määramise täiendavate kriteeriumidena.  Näiteks võib teie pank nõuda lisatasu USA dollarites saadud maksete eest, kuna nad teevad üldjuhul tehinguid ainult eurodes.  
16. Valige, kas tasu on protsent, summa või intervall.
17. Sisestage välja **Protsent/summa**, kas maksu protsent või summa. Kui välja Protsent/summa väärtuseks on Protsent, on siin sisestatud väärtus protsent. Kui välja Protsent/summa väärtuseks on Summa, on siin sisestatud väärtus summa. Kui välja Protsent/summa väärtuseks on Intervall, kasutage kihtide määratlemiseks vahekaarti Intervall.  
18. Valige väljas **Maksu valuuta** maksu valuuta. See on valuuta, milles tasu luuakse.  
19. Klõpsake valikut **Salvesta**.

