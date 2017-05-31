---
title: "Pangaväljavõtete vastavusseviimine täpsema panga vastavusseviimise abil"
description: "Täpsema panga vastavusseviimise funktsiooni abil saate importida elektroonilisi pangaväljavõtteid ja neid rakenduses Microsoft Dynamics 365 for Operations automaatselt pangakannetega vastavusse viia. Selles teemas selgitatakse vastavusseviimise protsessi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 81368294164ca4ca1915d73f8f5622e61f5d1fc8
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Pangaväljavõtete vastavusseviimine täpsema panga vastavusseviimise abil

[!include[banner](../includes/banner.md)]


Täpsema panga vastavusseviimise funktsiooni abil saate importida elektroonilisi pangaväljavõtteid ja neid rakenduses Microsoft Dynamics 365 for Operations automaatselt pangakannetega vastavusse viia. Selles teemas selgitatakse vastavusseviimise protsessi.  

<a name="import-an-electronic-bank-statement"></a>Elektroonilise pangaväljavõtte importimine
-----------------------------------

Pangaväljavõtteid imporditakse toiminguga **Väljavõtte importimine** lehel **Pangaväljavõtted**. Pangakonto on pangaväljavõttes näidatud väärtuste kombinatsiooni kaudu, mis on määratud pangakonto andmetes. Nende väärtuste hulka kuuluvad panga nimi, pangakonto number, protsessikood, SWIFT (Society for Worldwide Interbank Financial Telecommunication) kood ja rahvusvaheline pangakonto number (IBAN). 

Saate laadida üles pangaväljavõtte, mis sisaldab teavet ühe või mitme konto kohta. Kui teil on mitu kontot, saavad kontod olla erinevates juriidilistes isikutes.

-   Ühe konto ühe pangaväljavõtte faili importimiseks määrake valiku **Mitme pangakonto väljavõtte importimine kõikide juriidiliste isikute puhul** väärtuseks **Ei** ja valige väljavõttega seotud pangakonto. Klõpsake valikut **Sirvi** seotud pangaväljavõtte faili valimiseks ja klõpsake siis käsku **Laadi üles**.
-   Ühe pangaväljavõtte faili importimiseks mitme konto jaoks määrake valiku **Mitme pangakonto väljavõtte importimine kõikide juriidiliste isikute puhul** väärtuseks **Jah**. Klõpsake valikut **Sirvi** seotud pangaväljavõtte faili valimiseks ja klõpsake siis käsku **Laadi üles**.

Kui mis tahes väljavõtet elektroonilises failis ei saa pangakontoga seostada tuvastatavaid välju kasutades, siis neid ei impordita. Siiski saab importida teisi väljavõtteid failis. Kasutaja saab seejärel teate, mis ütleb, et pangaväljavõtete importimine oli kindlate pangakontode puhul ebaedukas. Pange tähele, et pangaväljavõtte faili importival kasutajal peab olema juurdepääs juriidilisele isikule, et importida selle juriidilise isiku pangakontode väljavõtted. 

Saate kasutada zip-faili, et laadida mitu väljavõttefaili rakendusse Microsoft Dynamics 365 for Operations üles ühe protsessina. Mitme pangaväljavõtte faili importimiseks mitme konto kohta ühendage kõik pangaväljavõtte failid ühte zip-faili. Määrake dialoogiboksis **Pangaväljavõtete importimine** valiku **Mitme pangakonto väljavõtte importimine kõikide juriidiliste isikute puhul** väärtuseks **Jah**. Klõpsake valikut **Sirvi** pangaväljavõtte faile sisaldava zip-faili valimiseks ja klõpsake siis käsku **Laadi üles**. Importimisprotsess tuvastab zip-faili ja laeb iga sellesse kaasatud väljavõtte üles hoolimata pangakonto juriidilisest isikust. 

Saadaval on valik **Vii pärast importi vastavusse**. Kui määrate selle valiku väärtuseks **Jah**, kinnitab süsteem automaatselt pangaväljavõtte, loob uue panga vastavusseviimise ja töölehe ning käivitab pangaväljavõtte üleslaadimisel vaike-vastendamisreegli. See funktsioon automatiseerib protsessi kuni punktini, kus tehingud tuleb käsitsi vastendada.

