---
title: Märgukirjaseeria loomine
description: Kasutage seda protseduuri kogumistähtede jada loomiseks.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734154"
---
# <a name="create-a-collection-letter-sequence"></a>Märgukirjaseeria loomine

[!include [banner](../../includes/banner.md)]

Kasutage seda protseduuri kogumistähtede jada loomiseks. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Minge moodulisse **Kreedit ja > > saate seadistada märgukirjaseeria**.
2. Klõpsake valikut **Uus**.
3. Sisestage seeriat tähistav seeria ID väljale **Märgukirja seeria**. Seda kasutatakse sisestusreeglite seadistamiseks.
4. Sisestage väärtus väljale **Kirjeldus**. Maksetingimused on valikulised. Kui sisestate väärtuse siia, kasutab märgukirja tasu arve neid maksetingimusi kliendi puhul salvestatud maksetingimuste asemel.  
5. **Valige märgukirja koodi** väljalt esimese märgukirja kood, mille soovite saata. Esimene märgukiri luuakse arve maksetähtaja, selle rea väljale Päevad ajapikendusperioodi puhul sisestatud väärtuse ja muu sellele reale sisestatud teabe järgi.  
6. Sisestage väärtus väljale **Kirjeldus**. 
7. Tasu vaikevaluuta on juriidilise isiku valuuta. Valuutakood võib arve valuutast erineda.   
8. Seerias järgmisena saadetava märgukirja lisamiseks klõpsake nuppu **Lisa**. Paljudel juhtudel on esimene märgukiri ainult hoiatus. Vajaduse korral saate lisada tasud.  
9. Väljal **Märgukirja kood** valige seerias järgmisena saadetav märgukiri.
10. Väljal **Põhikonto** valige tulukonto, mida kasutatakse tasude jaoks.
11. Sisestage tasu, mis tuleb maksta selle märgukirja sisestamisel.
12. Klõpsake väljal **Kauba käibemaksu rühm** ripploendi nuppu otsingu avamiseks. Kui tasu puhul tuleb arvutada käibemaksu, valige kauba käibemaksugrupp.  
13. Klõpsake loendis valitud real olevat linki.
14. Väljale **Minimaalne tähtaja ületamise saldo** sisestage enne märgukirja saatmist nõutav minimaalne tähtaja ületamise saldo.
15. Väljale **Päevad** sisestage ajapikenduspäevade arv, mida lubate. See on päevade arv pärast maksetähtaega, mil saab luua märgukirja. Arvutamisel kasutatav maksetähtaeg oleneb märgukirja asukohast märgukirjaseerias järgmiselt: ⦁
    - Ajapikenduse periood 1. märgukirja puhul on seotud arve tähtajaga.
    - 2. ja edasiste märgukirjade ajapikenduse periood on seotud eelmise märgukirja sisestamise või printimise kuupäevaga, olenevalt välja Värskenda märgukirja koodi valikust lehel Müügireskontro parameetrid.  
16. Seerias viimase märgukirja lisamiseks klõpsake nuppu **Lisa**. Saate märgukirjaseeria puhul lisada kuni viis märgukirjakoodi.  
17. Väljal **Märgukirja kood** valige seerias järgmisena saadetav märgukiri.
18. Sisestage väärtus väljale **Kirjeldus**.
19. Määratlega väljal **Põhikonto** soovitud väärtused.
20. Sisestage number väljale **Tasu valuutas**.
21. Klõpsake väljal **Kauba käibemaksu rühm** ripploendi nuppu otsingu avamiseks.
22. Klõpsake loendis valitud real olevat linki.
23. Sisestage number väljale **Minimaalne tähtaja ületanud saldo**.
24. Sisestage number väljale **Päevad**.
25. Valige märkeruut **Blokeering**, et peatada kliendil edasiste saadetiste ja arvete saatmine. Konto blokeerimise tühistamiseks valige klientide **lehel** **Arvete koostamine ja tarne ootel** **väli** Ei.  
26. Laiendage kiirkaarti **Märkus**.
27. Sisestage valitud märgukirjakoodi puhul märgukirjas kuvatav tekst. Selle teksti saate märkuseboksi kohal asuvat tõlkemenüüd **kasutades tõlkida** mitmesse keelde.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
