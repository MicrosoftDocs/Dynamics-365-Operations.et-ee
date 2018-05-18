--- 
title: "Ostureskontro arvete võrdlemise seadistamine"
description: "Salvestamisel kasutatakse demoettevõtte USMF-i."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9bf83269c34133509734691fd018ee703c40626
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Ostureskontro arvete võrdlemise seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Salvestamisel kasutatakse demoettevõtte USMF-i. Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli. Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine. Kui teie juriidiline isik jälgib tasude abil kulusid (nt veokulu), siis veenduge, et on valitud konfiguratsioonivõti Tasud.  Ostureskontro arvete võrdlemine on hankija arve, ostutellimuse ja toote sissetuleku teabe vastavusse viimise protsess. Nende dokumentide vahelisi erinevusi nimetatakse vastendamise lahknevusteks. Vastavusseviimise lahknevusi võrreldakse määratud hälvetega. Kui vastendamise lahknevus ületab lubatud kõikumisprotsendi või summa, kuvatakse vastendamise hälbe ikoonid vormil Hankija arve ja vormil Arvete võrdlemise üksikasjad.

1. Avage Ostureskontro > Seadistus > Ostureskontro parameetrid.
2. Klõpsake vahekaarti Arve kinnitamine.
3. Märkige või tühjendage ruut Luba arvete võrdlemise kontrollimine.
    * Valige, kas enne arvete võrdlemisel erinevusi sisaldava arve sisestamist on nõutav kinnitus. Kui see on seatud valikule Luba hoiatusega, kuvatakse visuaalne näit, kui arvete võrdlemise erinevus ületab lubatud hälbe. Saate arve siiski sisestada. Töövoogude kasutamiseks koos arvete võrdlemise kinnitamisega veenduge, et väli Lahknevustega arvete sisestamine on määratud suvandile Luba hoiatusega, et vältida korduvat kinnitamist.  
    * Valige väljalt Arve päise vastendamise oleku automaatne värskendamine, kas süsteem võrdleb arve andmete sisestamisel automaatselt. Soovitatav säte on Jah, v.a juhul, kui teil on tekkinud andmete sisestamise jõudluse probleeme. Automaatsete värskenduste keelamine võib lubada süsteemi jõudluse kiirenemist, kuna arvete võrdlemise kontrollimine jäetakse andmesisestusel vahele. Andmete sisestamise ametnik peab arvete võrdlemise olekut käsitsi värskendama, et näha arvete võrdlemise kinnitamise tulemusi, kui see on seatud väärtusele Ei.  
4. Lülitage jaotise Arvesummade võrdlemine laiendamist.
5. Märkige või tühjendage ruut Võrdle arvesummasid, et võrrelda tegelikke arvesummasid eeldatavate kogusummadega.
    * Valige, kas kuvada ikoon, kui erinevus ületab arvete võrdlemisel lubatud hälbe. Saate valida ikooni kuvamise, kui positiivne erinevus ületab lubatud hälbe, või kui positiivne või negatiivne erinevus ületab lubatud hälbe.  
    * Näide: hälve on 5 protsenti ja ostutellimuse arve kogusumma on 100.00. Seetõttu kuvatakse hinna vastavuse ikoon, kui arve kogusumma ületab 105.00. Kui teete valiku Kui kõikumisest suuremad või väiksemad, kuvatakse samuti ikoon, kui arve summa on väiksem kui 95,00.  
6. Sisestage number väljale Arvesummade lubatud kõikumisprotsent.
7. Lülitage jaotise Hinna ja koguse võrdlemine laiendamist.
    * Valige väljalt Rea vastavusse viimise poliitika väärtus, mida kasutada vaikepoliitikana juriidilise isiku puhul, kellega töötate. Pole nõutav tähendab, et üksiku arverea hindade kontrollimine ostutellimuse hinnaga või arve koguste kontrollimine saatelehe kogustega pole nõutav. Kahesuunaline vastavusse viimine tähendab, et arveridade kontrollimine on nõutav, kuid kontrollimine hõlmab ainult ostutellimust ja tarnija arve dokumente. Toote sissetulekut vastavusse viimise kontrollimisel ei arvestata. Kolmesuunaline vastavusse viimine tähendab, et arve ühiku netohinda võrreldakse ostutellimuse ühiku netohinnaga ja ühtivat toote sissetuleku kogust võrreldakse arve kogusega.  
    * Kui kasutate rea vastavusse viimise poliitika kahesuunalist vastavusse viimist või kolmesuunalist vastavusse viimist, saate seadistada hinnakõikumisprotsendid juriidilise isiku, kaupade ja hankijate puhul lehel Kauba hinna kõikumine. Kui hankijaarveid ostutellimuste teabega võrreldakse, otsitakse sobivat hinnakõikumisprotsenti.  
8. Valige suvand väljalt Rea vastavusse viimise poliitika.
    * Teistsuguse vastendamise taseme rakendamise lubamiseks kauba, hankija, hankija ja kauba kombinatsiooni või ostutellimuse rea puhul valige väärtus väljalt Luba vastavusse viimise poliitika alistamine. Juriidilise isiku rea vastavusse viimise poliitika saab alistada kindla hankija, kauba või hankija ja kauba kombinatsiooni puhul lehel Vastavusse viimise poliitika.  
    * Rea kaupade hinna kogusummade vastendamiseks arvetel valige väärtus väljalt Hinna kogusumma vastendamine. Seda tüüpi vastendamine on kasulik, kui hankija saadab sama ostutellimuse rea puhul mitu arvet. Saate võrrelda iga arve rea ja kõikide ootel ja varem sisestatud arve ridade netosumma hinnateavet asjakohase ostutellimuse rea netosummaga.  
9. Valige suvand väljalt Vastenda hinna kogusummad.
10. Sisestage number väljale Ostuhinna kogusumma hälve.
11. Lülitage jaotise Tasude võrdlemine laiendamist.
12. Tegelike tasude võrdlemiseks eeldatavate tasudega, tuginedes ostutellimuse teabele, märkige ruut Võrdle tasusid.
13. Sulgege leht.


