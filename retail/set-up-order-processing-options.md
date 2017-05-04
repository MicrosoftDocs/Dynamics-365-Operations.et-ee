---
title: "Tellimuse töötlemise suvandite seadistamine"
description: "See teema annab teavet, kuidas töödelda tellimusi kõnekeskustesse, kasutades rakendust Microsoft Dynamics 365 for Operations – jaemüük."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eb62073fdfa50576d2c613594f3d85cbc0b322f6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-order-processing-options"></a>Tellimuse töötlemise suvandite seadistamine

[!include[banner](includes/banner.md)]


See teema annab teavet, kuidas töödelda tellimusi kõnekeskustesse, kasutades rakendust Microsoft Dynamics 365 for Operations – jaemüük. 

Jaemüük ja kaubandus rakenduses Dynamics 365 for Operations toetab mitut jaemüügikanalit, nagu võrgupoed, traditsioonilised kauplused ja kõnekeskused. Kõnekeskustes võtavad töötajad klientide tellimused vastu telefoni teel ja loovad müügitellimused. Selles teemas kirjeldatakse kõnekeskuse loomist ja kõnekeskuse suvandite konfigureerimist. Igal kõnekeskusel võivad olla oma kasutajad, makseviisid, hinnagrupid, finantsdimensioonid ja tarneviisid. Saate neid suvandeid konfigureerida kõnekeskuse loomisel. **Oluline.** Enne kui praguse Dynamics AX-i kasutaja müügitellimuste loomisel saab kasutada kõnekeskuse töövooge, peab kasutaja olema registreeritud kõnekeskusesse kõnkeskuse kasutajana. Saate kasutada lehte **Kõnekeskus**, et lubada või keelata funktsioonide grupid, mis on kõneskuste puhul kordumatud. Lubada saab järgmisi funktsioonigruppe.

-   **Tellimuse lõpuleviimine** – see grupp hõlmab funktsioone, mis on seotud maksete ja tellimuse lõpulevimisega lehel **Müügitellimus**.
-   **Suunatud müük** – see grupp hõlmab funktsioone, mis on seotud lähtekoodide, skriptide ja kataloogitaotlustega.

Kõnekeskuse sätetes nende funktsioonide lubamisel on need kõnekeskusega seostatud kasutajatele saadaval lehel **Müügitellimus**. Enamik neist funktsioonidest nõuab enne kasutamist lisaseadistamist. Pildid ja skriptid on lubatud kindla kõnekeskuse suunatud müügi sätte osana. Kui need funktsioonid on lubatud, kuvatakse skriptid ja tootepildid lehe **Müügitellimus** paanil Kiirinfo. Kuvatakse tootele määratud vaikepilt. Skripte saab konfigureerida kaubale, kataloogile, kliendile või kaubale kataloogi kontekstis. Kõnekeskuse tellimused võivad kuvada täiendavaid üksikasju kindla tellimuse rea hinna tuletamise kohta. Näiteks näitavad tellimused, milliseid allahindlusi rakendati. Lubate selle funktsiooni valikus **Müügireskontro** &gt; **Seadistus** &gt; **Müügireskontro parameetrid** &gt; **Hinnad** &gt; **Hinna üksikasjad**. Pääsete lehele **Hinna üksikasjad** ripploendist **Müügitellimuse rida**. Tellimuse sündmuste jälgimist saab kasutada auditeerimise eesmärgil, et vaadata üle toimingud, mida tellimusega seoses tellimuse elutsükli vältel tehakse või jälgida kindla kasutaja tegevusi. Näiteks saate salvestada tegevuse iga kord, kui kasutaja loob müügitellimuse, paneb tellimuse ootele, alistab tasu või uuendab tellimuserida. Saate seadistada tellimuse sündmused kindlate kasutajate, kasutajagruppide või kõigi kasutajate tegevuste jälgimiseks kindla ajavahemiku jooksul. Saate vaadata dokumendiga tehtud tegevusi, avades selle dokumendi lehe tegevuspaanil lehe **Tellimussündmused**. Saate konfigureerida tellimuse sündmusi valikus **Müük ja turundus** &gt; **Seadistus** &gt; **Sündmused** &gt; **Tellimussündmused**. Kui kliendi tellimust ei saa õigel ajal lähetada, saab ettevõte saata kliendile automaatselt meiliteatise, et selgitada tellimuse olekut ja anda kliendile võimaluse tellimus tühistada. Kui viivitus ületab teatud läve, saab tellimuse automaatselt tühistada. Määratud ajaintervalliga saab saata kuni kolm meilisõnumit.

1.  **Esimene tühistusteade** – klient saab tellimuse tühistada.
2.  **Teine tühistusteade** – klient saab tellimuse tühistada.
3.  **Viimane tühistusteade** – süsteem tühistab tellimuse ja klienti teavitatakse tühistamisest.

Saate üksikud kliendid ja tooted automaatsest teavitus- ja tühistusprotsessist vabastada. Marginaaliteatis käivitatakse tellimusse kauba lisamisel. Teatis sisaldab olulist teavet kauba kohta, nagu hinnamarginaali ja kauba tulusust. Seda teavet saate kasutada otsustamiseks, kas hinna alistamine on kauba müügitellimusele lisamisel sobiv. Näiteks saate seadistada kaubandusmarginaalide läved määramiseks, et kauba puhul on vastuvõetav lävi vähemalt 40% üle kulu, kuid lävi 20–39% üle kulu on kahtlane. Sel juhuk käivitab hoiatuse iga kaup, mille lävi on vahemikus 20 ja 39 protsenti. Kaupu, mille lävi on väiksem kui 20 protsenti üle kulu, ei saa müüa, ja kauba hinda ei saa korrigeerida. Saate konfigureerida marginaali teatised, valides suvandid **Müügireskontro** &gt; **Seadistus** &gt; **Müügireskontro parameetrid** &gt; **Marginaali teatised**. Käibemaksu määramise seadistamisel vaikereeglite põhjal saate määratleda aadressielementide vastavusseviimise prioriteedi. Näiteks saate määrata, et vastav käibemaksugrupp sihtnumbri järgi on kõrgema prioriteetsusega kui vastav käibemaksugrupp riigi järgi. Kui sisestate uue kliendi aadressi andmed, määratakse käibemaksugrupp automaatselt selle põhjal, kuidas kliendi aadress vastab teie määratletud vaikereeglitele ja prioriteedile. Saate selle funktsiooni konfigureerida lehel **Pearaamatu parameetrid**.