## <a name="validate-the-bank-statement"></a>Pangaväljavõtte kinnitamine
Väljavõtte kinnitamiseks klõpsake lehel **Pangaväljavõtted** valikut **Kinnita**. Pangaväljavõtted tuleb kinnitada enne, kui neid saab vastavusse viia. See toiming viiakse automaatselt lõpule, kui valiku **Vii pärast importi vastavusse** väärtuseks oli importimise ajal määratud **Jah**. 

Pangaväljavõtte kinnitamisel kontrollitakse järgmisi andmeid.

-   Pangaväljavõte vastab valitud pangakontole.
-   Pangaväljavõtte valuuta vastab valitud pangakonto valuutale.
-   Väljavõtte algsaldo võrdub pangakonto eelmise väljavõtte sulgemissaldoga.
-   Kuupäev ei kattu sama pangakonto teise pangaväljavõtte kuupäevaga.
-   Pangakonto väljavõtete kuupäevades ei ole vahesid.
-   Väljavõtte ridade kuupäevad on pangaväljavõtte algus- ja lõpukuupäevade vahel.
-   Algsaldo ja reasummad võrduvad lõppsaldoga.

Kui kinnitamine on valmis, määratakse pangaväljavõtte olekuks **Kinnitatud**. Pangaväljavõte tuleb kinnitada enne, kui selle saab vastavusse viia.

## <a name="reconcile-the-bank-statement"></a>Pangaväljavõtte vastavusseviimine
Kui olete elektroonilise pangaväljavõtte importinud ja kinnitanud selle lehel **Pangaväljavõtted**, saate pangaväljavõtte lehtede **Panga vastavusseviimine** ja **Panga vastavusseviimise tööleht** abil vastavusse viia. 

Klõpsake lehel **Panga vastavusseviimine** valikut **Uus** uue vastavusseviimise loomiseks ja valige siis imporditud väljavõtte pangakonto. Pangakontol võib olla ainult üks avatud panga vastavusseviimine. Tähtaeg määrab pangaväljavõtte kanded ja Operationsi pangakanded, mis vastavusseviimise töölehel sisalduvad. Vaikimisi kasutatakse tähtajana kehtivat süsteemi kuupäeva, kuid saate vastavusseviimise kuupäeva muuta. Ülejäänud päise teave võetakse automaatselt väljavõttest. See toiming viiakse automaatselt lõpule, kui valiku **Vii pärast importi vastavusse** väärtuseks oli importimise ajal määratud **Jah**. 

Klõpsake lehel **Panga vastavusseviimine** valikut **Tööleht** lehe **Panga vastavusseviimise tööleht** avamiseks. Kui määrate valiku **Vii pärast importi vastavusse** väärtuseks **Jah**, käivitatakse vastavusse viimiseks automaatselt vaike-vastendamisreegel. Vastendamisreeglite käsitsi käivitamiseks klõpsake valikut **Käivita vastendusreeglid** vastendusreeglite kogumite või vastendusreeglite valimiseks, mida pangakannete suhtes käitada. Kui teil on palju töödeldavaid kandeid, võite läbida selle toimingu pakettprotsessina. 

Lehel **Panga vastavusseviimise tööleht** on neli ruudustikku, mis sisaldavad kandeid. Kahes ülemises ruudustikus on näidatud need pangaväljavõtte ja Operationsi kanded, mida pole veel vastendatud. Kahes alumises ruudustikus on näidatud vastendatud kanded. Vahekaardil **Pangaväljavõtte kande üksikasjad** on näidatud ülemises ruudustikus valitud vastendamata pangaväljavõtte kande üksikasjad. 

Pangaväljavõtte kannete vastendamiseks või vastavusse viimiseks on kolm võimalust.

-   Kannete vastendamine Operationsi pangakannetega.
-   Kannete vastendamine tühistava pangaväljavõtte kandega.
-   Märkige kanded väärtusega **Uus**, et neid saaks hiljem rakenduses Dynamics 365 for Operations pangakannetena sisestada.

