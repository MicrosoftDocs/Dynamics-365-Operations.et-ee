--- 
title: "Pakkumiskutse pakkumiste sisestamine ja võrdlemine ning lepingute määramine"
description: "See protseduur näitab, kuidas sisestada pakkumiskutsele vastuseid, pakkumisi hinnata ja võrrelda ning seejärel määrata pakkumine ühele hankijatest."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d7c76eab2cca4e15c13dd9f79432b9c6d81071a2
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Pakkumiskutse pakkumiste sisestamine ja võrdlemine ning lepingute määramine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas sisestada pakkumiskutsele vastuseid, pakkumisi hinnata ja võrrelda ning seejärel määrata pakkumine ühele hankijatest. Saate seda protseduuri kasutada demoandmete ettevõttes USMF. Enne alustamist peab teil olema pakkumiskutse kahe reaga, mis on saadetud vähemalt kahele hankijale. Selle loomiseks saate käitada eeltingimusena protseduuri Pakkumiskutse loomine. Teil on vaja seadistada hindamiskriteeriumid, enne kui saate seda protseduuri käitada.


## <a name="enter-a-reply-from-a-vendor"></a>Hankija vastuse sisestamine
1. Avage Hanked > Pakkumiskutsed > Kõik pakkumiskutsed.
2. Valige pakkumiskutse, mille olek on Saadetud, ja klõpsake linki pakkumiskutse juhtumi numbril.
    * Pakkumiskutse peaks olema saadetud vähemalt 2 hankijale.  
3. Klõpsake päist, et avada hankijate loend.
4. Valige hankija, kellele soovite pakkumiskutses vastust sisestada.
5. Klõpsake nuppu Sisesta vastus.
6. Klõpsake toimingupaanil käsku Vasta.
7. Klõpsake käsku Kopeeri andmed vastuseväljadele.
    * Selle toiminguga kopeeritakse valitud andmed, näiteks kogus pakkumiskutse juhtumist pakkumiskutse vastusesse. Teise võimalusena saate selle toimingu vahele jätta ja täita kõik väljad käsitsi vastust redigeerides.  
8. Klõpsake nuppu Redigeeri.
9. Sisestage arv väljale Ühiku hind.
10. Valige muu pakkumise rida.
11. Sisestage arv väljale Ühiku hind.

## <a name="score-the-bid"></a>Pakkumise hindamine
1. Klõpsake päist, et avada pakkumise hindamine.
2. Laiendage jaotist Pakkumise hindamine.
3. Sisestage väljale Punktisumma number ühe hindamiskriteeriumi kohta.
    * Kui liigute hiirega üle mõne hindamiskriteeriumi, näitab kohtspikker vahemiku, millesse punktisumma peab jääma. Selles demos saate lisada mis tahes kriteeriumidele arvu vahemikus 1 ja 5.  
4. Valige teine hindamiskriteerium.
5. Sisestage väljale Punktisumma number.
6. Laiendage jaotist Küsimustikud.
    * Kui pakkumiskutse juhtumil on küsimustik, mis saadeti hankijatele, saate sisestada nende vastused küsimustiku ossa.  
7. Sulgege leht.

## <a name="enter-a-reply-for-another-vendor"></a>Teisele hankijale vastuse sisestamine
1. Valige järgmine hankija, kustutades hankija, kellele äsja vastuse sisestasite, ja valides seejärel rea järgmisele hankijale.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake nuppu Sisesta vastus.
4. Klõpsake käsku Kopeeri andmed vastuseväljadele.
5. Klõpsake nuppu Redigeeri.
6. Sisestage arv väljale Ühiku hind.
7. Valige muu pakkumise rida.
8. Sisestage arv väljale Ühiku hind.

## <a name="score-the-second-bid"></a>Teise pakkumise hindamine
1. Klõpsake päist, et avada pakkumise hindamine.
2. Sisestage väljale Punktisumma number.
3. Otsige loendist ja valige soovitud kirje.
4. Sisestage väljale Punktisumma number.

