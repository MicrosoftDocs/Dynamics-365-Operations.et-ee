---
title: "Aastalõpu sulgemine"
description: "See teema kirjeldab nõutavat seadistust ja juhiseid pearaamatu aastalõpu sulgemise protsessi käivitamiseks."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 50a6a23febc725eb05d30d5db4f97ca699607461
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="year-end-close"></a>Aastalõpu sulgemine

[!include[banner](../includes/banner.md)]


See teema kirjeldab nõutavat seadistust ja juhiseid pearaamatu aastalõpu sulgemise protsessi käivitamiseks. 

Rahandusaasta lõpus peate käivitama aastalõpu sulgemisprotsessi algsaldode ülekandmiseks uude aastasse. Enamik organisatsioone käivitavad aastalõpu sulgemise protsessi mitu korda. Esimene kord tuleks saldod uude finantsaastasse teisaldada. Aastalõpu sulgemise saab seejärel uuesti käivitada nii palju kordi, kui on vaja, et teisaldada saldod kirjete reguleerimisest uude finantsaastasse. 

Aastalõpu sulgemise protsessi käigus on loodud kaks võimalikku kannete tüüpi. Avamiskanne luuakse alati ja seda kasutatakse uues finantsaastas algsaldode loomiseks. Avamiskanne näitab uue finantsaasta bilansi pearaamatukonto saldosid ja jaotamata kasumi pearaamatukontol olevate kasumi ja kahjumi pearaamatukonto saldodest pärinevaid saldosid. Sulgemiskanne luuakse valikuliselt, et tuua kasumi- ja kahjumikontode saldod suletavas finantsaastas alla nullini.

## <a name="prepare-to-run-the-year-end-close"></a>Aastalõpu sulgemise käitamiseks ettevalmistamine
Enne aastalõpu sulgemisprotsessi käitamist kinnitage sätted järgmisesse kohta. 

**Põhikonto** lehel

-   Kinnitage, et **Põhikonto tüüp** on iga põhikonto jaoks õigesti määratletud. Põhikonto tüüpi kasutatakse määramaks, kas põhikonto saldo tuuakse edasi algsaldona või suletakse avamiskandes jaotamata kasumisse.
-   Välja **Avamiskonto** saab kasutada aastalõpu sulgemise käigus põhikonto saldo üleviimiseks uuele põhikontole. Uus põhikonto sisestatakse väljale **Avamiskonto**. Tavaliselt kasutatakse seda bilansi põhikontode jaoks, kui põhikonto on inaktiveeritud ja uut põhikontot kasutatakse uue finantsaasta jaoks.

Lehel **Pearaamatu parameetrid** valikus **Finantsaasta sulgemine** toimige järgmiselt.

-   Valikut **Kustuta aasta lõpetamise kanded ülekandmisel** kasutatakse määramiseks, kas süsteemi loodud avamiskanne eelmisest aastalõpu sulgemisest tuleks kustutada, kui aastalõpu sulgemine käivitatakse uuesti. Kui see valik on seatud olekusse **Jah**, kustutatakse eelmine avamiskanne ja uus avamiskanne luuakse praeguste saldode põhjal. Kui see valik on seatud olekusse **Ei**, püsib eelmine avamiskanne ja luuakse täiendav avamiskanne, et teisaldada saldod edasi pärast eelmist aastalõpu sulgemist sisestatud kannete reguleerimist.
-   Valikut **Loo ülekande ajal sulgemiskanded** kasutatakse sulgemiskannete loomiseks suletaval finantsaastal, et viia kasumi- ja kahjumikontode saldod nulli. Kui see valik on seatud olekusse **Jah**, luuakse nii avamis- kui ka sulgemiskanne. Kui see valik on seatud olekusse **Ei**, luuakse järgmisel finantsaastal saldode üleviimiseks ainult avamiskanne. Kasumi- ja kahjumikonto saldod püsivad finantsaasta lõpus.
-   Valik **Rahandusaasta oleku määramine püsivalt suletuks** kasutatakse finantsaasta seadmiseks püsivalt suletud olekusse. Kasutage seda sätet ettevaatlikult, kuna kõiki püsivalt suletud olekuga perioode ei saa uuesti avada, ennetades korrigeerimiste sisestamist finantsaastasse. Selle valiku olekuks tasub määrata **Ei**.
-   Valikut **Kande number peab olema täidetud** kasutatakse määratlemiseks, kas kande number on aastalõpu sulgemisprotsessi käitamisel kohustuslik. On hea tava nõuda kande numbrit, et avamiskannet hõlpsasti tuvastada.

