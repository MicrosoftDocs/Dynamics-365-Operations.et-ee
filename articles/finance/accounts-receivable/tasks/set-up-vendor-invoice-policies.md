---
title: Hankija arve poliitikate seadistamine
description: Selles teemas selgitatakse, kuidas seadistada tarnijate arvete poliitikat.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79cbabba74fdb76d8fcc0553d39e0f140aacf03e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995443"
---
# <a name="set-up-vendor-invoice-policies"></a>Hankija arve poliitikate seadistamine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada tarnijate arvete poliitikat. Hankija arvepoliitikad käivitatakse, kui sisestate hankija arve leheküljel Hankija arve ja avate lehekülje Hankija arve poliitika rikkumised. Hankija arve töövoogu saate konfigureerida ka selliselt, et hankija arve poliitikad käivitatakse iga kord, kui sisestate arve töövoogu. 

- Hankija arvepoliitikad ei kehti arvetele, mis on loodud arveregistris või arve töölehel.  
- Arvete võrdlemise kinnitamisel ei kasutata hankija arvepoliitikaid, vaid selle sätted määratakse leheküljel Ostureskontro parameetrid.  
- Salvestamisel kasutatakse demoettevõtte USMF-i. Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli. Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine.


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

