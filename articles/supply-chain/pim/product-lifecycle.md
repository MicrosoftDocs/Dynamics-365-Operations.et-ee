---
title: Toote töötsükli olekute ülevaade
description: Toote elutsükli olek dokumenteerib väljastatud toote või tootevariandi elutsükli oleku.
author: t-benebo
ms.date: 01/06/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: f71ce701adbe60b69b25e41810dda7adeec1d390
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983790"
---
# <a name="product-lifecycle-state-overview"></a>Toote töötsükli olekute ülevaade

[!include [banner](../includes/banner.md)]

Toote elutsükli olek dokumenteerib väljastatud toote või tootevariandi elutsükli oleku. Toote elutsükli olekud määratleb kasutaja, tavaliselt tootejuht või tooteetaloni andmehaldur. Kindel elutsükli olek võib mõjutada konkreetseid äriprotsesse, näiteks koondplaneerimist.

Väljastatud toote või tootevariandi saab seostada toote elutsükli olekuga, mis dokumenteerib, millises elutsükli olekus konkreetne toode või variant praegu on. Saate määratleda mis tahes arvu toote elutsükleid, määrates oleku nime ja kirjelduse. Saate valida ühe elutsükli oleku uute väljastatud toodete vaikeolekuks. Väljastatud tootevariandid pärivad oma toote elutsükli oleku loomise ajal oma väljastatud tooteetalonilt. Väljastatud tooteetaloni elutsükli oleku muutmisel saate värskendada kõik sama algolekuga variandid.  

## <a name="create-a-new-product-lifecycle-state"></a>Toote töötsükli uue oleku loomine

- Uue toote töötsükli oleku loomiseks vaadake teemat [Toote töötsükli uue oleku loomine](tasks/new-product-lifecycle-state.md).

- Toote töötsükli vaikeoleku loomiseks vaadake teemat [Toote töötsükli vaikeoleku loomine](tasks/default-product-lifecycle-state.md).

## <a name="associate-product-lifecycle-states-to-released-products"></a>Toote elutsükli olekute seostamine väljastatud toodetega  

Toote elutsükli oleku seostamiseks väljastatud toodete või tootevariantidega on mitu võimalust.

- Uue väljastatud toote loomisel määratakse sellele automaatselt vaikimisi **Toote elutsükli olek**.
- Toote väljastamisel juriidilisele isikule määratakse sellele automaatselt vaikimisi **Toote elutsükli olek**.
- Tootevariandi väljastamisel juriidilisele isikule määratakse uuele variandile automaatselt selles juriidilises isikus väljasatud tooteetaloniga seostatud **Toote elutsükli olek**.

Toote elutsükli oleku käsitsi värskendamiseks on järgmised võimalused.

- Loendileht **Väljastatud tooted** või **Üksikasjavaade**.
- Loendileht **Väljastatud tootevariandid** või **Üksikasjavaade**.
- Saate leida aegunud tooted või tootevariandid nõudluse põhjal ja seostada need elutsükli olekuga.  

Allpool on lisateave.

- Toote töötsükli oleku seostamiseks väljastatud tooteetaloniga lugege teemat [Toote töötsükli oleku määramine väljastatud tooteetalonile](tasks/product-lifecycle-state-released-product-master.md).

- Toote töötsükli oleku seostamiseks väljastatud tootega lugege teemat [Toote töötsükli oleku määramine väljastatud tooteetalonile](tasks/product-lifecycle-state-released-product.md).

## <a name="impact-on-master-planning"></a>Mõju koondplaneerimisele

Toote elutsükli olekul on ainult üks juhtlipp: **On planeerimiseks aktiivne**. Vaikimisi on selle sätteks kõigi loodud toote elutsükli olekut puhul **Jah**, kuid selle saab muuta sättele **Ei**. Kui valitud on säte **Ei**, on seostatud väljastatud tooted või väljastatud tootevariandid:

- välistatud koondplaneerimisest;
- välistatud koosluse taseme arvutusest.

Täpsema teabe saamiseks selle kohta, kuidas kasutada toote töötsükli olekut toodete välistamiseks koondplaneerimisest ja koosluse taseme arvutustest, lugege teemat [Toote töötsükli oleku loomine toote välistamiseks koondplaneerimisest](tasks/exclude-products-master-planning.md)

