---
title: Integratsiooni teatis
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse ja teenuse vahel.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c73da804d724ea75ae6ccd479d1b7f3cf02d48c4
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062771"
---
# <a name="note-integration"></a>Integratsiooni teatis

[!include [banner](../../includes/banner.md)]



Äriprotsesside jooksul Microsoft Dynamics 365 kasutajad koguvad sageli teavet oma klientide kohta. See teave kirjendatakse tegevuste ja märkustena. Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse ja teenuse vahel.

Kliendi teavet saab klassifitseerida järgmiselt:

+ **Käivitatav teave, mida Dynamics 365 kasutaja kliendi eest käsitseb** – näiteks Contoso (Dynamics 365 kasutaja) viib läbi värskendusseansi. Üks Contoso klientidest (klient) soovib osaleda shows. Klient palub Contoso töötajal reserveerida nende jaoks vaba pesa. Reserveerimine toimub Contoso sündmuses osaleja kalendris.
+ **Dynamics 365 kasutaja toimingu teave** – näiteks klient, kes ostab Surface'i ühikut, sisestab erijuhised, mis näitavad, et seade peaks enne tarnet olemakingituseks. Need juhised on tegevusatav teave, mida peaks käsitsema pakendamise eest vastutav Contoso töötaja.
+ **Mittetegevuslik teave** – näiteks klient külastab Contoso kauplust ja väljendab vestluse ajal kauplusepartneriga huvi *Halo* mängu ja mängutarvikute vastu. Kaupluse seostamine teeb selle teabe kohta märkuse. Tootesoovituste mootor kasutab seda siis kliendile soovituste andmiseks.

Üldiselt jäädvustatakse teostatav teave tegevustena *Finance* and Operationsi rakendustes ja klientide kaasamise rakendustes. Mittevastav teave jäädvustatakse finance and Operationsi rakendustes märkmetena *ja* kliendi kaasamise rakendustes *marginaalidena*.

> [!TIP]
> Ehkki märkused on mõeldud mittetegevustava teabe jaoks, ei takista rakendused teil neid kasutamast talletada ja käsitseda tegevustavat teavet, kui soovite neid sel viisil kasutada.

Microsoft vabastab praegu funktsiooni märkuse integreerimiseks. (Tegevuse integreerimise funktsioon vabastatakse hiljem.) Märkuse integreerimine on saadaval klientide, hankijate, müügitellimuste ja ostutellimuste puhul.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Märkuse loomine kliendikogemuse rakenduses

Kliendi kaasamise rakenduses märkme loomiseks ja seejärel sünkroonige see rakendusega Finance and Operations, tehke järgmist.

1. Kliendi kaasamise rakenduses avage kliendi kontokirje.
2. Paanil **Ajajoon** valige plussmärk (**+**) ja seejärel valige **Märkus** märkuse loomiseks.

    ![Märkuse loomine customer engagement rakenduses.](media/notes-ce-1.png)

3. Sisestage pealkiri ja kirjeldus ning seejärel valige käsk **Lisa märkus**.

    ![Sisestage pealkiri ja kirjeldus.](media/notes-ce-2.png)

    Uus märkus lisatakse kliendi ajajoonele.

    ![Uus märkus kliendi ajajoonel.](media/notes-ce-3.png)

4. Logige rakendusse Finance and Operations sisse ja avage sama kliendikirje. Pange tähele, et **Ma nused** nupp (paberi märkide sümbol) ülemises parempoolses nurgas näitab, et kirje on manusega.

    ![Manuse teatis.](media/notes-ce-4.png)

5. Lehe **Manused** avamiseks valige nupp **Manused** lehel. Peaksite leidma teate, mille lõite Customer Engagementi rakenduses.

    ![Märkus kliendikogemuse rakendusest.](media/notes-ce-5.png)

Kõik märkme värskendused sünkroonitakse edasi-tagasi rakenduse Finance and Operations ja kliendi kaasamise rakenduse vahel.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Märkme loomine rakenduses Finance and Operations

Märkuse saate luua ka rakenduses Finance and Operations ja see sünkroonitakse kliendi kaasamise rakendusega.

Märkuse loomiseks finance and Operationsi rakenduses ja seejärel sünkroonige see kliendi kaasamise rakendusega, tehke järgmist.

1. Valige rakenduse **Finance and Operations lehel** Manused **Uus** \> **märkus.**

    ![Märkme loomine rakenduses Finance and Operations.](media/notes-fo-1.png)

2. Sisestage pealkiri ja lühikirjeldus ning seejärel valige **Salvestamine**.

    ![Sisestage pealkiri ja kirjeldus.](media/notes-fo-2.png)

3. Kliendikogemuse rakenduses värskendage kirjet. Uue märkuse leiate ajajoonelt.

    ![Uus märkus customer engagement rakenduse ajajoones.](media/notes-fo-3.png)

Te saate liigitada märkuse nii sisemiseks kui väliseks.

- Avage rakenduses **Rahandus ja Toimingud leht Manused** märkus ja seejärel valige **väljal** Piirang **Sisemine** või **Väline**.

    ![Piiranguväli.](media/notes-fo-4.png)

Samuti saate luua URLi.

1. Valige rakenduse **Finance and Operations lehel** Manused **Uus** \> **URL.**
2. Sisestage pealkiri ja URL.
3. Väljal **Piirang** valige **Sisemine** või **Väline**.

    ![URL-i loomine rakenduses Finance and Operations.](media/notes-fo-5.png)

4. Valige käsk **Salvesta**.

    Kuna klienditeenuse rakendustel ei ole URL-i tüüpi, integreeritakse URL märkusena topeltkirjutusega.

    ![URLi loomine customer engagement rakenduses.](media/notes-ce-6.png)

> [!NOTE]
> Failimanuseid ei toetata.

## <a name="templates"></a>Mallid

Maksuandmed sisaldavad tabeli kaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

| Rakendus Finance and Operations | Klientide kaasamise rakendus | Kirjeldus |
|----------------------------|-------------------------|-------------|
| [Kliendi manused](mapping-reference.md#230) | Märkused | Ettevõtted, mis kasutavad kliendispetsiifilise teabe kogumiseks (nii organisatsioonide kui ka isikute puhul) lihtteksti ja URL-e. |
| [Hankija dokumendimanused](mapping-reference.md#231) | Märkused | Ettevõtted, mis kasutavad kliendispetsiifilise teabe kogumiseks (nii organisatsioonide kui ka isikute puhul) lihtteksti ja URL-e. |
| [Müügitellimuse päise dokumendi manused](mapping-reference.md#229) | Märkused | Ettevõtted, mis kasutavad müügitellimuse teabe kogumiseks lihtteksti ja URL-e. |
| [Ostutellimuse päise dokumendi manused](mapping-reference.md#232) | Märkused | Ettevõtted, mis kasutavad müügitellimuse teabe kogumiseks lihtteksti ja URL-e. |

## <a name="limitations"></a>Kitsendused

Pärast märkmelahenduse installimist ei saa te seda desinstallida. 

Lisateavet vt [topeltkirjutuse vastendamise viitest](mapping-reference.md).
