---
title: Hankija konto loomine
description: See protseduur selgitab, kuidas luua hankijakontot ning lisada aadressi ja kontaktteavet.
author: mkirknel
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba585a9bb1a296bbf7181530e151d737bfa22fc2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149592"
---
# <a name="create-a-vendor-account"></a>Hankija konto loomine

[!include [banner](../../includes/banner.md)]

See protseduur selgitab, kuidas luua hankijakontot ning lisada aadressi ja kontaktteavet. Protseduur ei näita, kuidas täita kõiki välju ostmiseks ja lõplikuks eesmärgiks. Lisateavet nende väljade kohta leiate väljade kirjeldusest. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades. Hankijakontod loob tavaliselt hankespetsialist või müügireskontro personal.


## <a name="create-a-vendor-account"></a>Hankija konto loomine
1. Avage **Navigeerimispaan > Moodulid > Hanked > Hankijad > Kõik hankijad**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Hankija konto**.
    - Väärtus võidakse sisestada automaatselt. Sel juhul võite selle etapi vahele jätta.  
    - Saate luua hankijakontod isikule või organisatsioonile. See mõjutab, millised väljad on saadaval. Selles näites loome organisatsioonile hankija konto.   
4. Sisestage või valige väärtus väljal **Nimi**. Kui teie hankija on süsteemis juba registreeritud osapool, saate ta sellele väljale valida ripploendi abil ning uus hankijakonto pärib juba registreeritud aadressi ja kontaktteabe.
5. Sisestage või valige väärtus väljal **Grupp**. Hankijagruppi kasutatakse nende hankijate grupeerimiseks, kellel on mis tahes järgmised ühised parameetrid: maksetingimused, tasakaalustusperiood, varude sisestamise pearaamatukontod, sh käibemaksugrupp, vaikepearaamatukontod, tootefiltri koodid või tarneprognoosi konfiguratsioon.
6. Sisestage arv väljale **Töötajate arv**.
7. Sisestage väärtus väljale **Organisatsiooni number**.

## <a name="add-an-address"></a>Aadressi lisamine
1. Laiendage jaotist **Aadressid**.
2. Klõpsake käsku **Lisa**.
3. Sisestage või valige väärtus väljal **Eesmärk**. Saate valida ühe või mitu eesmärki. Neid kasutatakse, et valida õige aadress antud eesmärgi jaoks. Näiteks kui eesmärk on „Arve”, kasutatakse seda aadressi arvete saatmisel.
4. Sisestage väärtus väljale **Nimi või kirjeldus**.
5. Sisestage või valige väärtus väljale **Riik/regioon**. Sisestage aadressi üksikasjad. Valitud riik/piirkond määratleb teile kuvatavad väljad olenevalt selle riigi/piirkonna aadressivormingust. 
6. Klõpsake valikut **OK**.

## <a name="add-contact-information"></a>Kontaktteabe lisamine
1. Laiendage jaotist **Kontaktteave**.
2. Klõpsake käsku **Lisa**.
3. Sisestage väärtus väljale **Kirjeldus**.
4. Valige suvand väljalt **Tüüp**.
5. Sisestage väärtus väljale **Kontaktnumber/aadress**. Saate valida märkeruudu Esmane, kui see on esmane kontakt.  
6. Klõpsake valikut **Salvesta**.
7. Sulgege leht.
8. Sulgege leht.

