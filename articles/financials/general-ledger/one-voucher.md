---
title: "Üks kanne"
description: "Ühe kandega finantstöölehtede jaoks (üldine tööleht, põhivara tööleht, hankija maksete tööleht jne) saate sisestada mitu alampearaamatu kannet ühes kandes."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Üks kanne

[!include [banner](../includes/banner.md)]

> [!NOTE]
>  See funktsioon on saadaval rakenduse Dynamics 365 for Finance and Operations versioonis 8.0, mis on saadaval 2018. aasta kevade väljaandes.   

<a name="what-is-one-voucher"></a>Mis on funktsioon Üks kanne?
======================

Olemasoleva funktsiooniga finantstöölehtede jaoks (üldine tööleht, põhivara tööleht, hankija maksete tööleht jne) saate sisestada mitu alampearaamatu kannet ühes kandes. Nimetame seda funktsiooni üheks kandeks. Saate ühe kande loomisel kasutada üht järgmistest viisidest.

-   Seadistage töölehe nimi (**Pearaamat** \> **Töölehe seadistus** \>**Töölehe nimed**), nii et välja **Uus kanne** väärtus oleks **Ainult üks kande number**. * Iga töölehele lisatud rida lisatakse nüüd samale kandele. Kuna iga rida lisatakse samale kandele, saab kande sisestada mitmerealise kandena, konto/vastaskonto samal real või kombinatsioonina.

