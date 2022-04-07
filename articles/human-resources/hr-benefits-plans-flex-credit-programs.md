---
title: Paindliku krediidiga programmide seadistamine
description: Saate kasutada rakenduses Microsoft Dynamics 365 Human Resources paindliku krediidiga programme, et registreerida töötajad eelmääratud hulgale paindlikule krediidile.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1808d703983fd11e29f83c13f6181fb3068bc49
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533764"
---
# <a name="set-up-flex-credit-programs"></a>Paindliku krediidiga programmide seadistamine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate kasutada rakenduses Microsoft Dynamics 365 Human Resources paindliku krediidiga programme, et registreerida töötajad eelmääratud hulgale paindlikule krediidile. Töötajad saavad valida, kuidas oma paindlikku krediiti jaotada. Näiteks kui töötaja on kaetud oma abikaasa ravikindlustusplaaniga, võivad nad soovida kasutada krediiti, mida nad oleks muidu kasutanud tervisekindlustuse jaoks, teisteks soodustusteks. 

1. Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Paindliku krediidiga programmid**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Soodustuse krediidi ID** | Paindliku krediidiga programmi kordumatu identifikaator. |
   | **Kirjeldus** | Paindliku krediidiga programm kirjeldus. | 
   | **Kehtivuse alguskuupäev** | Paindliku krediidiga programmi aktiivseks muutumise kuupäev. |
   | **Kuupäevani** | Paindliku krediidiga programmi lõpukuupäev. Saate jätta vaikeväärtuse (12/31/2154), mis näitab, et paindliku krediidiga programmil ei ole plaanitud aegumist. |
   | **Krediidi koguväärtus** | Krediidi hulk, mida iga töövõtja saab nende soodustuste jaoks kasutada. |
   | **Proportsionaalse jaotumise reegel** | Reeglit kasutatakse paindliku krediidi proportsionaalseks jaotamiseks, kui töövõtja palgatakse paindliku krediidi perioodi keskel. </br></br><ul><li>**Pole** – töövõtja ei saa paindlikku krediiti, kui ta on palgatud pärast paindliku krediidiga programmi perioodi algust.</li><li>**Täiskrediit** – töötaja saab paindliku krediidi koguhulga, olenemata nende palkamise ajast.</li><li>**Jaota proportsionaalselt** – töövõtja saab proportsionaalselt jaotatud hulga paindlikku krediiti, olenevalt nende tööhõive alguskuupäevast.</li></ul> |
   | **Paindliku krediidi proportsionaalse jaotamise valem** | Reeglit kasutatakse paindliku krediidi proportsionaalseks jaotamiseks töövõtjatele, kes palgatakse paindliku krediidi programmi soodustuste perioodi keskel. Proportsionaalne jaotamine põhineb tööhõive alguskuupäeval. Seda välja kasutatakse ainult siis kui valite suvandi **Jaota proportsionaalselt** väljal **Proportsionaalselt jaotamise reegel**. </br></br><ul><li>**Igapäevane** – jaotab töövõtja saadava paindliku krediidi hulga proportsionaalselt päevade tasemel. Paindliku krediidi koguhulk jagatakse perioodi päevade arvuga. Näiteks kui teie soodustuste periood on 400 päeva, jaotab süsteem paindliku krediidi koguhulga 400-ga, et arvutada paindliku krediidi hulga, mida töötaja päevas saab.</li><li>**Jooksev kuu** – jaotab töövõtja saadava paindliku krediidi hulga proportsionaalselt kuu tasemel, ümardatuna praeguse kuuni. Paindliku krediidi koguhulk jagatakse perioodi kuude arvuga. Näiteks kui teie soodustuste periood on 15 kuud, jaotab süsteem paindliku krediidi koguhulga 15-ga, et arvutada paindliku krediidi hulga, mida töötaja kuus saab.</li><li>**Järgmine kuu** – jaotab töövõtja saadava paindliku krediidi hulga proportsionaalselt kuu tasemel, ümardatuna järgmise kuuni. Paindliku krediidi koguhulk jagatakse perioodi kuude arvuga. Näiteks kui teie soodustuste periood on 15 kuud, jaotab süsteem paindliku krediidi koguhulga 15-ga, et arvutada paindliku krediidi hulga, mida töötaja kuus saab.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
