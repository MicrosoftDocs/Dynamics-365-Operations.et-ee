---
title: Intressi töötlemine
description: See protseduur kirjeldab viivisearvete loomist, printimist ja sisestamist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4f1ed6d0199235e946d55dfa904246c109acba42
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220127"
---
# <a name="process-interest"></a>Intressi töötlemine

[!include [banner](../../includes/banner.md)]

See protseduur kirjeldab viivisearvete loomist, printimist ja sisestamist. See ülesanne kasutab demoettevõtte USMF andmeid.


## <a name="set-up-interest-on-the-posting-profile"></a>Viivise seadistamine sisestusreeglis
1. **Navigeerimispaanis** minge **Moodulid > Krediit ja sissenõuded > Seadistus > Kliendi postitusprofiil**.
2. Klõpsake valikut **Redigeeri**.
3. Valige **Seadistus fastTab** moodulis **intressi koodi** väljal ripploendist intressi kood. Kui te ei soovi, et viivist arvutataks kannete puhul selle sisestusreegliga, jätke väli tühjaks. **Tabeli piirangu** fastTab abil saate muuta viisi, kuidas intressi töödeldakse. Kui väli on seatud olekusse Jah, arvutatakse viivist selle sisestusreegli puhul.  

## <a name="calculate-interest"></a>Arvuta intress
1. **Navigeerimispaanis** minge **Moodulid > Krediit ja sissenõuded > Intress > Viivisearve loomine**.
2. Valige kandetüübid, mille puhul viivist arvutatakse. Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.  
3. Kui te seadistate **Intress** kui "Jah" arvutate viivisearve viivise. Võite soovida enne nende kannete kaasamist kontrollida viivisearve viivise arvutamise seadusi.  
4. Sisestage väljale **Alates** kuupäev, millest alates intressi arvutatakse. Kui te ei täpsusta kuupäeva **Alates**, tühistatakse kõik sisestamata viivisearved ja viivis arvutatakse kande alguskuupäevast alates ümber.
5. Sisestage väljale **Kuupäevani** kuupäev, milleni intressi arvutatakse.
6. Tehke väljal **Kasuta postitusprofiili** valik. Sisestusreegli jaoks kolm võimalust:
    - Konto – kasutab iga viivisearve kohta kliendi kontole määratud sisestusreeglit. 
    - Vali – kasutage sisestusreeglit, mille valite väljal Sisestusreegel.
    - Kanne – kasutage eraldi sisestusprofiile kannetest, milles arvutatakse viivis iga viivisearve jaoks. Kanded, millele ei ole sisestusprofiili määratud, kasutavad sisestusprofiili, mis on määratletud vormi Müügireskontro parameetrid alal Pearaamat ja käibemaks.  
7. Jaotise kaasamiseks laiendage fastTab valikut **Kirjed kaasamiseks**.
8. Klõpsake käsku **Filtreeri**.
9. Sisestage kliendi ID väljale **Kriteeriumid**. Sisestage näiteks US-001.
6. Klõpsake valikut **OK**.
7. Klõpsake valikut **OK**.

## <a name="print-interest-notes"></a>Viivisearvete printimine
1. **Navigeerimispaanis** minge **Moodulid > Krediit ja sissenõuded > Intress > Viivisearve ülevaade ja töötlemine**.
2. Valige väljal **Olek** suvand "Loodud".
3. Valige väljal **Prinditud** suvand "Printimata".
4. Klõpsake **Prindi**.
5. Jaotise kaasamiseks laiendage fastTab valikut **Kirjed kaasamiseks**.
6. Klõpsake valikut **OK**.
7. Sulgege leht.

## <a name="post-the-interest-note"></a>Viivisearve sisestamine
1. Valige viivisearve, mis on sisestamiseks valmis (olek on loodud).
2. Klõpsake käsku **Sisesta**.
3. Sisestage viivisearve sisestamise kuupäev. Iga viivisearve kohta pearaamatukande loomiseks valige suvand Jah. Valiku Jah mittemärkimisel summeeritakse kliendi kõigi viivisearvete viivised ja sisestatakse pearaamatusse ühe kandega.  
4. Jaotise kaasamiseks laiendage fastTab valikut **Kirjed kaasamiseks**.
5. Klõpsake valikut **OK**.
6. Valige väljal **Olek** suvand "Sisestatud".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]