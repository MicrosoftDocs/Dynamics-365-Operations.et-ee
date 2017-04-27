---
title: Toote konfiguratsioonimudeli seadistamine
description: See artikkel kirjeldab toote konfiguratsioonimudeli seadistamise ja loomise samme.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: e7138dcc15cb8e16ad5cee83b40ba72555d89e6a
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-a-product-configuration-model"></a>Toote konfiguratsioonimudeli seadistamine

[!include[banner](../includes/banner.md)]


See artikkel kirjeldab toote konfiguratsioonimudeli seadistamise ja loomise samme.

| Ülesanne                                                        | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tooteetaloni loomine.                                    | Tooteetaloni saate luua loendist **Tooteetalon**. Vabastage tooteetalon kõikidesse asjakohastesse ettevõtetesse. Toote konfiguratsioonimudeli või alamkomponendi versioonina kasutatava tooteetaloni puhul tuleb konfiguratsioonitehnoloogiana valida **Piirangupõhine konfiguratsioon** ja tootedimensiooni grupiga jaoks tuleb valida ainult konfiguratsioonidimensioon. |
| Komponentide loomine.                                          | Komponendid saate luua lehel **Komponendid**. Komponendid on toote konfiguratsioonimudeli ehitusplokid ja neid saab mitme tootekonfiguratsiooni mudeli puhul korduvalt kasutada.                                                                                                                                                                                                                      |
| Atribuuditüüpide loomine.                                     | Atribuuditüübid saate luua lehel **Atribuuditüübid**. Atribuuditüübid määravad andmetüübid kõigile atribuutidele, mida kasutatakse toote konfiguratsioonimudelites. Atribuuditüübid **Kahendmuutuja**, **Tekst** fikseeritud loendiga ja **Täisarv** vahemikuga esitavad toote konfiguratsioonimudeli põhjal tootevariandi konfigureerimisel saadaolevate väärtuste komplekti.       |
| Toote konfiguratsioonimudeli loomine.                       | Toote konfiguratsioonimudeli saate luua lehel **Uus toote konfiguratsioonimudel**.                                                                                                                                                                                                                                                                                                              |
| Toote konfiguratsioonimudelile atribuutide lisamine.            | Looge atribuut lehe **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** kiirkaardil **Atribuudid**. Atribuudid kirjeldavad toote konfiguratsioonimudeli funktsioone.                                                                                                                                                                                                       |
| Toote konfiguratsioonimudelile piirangute lisamine.           | Looge piirangud lehe **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** kiirkaardil **Piirangud**. Piiranguid on piirangud, millele peab toote konfiguratsioon vastama. Piirangud saavad olla avaldisepiirangud või tabelipiirangud.                                                                                                                                 |
| Toote konfiguratsioonimudelile alamkomponentide lisamine.         | Looge alamkomponendid lehe **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** kiirkaardil **Alamkomponendid**. Alamkomponendid on seotud komponentidega ja lingitud seda alamkomponenti esindavate kaupadega.                                                                                                                                                                       |
| Toote konfiguratsioonimudelile kasutajanõuete lisamine.     | Kasutajanõuded sarnanevad alamkomponentidele, kuid ei viita kaubale. Võite käsitleda kasutajanõudeid kui fiktiivset kooslust. Otse kasutajanõuete alla paigutatavad koosluseread või protsessioperatsioonid koondatakse ülemkomponenti.                                                                                                                       |
| Toote konfiguratsioonimudelile koosluseridade lisamine.             | Looge koosluseread lehe **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** kiirkaardil **Koosluseread**. Koosluseread on tootevariandi loomiseks nõutav osa.                                                                                                                                                                                                 |
| Toote konfiguratsioonimudelile protsessioperatsioonide lisamine.      | Looge protsessioperatsioonid lehe **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** kiirkaardil **Protsessioperatsioonid**. Protsessioperatsioonid on samm tootevariandi valmistamiseks läbitavate sammude jadas.                                                                                                                                                    |
| Toote konfiguratsioonimudeli aktiivse versiooni loomine. | Toote konfiguratsioonimudeli aktiivse versiooni saate luua lehel **Versioonid**. Versioon on seos toote konfiguratsioonimudeli ja tooteetaloni vahel. Toote konfiguratsioonimudelit, millel on aktiivne versioon, saab konfigureerida müügitellimuselt, müügipakkumiselt, ostutellimuselt või tootmistellimuselt.                                                               |
| Toote konfiguratsioonimudeli testimine.                         | Toote konfiguratsioonimudelit saate testida kas lehel **Piirangupõhise toote konfiguratsioonimudeli üksikasjad** või **Toote konfiguratsioonimudelite loend**. Toote konfiguratsioonimudelite testimine simuleerib tootemudeli konfigureerimisprotsessi, mis toimub tellimuse töötlemise ajal.                                                                                                |
| Toote konfiguratsioonimudeli malli loomine.                | Toote konfiguratsioonimudeli malli saate luua lehel **Konfiguratsioonimallid**. Konfiguratsioonimall sisaldab toote konfiguratsioonimudeli atribuutide väärtusi. Valige atribuudiväärtused lehel **Rea konfigureerimine**. Saate laadida tootemudeli konfiguratsioonimalli tootemudeli konfigureerimisel.                                                   |
| Kauba konfigureerimine.                                          | Toote konfiguratsioonimudeleid saab konfigureerida müügitellimuselt, müügipakkumiselt, ostutellimuselt või tootmistellimuselt.                                                                                                                                                                                                                                                                           |






