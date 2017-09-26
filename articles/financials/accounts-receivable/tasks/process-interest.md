--- 
title: "Intressi töötlemine"
description: See protseduur kirjeldab viivisearvete loomist, printimist ja sisestamist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8a53c4deb146d336fdd8ca88a081e6a5af71465a
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="process-interest"></a>Intressi töötlemine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur kirjeldab viivisearvete loomist, printimist ja sisestamist. See ülesanne kasutab demoettevõtte USMF andmeid.


## <a name="set-up-interest-on-the-posting-profile"></a>Viivise seadistamine sisestusreeglis
1. Avage Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid.
2. Klõpsake nuppu Redigeeri.
    * Valige ripploendist viivise kood. Kui te ei soovi, et viivist arvutataks kannete puhul selle sisestusreegliga, jätke väli tühjaks.  
    * Piirangu vahekaardil Tabel saate muuta seda, kuidas viivist töödeldakse. Kui väli on seatud olekusse Jah, arvutatakse viivist selle sisestusreegli puhul.  

## <a name="calculate-interest"></a>Arvuta intress
1. Avage Krediit ja sissenõuded > Intress > Viivisearvete loomine.
    * Valige kandetüübid, mille puhul viivist arvutatakse. Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.  
    * Viivise valimisel arvutate viivisearve viivise. Võite soovida enne nende kannete kaasamist kontrollida viivisearve viivise arvutamise seadusi.  
    * Viivist arvutatakse alates sellest kuupäevast kuni sihtkuupäevani. Kui te alguskuupäeva ei täpsusta, tühistatakse kõik sisestamata viivisearved ja viivis arvutatakse kande alguskuupäevast alates ümber.  
2. Sisestage viivisearve kuupäev.
    * Saadaval on kolm sisestusreeglit: Konto – kasutage iga viivisearve puhul kliendi kontole määratud sisestusreeglit.   Vali – kasutage sisestusreeglit, mille valite väljal Sisestusreegel.   Kanne – kasutage eraldi sisestusprofiile kannetest, milles arvutatakse viivis iga viivisearve jaoks. Kanded, millele ei ole sisestusprofiili määratud, kasutavad sisestusprofiili, mis on määratletud vormi Müügireskontro parameetrid alal Pearaamat ja käibemaks.  
    * Valige sisestusreegel siin, kui määrasite suvandi Kasuta sisestusreegleid olekusse Vali.  
3. Laiendage või ahendage jaotist Kaasatavad kirjed.
4. Klõpsake käsku Filtreeri.
5. Sisestage kliendi ID väljale Kriteeriumid. Näiteks sisestage US-001.
6. Klõpsake nuppu OK.
7. Klõpsake nuppu OK.

## <a name="print-interest-notes"></a>Viivisearvete printimine
1. Avage Krediit ja sissenõuded > Intress > Viivisearvete ülevaade ja töötlus.
2. Valige väljal Olek suvand Loodud.
3. Valige väljal Prinditud suvand Printimata.
4. Klõpsake Prindi.
5. Laiendage või ahendage jaotist Kaasatavad kirjed.
6. Klõpsake nuppu OK.
7. Sulgege leht.

## <a name="post-the-interest-note"></a>Viivisearve sisestamine
1. Valige viivisearve, mis on sisestamiseks valmis (olek on loodud).
2. Klõpsake valikut Sisesta.
3. Sisestage viivisearve sisestamise kuupäev.
    * Iga viivisearve kohta pearaamatukande loomiseks valige suvand Jah.     Valiku Jah mittemärkimisel summeeritakse kliendi kõigi viivisearvete viivised ja sisestatakse pearaamatusse ühe kandega.  
4. Laiendage või ahendage jaotist Kaasatavad kirjed.
5. Klõpsake nuppu OK.
6. Valige väljal Olek suvand Sisestatud.


