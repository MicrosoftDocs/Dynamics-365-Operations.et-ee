---
title: "Toote töötsükli olek"
description: "Toote elutsükli olek dokumenteerib väljastatud toote või tootevariandi elutsükli oleku."
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: conradv
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 33130a4061f22335aeeffa69c478b693604393a9
ms.openlocfilehash: a57f306ba02c5758c39c4bd29d9a4fa0d7efbcd3
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2017

---

# <a name="product-lifecycle-state"></a>Toote töötsükli olek 

[!include[banner](../includes/banner.md)]


Toote elutsükli olek dokumenteerib väljastatud toote või tootevariandi elutsükli oleku. Toote elutsükli olekud määratleb kasutaja, tavaliselt tootejuht või tooteetaloni andmehaldur. Kindel elutsükli olek võib mõjutada konkreetseid äriprotsesse, näiteks koondplaneerimist.   
 
Väljastatud toote või tootevariandi saab seostada toote elutsükli olekuga, mis dokumenteerib, millises elutsükli olekus konkreetne toode või variant praegu on. Saate määratleda mis tahes arvu toote elutsükleid, määrates oleku nime ja kirjelduse. Saate valida ühe elutsükli oleku uute väljastatud toodete vaikeolekuks. Väljastatud tootevariandid pärivad oma toote elutsükli oleku loomise ajal oma väljastatud tooteetalonilt. Väljastatud tooteetaloni elutsükli oleku muutmisel saate värskendada kõik sama algolekuga variandid.  

## <a name="create-a-new-product-lifecycle-state"></a>Uue toote elutsükli oleku loomine 
 
- Uue toote elutsükli oleku loomiseks esitage või lugege tegevusejuhist **Uue toote elutsükli oleku loomine**. 

-  Toote elutsükli vaikeoleku loomiseks esitage või lugege tegevusejuhist **Toote elutsükli vaikeoleku loomine**.   

## <a name="associate-product-lifecycle-states-to-released-products"></a>Toote elutsükli olekute seostamine väljastatud toodetega  

Toote elutsükli oleku seostamiseks väljastatud toodete või tootevariantidega on mitu võimalust.

-  Uue väljastatud toote loomisel määratakse sellele automaatselt vaikimisi **Toote elutsükli olek**. 
-  Toote väljastamisel juriidilisele isikule määratakse sellele automaatselt vaikimisi **Toote elutsükli olek**. 
-  Tootevariandi väljastamisel juriidilisele isikule määratakse uuele variandile automaatselt selles juriidilises isikus väljasatud tooteetaloniga seostatud **Toote elutsükli olek**. 

Toote elutsükli oleku käsitsi värskendamiseks on järgmised võimalused. 

-    Loendileht **Väljastatud tooted** või **Üksikasjavaade**. 
-  Loendileht **Väljastatud tootevariandid** või **Üksikasjavaade**. 
-  Saate leida aegunud tooted või tootevariandid nõudluse põhjal ja seostada need elutsükli olekuga.  

Üksikasjalikku teavet toote elutsükli olekute seostaimseks esitage või lugege kaht järgmist tegevusejuhist.

-  Toote elutsükli oleku seostamiseks väljastatud tooteetaloniga esitage või lugege tegevusejuhist **Toote elutsükli oleku määramine väljastatud tooteetalonile**. 

-  Toote elutsükli oleku seostamiseks väljastatud tootega esitage või lugege tegevusejuhist **Toote elutsükli oleku määramine väljastatud tootele**. 

## <a name="impact-on-master-planning"></a>Mõju koondplaneerimisele 

Toote elutsükli olekul on ainult üks juhtlipp: **On planeerimiseks aktiivne**. Vaikimisi on selle sätteks kõigi loodud toote elutsükli olekut puhul **Jah**, kuid selle saab muuta sättele **Ei**. Kui valitud on säte **Ei**, on seostatud väljastatud tooted või väljastatud tootevariandid: 

-  välistatud koondplaneerimisest; 
-  välistatud koosluse taseme arvutusest. 

Täpsema teabe saamiseks selle kohta, kuidas kasutada toote elutsükli olekut toodete välistamiseks koondplaneerimisest ja koosluse taseme arvutustest, esitage või lugege tegevusejuhist **Toote elutsükli oleku loomine toote välistamiseks koondplaneerimisest**.

> [!NOTE]
> Jõudluse huvides on väga soovitatav seostada kõik aegunud väljastatud tooted või tootevariandid, eriti kui töötate ühekordselt kasutatavate toote konfiguratsioonivariantidega, toote elutsükli olekuga, mis on koondplaneerimise jaoks inaktiveeritud.  
 
