---
title: Toiminguressursi loomine
description: Operatsiooniressurss sooritab projekti või tootmisprotsessi tegevusi.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b91d5ea7618010ab9d4006d643c59a7f995eb0c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981227"
---
# <a name="create-an-operations-resource"></a>Toiminguressursi loomine

[!include [banner](../../includes/banner.md)]

Operatsiooniressurss sooritab projekti või tootmisprotsessi tegevusi. Selles protseduuris näitlikustatakse, kuidas määratleda operatsiooniressurssi. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.

1. Avage Ressursid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Ressurss.
4. Sisestage väljale Kirjeldus soovitud väärtus.

## <a name="define-capacity-and-consumption-parameters"></a>Võimsus- ja tarbimisparameetrite määratlemine
1. Laiendage jaotist Toiming.
2. Sisestage arv väljale Praagi protsent.
3. Sisestage või valige väärtus väljal Seadistuse kategooria.
    * Määrake kulukategooria, mis määratleb seadistuskulu konto.  
4. Sisestage või valige väärtus väljal Käitusaja kategooria.
    * Määrake kulukategooria, mis määratleb käitusaja kulu konto.  
5. Valige või sisestage väärtus väljal Koguse kategooria.
    * Määrake kulukategooria, mis määratleb väljundkoguse põhjal ressursikulu konto.  
6. Valige suvand väljal Võimsusühik.
    * Määrake operatsiooniressursside võimsuse väljendamise ühik.  
7. Sisestage arv väljale Võimsus.
8. Sisestage arv väljale Efektiivsusprotsent.
    * Määrake operatsiooniressursside oodatav efektiivsus. Efektiivsusprotsent reguleerib operatsiooniressursside läbilaskevõimet ja mõjutab ressursile reserveeritud aega.  
9. Sisestage arv väljale Operatsioonide planeerimise protsent.
    * Määrake operatsiooniressursi suurim tootmisvõimsuse protsent, mida soovite operatsioonide planeerimisel kasutada.  
10. Valige väljal Piiratud võimsus suvand Jah.
    * Valige suvand Jah, kui operatsiooniressurss tuleks planeerida tegeliku saadavaloleva võimsuse alusel ning kui arvesse tuleks võtta olemasolevaid võimsuse reserveeringuid. Kui valitud on suvand Ei, eeldatakse, et operatsiooniressursil on piiramatu võimsus, mistõttu ressurss võib olla üle broneeritud.  
11. Valige suvand Jah väljal Kitsaskohana toimiv ressurss.

## <a name="define-working-times"></a>Tööaegade määratlemine
1. Laiendage jaotist Kalendrid.
2. Klõpsake vahekaarti Lisa.
3. Sisestage või valige väärtus väljal Kalender.
    * Määrake ressursi võimsust (tundides) määratlev töögraafik.  
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.

## <a name="define-resource-capabilities"></a>Ressursivõimaluste määratlemine
1. Laiendage jaotist Võimalused.
2. Klõpsake vahekaarti Lisa.
    * Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada. Planeerimismootor eraldab ressursid, sobitades iga tegevuse ressursinõuded saadaolevate operatsiooniressursside võimsustega.  
3. Sisestage või valige väärtus väljal Võimalus.
4. Sisestage arv väljale Tase.
    * Määrake oskusetase, mille alusel ressurss võimsust töötleb.  
5. Sisestage arv väljale Prioriteet.
    * Määrake operatsiooniressursi prioriteet võimsuse suhtes. Prioriteedi planeerimisel valitakse esmalt kõrgeima prioriteediga (madalaima arvväärtusega) operatsiooniressurss.  

## <a name="assign-resource-to-resource-group"></a>Ressursigrupile ressursi määramine
1. Laiendage jaotist Ressursigrupid.
2. Klõpsake vahekaarti Lisa.
    * Ressursigrupp määratleb operatsiooniressursside koha, tootmisüksuse ja lao konteksti. Operatsiooniressurssi saab planeerida ainult juhul, kui see määratakse ressursigrupile, ja ainult kohta, kus on ressursigrupi asukoht.  
3. Sisestage või valige väärtus väljal Ressursigrupp.
4. Sisestage või valige väärtus väljal Sisendasukoht.
    * Määrake operatsiooniressursi tarbitavate materjalide lao asukoht.  

