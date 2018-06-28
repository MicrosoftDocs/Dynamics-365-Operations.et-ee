---
title: Pettuseteatiste seadistamine
description: "Selles teemas kirjeldatakse, kuidas seadistada reegleid, et tellimuste töötlemise käigus teavitada klienditeeninduse esindajaid potentsiaalsetest valeandmetest. Saate määratleda spetsiaalsed koodid, mida kasutatakse kahtlaste tellimust automaatselt või manuaalselt ootele panekuks."
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e4f89d86b64e0c8c76c15d3c2c1c00af353e9ca
ms.openlocfilehash: 2534e687623ab750f349287a762a354bc0fcf12b
ms.contentlocale: et-ee
ms.lasthandoff: 05/17/2018

---

# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Kõnekeskuse pettuseteatiste seadistamine ja kasutamine

[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada kriteeriume ja reegleid, et panna potentsiaalselt petturlikud müügitellimused täiendavaks ülevaatamiseks ootele. Pettuse kontrolli funktsioon võimaldab kontrollida müügitellimuse teabe kehtivust. Kui müügitellimuse teave tundub organisatsiooni petturliku tegevuse kriteeriumite ja reeglite alusel kahtlane, võidakse tellimus täiendavaks ülevaatamiseks ootele panna. Sel juhul ei saa tellimust lattu täiendavaks töötlemiseks edastada enne, kui ootelolek on tühistatud.

> [!NOTE]
> Seda funktsiooni saab kasutada ainult Retaili kõnekeskuse kanali müügitellimuse töötlemisel.

## <a name="turning-on-the-fraud-check-feature"></a>Pettuse kontrolli funktsiooni sisselülitamine

Pettuse kontrolli funktsiooni kasutamiseks peate määrama kanali suvandi **Tellimuse lõpetamise lubamine** olekuks **Jah**, kui kõnekeskuse kanal on [määratletud](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/set-up-order-processing-options). Kui tellimuse lõpetamine on sisse lülitatud, peavad kõnekeskuse kasutajad kõigi loodud müügitellimuste jaoks müügitellimuse lehel valima suvandi **Lõpule viidud**. Tegevus Lõpule viidud toob kaasa lehe **Müügitellimuse kokkuvõte** avanemise. Kui kasutajad on lehel **Müügitellimuse kokkuvõte** sisestanud vajalikud makseandmed, peavad nad tellimuse lõpuleviimiseks klõpsama käsku **Edasta**. Tellimuse esitamisel käivitatakse pettuse kontrolli funktsioon ja süsteemis olevad aktiivsed reeglid kinnitatakse automaatselt.

Kõnekeskuse kasutajad saavad ka käsitsi müügitellimuse pettuse tõttu ülevaatamise jaoks ootele panna, enne kui nad klõpsavad käsku **Edasta**. Müügitellimuse käsitsi ootele panemiseks valige lehel **Müügitellimuse kokkuvõte** suvand **Pane ootele** \> **Pettuse tõttu käsitsi ootele panemine**. Seejärel palutakse teil sisestada kommentaar tellimuse ootelepaneku põhjuse selgitamiseks. See kommentaar kuvatakse töölaual [ootel tellimused](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds), et anda konteksti ootel olevaid tellimusi ülevaatavale kasutajale, et ta saaks otsustada, kas tellimus tuleks väljastada.

Lisaks kanalil suvandi **Tellimuse lõpetamise lubamine** konfigureerimisele peate kõnekeskuse parameetrites konfigureerima ka pettuse kontrolli funktsiooni. Avage **Retail** \> **Kanali häälestus** \> **Kõnekeskuse seadistamine** \> **Kõnekeskuse parameetrid**. Lehel **Kõnekeskuse parameetrid** määrake vahekaardil **Ootel** suvandi **Pettuse kontroll** olekuks **Jah**.

Vahekaardil **Ootel** peaksite määratlema ka [ooteloleku koodid](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds), mis rakendatakse tellimusele, mis on kas käsitsi või automaatselt pettuse tõttu ülevaatamise jaoks ootele pandud. Määrake ooteloleku koodid väljadel **Pettusest tuleneva ooteloleku kood** ja **Pettusest tuleneva ooteloleku kood**. Kasulik võib olla kahe kordumatu ooteloleku koodi loomine, nii et kasutajad, kes töötavad ooteloleku töölaual, saaksid hõlpsalt filtreerida ja eristada automaatseid ja käsitsi ootele pandud tellimusi.

Et pettuse kontrolli funktsiooni töötaks tõhusalt, peate määrama ka välja **Miinimumskoor**. Igal pettuse kriteeriumil ja reeglil, mis on süsteemis määratletud, on skoor. Kui müügitellimust kontrollitakse pettuse vastete suhtes, siis ühe või mitme vaste leidmisel liidetakse skoorid kokku, et esitada pettuse koguskoor. Kui pettuse koguskoor ületab välja **Miinimumskoor** väärtust, pannakse tellimus automaatselt ootele. Soovi korral saate vahekaardil **Ootel** kasutada teisi skooriga seotud välju, et määratleda meiliaadressi skoor, telefoninumbri skoor, sihtnumbri skoor ja laiendatud sihtnumbri skoor. Kui te ei määra ühelegi staatilise pettuse kriteeriumile skoori, kui määratlete neid lehel **Staatilised pettuse andmed**, annab süsteem neile skoorid, kasutades vaikeskoore, mille määrate vahekaardil **Ootel** lehel **Kõnekeskuse parameetrid**.

Lõpetuseks kasutage välja **Pettuse kommentaar**, et määrada dokumendi tüüp, mida tuleb kasutada, kui kasutaja sisestab kommentaarid, kui ta paneb tellimuse pettuse tõttu ülevaatamise jaoks käsitsi ootele. Enamasti on selle välja väärtuseks **Märkus**.

## <a name="defining-fraud-criteria-and-rules"></a>Pettuse kriteeriumide ja reeglite määratlemine

Süsteem järgib kaht tüüpi pettuse kriteeriume, et määratleda, kas tellimus tuleks pettuse tõttu ülevaatamise ootele panna.

- **Staatilised pettuse andmed** kasutab kindlat väärtust, nt telefoninumber, mis on pandud blokeeritud numbrite loendisse, või e-posti aadress, mis on märgitud lipuga, sest seda on teadaolevalt varem kasutatud petturlike kannete tegemiseks. Staatiliste pettuseandmete seadistamiseks avage **Retail** \> **Kanali häälestus** \> **Kõnekeskuse seadistamine** \> **Pettus** \> **Staatilised pettuse andmed**. Lehel **Staatilised pettuse andmed** saate lisada pettuse kriteeriume käsitsi või andmeimpordi kaudu. Petturlikule teabele lisatakse skoorid. Kui pettuse kontrolli funktsioon on sisse lülitatud, võrreldakse iga sisestatud müügitellimust staatiliste andmetega. Kui andmed leitakse kas kliendi arveldusaadressist või tarneaadressist, mis on seotud tellimuse päisega, või kui andmed leitakse tarneaadressidest, mis on seotud selle müügitellimuse ridadega, liidetakse kõigi kordumatute vastete skoorid kokku ja võrreldakse väärtusega **Miinimumskoor**, et määrata kindlaks, kas tellimus tuleks ootele panna.
- **Pettuse reeglid** koosnevad kasutaja määratletud muutujatest ja tingimustest, mis on nende muutujate jaoks määratletud. Reeglite loomiseks avage **Retail** \> **Kanali häälestus** \> **Kõnekeskuse seadistamine** \> **Pettus** \> **Reeglid**. Pettuse reeglid võimaldavad ettevõttel konfigureerida keerukama reeglikomplekti, mis sisaldab avaldisi **AND** või **OR** mitme tingimuse hindamiseks. Näiteks, kasutaja soovib pettuse tõttu ülevaatamiseks panna kõik tellimused, mis on seotud klientidega, kes kuuluvad kindlasse kliendigruppi ja kes tellisid kindla toote. Sel juhul määratakse tingimused kliendi ja toodete kontrollimiseks lehel **Reeglid** ja kasutatakse tingimust AND. Tellimus pannakse sellisel juhul ootele ainult siis, kui mõlemad tingimused on täidetud ja kui reeglile määratud skoori väärtus, pluss teiste reeglite skoori väärtus, millele tellimus vastab, tõstab tellimuse pettuse koguskoori üle väärtuse **Minimaalne skoor**, mis on määratletud lehel **Kõnekeskuse parameetrid**.

> [!NOTE]
> Mitme reegli või liiga keerukate reeglite kasutamine mõjutab süsteemi jõudlust müügitellimuste edastamisel. Pettuse kontrolli funktsioon ei ole optimeeritud käsitlema suurt hulka staatiliste pettuse andmete kirjeid ja paljusid aktiivseid reegleid. Pidage meeles, et iga reeglit hinnatakse, kui kõnekeskuse kasutaja klõpsab müügitellimuse sisestamise ajal käsku **Edasta**. Reegleid võrreldakse müügitellimuse päise ja tellimuse kõigi ridadega. Mida rohkem on reegleid ja mida keerukamad on nende avaldised, seda rohkem kulub töötlemiseks aega. Kui tellimuses on palju rea kaupu ning palju aktiivseid reegleid ja staatilisi andmekirjeid, võib kõikide andmete ülevaatamise ja kontrollimise ning pettuse skoori arvutamise automaatne protsess jõudlust märkimisväärselt mõjutada. Seda funktsiooni kasutavad organisatsioonid peavad enne reeglimuudatuste või staatiliste pettuse kriteeriumite muudatuste tootmiskeskkonnas juurutamist alati testima ja kinnitama, et tellimuste edastamisel töötlemisele kuluv aeg oleks aktsepteeritav.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Pettuse tõttu ülevaatamisel olevate tellimuste tuvastamine

Kui kõnekeskuse kasutajad esitavad müügitellimuse, siis kui tellimus vastab pettuse kriteeriumidele või reeglitele, ja kui skoor ületab miinimumi, saab kasutaja hoiatusteate, mis ütleb, et tellimus on pandud ootele. Kasutaja saab selle teate sulgeda, sest see on mõeldud ainult teavitamiseks. Kasutajad saavad soovi korral selle teabe edastada kliendile. Ettevõtte peab määrama protokolli, mida kasutajad sellisel juhul järgivad.

Tellimus on salvestatud, kuid sellele on märgitud lipp **Ära töötle**. See lipp aitab tagada, et tellimust ei saa lattu väljastada. Kasutajad saavad iga müügitellimuse korral lipu **Ära töötle** sätet lehel **Üksikasjalik olek** igal hetkel vaadata. Selle lehe saab avada lehtedel **Kõik müügitellimused** ja **Klienditeenindus**. Süsteem uuendab ka tellimuse välja **Üksikasjalik olek** väärtuseks **Pettusest tulenev ootelolek**.

Pettuse tõttu ülevaatamisel olevate tellimuste vaatamiseks ja haldamiseks avage **Retail** \> **Kliendid** \> **Ootelolevad tellimused**. Lehel **Ootelolevad tellimused** valige loendist kirje ja klõpsake nuppu **Ootelolev tellimus**, et näha üksikasjalikumat vaadet, mis sisaldab teavet ooteloleku põhjuse kohta. Kiirkaardil **Pettuse üksikasjad** saate vaadata süstemaatilisi pettuse kriteeriume, mis leiti olevat tellimuse vasted ja millele rakendati skoorid. Kui tellimus pandi käsitsi ootele, saate vaadata üle tellimuse ootele pannud kasutaja kommentaarid vaadates jaotist **Pettusemärkmed** kiirkaardil **Märkused**.

Lisateavet selle kohta, kuidas töötada ootel olevate tellimustega, vt teemast [Ootelolevad tellimused](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds).

