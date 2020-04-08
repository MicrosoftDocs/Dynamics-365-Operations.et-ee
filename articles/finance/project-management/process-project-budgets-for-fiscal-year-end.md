---
title: Projektieelarvete ülekandmine finantsaasta lõpus
description: Selles artiklis kirjeldatakse kuidas järelejäänud eelarvesummasid järgmistesse aastatesse üle kanda ja eelarveregistri üksikasju luua.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172326"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projektieelarvete ülekandmine finantsaasta lõpus

[!include [banner](../includes/banner.md)]

Mitmeaastase projektiga töötamisel võib teil finantsaasta lõpus tekkida eelarve ülejääk. Saate kanda eelarve jääksummad üle valitud tulevasse aastasse ja luua seostatud pearaamatusse nende summadega eelarveregistri üksikasjad. Enne jääksummade ülekandmist vaadake üle ja analüüsige järelejäänud eelarve summasid.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Eelarve jääksummade ülevaatamine ja analüüsimine

Läbige järgmised etapid projektide aastalõpu eelarvesummade ülevaatamiseks, kuid mitte nende summade edasi kandmiseks.

1. Avage jaotis **Projektihaldus ja -arvestus** > **Perioodiline** > **Eelarved** > **Edasikantavad eelarved**. 
2. Lehe **Projekti eelarve edasikandmisprotsess** vahekaardil **Aastalõpu suvandid** veenduge, et suvand **Projektieelarve jääksumma edasikandmine** ei oleks lubatud.
3. Vahekaardi **Parameetrid** väljal **Projekti eelarveaasta** valige selle finantsaasta, mille eelarve jääksummat vaadata soovite. 
4. Väljal **Avatud finantsaasta** valige see finantsaasta, mille eelarve jääksummasid vaadata soovite. 
5. Väljal **Prognoosimudelist** valige **Järelejäänud eelarve**. 
6. Teie valitud kriteeriumitele vastavate projektide kaasamiseks ilma järelejääva eelarveta valige **Nulljäägi kuvamine**.  
7. Valige vahekaardil **Eelarvete valimine** käsk **Too kõik eelarved**, et laadida kõik eelarved, mis vastavad teie valitud kriteeriumitele ja seejärel valige **Töötle**. 
8. Andmebaasipäringu loomiseks, mis laadib paani konkreetse eelarvete kogumi, klõpsake valikut **Too valitud eelarved**.

Paanil kindla rea kohta kohta saamiseks valige see rida ja seejärel valige **Kuva eelarve üksikasjad** või **Vaata kontosid**.

## <a name="carry-forward-remaining-budget-amounts"></a>Kanna eelarve järelejäänud summad edasi 