Kannete käsitsi vastendamiseks valige kanded ruudustikus **Pangaväljavõtte kanded**, valige ruudustikus **Operationsi pangakanded** vastavad kanded ja klõpsake siis käsku **Vastenda**. Valitud vastendamata kanded viiakse ülemistesse ruutudesse ja vastendatud kanded alumistesse ruutudesse. Lisaks värskendatakse vastendatud ja vastendamata koondsummasid. Kande vastavused võivad olla üks-ühele, mitu ühele ja mitu mitmele. Vastavused peavad järgima reegleid lubatud kuupäevaerinevuste ja kandetüübi vastendamise kohta. Need reeglid on määratud lehel **Sularaha- ja pangahalduse parameetrid**.

Vastavusseviimises võib ilmneda sendierinevusi. Saate vastendada üksiku pangaväljavõtte kande üksiku Operationsi pangakandega, millel on sendierinevusi, kui sendierinevused jäävad pangakonto väljal **Lubatud sendierinevus** määratud lubatud hälbe piiridesse. Summa kuvatakse vastendatud Operationsi pangakande väljal **Parandussumma**. Kui panga vastavusseviimine märgitakse vastavusseviiduks, sisestatakse parandused automaatselt, kasutades põhikontot, mis on määratletud seostatud pangakande tüübis. Parandusi ei toetata dokumendi tüüpide **Tšekk** ja **Deposiit** puhul. 

Pangaväljavõtte kannete tühistamised vastendatakse vastavusseviimise töölehe abil. Kaks väljavõtte rida saab vastendada, kui summad on vastupidised ja kui üks kanne on märgitud tühistamiseks. Saate seadistada vastendusreegli ka toimingule **Tagasimaksmise väljavõtteridade tühjendamine**.

Tühistatud Operationsi pangakanded tuleb viia vastavusse, kasutades lehte **Operationsi pangakanded**. Kaks Operationsi pangakannet saab omavahel vastavusse viia, kui dokumentidel on sama pangakonto, dokumendi tüüp ja makseviide ja kui neil on vastupidised summad. Saate viia vastavusse ka üksiku tühistatud tšeki, et vältida nende kannete kuvamist vastavusseviimise töölehel. 

Kui on uusi panga algatatud kandeid (nt intresse, tasusid ja kulusid, mis pole veel rakenduses Dynamics 365 for Operations, võite lisada need töölehele, mis on seotud valitud pangaväljavõtte kandega. Valige pangaväljavõtte kanne vastendamata kannete ruudustikust **Pangaväljavõtte kanded** ja klõpsake siis valikut **Märgi uueks**. Kande olekuks määratakse **Uus** ja kanne viiakse vastendatud kannete ruudustikku **Pangaväljavõtte kanded**. Kanded, mis on märgitud väärtusega **Uus**, sisestatakse hiljem lehelt **Pangaväljavõte**. 

Saate ekslikult vastendatud kannete vastenduse tühistada. Valige vastendatud pangaväljavõtte tehing ja klõpsake käsku **Tühista vastendamine**. Kõik seotud kanded viiakse tagasi vastendamata kannete ülemistesse ruudustikesse ja vastendatud ning vastendamata kogusummasid värskendatakse. 

Pärast kõigi väljavõtte ridade töötlemist tuleb märkida tööleht Panga vastavusseviimine vastavusse viiduks.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Vastendusega seotud uute kannete sisestamine
Pangaväljavõtte kanded, mis märkisite vastavusseviimise töölehel väärtusega **Uus**, sisestatakse lehele **Pangaväljavõte**. Valige lehelt **Pangaväljavõte** väljavõtte üksikasjade vaatamiseks väljavõtte ID. Menüüs **Raamatupidamine** saate kasutada valikuid **Jaotuste kuvamine** ja **Raamatupidamise kuvamine** uute kannete ja seotud pearaamatukannete üksikasjade vaatamiseks. Tehke valik **Sisesta** väärtusega **Uus** märgitud pangaväljavõtte ridade sisestamiseks pearaamatusse. Pange tähele, et sisestamine saab toimuda vaid üks kord pangaväljavõtte kohta.




