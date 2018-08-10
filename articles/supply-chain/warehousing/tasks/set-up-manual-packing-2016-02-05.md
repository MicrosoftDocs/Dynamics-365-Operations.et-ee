--- 
title: "Käsitsi pakkimise seadistamine (ainult veebruar ja mai 2016)"
description: "Pakkimisprotsess võimaldab toodete kinnitamist ja pakendamist konteineritesse."
author: ShylaThompson
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7f992a6a1655cd868d79228c490d59b46bfae715
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a>Käsitsi pakkimise seadistamine (ainult veebruar ja mai 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Pakkimisprotsess võimaldab toodete kinnitamist ja pakendamist konteineritesse. Selle protsessi käigus valivad laotöötajad tooteid ladustamiskohtadest ja teisaldavad need pakendamisjaama, kus kontrollitakse kauba kogust ja tüüpe ning määratakse neile sobivad konteinerid. Kui konteiner on täis, saab selle sulgeda ja teisaldada see lähetusalale ning tooted on saatmiseks valmis. See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="set-up-location-profiles"></a>Asukohaprofiilide häälestamine
1. Avage Laohaldus > Seadistus > Ladu > Asukohaprofiilid.
2. Klõpsake valikut Uus.
    * Asukoha profiili kasutatakse pakkimisjaamade jaoks ja see sisaldab teavet ning reegleid asukoha kohta.  
3. Sisestage väärtus väljale Asukohaprofiili ID.
4. Sisestage väärtus väljale Nimi.
5. Sisestage või valige väärtus väljal Asukoha vorming.
6. Sisestage või valige väärtus väljal Asukoha tüüp.
7. Tehke väljal Luba segakaubad valik Jah.
8. Tehke väljal Luba lao segaolekud valik Jah.
9. Tehke väljal Alista partiipäevade reeglid valik Jah.
10. Sulgege leht.

## <a name="set-up-warehouse-management-parameters"></a>Laohalduse parameetrite seadistamine 
1. Avage Laohaldus > Seadistus > Laohalduse parameetrid.
2. Klõpsake vahekaarti Pakkimine.
3. Sisestage või valige väärtus väljal Pakkimise asukoha profiili ID.
    * Valige asukoha profiil, mida soovite pakkimisel kasutada.  
4. Sulgege leht.

## <a name="set-up-container-types"></a>Konteineri tüüpide seadistamine
1. Avage Laohaldus > Seadistus > Konteinerid > Konteinerite tüübid.
2. Klõpsake valikut Uus.
    * Saate määratleda kasutatavate konteinerite tüübi. Saate määrata konteineri füüsilised mõõdud, sh taara kaalu ja maksimaalse kaalu, maksimaalse mahu, pikkuse, laiuse ning kaalu.  Atribuudid on kohandatud väljad, mis võimaldavad teil lisada konteineri tüübile täiendavad dimensioone.     
3. Tippige väärtus väljale Konteineri tüübi kood.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sisestage number väljale Taarakaal.
6. Sisestage number väljale Maksimaalne kaal.
7. Sisestage number väljale Maht.
8. Sisestage number väljale Pikkus.
9. Sisestage number väljale Laius.
10. Sisestage number väljale Kõrgus.
11. Klõpsake nuppu Salvesta.
12. Sulgege leht.

## <a name="set-up-packing-profiles"></a>Pakkimisprofiilide seadistamine
1. Avage Laohaldus > Seadistus > Pakkimine > Pakkimisprofiilid.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Pakkimisprofiili ID.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sisestage või valige väärtus väljal Konteineri sulgemise profiili ID.
    * Konteineri sulgemise profiili ID on valikuline ja see on selle pakkimisprofiili konteineri sulgemise vaikeprofiil.  
6. Valige suvand väljal Konteineri ID režiim.
    * See suvand määrab, kas konteineri ID luuakse automaatselt konteineri loomisel või kas konteineri ID luuakse käsitsi.  
7. Sisestage või valige väärtus väljal Konteineri tüüp.
    * Konteineri tüüpi kasutatakse vaikimisi uue konteineri loomisel.  
8. Märkige ruut Loo konteineri sulgemisel konteiner automaatselt.
9. Klõpsake nuppu Salvesta.
10. Sulgege leht.

## <a name="set-up-container-closing-profiles"></a>Konteineri sulgemise profiilide seadistamine
1. Avage Laohaldus > Seadistus > Konteinerid > Konteineri sulgemise profiilid.
    * Konteineri sulgemise profiilid määratlevad, mis juhtub, kui konteiner on suletud. Saate seadistada mitu konteineri sulgemise profiili.       
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Konteineri sulgemise profiili ID.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige suvand väljal Manifest.
    * Määrake, kas avaldamine ilmneb konteinerite sulgemisel või saadetise kinnitamisel. Arvestage sellega, et avaldamine nõuab transpordihaldust. Avaldamine tuleb teha transpordimootorites, et see töötaks.  
6. Sisestage või valige väärtus väljal Ladu.
7. Sisestage või valige väärtus väljal Lõppsaadetise vaikeasukoht.
    * See on asukoht, kuhu tooted pärast konteinerite sulgemist teisaldatakse. Sellel asukohal peab olema määratud lao parameetrites asukoha profiil.  
8. Sisestage või valige väärtus väljal Kaaluühik.
9. Klõpsake nuppu Salvesta.


