---
title: Integratsiooni teatis
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse ja teenuse vahel.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: beab7f2fc4fd96ce7a28734d2449445b3b5d4451
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750832"
---
# <a name="note-integration"></a>Integratsiooni teatis

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Äriprotsesside jooksul Microsoft Dynamics 365 kasutajad koguvad sageli teavet oma klientide kohta. See teave kirjendatakse tegevuste ja märkustena. Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse ja teenuse vahel.

Kliendi teavet saab klassifitseerida järgmiselt:

+ **Käivitatav teave, mida Dynamics 365 kasutaja kliendi eest käsitseb** – näiteks Contoso (Dynamics 365 kasutaja) viib läbi värskendusseansi. Üks Contoso klientidest (klient) soovib osaleda shows. Klient palub Contoso töötajal reserveerida nende jaoks vaba pesa. Reserveerimine toimub Contoso sündmuses osaleja kalendris.
+ **Dynamics 365 kasutaja toimingu teave** – näiteks klient, kes ostab Surface'i ühikut, sisestab erijuhised, mis näitavad, et seade peaks enne tarnet olemakingituseks. Need juhised on tegevusatav teave, mida peaks käsitsema pakendamise eest vastutav Contoso töötaja.
+ **Mittetegevuslik teave** – näiteks klient külastab Contoso kauplust ja väljendab vestluse ajal kauplusepartneriga huvi *Halo* mängu ja mängutarvikute vastu. Kaupluse seostamine teeb selle teabe kohta märkuse. Tootesoovituste mootor kasutab seda siis kliendile soovituste andmiseks.

Üldiselt on tegutsetav teave hõivatud *tegevustena* Finance and Operations rakendustes ja kliendikogemuste rakenduses. Mittetegutsetav teave on hõivatud *teadetena* Finance and Operations rakenduses ja *märkustena* kliendikogemuse rakendustes.

> [!TIP]
> Ehkki märkused on mõeldud mittetegevustava teabe jaoks, ei takista rakendused teil neid kasutamast talletada ja käsitseda tegevustavat teavet, kui soovite neid sel viisil kasutada.

Microsoft vabastab praegu funktsiooni märkuse integreerimiseks. (Tegevuse integreerimise funktsioon vabastatakse hiljem.) Märkuse integreerimine on saadaval klientide, hankijate, müügitellimuste ja ostutellimuste puhul.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Märkuse loomine kliendikogemuse rakenduses

Märkuse loomiseks kliendi teenuse rakendusesse ja seejärel sünkroonige see Finance and Operations rakendusega, järgige neid samme.

1. Kliendi kaasamise rakenduses avage kliendi kontokirje.
2. Paanil **Ajajoon** valige plussmärk (**+**) ja seejärel valige **Märkus** märkuse loomiseks.

    ![Märkuse loomine kliendikogemuse rakenduses](media/notes-ce-1.png)

3. Sisestage pealkiri ja kirjeldus ning seejärel valige käsk **Lisa märkus**.

    ![Sisestage pealkiri ja kirjeldus](media/notes-ce-2.png)

    Uus märkus lisatakse kliendi ajajoonele.

    ![Uus märkus kliendi ajajoonel](media/notes-ce-3.png)

4. Logige sisse Finance and Operations rakendusse ja avage sama kliendikirje. Pange tähele, et **Ma nused** nupp (paberi märkide sümbol) ülemises parempoolses nurgas näitab, et kirje on manusega.

    ![Manuse teatis](media/notes-ce-4.png)

5. Lehe **Manused** avamiseks valige nupp **Manused** lehel. Peaksite leidma teate, mille lõite Customer Engagementi rakenduses.

    ![Märkus kliendikogemuse rakendusest](media/notes-ce-5.png)

Kõik märkuse uuendused sünkroonitakse edasi-tagasi rakenduse Finance and Operations ja kliendikogemuse rakenduse vahel.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Märkuse loomine Finance and Operations kliendikogemuse rakenduses

Saate luua Finance and Operations rakendusse märkuse ja seejärel see sünkroonitakse kliendikogemuse rakendusega.

Märkuse loomiseks Finance and Operations rakenduses ja seejärel selle kliendikogemuse sünkroniseerimiseks, järgige järgmisi samme.

1. Valige Finance and Operations rakenduse lehel **Manused** suvand **Uus** \> **Märkus**.

    ![Märkuse loomine Finance and Operations rakenduses](media/notes-fo-1.png)

2. Sisestage pealkiri ja lühikirjeldus ning seejärel valige **Salvestamine**.

    ![Sisestage pealkiri ja kirjeldus](media/notes-fo-2.png)

3. Kliendikogemuse rakenduses värskendage kirjet. Uue märkuse leiate ajajoonelt.

    ![Uus märkus kliendi kaasamise rakenduse ajajoones](media/notes-fo-3.png)

Te saate liigitada märkuse nii sisemiseks kui väliseks.

- Avage Finance and Operations rakenduses **Manused** leheküljel märkus ja seejärel valige suvand **Piirang** väljal **Sisemine** või **Väline**.

    ![Piiranguväli](media/notes-fo-4.png)

Samuti saate luua URLi.

1. Valige Finance and Operations rakenduse lehel **Manused** suvand **Uus** \> **url**.
2. Sisestage pealkiri ja URL.
3. Väljal **Piirang** valige **Sisemine** või **Väline**.

    ![URLi loomine Finance and Operations rakenduses](media/notes-fo-5.png)

4. Valige käsk **Salvesta**.

    Kuna klienditeenuse rakendustel ei ole URL-i tüüpi, integreeritakse URL märkusena topeltkirjutusega.

    ![URLi loomine kliendikogemuse rakenduses](media/notes-ce-6.png)

> [!NOTE]
> Failimanuseid ei toetata.

## <a name="templates"></a>Mallid

Maksuandmed sisaldavad tabeli kaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

| Finance and Operations rakendus | Klientide kaasamise rakendus | Kirjeldus |
|----------------------------|-------------------------|-------------|
| [Kliendi manused](mapping-reference.md#230) | Märkused | Ettevõtted, mis kasutavad kliendispetsiifilise teabe kogumiseks (nii organisatsioonide kui ka isikute puhul) lihtteksti ja URL-e. |
| [Hankija dokumendimanused](mapping-reference.md#231) | Märkused | Ettevõtted, mis kasutavad kliendispetsiifilise teabe kogumiseks (nii organisatsioonide kui ka isikute puhul) lihtteksti ja URL-e. |
| [Müügitellimuse päise dokumendi manused](mapping-reference.md#229) | Märkused | Ettevõtted, mis kasutavad müügitellimuse teabe kogumiseks lihtteksti ja URL-e. |
| [Ostutellimuse päise dokumendi manused](mapping-reference.md#232) | Märkused | Ettevõtted, mis kasutavad müügitellimuse teabe kogumiseks lihtteksti ja URL-e. |

Lisateavet vt [topeltkirjutuse vastendamise viitest](mapping-reference.md).
