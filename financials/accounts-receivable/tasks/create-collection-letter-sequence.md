--- 
title: "Märgukirjaseeria loomine"
description: "Kasutage seda ülesande juhendit märgukirjaseeria loomiseks."
author: mikefalkner
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
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3b050d47910c146b9691e7aae5b4a1a847ce716e
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-collection-letter-sequence"></a>Märgukirjaseeria loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kasutage seda ülesande juhendit märgukirjaseeria loomiseks. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage Krediit ja sissenõuded > Seadistus > Märgukirjaseeria seadistamine.
2. Klõpsake valikut Uus.
3. Sisestage seeriat tähistav seeria ID väljale Märgukirjaseeria. Seda kasutatakse sisestusreeglite seadistamiseks.
4. Sisestage väljale Kirjeldus soovitud väärtus.
    * Maksetingimused on valikulised. Kui sisestate väärtuse siia, kasutab märgukirja tasu arve neid maksetingimusi kliendi puhul salvestatud maksetingimuste asemel.  
5. Valige märgukirja koodi väljalt esimese märgukirja kood, mille soovite saata.
    * Esimene märgukiri luuakse arve maksetähtaja, selle rea väljale Päevad ajapikendusperioodi puhul sisestatud väärtuse ja muu sellele reale sisestatud teabe järgi.  
6. Sisestage väljale Kirjeldus soovitud väärtus.
    * Tasu valuuta on vaikimisi kliendi valuutas. Valuutakood võib arve valuutast erineda.  
7. Seerias järgmisena saadetava märgukirja lisamiseks klõpsake nuppu Lisa
    * Paljudel juhtudel on esimene märgukiri ainult hoiatus. Vajaduse korral saate lisada tasud.  
8. Valige märgukirja koodi väljalt seerias järgmisena saadetav märgukiri.
9. Sisestage väärtus väljale Kirjeldus.
10. Valige põhikonto väljalt tasude puhul kasutatav tulukonto.
11. Sisestage tasu, mis tuleb maksta selle märgukirja sisestamisel.
12. Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.
    * Kui tasu puhul tuleb arvutada käibemaksu, valige kauba käibemaksugrupp.  
13. Klõpsake loendis valitud real olevat linki.
14. Sisestage minimaalne tähtaja ületanud saldo, mis on nõutav enne märgukirja saatmist.
15. Sisestage teie lubatavate ajapikenduspäevade arv.
    * See on päevade arv pärast maksetähtaega, mil saab luua märgukirja. Arvutuses kasutatav tähtaeg oleneb märgukirja paigutusest märgukirjade järjestuses: ⦁ 1. märgukirja ajapikenduse periood on seotud arve maksetähtajaga.  ⦁ 2. ja edasiste märgukirjade ajapikenduse periood on seotud eelmise märgukirja sisestamise või printimise kuupäevaga, olenevalt välja Värskenda märgukirja koodi valikust lehel Müügireskontro parameetrid.  
16. Seerias viimase märgukirja lisamiseks klõpsake nuppu Lisa.
    * Saate märgukirjaseeria puhul lisada kuni viis märgukirjakoodi.  
17. Valige märgukirja koodi väljalt seerias järgmisena saadetav märgukiri.
18. Sisestage väärtus väljale Kirjeldus.
19. Täpsustage soovitud väärtusi väljal Põhikonto.
20. Sisestage number väljale Tasu valuutas.
21. Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.
22. Klõpsake loendis valitud real olevat linki.
23. Sisestage number väljale Minimaalne tähtaja ületanud saldo.
24. Sisestage number väljale Päevad.
25. Märkige see ruut kliendi jaoks täiendavate tarnete ja arvelduste peatamiseks.
    * Kontolt blokeeringu eemaldamiseks tehke lehe Kliendid väljal Arveldamine ja tarne ootel valik Ei.  
26. Laiendage kiirkaarti Märkus.
27. Sisestage valitud märgukirjakoodi puhul märgukirjas kuvatav tekst.
    * Saate selle teksti tõlkida mitmesse keelde, kasutades märkuse kasti kohal olevat menüüd Tõlked.  