Kui töötlete eelarve jääksummasid, saate luua pearaamatusse kanded edasikantavate summade kohta. Pearaamatu kannete loomiseks tehke järgmised toimingud jaotises [Eelarve summade edasi kandmine ja pearaamatu kannete loomine](#carry-forward). 

> [!NOTE]
> Edasikantud eelarvesummad kantakse üle eelarvemudelisse, mis on valitud lehel **Eelarvemudelid** edasikandmise eelarvemudeliks.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Eelarvesummade edasikandmine ja pearaamatu kannete loomine

1.  Valige **Projektihaldus ja -arvestus** > **Perioodiline** > **Eelarved** > **Edasikantavad eelarved**. 
2. Lehel **Projekti eelarve edasikandmisprotsess** valige **Aastalõpp** ja seejärel lubage **Projekti eelarve jääksummade edasikandmine** ja **Eelarveregistri kirjete loomine pearaamatus**. 
3. Tehke järgmised valikud vahekaardi **Parameetrid** väljagrupis **Projekti parameetrid**.

   - **Projekti eelarveaasta**: valige selle finantsaasta algus, mille eelarve jääksummasid vaadata soovite. 
   - **Kasum ja kahjum**: looge pearaamatus kasumi ja kahjumi kanded. 
   -  **WIP**: looge pearaamatus poolelioleva töö (WIP) kanded.
   -  **Palgaarvestus**: looge pearaamatus palgaarvestuse eraldamise kanded. 

5. Sisestage järgmine teave väljagrupis **Pearaamat**. 

   - Väljal **Avatud finantsaasta** valige see finantsaasta, millele projektide eelarve jääksummasid üle kanda soovite. Vaikeväärtus on üks aasta pärast välja **Projekti eelarveaasta** väärtust.
   -  Väljal **Edasikandmise periood** valige periood, milles soovite pearaamatusse eelarveregistri üksikasju luua. See on tavaliselt avatud finantsaasta esimene periood.

6. Sisestage järgmine teave väljagrupis **Kopeeri üksusest/üksusesse**.

   - Väljal **Eelarvemudelist** valige projekti eelarvemudel, mis on seostatud eelarve jääksummadega, mida soovite projektide puhul üle kanda. 
   - Väljal **Pearaamatu eelarvemudelisse** valige pearaamatu eelarvemudel, mis on seostatud eelarvesummadega, mida soovite pearaamatusse üle kanda. 
   -  Valige **Müügivaluuta ülekandmine** projekti müügivaluuta kasutamiseks pearaamatu kannetel, mis luuakse projektide eelarvesummade ülekandmisel. Kui seda suvandit pole valitud, kasutavad kanded arvestusvaluutat. 
   -  Valige **Nulljäägi kuvamine**, et kaasata ilma eelarve jääksummata projektid, kuid mis vastavad muudele valitud kriteeriumitele paani allservas kuvatud projektidel.

7. Valige vahekaardil **Eelarvete valimine** käsk **Too kõik eelarved**, et laadida kõik eelarved, mis vastavad teie valitud kriteeriumitele. Kui eelistate luua andmebaasipäringu, mis laadib paani konkreetse projekti eelarvete kogumi, klõpsake valikut **Too valitud eelarved**.
8. Iga projekti puhul, mida soovite töödelda, valige suvand vastava projekti rea alguses.

    > [!TIP]
    > Kõigi või enamiku projektide valimiseks valige märge ülemises vasakus nurgas. Mis tahes projekti töötlemise välistamiseks tühjendage selle projekti märge.

9. Selleks , et kanda valitud projektide eelarve jääksummad üle valitud finantsaastasse ja luua pearaamatusse eelarveregistri üksikasjad, valige **Töötle**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Eelarvesummade edasikandmine ilma pearaamatu kannete loomiseta

1. Avage jaotis **Projektihaldus ja -arvestus** > **Perioodiline** > **Eelarved** > **Edasikantavad eelarved**.
2. Lehe **Projekti eelarve edasikandmisprotsess** väljal **Aastalõpu suvandid** valige **Projektieelarve jääksumma edasikandmine**.
3. Grupi **Parameetrid** väljal **Projekti eelarveaasta** valige selle finantsaasta, mille eelarve jääksummasid vaadata soovite.
4. Sisestage järgmine teave grupis **Kopeeri üksusest/üksusesse**.

   - Väljal **Eelarvemudelist** valige projekti eelarvemudel, mis on seostatud eelarve jääksummadega, mida soovite projektide puhul üle kanda. 
   - Valige **Nulljäägi kuvamine** teie valitud kriteeriumitele vastavate projektide kaasamiseks ilma järelejääva eelarveta.
   - Valige grupis **Eelarvete valimine** käsk **Too kõik eelarved**, et laadida kõik eelarved, mis vastavad teie valitud kriteeriumitele. Andmebaasipäringu loomiseks, mis laadib paani konkreetse projekti eelarvete kogumi, klõpsake valikut **Too valitud eelarved**.

5. Iga projekti puhul, mida soovite töödelda, valige suvand vastava projekti rea alguses. 
6. Valige **Töötle**, et kanda valitud projektide eelarve jääksummad üle valitud finantsaastale.

