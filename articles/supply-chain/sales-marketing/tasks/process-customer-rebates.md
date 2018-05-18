--- 
title: "Kliendi tagasimaksete genereerimine ja töötlemine"
description: "See protseduur näitab, kuidas töödelda kliendi tagasimakseid nõude loomisest kuni nende edastamiseni viitvõlgadena müügireskontrole."
author: omulvad
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 348793abc6d219f38bcdc2629b77343d93927005
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="generate-and-process-customer-rebates"></a>Kliendi tagasimaksete genereerimine ja töötlemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas töödelda kliendi tagasimakseid nõude loomisest kuni nende edastamiseni viitvõlgadena müügireskontrole. Teile selgitatakse konkreetse näite abil, kuidas mõjutavad erinevad tingimused tagasimakseridadel kliendile krediteeritavaid lõppsummasid. Peate kasutama demoettevõtte USMF andmeid ja täitma enne juhendi käivitamist järgmised ülesanded. 1) Minge lehele Müügireskontro parameetrid ning laiendage vahekaarti Hinnad ja siis vahekaarti Hinna üksikasjad, seejärel kontrollige, kas suvandi Hinna üksikasjade lubamine sätteks on valitud Jah. 2) Minge lehele Tagasimakselepped ja valige kliendi tagasimakselepe USMF-000001. Kui välja Töövoo kinnitamise olek sätteks pole valitud Kinnitatud, peate selle kinnitamiseks klõpsama tegevuspaanil suvandit Kinnitamine.


## <a name="review-a-customer-rebate-agreement"></a>Kliendi tagasimakseleppe läbivaatus
1. Avage Müük ja turundus > Kliendi tagasimaksed > Tagasimakselepped.
    * Järgmised etapid annavad ülevaate leppe USMF-000001 tingimustest. See aitab selgitada, kuidas arvutatakse kliendi krediidiväärtusi protseduuri hilisemates etappides.  
    * Lepe on kehtib üksiku kliendi puhul, selles näiteks on selleks klient US-009.  
    * Tagasimakse tehakse kliendile, kui ta ostab teatud toodet. Praegusel juhul on toote kaubakood T0020.   
    * Kliendi müügitulemus, mille alusel määratakse hinnangulised tagasimaksesummad, arvestatakse kokku kord nädalas.  
    * Suvandi Hinna alus säte on Bruto, mis tähendab, et rea müügisummat, mille põhjal nõuet hinnatakse, ei vähendata rea allahindluse võrra.  
    * Väli Tagasimakserea katkestuse tüüp näitab tagasimaksete arvutamise viis. Selles näites on tagasimaksete hindamise aluseks oleva müügiplaani sätteks Kogus.   
    * Lepingu read määravad tagasmaksesumma tüübi, tegeliku tagasimakseväärtuse ja läviväärtused. Selles näites kvalifitseerub klient tagasimaksele 20 USA dollarit iga müüdud ühiku kohta, kui tema nädalane tooteost jääb 1 kuni 50 ühiku piiresse, ja 40 USA dollarit ühiku kohta, kui ta ostab üle 50 ühiku.  
2. Sulgege leht.

## <a name="generate-rebate-claims"></a>Tagasimaksenõuete loomine
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
    * Tagasimaksenõuete loomise viisi matkimiseks on järgmine ülesanne luua müügitellimus, kus toode ja kogus kvalifitseerivad kõnealuse kliendi tagasimakse saamiseks.  
3. Valige või sisestage väärtus väljal Kliendi konto.
4. Klõpsake nuppu OK.
5. Sisestage või valige väärtus väljal Kaubakood.
6. Määrake koguse väärtuseks 40.
7. Klõpsake valikut Müügitellimuse rida.
8. Klõpsake suvandit Hinna üksikasjad.
    * Kui te seda suvandit ei näe, pole te enne juhendi käivitamist määranud suvandi Luba hinna üksikasjad sätteks Jah.  