Lehel **Rahanduskalender** toimige järgmiselt.

-   Järgmine finantsaasta peab eksisteerima enne aastalõpu sulgemise käitamist. Järgmine finantsaasta on kohustuslik, et luua avamisperioodil algsaldod.

Lehel **Pearaamatu kalender** toimige järgmiselt.

-   Valikuline: iga suletavat finantsaasta rahandusaastat saab määrata olekusse **Ootel**, et takistada uute kannete sisestamist. Korrigeerivate sisestuste tuvastamisel saab ooteloleku perioodid korrigeerivate sisestuste sisestamiseks taasavada isegi siis, kui aastalõpu sulgemisprotsess on juba käivitatud.

## <a name="define-year-end-close-templates"></a>Aastalõpu sulgemismallide määratlemine
Pärast süsteemi konfigureerimist saab käivitada aastalõpu sulgemisprotsessi. Lehel **Aastalõpu sulgemine** saab määratleda malli selliste juriidiliste isikute grupile, mille jaoks aastalõpu sulgemisprotsess käivitatakse. Malli taaskasutatakse igal aastalõpu sulgemisel, kuid seda saab muuta, kui teie organisatsioon muutub. 

Esmalt määratlege malli jaoks **Grupi nimi** ja valige rahanduskalender. Grupi nimi peaks identifitseerima lisatud juriidiliste isikute gruppi.  Näiteks saab mallid seadistada geograafia põhjal nii, et Põhja-Ameerika, EMEA ja APAC juriidiliste isikute jaoks on loodud eraldi grupid. 

Järgmisena saab mallile lisada juriidilised isikud. Juriidilisi isikute lisamiseks saate valida organisatsioonihierarhia või valida juriidilised isikud. Organisatsioonihierarhia valimisel lisatakse malli ainult hierarhiasisesed juriidilised isikud, kes kasutavad valitud rahanduskalendrit. Kui kasutate malli lisamiseks juriidilisi isikuid, saab lisada ainult sama rahanduskalendriga juriidilisi isikuid. Sama rahanduskalender on vajalik, kuna aastalõpu sulgemine käivitatakse finantsaasta valimisega, mis võib varieeruda olenevalt kalendrist. 

Pärast juriidiliste isikute lisamist määratlege iga juriidilise isiku jaoks kinnipeetud tulude põhikontod. Välja **Viimase rahandusaasta sulgemise kuupäev** värskendatakse iga kord, kui juriidilise isiku jaoks käivitatakse aastalõpu sulgemine. 

Vahekaarti **Finantsdimensioon** kasutatakse määratlemiseks, milliseid finantsdimensioone avamiskandel kasutatakse. Pange tähele, et määratletavad sätted on asjakohased ainult ruudustikus **Juriidilised isikud** valitud juriidilisele isikule. Korrake seadistust iga ruudustikus oleva juriidilise isiku jaoks. 

Valikut **Bilansi dimensioonide ülekandmine** kasutatakse määratlemiseks, kas bilansikontodele sisestatud kannetel olevaid finantsdimensioone tuleks säilitada avamiskandes. Selle valiku olekuks tasub seada **Jah**. Valikut **Kasumi ja kahjumi dimensioonide ülekandmine** kasutatakse määratlemiseks, millised kasumi- ja kahjumikontole sisestatud finantsdimensioonid viiakse üle jaotamata kasumi põhikontole. Esmalt tuvastage valitud juriidilisele isikule asjakohased finantsdimensioonid. See peaks hõlmama kõiki finantsdimensioone, mille suhtes on aasta jooksul sisestatud, isegi kui finantsdimensioon ei ole osa aktiivsest kontostruktuurist. Järgmisena määratlege iga dimensioon kui **Sule üksik** või **Sule kõik**.  Vaikesäte on **Sule kõik**, mis säilitab algsed finantsdimensiooni väärtused sisestatud kannetest ja kasutab neid jaotamata kasumi konto jaoks avamissaldode loomiseks. Eraldi jaotamata kasumi algsaldod luuakse iga unikaalse finantsdimensiooni väärtuste unikaalse kombinatsiooni puhul. Valiku **Sule üksik** tegemisel võetakse kõik selle finantsdimensiooniga sisestatud kanded kokku jaotamata kasumi algsaldosse valiku **Sule üksik** väljale sisestatud dimensiooniväärtuse puhul. Näiteks eeldame, et kõik finantsaasta kanded sisestati põhikonto struktuuriga – osakond. Malli osakonna finantsdimensioonis tehakse valik **Sule üksik** ja sisestatakse väärtus 100. Kui kõik osakondadesse 200, 300 ja 400 sisestatud kanded on 100 000 dollarit, luuakse jaotamata kasumi jaoks üks algsaldo – 100. Kui teete valiku **Sule üksik** ja jätate finantsdimensiooni väärtuse tühjaks, sisestatakse kõik kanded jaotamata kasumisse nii, et dimensiooni väärtus on tühi. 

