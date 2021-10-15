---
title: Toote konfiguratsioonimudeli seadistamine
description: See artikkel kirjeldab toote konfiguratsioonimudeli seadistamise ja loomise samme.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dc9f46d91dc298a5c8babee2b370fea09f61741
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578220"
---
# <a name="set-up-a-product-configuration-model"></a>Toote konfiguratsioonimudeli seadistamine

[!include [banner](../includes/banner.md)]

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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]