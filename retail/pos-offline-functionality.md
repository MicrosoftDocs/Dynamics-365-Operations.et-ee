---
title: "Kassa võrguühenduseta funktsioonid"
description: "Selles artiklis antakse teavet Retail Modern POS-i ühenduseta režiimi kohta, kus kassaseadmed lülituvad automaatselt kanali andmebaasist võrguühenduseta andmebaasi, kui jaemüügiserver pole saadaval. Artikkel sisaldab ka teavet ühenduseta režiimi üldise seadistuse kohta ja selgitab andmete sünkroonimist, mis toimub ühenduseta andmebaasi ja kanali andmebaasi vahel."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>Kassa võrguühenduseta funktsioonid

Selles artiklis antakse teavet Retail Modern POS-i ühenduseta režiimi kohta, kus kassaseadmed lülituvad automaatselt kanali andmebaasist võrguühenduseta andmebaasi, kui jaemüügiserver pole saadaval. Artikkel sisaldab ka teavet ühenduseta režiimi üldise seadistuse kohta ja selgitab andmete sünkroonimist, mis toimub ühenduseta andmebaasi ja kanali andmebaasi vahel.

<a name="overview"></a>Ülevaade
--------

Jaemüügi kaasaegne POS, point Müügikoht (POS) seade läheb ühenduseta režiimis kui jaemüügi server pole saadaval. Seega, kui jaemüügi serveri ühendus on kadunud, jaemüügi kaasaegne POS lülitub automaatselt võrguühenduseta andmebaasi. Kui andmetaotlus müügikande ajal ühenduseta profiilis konfigureeritud aegumisintervalli jooksul ei õnnestu, lülitub Retail Modern POS automaatselt ühenduseta andmebaasi ja jätkab müügikannet. Kui kassaseade on ühenduseta režiimis, püüab Retail Modern POS pärast ühenduseta profiilis määratud uuesti ühendamise intervalli uuesti jaemüügiserveriga ühendust luua. See uue ühenduse loomise katse toimub ainult kande alguses.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Retail Modern POS-i ühendusrežiimi määramine

Retail Modern POS-i olekupäis näitab ühenduse hetkeseisu ja aknas **Ühenduse olek** kuvatakse viimase ühenduseta andmebaasiga sünkroonimise katse olek. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Ühenduseta ja ühendusega režiimide vahel käsitsi liikumiseks nupu loomine

Saate lisada Retail Modern POS-i ühendusega ja ühenduseta režiimide vahel käsitsi liikumiseks nupu. Looge nupp kassatoimingule **917 – andmebaasiühenduse olek**. Selle nupu nimi on **Katkesta ühendus**, kui Retail Modern POS on jaemüügiserveriga ühendatud, ja **Ühenda**, kui ühendus puudub. Saate kasutada seda nuppu ühenduse vaatamiseks ja jaemüügiserveriga ühenduse katkestamiseks või ühenduse loomiseks. [![Katkesta nuppu jaemüügi kaasaegne POS](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Häälestamine
Ühenduseta tugi POS seadme (registri) lubamiseks seadke selle **toeta ühenduseta** võimalus **Jah** kohta on **registreerida** lehele. Uue kanali andmebaasi üksus on loodud ja poe kanali andmed gruppi. Siis käivitage kõik vajalikud jaotusgraafikud ühenduseta andmebaasile andmepakettide loomiseks. Seejärel installige jaemüügi kaasaegne POS ühenduseta versioon. Paigaldamise käigus loob ühenduseta andmebaasi. Lisaks installima Microsoft SQL Server 2014 kiire vajadusel. Ühenduseta andmete sünkroonimine algab pärast esmakordset sisselogimist Retail Modern POS-i.

## <a name="data-synchronization"></a>Andmete sünkroonimine
Kaupluse andmeedastaja abil saadetakse koondandmed ühenduseta andmebaasi. Vaikimisi saadetakse jaotusgraafiku käitamisel muudatused nii kanali andmebaasi kui ka ühenduseta andmebaasi. Retail Modern POS sisaldab Asynci sünkroonimisteeki, mis laadib alla kõik saadaolevad andmepaketid ja lisab need ühenduseta andmebaasi. Kui kõik kanded on ühenduseta loodud, laadib Retail Modern POS need jaemüügiserverisse, nii et neid saab lisada kanali andmebaasi. Ühenduseta andmete sünkroonimine saab toimuda ainult siis, kui Retail Modern POS töötab. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