## <a name="compare-the-replies"></a>Vastuste võrdlemine
1. Klõpsake toimingupaanil valikut Üldine.
2. Klõpsake käsku Võrdle vastuseid.
3. Sisestage väljale Tase number.
    * See leht näitab pakkumisi päise ja ridadega ning punktide kogusummat päise tasemel. Saate ridu võrrelda, sortides ruudustikus nii, et võrreldavad read on üksteise kõrval. Teave hõlmab ka väärtust Kogus: hankija pakutud kogus. See ei pruugi võrduda pakkumiskutses määratud kogusega.   Netosumma: hankija määratud hind real olevatele kaupadele pärast mis tahes allahindluste lahutamist.   Hälve: Deviation – päevade arv, mille võrra pakkumise päise või rea tarnekuupäev pakkumiskutses päises või real taotletud tarnekuupäevast hälbib.   Saate sisestada taseme iga pakkumise puhul.  
4. Valige päise rida teisele pakkumisele, mida soovite järjestada.
5. Sisestage väljale Tase number.
6. Klõpsake nuppu Salvesta.

## <a name="reject-a-bid"></a>Pakkumise tagasilükkamine
1. Valige päise rida pakkumisele, mille soovite tagasi lükata.
    * Ühe pakkumise puhul saate korraga aktsepteerida, tagasi lükata või tagastada ühe pakkumise või rea.  
2. Märkige ruut Märgi.
    * Kui valite pakkumise päises märkeruudu Märgi, märgitakse ka kõik read. Samuti saate märkida pakkumise puhul ridade alamkogumi selle tagasilükkamiseks või aktsepteerimiseks. On võimalik aktsepteerida ühe hankija pakkumise pakkumiskutse mõne rea puhul ja siis määrata muud pakkumiskutse read erinevale hankijale, kuid teil tuleb seda teha kahes etapis, korraga ühes pakkumises. Kui on olemas alternatiivsed read, saate aktsepteerida ainult esialgse pakkumise rea või selle alternatiivi, kuid mitte mõlemaid.  
3. Klõpsake käsku Lükka tagasi.
4. Klõpsake suvandit Parameetrid rippdialoogi avamiseks.
5. Väljal Tagasilükkamise põhjus sisestage või valige väärtus.
    * Tagasilükkamise põhjus salvestatakse vastuses.  
6. Klõpsake nuppu OK.
7. Klõpsake nuppu OK.
8. Sulgege leht.
9. Sulgege leht.
10. Värskendage lehte.

## <a name="accept-a-bid"></a>Pakkumise aktsepteerimine
1. Valige pakkumine, mille soovite aktsepteerida, ja seejärel klõpsake linki väljal Pakkumiskutse.
2. Klõpsake toimingupaanil käsku Vasta.
3. Klõpsake suvandit Nõustu.
    * Kui olete märkinud teatud read ja mitte teisi, hõlmab aktsepteerimistoiming ainult märgitud ridu. Kui soovite aktsepteerida kõiki pakkumise ridu, siis ei pea te ridu märkima.  
4. Klõpsake suvandit Parameetrid rippdialoogi avamiseks.
    * See võimaldab teil salvestada pakkumise aktsepteerimise põhjuse. Põhjus salvestatakse pakkumisse.  
5. Väljal Aktsepteerimise põhjus sisestage või valige väärtus.
6. Klõpsake nuppu OK.
7. Klõpsake nuppu OK.
    * Kui klõpsate nuppu OK, luuakse ostutellimus pakkumiskutse kinnitusse lisatud ridade alusel. Kui on teisi pakkumisi, mida ei ole töödeldud (aktsepteeritud, tagasi lükatud või tagastatud), siis palub süsteem teil ülejäänud pakkumised tagasi lükata.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Loodud ostutellimuse vaatamine
1. Klõpsake toimingupaanil valikut Üldine.
2. Klõpsake valikut Ostutellimus.
    * Siin saate vaadata ostutellimust, mis loodi pakkumise aktsepteerimisel.  
3. Sulgege leht.
4. Sulgege leht.
5. Sulgege leht.
6. Sulgege leht.


