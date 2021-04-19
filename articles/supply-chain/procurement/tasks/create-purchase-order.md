---
title: Ostutellimuse loomine
description: Selles teemas näidatakse teile, kuidas luua ostutellimust käsitsi.
author: kamaybac
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fca62bcfc1d6e15c8882bed32b82b63eb4c1666
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812298"
---
# <a name="create-a-purchase-order"></a>Ostutellimuse loomine

[!include [banner](../../includes/banner.md)]

Selles teemas näidatakse teile, kuidas luua ostutellimust käsitsi. Koondplaneerimise, otsetarne ja muude protsesside tulemusena luuakse ostutellimused tavaliselt automaatselt. Ostutellimused loob tavaliselt ostuagent. Siin esitatud näidet saab kasutada demoandmete ettevõttes USMF, kasutades väärtusi, mida on soovitatud erinevate etappide märkustes.


## <a name="create-the-purchase-order-header"></a>Ostutellimuse päise loomine
1. Minge **navigeerimispaanile > Moodulid > Hange ja hankimine > Ostutellimused > Kõik ostutellimused**.
2. Valige suvand **Uus**.
3. Valige hankija konto **US-101**. Kui valite hankija, kopeeritakse hankijakirje üksikasjad, nagu aadress, arvekonto, tarnetingimused ja -viis vaikeväärtustena tellimuse päisesse. Saate neid väärtusi alati muuta.  
4. Laiendage jaotist **Üldine**.

    - Väli **Sait** koos väljaga **Ladu** täpsustab, kuhu hangitud kaubad ja teenused peab tarnima. Vaikimisi kohaletoimetamise aadress on tegevuskoht. Mõlemad väljad saab täita valitud hankijale seadistatud väärtustega või määrata need käsitsi.  
    - Välja **Tarnekuupäev** kasutatakse, et täpsustada millal hangitud kaubad ja teenused peavad olema tarnitud. Saate määrata ühe tarnekuupäeva tellimuse kohta või anda üksikutele tellimuse ridadele ainulaadsed tarnekuupäevad. Kui siin määratud tarnekuupäeva ei saa teatud toodete või teenuste puhul kasutada, sest neil on pikemad täitmisajad, siis need read luuakse vastavalt sellele hilisema tarnekuupäevaga.  

5. Laiendage jaotist **Haldus**. Välja **Tellija** saab kasutada selleks, et täpsustada, kes on tellimuse teinud. Seda võib olla mugav hankijaga ühiskasutada, kui tal on vaja selle inimesega ühendust võtta. Väljale võidakse määrata väärtus automaatselt, kui praegune kasutajakonto on seotud nimega lehel **Kasutajad**.  
6. Valige nupp **OK**. Tellimuse päis on nüüd loodud. Kui töötate ostutellimuse ridadega, kuvatakse ainult päise teabe kokkuvõte. Kui teil on vaja kuvada ülejäänud teavet, valige **Päis**.  

## <a name="add-a-purchase-order-line"></a>Ostutellimuse rea lisamine
1. Valige rida **Ostutellimus**.
2. Valige **Dimensioonid**. Toodetel võivad olla variandid, mis on eristatavad dimensioonidega, nagu värv, suurus või stiil. Tooteid saab seadistada ka nii, et need kasutavad laoala dimensioone, nagu tegevuskoht ja ladu. On olemas ka valikulised jälgimisdimensioonid, nagu partii- ja seerianumber. Tellimuse sisestamise tõhususe parandamiseks saate lisada sagedamini kasutatavad dimensiooniväljad otse tellimuse ruudustikku.  
3. Märkige märkeruut **Värv**. Valikuline: kui valite välja **Salvesta seadistus**, kuvatakse teie valitud dimensioonid tellimusrea ruudustikus järgmine kord kui avate ostutellimuse lehe.  
4. Valige nupp **OK**.
5. Valige väljal **Kaubakood** väärtus **T0004**.

    - Tellimuse read luuakse toodetele ja teenustele, määrates kaubakoodi, või nagu kulud, määrates hankekategooria. 
    - Kategooriavälja **Hange** kasutatakse ridade lisamiseks, kui hangitud kaubad kantakse otse kuludesse, mitte ei lähe varudesse. See tähendab, et kui peate ostu kuludesse kandma, saate seda teha, luues ostutellimuse rea, mis määrab hankekategooria, mitte ei loo kaubakoodiga rida. Kaupu saab ka hankekategooriaga seostada ja sellisel juhul kuvatakse hankekategooria ainult informatiivse teabena.  

6. Väljale **Värv** sisestage või valige väärtus. Väljad **Sait** ja **Ladu** on tavaliselt täidetud väärtustega tellimuse päisest, kuid välju on võimalik tühistada, kui on ridu teistesse asukohtadesse viia.  
7. Sisestage arv väljale **Kogus**.

    - Valige kogus, mida soovite osta. Väli **Kogus** on automaatselt täidetud minimaalse toote tellimuse kogusega, kui see on seadistatud või väärtusega 1.  
    - Väli **Ühik** näitab tellitud koguse mõõtühikut. Tavaliselt tuleb ühik automaatselt tooteetaloni andmete ostuühikust, kuid saate seda muuta.  
    - Väli **Ühiku hind** sisaldab tavaliselt väärtust kas ostulepingust või kaubandusleppest. Ühiku hinda on võimalik üksikute tellimuse ridade puhul muuta, näiteks siis, kui hankijaga lepitakse kokku ainulaadne hind.  
    - Väli **Allahindlus** väljendab allahindluse summat ühiku kohta. See allahindlus vähendab seega ühiku hinda allahindluse võrra. See allahindlus tuleb tavaliselt automaatselt ostulepingutest või kaubanduslepetest, kuid seda on võimalik üksikutel ridadel tühistada, kui ainulaadsed allahindlused on hankijaga kokku lepitud.  
    - Saab sisestada allahindluse protsendi, mis vähendab rea netosummat vastavalt. See allahindluse protsent tuleb tihti automaatselt ostulepingutest või kaubanduslepetest, kuid seda on võimalik üksikutel ridadel tühistada, kui ainulaadne allahindluse protsent on hankijaga kokku lepitud.  
    - Väärtus väljal **Netosumma** on arvutatud rea teiste väljade põhjal, sealhulgas kogus, ühiku hind, allahindlus ja allahindluse protsent. Netosummat on võimalik muuta, kuid väljad **Ühiku hind**, **Allahindlus** ja **Allahindluse protsent** jäävad tühjaks ja kui sisestate rea suunas, on sisestatud summa proportsionaalne netosummaga. Tavaliselt kasutatakse välja **Netosumma** ainult rea netosumma kuvamiseks.  

8. Laiendage jaotist **Rea üksikasjad**.
9. Valige vahekaart **Tarne**. Igale reale määratakse unikaalne tarnekuupäev. Kuupäev on päritud ostutellimuse päise väljalt, kuid saate seda muuta.  

## <a name="review-order-totals"></a>Tellimuse kogusummade ülevaatamine
1. Valige **Kogusummad**.

    - Kui te ei näe toimingut **Kogusummad**, valige toimingupaanil vahekaart **Ostutellimus**.  
    - See dialoogiboks kuvab kogu tellimuse kogusummad.  
    - Väli **Valik** lubab teil muuta kogusummade arvutamise alust. Näiteks saate valida **Toote sissetuleku kogus**, et näidata kogusummasid, mis on seotud saadu toote/toodete summaga või **Tellitud kogus**, et näidata tellitud toodete hulka.  

2. Valige nupp **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]