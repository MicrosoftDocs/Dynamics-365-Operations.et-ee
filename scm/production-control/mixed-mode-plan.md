---
title: "Mixed mode planeerimine - ühendada diskreetse, protsessi ja lahja hankimine"
description: "Selles artiklis antakse teavet segarežiimis plaanimise kohta. Segarežiimis plaanimisel saate tarneahelat materjali voo alusel mudeldada. Tagab Microsoft Dynamics 365 operatsioonide sisendid ja väljundid järgib oma mudelid, sõltumata pakkumispõhist poliitikat, mis on valitud (kanbans, tootmistellimuste, ostutellimuste, partii tellimuste või üleviimistellimuste)."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d635421112f6d1e79a47090de3ffc4178b36b132
ms.lasthandoff: 03/31/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Mixed mode planeerimine - ühendada diskreetse, protsessi ja lahja hankimine

Selles artiklis antakse teavet segarežiimis plaanimise kohta. Segarežiimis plaanimisel saate tarneahelat materjali voo alusel mudeldada. Tagab Microsoft Dynamics 365 operatsioonide sisendid ja väljundid järgib oma mudelid, sõltumata pakkumispõhist poliitikat, mis on valitud (kanbans, tootmistellimuste, ostutellimuste, partii tellimuste või üleviimistellimuste). 

Saate valuda üleüldise toote tarnimise strateegia olenemata toote struktuurist.  

Näiteks võib kanbani juhtelement olla komplektis, kus materjale tootmistellimuste, kanbanide, kannete, partiitellimuste või teie tarneahela iseloomule vastava kombinatsiooni järgi koostepiirkonda väljastatakse, kuid teil on ikkagi täielik ülevaade kõikidest tarnetest. See võimalus viib optimeeritud tarneahela protsessideni ja parema nähtavuseni tarneahelas.  

Koondplaneerimises kasutatavate tarnepoliitikate granulaarsus oleneb laoala dimensioonidest, mis on lubatud kattedimensioonidena. Selleks, et koondplaneerimine juhiks eri tüüpi asukohtade täiendamist ja tarnet (nt eraldades tootmisosakonna erinevateks tootmisüksusteks või eraldades eri tüüpi materjalide ja lõpetatud kaupade laod), soovitame teil lubada suvandid Laoala ja Ladu kattedimensioonidena. Teise võimalusena saab suvandi Ladu kattedimensioonina välja jätta. Sellisel juhul, kui kasutate täiustatud laohaldust, juhib kõiki liikumisi laos laotöö, samas kui kõiki ladudevahelisi liikumisi saab juhtida tagastamise kanbanidega.

## <a name="supply-policies"></a>Tarnepoliitikad
Dynamics 365 operatsioonide planeerimise segaolek kontrollib, kuidas toode on tarnitud ja, vastavalt pakkumise, kuidas tuletatud vajadused (tarbimine koosluse kaupade materjalide \[komplekti\]) välja. Tellimuse tüübi alusel hangib süsteem automaatselt materjale, et nõuetele vastata.  

Tarnepoliitikaid saab määratleda toote tasemel või mis tahes granulaarsusega, mis teie nõudeid toetab. Määratlete tarnepoliitikate granulaarsuse lehel **Tellimuse vaikesätted**.  

Tarnepoliitikaid saab juhtida toote, kauba dimensioonide (konfiguratsioon, värv ja suurus), koha ja lao järgi. See seadistus on tehtud lehel **Kauba laovarud**.  

Tellimuse vaiketüüo juhib, mida tellimuse koondplaneerimine loob.  

Olenemata sellest, kuidas on kujundatud tarneahelas, Dynamics 365 toiminguteks toetab oma mix tarnekindluse põhimõtete. Saate kasutada tootmistellimusi, mis on hangitud kanbanidest. Teise võimalusena saate kasutada partiitellimust, mis nõuab toodet, mida tarnitakse kannete või kanbanidega.  

Dynamics 365 operatsioonide tagab, et sisendite järgib mudel.  

Ladu materjali komplekteerimiseks määratakse dünaamiliselt käitamise ajal pärast tarnepoliitika määratlemist.  

Tavaliselt ei looda kanbane tulevaste kuupäevadega, sest kanbanil on lühike elutsükkel. Tarneahela täieliku nähtavuse säilitamiseks oleme kasutusele võtnud uue plaanimise kontseptsiooni „plaanitud kanban”, mida kasutatakse tuletatud nõuete arvutamiseks ja mis aitab tagada, et nõuded hangitakse sama loogika alusel, mida kasutatakse tegeliku kanbani loomisel.  

Sama loogika kehtib kõikide muude tarnepoliitika tüüpide puhul. Seega põhineb pikaajaline materjalide plaanimine samal loogikal, mida eeldate käitada tegelike tellimuste puhul pärast tootmise ja tarnimise kinnitamist.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Materjalide eraldamise crosssupply suunatud ressursside tarbimise kooslusele
Ressursside tarbimise on oluline funktsionaalsus. Ressursi tarbimine võimaldab laol komplekteeritavate materjalide dünaamilist valimist, mis põhineb tarnepoliitikal (tellimuse tüüp), ja muudab alusandmete säilitamise lihtsamaks.  

Ressursi tarbimine nõuab, et laod, kust materjalid komplekteeritakse, määratakse selle alusel, kuidas toodet tarnitakse. Teisisõnu otsib süsteem käitamisel ressursid, mida tuleks tootmiseks kasutada. Nende ressursside alusel otsib süsteem komplekteerimislao.  

Tarnepoliitikast sõltumatu töö puhul ei pea te muutma koosluse teavet, kui tarnet muudetakse. Ajutisi muudatusi, Dynamics 365 operatsioonide tagab, et see võimaldaks õige laost.

## <a name="process-manufacturing--the-production-type"></a>Protsessi tootmine – toote tüüp
Täielik paindlikkus mixed mode, soovitame kasutada tootmise tüüp komplektide kõik tooted. Seejärel saate tootmistellimusi, kanbans, üleviimiskorralduste või ostutellimuste toote tarnida. Protsesstootmiseks peate kasutama tootmise tüüpi **Valem**, **Kaastoode**, **Kõrvalsaadus** või **Plaanimisüksus**. Kanbane ja tootmistellimusi ei saa nende tootmistüüpide puhul kasutada.