## <a name="default-migration-import-and-export"></a>Migratsiooni, impordi ja ekspordi vaikesätted 

Andmeüksused ei toeta toote elutsükli olekuid ja elutsükli olekut ei saa määrata väljastatud toote andmeüksuste kaudu muutuvaks.

-  Varasematest väljalasetest migreerimisel on kõigi toodete ja tootevariantide elutsükli olek tühi.  
-  Väljastatud toodete importimisel andmeüksuse kaudu rakendatakse loomisel elutsükli vaikeolek.  
-  Väljastatud tootevariantide importimisel andmeüksuse kaudu imporditakse väljastatud tooteetaloni toote elutsükli olek.   
 
## <a name="find-obsolete-products-and-products-variants"></a>Aegunud toodete ja tootevariantide leidmine 
 
Saate käivitada simulatsioonanalüüsi aegunud väljastatud toodete või tootevariantide leidmiseks ning seejärel nende toote elutsükli oleku värskendada. Aegunud toodete leidmiseks esitage ja lugege tegevusejuhist **Aegunud tootevariantide leidmine ja toote elutsükli oleku määramine**. Tegevusejuhis näitab, kuidas leida aegunud väljastatud tooteid või tootevariante ja kuidas seostada toote elutsükli olek aegunud toodetega. See näitab ka, kuidas vaadata simulatsiooni tulemusi ja hinnata, kui palju tooteid ning tootevariante uue toote elutsükli olekuga seostatakse, kui värskendus käivitatakse ilma simulatsioonita.  
 
Käivitades analüüsi simulatsioonirežiimis, kuvatakse aegununa tuvastatud tooted ja tootevariandid kindlal vormil, kus neid saab hõlpsasti üle vaadata. Analüüs otsib kandeid ja konkreetseid koondandmeid, et tuvastada tooteid, millel puuduvad muutuval perioodil nõudlus ja koondandmed, mis võivad nõudlust põhjustada. Uued väljastatud tooted muutuval perioodil saab analüüsist välja jätta. Kui analüüsi simulatsioon tagastab oodatud tulemuse, saab kasutaja käivitada analüüsi ja määrata uue toote elutsükli oleku kõigile toodetele, mille analüüs tuvastas aegununa.  
 
> [!NOTE]
> Pange tähele, et kogu analüüs ja kõik värskendused tuleb teha samas juriidilises isikus.  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Väljastatud toodete ja tootevariantide valimise ja värskendamise kriteeriumid 
 
Väljastatud toodete ja tootevariantide valimiseks ja värskendamiseks saate kasutada järgmisi kriteeriume. 

-    Toote või tootevariandi toote elutsükli olek peab erinema uuest soovitud olekust. 
-  Toode või tootevariant loodi mõni päev tagasi valiku dialoogiboksis sisestatud päevade arvu alusel. 
-  Toote või tootevariandi puhul ei ole avatud tootetellimusi (= olek < lõpetatud). 
-  Toote või tootevariandi pole avatud varude kandeid (= väljastamise olek valikult ReservPhysical valikule QuotationIssue või vastuvõtmise olek valikult Registreeritud valikule QuotationReceipt). 
-  Toote või tootevariandi puhul pole viimaste päevade jooksul ühtki varude kandeid. 
-  Toote või tootevariandi puhul puudub tulevane nõudlus või tarneprognoos.  
-  Toote või tootevariandi puhul pole kauba laovarudele minimaalset varude taset määratud. 
-  Toote või tootevariandi puhul pole aktiivset fikseeritud koguse kanban-reeglit.  
-  Toote või tootevariandi puhul pole teenuse tellimuserida. 
-  Toote või tootetellimuse puhul pole aktiivseid ega tulevasi müüke või ostutellimuse ridu. 
-  Toote või tootevarianti ei kasutata koosluses, mis on seostatud planeerimiseks aktiivse toote või tootevariandi puhul mitteaegunud kinnitatud koosluse versiooniga.

## <a name="related-topics"></a>Seotud dokumendid

-  Uue toote elutsükli oleku loomine
-  Uue toote elutsükli vaikeoleku loomine
-  Toote elutsükli oleku määramine väljastatud tooteetalonile
-  Toote elutsükli oleku määramine väljastatud tootele
-  Aegunud tootevariantide leidmine ja neile toote elutsükli oleku määramine
-  Toote elutsükli oleku loomine toodete välistamiseks koondplaneerimisest