Aastalõpu sulgemise protsess ei järgi kontostruktuure. Seda selle tõttu, et kontostruktuurid võivad muutuda finantsaasta jooksul ja nende muudatuste tõttu pole võimalik tuvastada asjakohast kontot.  Avamiskannete loomisel tuuakse saldod edasi finantsdimensioonidega, nagu on määratletud aastalõpu sulgemise mallis. Algsaldo kirjed võivad hõlmata praeguses kontostruktuuris ja segmendikombinatsioonides mittesisalduvaid finantsdimensioone, mis ei kehti enam praeguses kontostruktuuris. Kui teie organisatsioon soovib jaotamata kasumi algsaldo puhul finantsdimensiooni välja arvata, seadke finantsdimensioon valikule **Sule üksik** ja jätke dimensiooni väärtus tühjaks.

## <a name="run-the-year-end-close-process"></a>Aastalõpu sulgemisprotsessi käivitamine
Pärast aastalõpu sulgemismallide loomist käivitatakse aastalõpu sulgemisprotsess, valides tegumiribal suvandi **Käivita finantsaasta**. Valige mallilt kõik juriidilised isikud või nende alamkogum, mille puhul aastalõpu sulgemine käivitada. Finantsaastas esimest korda aastalõpu sulgemise käivitamisel valite tõenäoliselt kõik juriidilised isikud, et luua kõikide juriidiliste isikute jaoks algsaldod. Kui käivitate uuesti aastalõpu sulgemise, võite valida protsessi käivitamise ainult juriidilistele isikutele, kelle jaoks korrigeerivad kirjed sisestati. 

Valige finantsaasta, mille suhtes sooviksite käivitada aastalõpu sulgemisprotsessi. Kui finantsdimensiooni viimase perioodi kohta on olemas rohkem kui üks sulgemisperiood, muutub väli **Perioodi nimi** kättesaadavaks, et saaksite valida, millisesse sulgemisperioodi sulgemiskanne sisestada, kui seadistus määratletakse sulgemiskande loomiseks. 

Sisestage kandenumber, mis ei pruugi sõltuvalt pearaamatu parameetrite seadistusest olla vajalik. Sama kandenumbrit kasutatakse kõikide aastalõpu sulgemisprotsessi jaoks valitud juriidiliste isikute puhul. Kandenumbrit ei looda numbriseeriat kasutades. Kandenumber tuleks sisestada siis, kui see pole kohustuslik. Kandenumbri sisestamine muudab lihtsaks avamiskande leidmise uuel finantsaastal. Kui kandenumbrit ei sisestata, on kanne avamiskande puhul tühi. 

Kui sooviksite valitud finantsaasta puhul varasema aasta lõpu sulgemise ümber pöörata, seadke valik **Eelmise sulgemise tagasivõtmine** olekusse **Jah**. Aastalõpu sulgemine pööratakse ümber, kuid protsessi saab igal ajal uuesti käivitada. Kui pöörate aastalõpu sulgemise ümber, siis pole valik **Viimase rahandusaasta sulgemise kuupäev** enam saadaval. 

Aastalõpu sulgemise protsess läheb vaikimisi pakktöötlusrežiimi. Mõistlik on käivitada protsess pakktöötlusrežiimis, et lubada kasutajal naasta teiste tegevuste juurde. Pärast aastalõpu sulgemisprotsessi lõpuleviimist värskendatakse valikut **Viimase rahandusaasta sulgemise kuupäev**.

Lisateabe saamiseks vaadake teemat [Pearaamatu sulgemine perioodi lõpus](close-general-ledger-at-period-end.md).




