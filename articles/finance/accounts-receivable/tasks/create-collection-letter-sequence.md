---
title: Märgukirjaseeria loomine
description: Kasutage seda ülesande juhendit märgukirjaseeria loomiseks.
author: mikefalkner
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8cf5612fcd237ebaaede3f8f70da5eb443a94c34
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842414"
---
# <a name="create-a-collection-letter-sequence"></a>Märgukirjaseeria loomine

[!include [banner](../../includes/banner.md)]

Kasutage seda ülesande juhendit märgukirjaseeria loomiseks. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage navigeerimispaanil **Moodulid > Kreedit ja sissenõuded > Häälestus > Sätesta märgukirja seeria**.
2. Klõpsake valikut **Uus**.
3. Sisestage seeriat tähistav seeria ID väljale **Märgukirja seeria**. Seda kasutatakse sisestusreeglite seadistamiseks.
4. Sisestage väärtus väljale **Kirjeldus**.  Maksetingimused on valikulised. Kui sisestate väärtuse siia, kasutab märgukirja tasu arve neid maksetingimusi kliendi puhul salvestatud maksetingimuste asemel.  
5. **Valige märgukirja koodi** väljalt esimese märgukirja kood, mille soovite saata. Esimene märgukiri luuakse arve maksetähtaja, selle rea väljale Päevad ajapikendusperioodi puhul sisestatud väärtuse ja muu sellele reale sisestatud teabe järgi.  
6. Sisestage väärtus väljale **Kirjeldus**. Tasu valuuta on vaikimisi kliendi valuutas. Valuutakood võib arve valuutast erineda.  
7. Seerias järgmisena saadetava märgukirja lisamiseks klõpsake nuppu **Lisa**. Paljudel juhtudel on esimene märgukiri ainult hoiatus. Vajaduse korral saate lisada tasud.  
8. Valige märgukirja koodi väljalt seerias järgmisena saadetav märgukiri.
9. Sisestage väärtus väljale **Kirjeldus**.
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
25. Valige märkeruut **Blokeering**, et peatada kliendil edasiste saadetiste ja arvete saatmine. Kontolt blokeeringu eemaldamiseks tehke lehe Kliendid väljal Arveldamine ja tarne ootel valik **Ei**.  
26. Laiendage kiirkaarti **Märkus**.
27. Sisestage valitud märgukirjakoodi puhul märgukirjas kuvatav tekst. Saate selle teksti tõlkida mitmesse keelde, kasutades märkuse kasti kohal olevat menüüd Tõlked.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]