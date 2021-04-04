---
title: Kliendi tagasimaksete genereerimine ja töötlemine
description: See protseduur näitab, kuidas töödelda kliendi tagasimakseid nõude loomisest kuni nende edastamiseni viitvõlgadena müügireskontrole.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage, MCRBrokerWriteOffReason, MRCHierarchyAddCust, PdsItemRebateGroup, PdsRebate, PdsRebateProgramTMATable, PdsRebateTable, PdsRebateTableListPagePreviewPane, PdsRebateTrans, PdsRebateType_CustLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abd48482d567a427389c1feeb1142eba85ee8ab1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260331"
---
# <a name="generate-and-process-customer-rebates"></a>Kliendi tagasimaksete genereerimine ja töötlemine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas töödelda kliendi tagasimakseid nõude loomisest kuni nende edastamiseni viitvõlgadena müügireskontrole. Teile selgitatakse konkreetse näite abil, kuidas mõjutavad erinevad tingimused tagasimakseridadel kliendile krediteeritavaid lõppsummasid. Peate kasutama demoettevõtte USMF andmeid ja täitma enne juhendi käivitamist järgmised ülesanded. (1) Minge lehele Müügireskontro parameetrid ning laiendage vahekaarti Hinnad ja siis vahekaarti Hinna üksikasjad, seejärel kontrollige, kas suvandi Hinna üksikasjade lubamine sätteks on valitud Jah. (2) Minge lehele Tagasimakselepped ja valige kliendi tagasimakselepe USMF-000001. Kui välja Töövoo kinnitamise olek sätteks pole valitud Kinnitatud, peate selle kinnitamiseks klõpsama Toimingupaanil suvandit Kinnitamine.


## <a name="review-a-customer-rebate-agreement"></a>Kliendi tagasimakseleppe läbivaatus
1. Minge **Navigeerimispaan > Moodulid > Müük ja turundus > Kliendi tagasimaksed > Tagasimakselepped**.
    - Järgmised etapid annavad ülevaate leppe USMF-000001 tingimustest. See aitab selgitada, kuidas arvutatakse kliendi krediidiväärtusi protseduuri hilisemates etappides.  
    - Lepe on kehtib üksiku kliendi puhul, selles näiteks on selleks klient US-009.  
    - Tagasimakse tehakse kliendile, kui ta ostab teatud toodet. Praegusel juhul on toote kaubakood T0020.   
    - Kliendi müügitulemus, mille alusel määratakse hinnangulised tagasimaksesummad, arvestatakse kokku kord nädalas.  
    - Suvandi „Hinna alus” säte on Bruto, mis tähendab, et rea müügisummat, mille põhjal nõuet hinnatakse, ei vähendata rea allahindluse võrra.  
    - Väli Tagasimakserea katkestuse tüüp näitab tagasimaksete arvutamise viis. Selles näites on tagasimaksete hindamise aluseks oleva müügiplaani sätteks Kogus.   
    - Lepingu read määravad tagasmaksesumma tüübi, tegeliku tagasimakseväärtuse ja läviväärtused. Selles näites kvalifitseerub klient tagasimaksele 20 USA dollarit iga müüdud ühiku kohta, kui tema nädalane tooteost jääb 1 kuni 50 ühiku piiresse, ja 40 USA dollarit ühiku kohta, kui ta ostab üle 50 ühiku.  
2. Sulgege leht.