9. Laiendage jaotist Tagasimaksed.
    * Vahekaardil Tagasimakse on toodud kõik tagasimakselepped, mis kehtivad praeguse tellimuserea puhul, ja hinnanguline tagasimaksesumma. Pange tähele, et kuvatavad summad vaid viitavad sellele, millised võivad olla tulevased tagasimaksenõuded. Tegelikud tagasimaksesummad võivad erineda olenevalt kliendi kogu saavutatud müügimahust perioodilise tagasimakseleppe alusel, sellest, kas klient on tagastanud kõik või osalise koguse, ja sellest, kas kohalduv müügitellimus on arveldatud.  
10. Sulgege leht.
11. Klõpsake käsku Lisa rida.
12. Sisestage või valige väärtus väljal Kaubakood.
13. Määrake koguse väärtuseks 60.
14. Klõpsake nuppu Salvesta.
15. Klõpsake toimingupaanil valikut Arve.
16. Klõpsake valikut Arve.
17. Laiendage jaotis Parameetrid.
18. Valige väljal Kogus väärtus Kõik.
19. Klõpsake nuppu OK.
20. Klõpsake nuppu OK.

## <a name="process-rebate-claims"></a>Tagasimaksenõuete töötlemine
1. Avage Müük ja turundus > Kliendi tagasimaksed > Tagasimaksed.
    * Leht Tagasimaksed toimib töölauana, kus saate tagasimaksenõudeid üle vaadata, kinnitada ja töödelda. Nüüd töötlete te nõudeid, mis loodi kliendi US-009, kes on tagasimakseleppe USMF-000001 subjekt, müügitellimuse arveldamise tulemusena.   
    * Esimene rida näitab tagasimaksenõuet 800 USA dollarile, mis põhineb toote T0020 40 ühiku müügil ja mille arvutamise aluseks on 20 USA dollarit ühiku kohta. See vastab tagasimakseleppe esimese kogusekatkestuse tingimustele.  
    * Teine nõue on 2400 USA dollarit, mis põhineb toote T0020 60 ühiku müügil ja mille arvutamise aluseks on leppe teise kogusekatkestuse järgi 40 USA dollarit ühiku kohta.  
    * Mõlema nõude olek on Arvutamisele kuuluv väärtus. See tähendab, et need on seostatud lepega, mis jälgib kliendi müügitulemusi perioodiliselt, ja et need tuleb ümber arvutada kogu müügimahu arvestamiseks vastaval perioodil.   
2. Klõpsake suvandit Kumuleeri.
3. Sisestage või valige väärtus väljal Klient.
4. Valige tänane kuupäev väljal Alguskuupäev.
5. Klõpsake nuppu OK.
    * Funktsiooni Kumuleeri käitamise tagajärjel on nüüd hinnanguline nõudesumma korrigeeritud, et võtta arvesse fakti, et kliendi kogu müügimaht vastaval perioodil on suurem kui esimese tagasimakse loomisel. Täpsemalt öeldes, kuna ostetud täielik kogus on jõudnud 100 ühikuni, kvalifitseerub klient nüüd 40 USA dollarile ühiku kohta (leppe teise kogusekatkestuse järgi) või 400 USA dollarile tagasimakse kogusummana. See erinevus salvestatakse uue nõude korrigeerimisena täiendavale 800 USA dollarile. Kumulatiivsesse värskendusse kaasatud tagasimaksenõuete olek on nüüd Arvutatud.   
6. Märkige loendis kõik read.
7. Klõpsake nuppu Kinnita.
8. Klõpsake suvandit Töötle.
9. Sisestage või valige väärtus väljal Klient.
10. Klõpsake nuppu OK.
    * Kuvatakse teade, et tagasimakse on edukalt töödeldud ja nõuete olek on muudetud sättele Märgi. See tähendab, et tagasimakse juurdekasvu töölehe sisestamise tagajärjel on a) nõuded üle kantud vähendusena ajutisele kliendisaldole, b) tagasimakse juurdekasvukonto on krediteeritud, et kajastada tulevasi kohustusi kliendi suhtes, ja c) tagasimakse kulukonto on debiteeritud seoses müügiga kaasneva kulu tuvastamisega.   


