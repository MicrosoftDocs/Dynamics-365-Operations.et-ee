---
title: TDS-i tagastatava sertifikaadi numbrite kirjendamine
description: See teema selgitab, kuidas kasutada tagasisaadav sertide lehte, et kirjendada sertide numbreid ja kuupäevi allika (TDS) sertide jaoks, mis on vastu võetud kindla hankija, kliendi või pearaamatu jaoks.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5d62f560fe58a5fb7bd158bed9bcb111d75c7f00
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726486"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>TDS-i tagastatava sertifikaadi numbrite kirjendamine

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas kasutada **tagasisaadavat sertide** lehte, et kirjendada sertide numbreid ja kuupäevi allika (TDS) sertide jaoks, mis on vastu võetud kindla hankija, kliendi või pearaamatu jaoks. TDS-i serdi numbrite ja kuupäevade värskendamiseks, mis on kirjendatud TDS-i kannete jaoks sellel leheküljel, kasutage **Uuenda serti** lehte (**Pearaamat \> Perioodiline \> Kinnipeetava maksu \> Serdi värskendamine**). Pärast TDS-i serdinumbrite värskendamist sulgege need.

Järgige neid samme TDS-i serdi numbrite ja kuupäevade salvestamiseks.

1. Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> taastatavad serdid**.

    [![Taastatavate sertide leht.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Valige **taastatavad serid** lehel, **maksutüübi** väljal valige **TDS**.
3. Valige **Uus**, et luua uus kirje.
4. Väljale **Serdinumber** sisestage TDS-i kontsessiooniserdi number.
5. Valige **Kontotüübi** väljal konto tüüp, mille kohta TDS-sert on saadud: **Hanija**, **klient**, või **pearaamat**.
6. Sõltuvalt **Konto** väljast valige hankija-, kliendi-või pearaamatukonto number, sõltuvalt valitud kontotüübist. Väljal **Nimi** kuvatakse hankija, kliendi või pearaamatukonto nimi.
7. Väljal **Serte kokku** sisestage digitaalsete sertifikaatide kogus.
8. Väljale **Kuupäev** sisestage TDS-i kontsessiooniserdi numbri kuupäev.
9. Valige **Päringud** et avada **Serdi kannete** leht, kus saate vaadata TDS-i kandeid, mille jaoks on TDS-tunnistuse number ja kuupäev uuendatud. Seda teavet saab uuendada **Serdi värskendamine** lehel (**Maks \> Deklaratsioonid \> Kinnipeetav maks \> Värskenda sert**).

    **Serdi uuendamise** lehel kuvatakse TDS-kande kohta järgmine teave:

    - **Kuupäev** – TDS kannete sisestuskuupäev.
    - **Kviitung** - kuvatakse TDS tehingukande kviitungi number.
    - **Allikas** - moodul, kus TDS-kanne loodi.
    - **Konto** – hankija-, kliendi- või pearaamatukonto number, mille jaoks TDS-kanne loodi.
    - **Nimi** – hankija-, kliendi- või pearaamatukonto number, mille jaoks TDS-kanne loodi.
    - **Summa** - arvele sisestatud summa, mida TDS on arvutanud.
    - **Maksusumma** – TDS-i maksusumma, mis kande jaoks arvutatud.
    - **Serdi kuupäev** – TDS-i serdi kuupäev, mis uuendati TDS-kande jaoks.
    - **Serdi number** – TDS-i serdi number, mis uuendati TDS-kande jaoks.

10. Lehel **Taastatavad serdid** valige märkeruut **Suletud** et sulgeda TDS-i serdi number pärast seda, kui olete selle TDS-kannete värskendamise lõpetanud **Värskenda sertifikaat** lehel.

    Kõigi leheküljel kirjete jaoks **Suletud** märkeruudu märkimiseks valige **Märgi kõik**.

    > [!NOTE]
    > TDS-i serdinumbrid, mille jaoks on valitud märkeruut **Suletud**, pole saadaval **serdi värskendamise** lehel.
