---
title: Erandite uurimine või lahendamine
description: Hankija arvepoliitikad käivitatakse, kui sisestate hankija arve leheküljel Hankija arve ja avate lehekülje Hankija arve poliitika rikkumised.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ff53198f61e1d1af3c437e9488c2a246cf820a
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8110015"
---
# <a name="research-or-resolve-exceptions"></a>Erandite uurimine või lahendamine

[!include [banner](../../includes/banner.md)]

Hankija arvepoliitikad käivitatakse, kui sisestate **hankija** arve, kasutades lehte Hankija arve ja kui avate hankija arve poliitika **rikkumiste** lehe. Hankija arve töövoogu saate konfigureerida ka selliselt, et hankija arve poliitikad käivitatakse iga kord, kui sisestate arve töövoogu. 

Hankija arvepoliitikaid ei rakendata arvete registris või **arve töölehel** loodud **arvetele**. 

Arvete vastendamise kontrollimine ei kasuta hankija arvepoliitikaid, vaid on häälestatud ostureskontro **parameetrite** lehel.

Salvestamisel kasutatakse demoettevõtte USMF-i. Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli. Enne alustamist veenduge, et arvete vastendamise **konfiguratsioonivõti** on valitud.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Hankija arve poliitikate loomise ettevalmistus
1. Avage **Ostureskontro > Seadistus > Ostusreskontro parameetrid**.
2. Klõpsake vahekaardil **Arve kinnitamine**.
3. Märkige või tühjendage **ruut Uuenda arvepäise olekut** automaatselt.
4. Klõpsake valikut **OK**.
5. Valige suvand väljal **Lahknevustega arve sisestamine**.
6. Sulgege leht.
7. Minge > **ostureskontro > poliitika seadistamiseks**.
8. Klõpsake **parameetreid**.
9. Klõpsake käsku **Lisa**.
10. Sulgege leht.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Hankija arvete poliitika reegli tüüpide loomine
1. Minge > **ostureskontro > poliitika seadistamiseks**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Reegli nimi**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. **Otsingu avamiseks** klõpsake päringu nime väljal ripploendit.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake nuppu **Salvesta**.
9. Sulgege leht.

## <a name="define-a-vendor-invoice-policy"></a>Hankija arvepoliitika määratlemine
1. Minge > **ostureskontro > poliitika seadistamiseks**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Nimi**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Laiendage või ahendage jaotist **Poliitika organisatsioonid**.
6. Valige puul Contoso Entertainment System USA.
7. Klõpsake käsku **Lisa**.
8. Laiendage või ahendage jaotist **Poliitika reeglid**.
9. Klõpsake nuppu **Poliitika reegli loomine**.
10. Sisestage väärtus väljale **Poliitika reegli kirjeldus**.
11. Klõpsake käsku **Filtreeri**.
12. Klõpsake käsku **Lisa**.
13. Märkige loendis valitud rida.
14. **Otsingu** avamiseks klõpsake väljal Tabel ripploendit.
15. Klõpsake loendis valitud real olevat linki.
16. **Otsingu avamiseks** klõpsake väljal Tuletatud tabel ripploendit.
17. Klõpsake loendis valitud real olevat linki.
18. **Otsingu** avamiseks klõpsake väljal Väli ripploendit.
19. **Tippige väärtus** väljale Välja.
20. Sulgege leht.
21. Sisestage väärtus väljale **Kriteerium**.
22. Klõpsake valikut **OK**.
23. Klõpsake valikut **OK**.
24. Sulgege leht.
25. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
