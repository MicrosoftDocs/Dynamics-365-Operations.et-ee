---
title: Saate häälestada hankija arve poliitikaid.
description: See artikkel selgitab, kuidas seadistada hankija arve poliitikaid.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 049b38b6feba5f4369d79b89b4c81a8195dd7758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904726"
---
# <a name="set-up-vendor-invoice-policies"></a>Saate häälestada hankija arve poliitikaid.

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas seadistada hankija arve poliitikaid. Hankija arvepoliitikad käivitatakse, kui sisestate **hankija** arve, kasutades lehte Hankija arve ja kui avate hankija arve poliitika **rikkumiste** lehe. Hankija arve töövoogu saate konfigureerida ka selliselt, et hankija arve poliitikad käivitatakse iga kord, kui sisestate arve töövoogu. 

- Hankija arvepoliitikad ei kehti arvetele, mis on loodud arveregistris või arve töölehel.  
- Arvete vastendamise kontrollimine ei kasuta hankija arvepoliitikaid, vaid seadistatakse selle asemel ostureskontro **parameetrite** lehel.  
- Salvestamisel kasutatakse demoettevõtte USMF-i. Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli. Enne alustamist veenduge, et arvete vastendamise **konfiguratsioonivõti** on valitud.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Hankija arve poliitikate loomise ettevalmistus
1. Avage **Navigeerimispaan > Moodulid > Ostureskontro > Häälestus > Ostureskontro parameetrid**.
2. Valige vahekaart **Arve kinnitamine**.
3. Valige või tühjendage oleku **Arve päise automaatne uuendamine** märkeruut.
4. Valige nupp **OK**.
5. Valige suvand väljal **Lahknevustega arve sisestamine**.
6. Sulgege leht.
7. Avage **Navigeerimispaan > Moodulid > Ostureskontro > Poliitika häälestus > Hankija arve poliitika**.
8. Valige **Parameetrid**.
9. Valige **Lisa**.
10. Avalehele naasmiseks sulgege lehekülg.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Hankija arvete poliitika reegli tüüpide loomine
1. Avage **Navigeerimispaan > Moodulid > Ostureskontro > Poliitika häälestus > Hankija arve poliitika reegli tüübid**.
2. Valige suvand **Uus**.
3. Sisestage väärtused väljadele **Reegli nimi** ja **Kirjeldus**.
4. Valige väljal **Päringu nimi** otsingu avamiseks ripploendi nupp ja seejärel valige soovitud kirje.
5. Valige käsk **Salvesta**.
6. Avalehele naasmiseks sulgege lehekülg.

## <a name="define-a-vendor-invoice-policy"></a>Hankija arvepoliitika määratlemine
1. Avage **Navigeerimispaan > Moodulid > Ostureskontro > Poliitika häälestus > Hankija arve poliitika**.
2. Valige suvand **Uus**.
3. Sisestage väärtused väljadele **Nimi** ja **Kirjeldus**.
4. Laiendage või ahendage jaotist **Poliitika organisatsioonid**.
5. Valige puust **Contoso Entertainment System USA**.
6. Valige **Lisa**.
7. Laiendage või ahendage jaotist **Poliitika reeglid**.
8. Valige **Poliitika reegli loomine**.
9. Sisestage väärtus väljale **Poliitika reegli kirjeldus**.
10. Valige **Filter**.
11. Valige **Lisa**. Valige soovitud kirje.
12. Väljadel **Tabel**, **Tuletatud tabel** ja **Väli**, valige või sisestage suvandid ripploendi menüüdest.
13. Sulgege leht.
14. Sisestage väärtus väljale **Kriteerium**.
15. Valige nupp **OK**.
16. Valige nupp **OK**.
17. Avalehele naasmiseks sulgege leheküljed.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
