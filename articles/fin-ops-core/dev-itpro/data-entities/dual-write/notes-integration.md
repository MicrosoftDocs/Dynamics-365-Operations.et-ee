---
title: Integratsiooni teatis
description: See artikkel kirjeldab märkuse andmete integreerimist topeltkirjutuses.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 8e1444aa311bb2dc74705a3791e58c3187ecd8ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876711"
---
# <a name="note-integration"></a>Integratsiooni teatis

[!include [banner](../../includes/banner.md)]



Äriprotsesside jooksul Microsoft Dynamics 365 kasutajad koguvad sageli teavet oma klientide kohta. See teave kirjendatakse tegevuste ja märkustena. See artikkel kirjeldab märkuse andmete integreerimist topeltkirjutuses.

Kliendi teavet saab klassifitseerida järgmiselt:

+ **Käivitatav teave, mida Dynamics 365 kasutaja kliendi eest käsitseb** – näiteks Contoso (Dynamics 365 kasutaja) viib läbi värskendusseansi. Üks Contoso klientidest (klient) soovib osaleda shows. Klient palub Contoso töötajal reserveerida nende jaoks vaba pesa. Reserveerimine toimub Contoso sündmuses osaleja kalendris.
+ **Dynamics 365 kasutaja toimingu teave** – näiteks klient, kes ostab Surface'i ühikut, sisestab erijuhised, mis näitavad, et seade peaks enne tarnet olemakingituseks. Need juhised on tegevusatav teave, mida peaks käsitsema pakendamise eest vastutav Contoso töötaja.
+ **Mittetegevuslik teave** – näiteks klient külastab Contoso kauplust ja väljendab vestluse ajal kauplusepartneriga huvi *Halo* mängu ja mängutarvikute vastu. Kaupluse seostamine teeb selle teabe kohta märkuse. Tootesoovituste mootor kasutab seda siis kliendile soovituste andmiseks.

Üldiselt on tegutsetav teave hõivatud tegevustena Finantside ja *toimingute* rakendustes ja kliendi kaasamise rakendustes. Mittetegevuslik teave salvestatakse märkustena *Finantside* ja toimingute rakendustes *ning marginaalidena kliendikogemuse* rakendustes.

> [!TIP]
> Ehkki märkused on mõeldud mittetegevustava teabe jaoks, ei takista rakendused teil neid kasutamast talletada ja käsitseda tegevustavat teavet, kui soovite neid sel viisil kasutada.

Microsoft vabastab praegu funktsiooni märkuse integreerimiseks. (Tegevuse integreerimise funktsioon vabastatakse hiljem.) Märkuse integreerimine on saadaval klientide, hankijate, müügitellimuste ja ostutellimuste puhul.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Märkuse loomine kliendikogemuse rakenduses

Märkuse loomiseks kliendikogemuse rakenduses ja seejärel sünkroonige see Finantside ja Toimingute rakendusega, järgige neid samme.

1. Kliendi kaasamise rakenduses avage kliendi kontokirje.
2. Paanil **Ajajoon** valige plussmärk (**+**) ja seejärel valige **Märkus** märkuse loomiseks.

    ![Märkuse loomine customer engagement rakenduses.](media/notes-ce-1.png)

3. Sisestage pealkiri ja kirjeldus ning seejärel valige käsk **Lisa märkus**.

    ![Sisestage pealkiri ja kirjeldus.](media/notes-ce-2.png)

    Uus märkus lisatakse kliendi ajajoonele.

    ![Uus märkus kliendi ajajoonel.](media/notes-ce-3.png)

4. Logige rakendusse Finantsid ja Toimingud sisse ja avage sama kliendikirje. Pange tähele, et **Ma nused** nupp (paberi märkide sümbol) ülemises parempoolses nurgas näitab, et kirje on manusega.

    ![Manuse teatis.](media/notes-ce-4.png)

5. Lehe **Manused** avamiseks valige nupp **Manused** lehel. Peaksite leidma teate, mille lõite Customer Engagementi rakenduses.

    ![Märkus kliendikogemuse rakendusest.](media/notes-ce-5.png)

Märkuse uuendused sünkroonitakse edasi-tagasi rakenduse Finants ja Toimingud ja kliendikogemuse rakenduse vahel.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Märkuse loomine rakenduses Finantsid ja toimingud

Samuti saate luua märkuse Rakenduses Finantsid ja Toimingud ja see sünkroonitakse customer Engagementi rakendusega.

Märkuse loomiseks rakenduses Finantsid ja toimingud ja seejärel sünkroonige see kliendikogemuse rakendusega, järgige neid samme.

1. Valige finantside ja toimingute rakenduse lehel **Manused suvand** Uus **·** \> **märkus.**

    ![Märkuse loomine rakenduses Finantsid ja toimingud.](media/notes-fo-1.png)

2. Sisestage pealkiri ja lühikirjeldus ning seejärel valige **Salvestamine**.

    ![Sisestage pealkiri ja kirjeldus.](media/notes-fo-2.png)

3. Kliendikogemuse rakenduses värskendage kirjet. Uue märkuse leiate ajajoonelt.

    ![Uus märkus customer engagement rakenduse ajajoones.](media/notes-fo-3.png)

Te saate liigitada märkuse nii sisemiseks kui väliseks.

- Finantside ja toimingute rakenduse **lehel Manused** avage märkus ja seejärel **valige välja Piirang** suvand Sisemine **või** **Väline**.

    ![Piiranguväli.](media/notes-fo-4.png)

Samuti saate luua URLi.

1. Valige finantside ja toimingute rakenduse lehel **Manused** **·**\> uus **URL.**
2. Sisestage pealkiri ja URL.
3. Väljal **Piirang** valige **Sisemine** või **Väline**.

    ![URL-i loomine rakenduses Finantsid ja toimingud.](media/notes-fo-5.png)

4. Valige käsk **Salvesta**.

    Kuna klienditeenuse rakendustel ei ole URL-i tüüpi, integreeritakse URL märkusena topeltkirjutusega.

    ![URLi loomine customer engagement rakenduses.](media/notes-ce-6.png)

> [!NOTE]
> Failimanuseid ei toetata.

## <a name="templates"></a>Mallid

Maksuandmed sisaldavad tabeli kaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

| Finantside ja toimingute rakendus | Klientide kaasamise rakendus | Kirjeldus |
|----------------------------|-------------------------|-------------|
| [Kliendi manused](mapping-reference.md#230) | Märkused | Ettevõtted, mis kasutavad kliendispetsiifilise teabe kogumiseks (nii organisatsioonide kui ka isikute puhul) lihtteksti ja URL-e. |
| [Hankija dokumendimanused](mapping-reference.md#231) | Märkused | Ettevõtted, mis kasutavad kliendispetsiifilise teabe kogumiseks (nii organisatsioonide kui ka isikute puhul) lihtteksti ja URL-e. |
| [Müügitellimuse päise dokumendi manused](mapping-reference.md#229) | Märkused | Ettevõtted, mis kasutavad müügitellimuse teabe kogumiseks lihtteksti ja URL-e. |
| [Ostutellimuse päise dokumendi manused](mapping-reference.md#232) | Märkused | Ettevõtted, mis kasutavad müügitellimuse teabe kogumiseks lihtteksti ja URL-e. |

## <a name="limitations"></a>Kitsendused

Pärast märkmelahenduse installimist ei saa te seda desinstallida. 

Lisateavet vt [topeltkirjutuse vastendamise viitest](mapping-reference.md).