> [!NOTE]
> Jõudluse huvides on väga soovitatav seostada kõik aegunud väljastatud tooted või tootevariandid, eriti kui töötate ühekordselt kasutatavate toote konfiguratsioonivariantidega, toote elutsükli olekuga, mis on koondplaneerimise jaoks inaktiveeritud.  

## <a name="default-migration-import-and-export"></a>Migratsiooni, impordi ja ekspordi vaikesätted

Andmeüksused toetavad toote elutsükli olekuid ja elutsükli oleku saab määrata kas väljastatud toote andmeüksuste või väljastatud variandi andmeüksuse kaudu muutuvaks.

## <a name="find-obsolete-products-and-products-variants"></a>Aegunud toodete ja tootevariantide leidmine

Saate käivitada simulatsioonanalüüsi aegunud väljastatud toodete või tootevariantide leidmiseks ning seejärel nende toote elutsükli oleku värskendada. iganenud toodete leidmiseks lugege teemat [Iganenud tootevariantide leidmine ja toote töötsükli oleku määramine](tasks/obsolete-product-variants.md). Teema näitab, kuidas leida iganenud välja antud tooteid või tootevariante ja kuidas seostada toote tööstükli olek iganenud toodetega. See näitab ka, kuidas vaadata simulatsiooni tulemusi ja hinnata, kui palju tooteid ning tootevariante uue toote elutsükli olekuga seostatakse, kui värskendus käivitatakse ilma simulatsioonita.  

Käivitades analüüsi simulatsioonirežiimis, kuvatakse aegununa tuvastatud tooted ja tootevariandid kindlal vormil, kus neid saab hõlpsasti üle vaadata. Analüüs otsib kandeid ja konkreetseid koondandmeid, et tuvastada tooteid, millel puuduvad muutuval perioodil nõudlus ja koondandmed, mis võivad nõudlust põhjustada. Uued väljastatud tooted muutuval perioodil saab analüüsist välja jätta. Kui analüüsi simulatsioon tagastab oodatud tulemuse, saab kasutaja käivitada analüüsi ja määrata uue toote elutsükli oleku kõigile toodetele, mille analüüs tuvastas aegununa.  

> [!NOTE]
> Pange tähele, et kogu analüüs ja kõik värskendused tuleb teha samas juriidilises isikus.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Väljastatud toodete ja tootevariantide valimise ja värskendamise kriteeriumid

Väljastatud toodete ja tootevariantide valimiseks ja värskendamiseks saate kasutada järgmisi kriteeriume.

- Toote või tootevariandi toote elutsükli olek peab erinema uuest soovitud olekust.
- Toode või tootevariant loodi mõni päev tagasi valiku dialoogiboksis sisestatud päevade arvu alusel.
- Toote või tootevariandi puhul ei ole avatud tootetellimusi (= olek < lõpetatud).
- Toote või tootevariandi pole avatud varude kandeid (= väljastamise olek valikult ReservPhysical valikule QuotationIssue või vastuvõtmise olek valikult Registreeritud valikule QuotationReceipt).
- Toote või tootevariandi puhul pole viimaste päevade jooksul ühtki varude kandeid.
- Toote või tootevariandi puhul puudub tulevane nõudlus või tarneprognoos.  
- Toote või tootevariandi puhul pole kauba laovarudele minimaalset varude taset määratud.
- Toote või tootevariandi puhul pole aktiivset fikseeritud koguse kanban-reeglit.  
- Toote või tootevariandi puhul pole teenuse tellimuserida.
- Toote või tootetellimuse puhul pole aktiivseid ega tulevasi müüke või ostutellimuse ridu.
- Toote või tootevarianti ei kasutata koosluses, mis on seostatud planeerimiseks aktiivse toote või tootevariandi puhul mitteaegunud kinnitatud koosluse versiooniga.

## <a name="related-topics"></a>Seotud dokumendid

- [Toote töötsükli uue oleku loomine](tasks/new-product-lifecycle-state.md)
- [Toote töötsükli vaikeoleku loomine](tasks/default-product-lifecycle-state.md)
- [Toote elutsükli oleku määramine väljastatud tooteetalonile](tasks/product-lifecycle-state-released-product-master.md)
- [Toote elutsükli oleku määramine väljastatud tootele](tasks/product-lifecycle-state-released-product.md)
- [Aegunud tootevariantide leidmine ja neile toote elutsükli oleku määramine](tasks/obsolete-product-variants.md)
- [Toote elutsükli oleku loomine toodete välistamiseks koondplaneerimisest](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]