[![Üks rida](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Pange tähele, et sätte „Üks kanne” definitsioon EI sisalda töölehe nimesid, mis on seadistatud ainult valikule **Üks kande number** ja kasutaja sisestab seejärel kande, mis sisaldab ainult tüüpe pearaamatukonto tüüpe.  Selles dokumendis tähendab „Üks kanne”, et olemas on üks kanne, mis sisaldab rohkem kui üht hankijat, klienti, panka, põhivara või projekti. 

-   Sisestage mitmerealine kanne, kus vastaskonto puudub.

[![Mitmerealine kanne](./media/Multi-line.png)](./media/Multi-line.png)

-   Sisestage kanne, kus nii konto kui ka vastaskonto sisaldavad alampearaamatu konto tüüpi, näiteks hankija/hankija, klient/klient, hankija/klient või pank/pank.

[![Alampearaamatu kanne](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Ühe kande probleemid
=======================

Ühe kande funktsioon tekitab probleeme tasakaalustamise, maksuarvestuse, alampearaamatu ja pearaamatu vastavusseviimise, finantsaruandluse ja muu ajal. (Näiteks lisateavet probleemide kohta, mis tekivad tasakaalustamise ajal, vt jaotisest [Üksik mitme kliendi- või hankijakirjega kanne](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Õigeks toimimiseks ja aruandluseks on nende protsesside ja aruannete jaoks vaja kande üksikasju. Kuigi mõni stsenaarium ei pruugi olenevalt organisatsiooni seadistusest siiski õigesti toimida, esineb sageli probleeme, kui ühte kandesse sisestatakse mitu kannet.

Näiteks sisestate järgmise kande.

[![Näide](./media/example.png)](./media/example.png)

Seejärel loote aruande **Kulud hankija järgi** tööruumi **Finantsülevaated**. Aruanderühm kulukonto tasakaalustatakse hankijagruppi ja seejärel hankija alla. Aruande loomisel ei suuda süsteem määrata, millised hankijagrupid/hankijad sisestasid kulu 250.00. Kuna kande üksikasjad on puudu, eeldab süsteem, et kogu 250.00 on sisestanud esimene kandes leiduv hankija. 250.00, mis sisaldub põhikonto 600120 saldol, kuvatakse seejärel selle hankijagrupi/hankija all. On väga tõenäoline, et kande esimene hankija ei ole õige hankija, nii et aruanne on vale.

[![Kulud](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Ühe kande tulevik
=========================

Ülaltoodud probleemide tõttu aegub ühe kande funktsioon. Kuid kuna on olemas sellest funktsioonist olenevad funktsionaalsed vahemikud, ei aegu funktsioon korraga. Selle asemel kasutame järgmist graafikut. 

- **2018. aasta kevade väljaanne** – funktsioon lülitatakse pearaamatu parameetriga vaikimisi välja. Saate funktsiooni siiski sisse lülitada, kui teie organisatsioonil on stsenaarium, mis langeb selles teemas allpool loetletud ettevõttestsenaariumi vahemikku.

  -   Kui kliendil on ettevõttestsenaarium, milleks pole üht kannet vaja, ärge funktsiooni sisse lülitage. Me ei paranda vigu aladel, millest räägitakse selles teemas allpool, kui seda funktsiooni kasutatakse, kuigi olemas on muu lahendus.

  -   Lõpetage ühe kande kasutamine rakenduse Microsoft Dynamics 365 Finance and Operations integratsioonidele, v.a juhul, kui see funktsioon on vajalik mõne funktsionaalse vahemiku jaoks.

- **2018. aasta sügise ja hilisemad väljaanded** – täidetakse funktsionaalsed vahemikud. Kui funktsionaalsed vahemikud on täidetud, lülitatakse ühe kande funktsioon püsivalt välja.

- > [!IMPORTANT]
  > Pange tähele, et suvandit **Ainult üks kande number** EI ole töölehe nime seadistusest eemaldatud.  Seda suvandit toetatakse endiselt, kui kanne sisaldab ainult pearaamatukonto tüüpe.  Kliendid peavad selle sätte kasutamisel olema ettevaatlikud, sest kannet ei sisestata, kui nad kasutavad suvandit **Ainult üks kande number**, kuid sisestavad rohkem kui ühe kliendi, hankija, panga, põhivara või kliendi.  Samuti saavad kliendid endiselt sisestada erinevate alampearaamatu tüüpide kombinatsiooni, nagu makse ühes kandes, mis sisaldab kontotüüpe Hankija/Pank.  

<a name="why-use-one-voucher"></a>Miks kasutada üht kannet?
====================

Klientidega peetud vestluste põhjal oleme koostanud järgmise loendi stsenaariumidest, kus kliendid kasutavad ühe kande funktsioonid, ja põhjustest, miks nad neid kasutavad. Mõnda neist ärivajadustest on võimalik täita vaid ühe kande funktsiooni kasutades. Kui paljude stsenaariumide korral võivad alternatiivsed lahendused vastata samadele ärivajadustele.

<a name="scenarios-that-require-one-voucher"></a>Stsenaariumid, mille jaoks on vaja ühe kande funktsiooni
----------------------------------

Järgmiseid stsenaariume on võimalik täita ainult ühe kande funktsiooni kasutades. Need funktsionaalsed vahemikud täidetakse teiste funktsioonidega 2018. aasta sügise ja hilisemate väljaannetega.

-   **Hankija või kliendi maksete sisestamine pangakonto kokkuvõttevormi**

    -   Organisatsioon edastab loendi hankijate ja summadega pangale ning pank kasutab seda loendit hankijatele organisatsiooni nimel maksmiseks. Pank sisestab maksete summa pangakontole üksiku tagastusena.

>   Hankija maksete summeerimist toetatakse vaid ühe kande funktsiooni kaudu. Iga hankija sisestatakse eraldi reana, et ostureskontro pearaamat oleks üksikasjalik, kuid kõikide maksete koondsumma tasakaalustatakse pangakonto ühe reaga. Seetõttu on tagastus panga alampearaamatus näidatud ühe koondsummana.

-   Organisatsioon hoiustab kliendimakseid või pank hoiustab kliendimakseid organisatsiooni nimel ja deposiit kuvatakse pangakontol tervikväljamaksena.

>   Kliendimaksete summeerimist toetab tavaliselt hoiustamise funktsioon. Kuid kui kasutate makseviisil vahekontot, toetatakse seda stsenaariumi vaid ühe kande funktsiooni kaudu. Kliendimaksed sisestatakse sama moodi, nagu on kirjeldatud hankija maksete summeerimise kohta.

-   **Ärisündmuse kannete grupeerimise mehhanism**

    -   Organisatsioonil on üks ärisündmus, mis käivitab mitu kannet. Kuid raamatupidamisosakond soovib paremaks auditeerimiseks vaadata raamatupidamiskirjeid koos.

>   Kui organisatsioon peab vaatama ärisündmuse raamatupidamiskirjeid koos, tuleb kasutada ühe kande funktsiooni. 

- **Riigikohased funktsioonid**

  -   Ühtse haldusdokumendi (SAD) funktsioon Poola jaoks nõuab praegu üksiku kande kasutamist. Kui selle funktsiooni jaoks on saadaval rühmitamisvalik, peate edasi kasutama ühe kande funktsiooni. Võib olla vee riigikohaseid funktsioone, mis nõuavad ühe kande funktsiooni.

- **Kliendi ettemakse tööleht, millel on maksud mitmel real**

  -   Klient teeb tellimusele ettemakse ja tellimuse ridades on eri maksud, mis tuleb ettemakse jaoks salvestada. Ettemakse kliendi makse on üks kanne, mis simuleerib tellimuse ridu, nii et iga rea summale saab salvestada sobiva maksu.

Selles stsenaariumis on ühe kande kliendid üks ja sama klient, sest kanne simuleerib kliendi tellimuse ridu. Ettemakse tuleb sisestada ühte kandesse, kuna maksuarvestus tuleb teha kliendi tehtud üksiku makse ridades.

-   **Põhivara hooldus: järelkulum, vara tükeldamine, likvideerimise kulumi arvutamine**

Järgmised põhivara kanded loovad samuti ühes kandes mitu kannet.
-   Varale tehakse täiendav soetamine ja arvutatakse järelkulum.
-   Vara tükeldatakse.
-   Likvideerimise kulumi arvutamiseks kasutatav parameeter on lubatud ja vara likvideeritakse.

<a name="scenarios-that-dont-require-one-voucher"></a>Stsenaariumid, mille jaoks ei ole vaja ühe kande funktsiooni
----------------------------------------

Järgmisi stsenaariume on võimalik teha muude vahenditega ja nende jaoks ei pea kasutama ühe kande funktsiooni.

-   **Kliendimaksete sisestamine pangakonto kokkuvõttevormi**

Organisatsioon hoiustab kliendimakseid või pank hoiustab kliendimakseid organisatsiooni nimel ja deposiit kuvatakse pangakontol tervikväljamaksena.

Kliendimaksete summeerimist toetatakse hoiustamise funktsiooni kaudu, kui vahekontot makseviisis ei kasutata.

-   **Tasaarveldus**

Tasaarvelduses tasaarveldatakse hankija ja kliendi saldod üksteisega, kuna hankija ja klient on üks ja sama osapool. See lähenemine vähendab rahavahetust organisatsiooni ja kliendi/hankija osapoole vahel.

Tasaarveldust saab teha, sisestades suurenemise ja vähenemise eraldi kannetesse ning sisestades tasaarvelduse pearaamatukontole tasakaalustuse.

-   **Koondsisestamine pearaamatusse**

Organisatsioonid soovivad sageli pearaamatusse koondsisestada, et vähendada andmete hulka. Kuid tavaliselt on organisatsioonidel siiski vaja, et kande üksikasjad jääks alles. Kui koondsisestamine läbi ühe kande on tehtud, ei ole kande üksikasjad teada ja neid ei saa säilitada.

   -   Kuna kande üksikasja ei saa praegu säilitada, soovitame ühe kande funktsiooni koondsisestamiseks mitte kasutada.
   -   Kui ühe kande tugi eemaldatakse, saame töölehtedele juurutada lähtedokumendi ja raamatupidamise raamistikud. Need raamistikud säilitavad siis kande üksikasja ja toetavad summeerimist pearaamatusse.

-   **Mitme sisestamata makse tasakaalustamine samale arvele**

Seda stsenaariumit leidub enamasti jaemüügi organisatsioonides, kus kliendid saavad ostude eest maksmiseks kasutada mitut makseviisi. Selles stsenaariumis peab organisatsioon suutma salvestada mitut sisestamata makset ja tasakaalustama neid kliendiarve suhtes.

Uue funktsiooniga, mis lisati rakenduse Microsoft Dynamics 365 for Operations versioonile 1611 (november 2016), saab mitut sisestamata makset tasakaalustada ühe arve suhtes. Mitut kliendimakset pole enam vaja sisestada ühte kandesse.

-   **Pangaväljavõtte kannete importimine**

Pangad sageli teevad makseid ja võtavad makseid vastu organisatsiooni nimel ning need kanded salvestatakse rakendusse Finance and Operations pangalt saadud faili kaudu. Organisatsioonid soovivad sageli neid kandeid kokku rühmitada, kasutades pangaväljavõtte numbrit failis. Kuna iga kanne on pangaväljavõttel üksikasjalikult esitatud, ei ole summeerimine panga alampearaamatus vajalik.

Kandeid saab rühmitada, kasutades töölehe muid välju, näiteks töölehe partiinumbrit või dokumendinumbrit.

-   **Kanna saldod üle**

Organisatsioonil võib olla vaja üle kanda saldo ühelt hankijalt teisele hankijale kas vea tõttu või kuna teine hankija on kohustuse üle võtnud. Seda tüüpi ülekanded esinevad ka kontotüüpide, näiteks kliendi- ja pangakontode kohta.

Saldo ülekandeid ühelt kontolt (hankija, kliendi-, pangakontolt jne) teisele kontole saab teha eraldi kannete kaudu ning tasaarvelduse pearaamatukontole saab sisestada tasakaalustuse.

-   **Algsaldode sisestamine**

Organisatsioonid sisestavad sageli alampearaamatu kontodele (hankija, kliendi-, põhivarakontodele jne) algsaldosid ühe kandena. Iga alampearaamatu konto algsaldosid saab sisestada eraldi kannetena ja tasaarvelduse pearaamatukontole saab sisestada tasakaalustuse.

-   **Sisestatud kliendi- või hankija dokumentide raamatupidamiskirje parandamine**

Organisatsioonil võib olla vaja parandada sisestatud arve raamatupidamiskirje müügireskontro või ostureskontro pearaamatukontot, aga seda arvet ei saa tühistada või parandada teise mehhanismi kaudu.

Kui parandus on vaja teha müügireskontro või ostureskontro pearaamatukontole, tuleb korrigeerida otse pearaamatukontot. Korrigeerida ei saa, sisestades hankija või kliendi kaudu. See lähenemine nõuab, et korrigeerimine tehakse seisakuajal, kui pearaamatukonto lubab ajutiselt käsitsi sisestamist.

-   **„Süsteem lubab seda”**

Organisatsioonid kasutavad sageli ühe kande funktsiooni lihtsalt seetõttu, et süsteem lubab neil seda kasutada, mõistmata selle mõju.

