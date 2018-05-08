--- 
title: Ostutellimuse loomine
description: "Selles protseduuris selgitatakse, kuidas luua ostutellimus käsitsi."
author: FrankDahl
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
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 27ed15e6d9a376c4203e5446d056f221bd3eb730
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order"></a>Ostutellimuse loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris selgitatakse, kuidas luua ostutellimus käsitsi. Koondplaneerimise, otsetarne ja muude protsesside tulemusena luuakse ostutellimused tavaliselt automaatselt. Ostutellimused loob tavaliselt ostuagent. Siin esitatud näidet saab kasutada demoandmete ettevõttes USMF, kasutades väärtusi, mida on soovitatud erinevate etappide märkustes.


## <a name="create-the-purchase-order-header"></a>Ostutellimuse päise loomine
1. Avage Hanked > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Valige hankija konto US-101.
    * Kui valite hankija, kopeeritakse hankijakirje üksikasjad, nagu aadress, arvekonto, tarnetingimused ja -viis vaikeväärtustena tellimuse päisesse. Saate neid väärtusi alati muuta.  
4. Laiendage jaotis Üldine.
    * Väli Tegevuskoht koos väljaga Ladu määrab, kuhu peab tarnitud kaubad või teenused tarnima. Vaikimisi kohaletoimetamise aadress on tegevuskoht. Mõlemad väljad saab täita valitud hankijale seadistatud väärtustega või määrata need käsitsi.  
    * Välja Tarnekuupäev kasutatakse selleks, et määrata, millal sisse ostetud kaubad ja teenused tarnida tuleb. Saate määrata ühe tarnekuupäeva tellimuse kohta või anda üksikutele tellimuse ridadele ainulaadsed tarnekuupäevad. Kui siin määratud tarnekuupäeva ei saa teatud toodete või teenuste puhul kasutada, sest neil on pikemad täitmisajad, siis need read luuakse vastavalt sellele hilisema tarnekuupäevaga.  
5. Ahendage jaotist Üldine.
6. Laiendage jaotist Administreerimine.
    * Välja Tellija abil saab määrata, kes tellimuse esitab. Seda võib olla mugav hankijaga ühiskasutada, kui tal on vaja selle inimesega ühendust võtta. Väljale võidakse määrata väärtus automaatselt, kui praegune kasutajakonto on seostatud nimega lehel Kasutajad.  
7. Ahendage jaotist Administreerimine.
8. Klõpsake nuppu OK.
    * Tellimuse päis on nüüd loodud. Kui töötate ostutellimuse ridadega, kuvatakse ainult päise teabe kokkuvõte. Kui peate vaatama ülejäänud teavet, klõpsake päist.  

## <a name="add-a-purchase-order-line"></a>Ostutellimuse rea lisamine
1. Klõpsake suvandit Ostutellimuse rida.
2. Klõpsake valikut Dimensioonid.
    * Toodetel võivad olla variandid, mis on eristatavad dimensioonidega, nagu värv, suurus või stiil. Tooteid saab seadistada ka nii, et need kasutavad laoala dimensioone, nagu tegevuskoht ja ladu. On olemas ka valikulised jälgimisdimensioonid, nagu partii- ja seerianumber. Tellimuse sisestamise tõhususe parandamiseks saate lisada sagedamini kasutatavad dimensiooniväljad otse tellimuse ruudustikku.  
3. Valige märkeruut Värv.
    * Valikuline: kui valite välja Salvesta seadistus, kuvatakse järgmisel ostutellimuse lehe avamisel tellimuse rea ruudustikus ka valitud dimensioone.  
4. Klõpsake nuppu OK.
5. Tehke väljal Kaubakood valik T0004.
    * Tellimuse read luuakse toodetele ja teenustele, määrates kaubakoodi, või nagu kulud, määrates hankekategooria.  
    * Välja Hankekategooria kasutatakse ridade lisamiseks juhul, kui hangitud kaubad kantakse kuludesse otse, mitte ei saadeta varudesse. See tähendab, et kui peate ostu kuludesse kandma, saate seda teha, luues ostutellimuse rea, mis määrab hankekategooria, mitte ei loo kaubakoodiga rida. Kaupu saab ka hankekategooriaga seostada ja sellisel juhul kuvatakse hankekategooria ainult informatiivse teabena.  
6. Sisestage või valige väärtus väljal Värv.
    * Väljad Tegevuskoht ja Ladu täidetakse tavaliselt tellimuse päisest pärit väärtustega, kuid on võimalik väljad alistada, kui mõned read tuleb tarnida erinevatesse asukohtadesse.  
7. Sisestage arv väljale Kogus.
    * Valige kogus, mida soovite osta. Koguse väli täidetakse automaatselt toote minimaalse tellimise kogusega, kui see on seadistatud, või väärtusega 1.  
    * Väli Ühik näitab tellitud koguse mõõtühikut. Tavaliselt tuleb ühik automaatselt tooteetaloni andmete ostuühikust, kuid saate seda muuta.  
    * Väli Ühiku hind sisaldab tavaliselt väärtust kas ostulepingust või kaubandusleppest. Ühiku hinda on võimalik üksikute tellimuse ridade puhul muuta, näiteks siis, kui hankijaga lepitakse kokku ainulaadne hind.  
    * Allahindluse väli tähistab allahindluse summat ühiku kohta. See allahindlus vähendab seega ühiku hinda allahindluse võrra. See allahindlus tuleb tavaliselt automaatselt ostulepingutest või kaubanduslepetest, kuid seda on võimalik üksikutel ridadel tühistada, kui ainulaadsed allahindlused on hankijaga kokku lepitud.  
    * Saab sisestada allahindluse protsendi, mis vähendab rea netosummat vastavalt. See allahindluse protsent tuleb tihti automaatselt ostulepingutest või kaubanduslepetest, kuid seda on võimalik üksikutel ridadel tühistada, kui ainulaadne allahindluse protsent on hankijaga kokku lepitud.  
    * Välja Netosumma väärtus arvutatakse rea teistest väljadest, sh kogus, ühiku hind, allahindlus ja allahindluse protsent. Netosummat on võimalik muuta, kuid siis jäävad väljad Ühiku hind, Allahindlus ja Allahindluse protsent tühjaks ning kui sisestate rea poole, siis on sisestatud summa neotosummaga proportsionaalne. Tavaliselt kasutatakse välja Netosumma ainult rea netosumma kuvamiseks.  
8. Laiendage jaotis Rea üksikasjad.
9. Klõpsake vahekaarti Tarne.
    * Igale tellimuse reale saab määrata kordumatu tarnekuupäeva. Kuupäev on päritud ostutellimuse päise väljalt, kuid saate seda muuta.  
10. Ahendage jaotist Rea üksikasjad.

## <a name="review-order-totals"></a>Tellimuse kogusummade ülevaatamine
1. Klõpsake valikut Kogusummad.
    * Kui te ei näe toimingut Kogusummad, klõpsake tegevusribal vahekaarti Ostutellimus.  
    * See dialoogiboks kuvab kogu tellimuse kogusummad.  
    * Väli Valik võimaldab muuta kogusummade arvutamise alust. Näiteks saate teha valiku, et väli Toote sissetuleku kogus kuvab kogusummad, mis on seotud vastu võetud toote/toodete summaga, või et välu Tellitud kogus kuvab tellitud toote summa.  
2. Klõpsake nuppu OK.