## <a name="generate-rebate-claims"></a>Tagasimaksenõuete loomine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.
2. Klõpsake valikut **Uus**. Tagasimaksenõuete loomise viisi matkimiseks on järgmine ülesanne luua müügitellimus, kus toode ja kogus kvalifitseerivad kõnealuse kliendi tagasimakse saamiseks.    
3. Väljale **Kliendi konto** sisestage või valige väärtus.
4. Klõpsake valikut **OK**.
5. Sisestage või valige väärtus väljale **Kauba kood**.
6. Määrake **Koguse** väärtuseks 40.
7. Valige jaotises **Müügitellimuse read** suvand **Müügitellimuse rida**.
8. Klõpsake suvandit **Hinna üksikasjad**. Kui te seda suvandit ei näe, pole te enne juhendi käivitamist määranud suvandi **Luba hinna üksikasjad** sätteks Jah.     
9. Laiendage jaotist **Tagasimaksed**. Vahekaardil **Tagasimaksed** on toodud kõik tagasimakselepped, mis kehtivad praeguse tellimuserea puhul, ja hinnanguline tagasimaksesumma. Pange tähele, et kuvatavad summad vaid viitavad sellele, millised võivad olla tulevased tagasimaksenõuded. Tegelikud tagasimaksesummad võivad erineda olenevalt kliendi kogu saavutatud müügimahust perioodilise tagasimakseleppe alusel, sellest, kas klient on tagastanud kõik või osalise koguse, ja sellest, kas kohalduv müügitellimus on arveldatud.
10. Sulgege leht.
11. Klõpsake käsku **Lisa rida**.
12. Sisestage või valige väärtus väljale **Kauba kood**.
13. Määrake **Koguse** väärtuseks 60.
14. Klõpsake valikut **Salvesta**.
15. Paanil **Toimingupaan** klõpsake **Arve**.
16. Klõpsake **Arve**.
17. Laiendage jaotist **Parameetrid**.
18. Väljal **Kogus** valige Kõik.
19. Klõpsake valikut **OK**.
20. Klõpsake valikut **OK**.

## <a name="process-rebate-claims"></a>Tagasimaksenõuete töötlemine
1. Minge **Navigeerimispaan > Moodulid > Müük ja turundus > Kliendi tagasimaksed > Tagasimakselepped**.
    - Leht Tagasimaksed toimib töölauana, kus saate tagasimaksenõudeid üle vaadata, kinnitada ja töödelda. Nüüd töötlete te nõudeid, mis loodi kliendi US-009, kes on tagasimakseleppe USMF-000001 subjekt, müügitellimuse arveldamise tulemusena.   
    - Esimene rida näitab tagasimaksenõuet 800 USA dollarile, mis põhineb toote T0020 40 ühiku müügil ja mille arvutamise aluseks on 20 USA dollarit ühiku kohta. See vastab tagasimakseleppe esimese kogusekatkestuse tingimustele.  
    - Teine nõue on 2400 USA dollarit, mis põhineb toote T0020 60 ühiku müügil ja mille arvutamise aluseks on leppe teise kogusekatkestuse järgi 40 USA dollarit ühiku kohta.  
    - Mõlema nõude olek on „Arvutamisele kuuluv”. See tähendab, et need on seostatud lepega, mis jälgib kliendi müügitulemusi perioodiliselt, ja et need tuleb ümber arvutada kogu müügimahu arvestamiseks vastaval perioodil.   
2. Klõpsake suvandit **Kumuleeri**.
3. Sisestage või valige väärtus väljal **Klient**.
4. Valige tänane kuupäev **Alguskuupäev**.
5. Klõpsake valikut **OK**. Funktsiooni **Kumuleeri** käitamise tagajärjel on nüüd hinnanguline nõudesumma korrigeeritud, et võtta arvesse fakti, et kliendi kogu müügimaht vastaval perioodil on suurem kui esimese tagasimakse loomisel. Täpsemalt öeldes, kuna ostetud täielik kogus on jõudnud 100 ühikuni, kvalifitseerub klient nüüd 40 USA dollarile ühiku kohta (leppe teise kogusekatkestuse järgi) või 400 USA dollarile tagasimakse kogusummana. See erinevus salvestatakse uue nõude korrigeerimisena täiendavale 800 USA dollarile. Kumulatiivsesse värskendusse kaasatud tagasimaksenõuete olek on nüüd Arvutatud. 
6. Märkige loendis kõik read.
7. Klõpsake nuppu **Kinnita**.
8. Klõpsake nuppu **Töötle**.
9. Sisestage või valige väärtus väljal **Klient**.
10. Klõpsake valikut **OK**. Kuvatakse teade, et tagasimakse on edukalt töödeldud ja nõuete olek on muudetud sättele Märgi. See tähendab, et tagasimakse viitvõlgade töölehe sisestamise tulemusena:
    - Nõuded on üle kantud mahaarvamistena ajutisele kliendisaldole.
    - Tagasimaksete juurdekasvukonto on krediteeritud, et kajastada kliendi tulevasi kohustusi.
    - Tagasimakse kulukonto on debiteeritud, et tuvastada müügiga kaasnevat kulu.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]