---
title: Varude inventuuri põhjusekoodid
description: Selles teemas kirjeldatakse põhjusekoodide seadistamist ja rakendamist inventuuriülesannete jaoks.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4510ed7033e7c4e5187905906dcbef63f05a130bafcb7d9f19bbb360a7298119
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012087"
---
# <a name="reason-codes-for-inventory-counting"></a>Varude inventuuri põhjusekoodid

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Põhjusekoodide abil saate analüüsida inventuuriprotsessi tulemusi ja protsessi käigus tekkivaid võimalikke lahknevusi. Saate määrata inventuuri tegemise põhjuse, nagu katkine kaubaalus või varude korrigeerimine, mis põhineb varude näidistel. Samal ajal saate kasutada korrigeerimisfunktsiooni, et sisestada vaba kaubavaru korrigeerimiste väärtus sobivale vastaskontole, mis põhineb iga laokorrektsiooni põhjusel.

## <a name="recommendation"></a>Soovitamine

Enne süsteemi häälestamist on soovitatav määratleda põhjusekoodidega töötamise strateegia. Proovige näiteks vastata järgmistele küsimustele.

- Kas põhjusekoodid peaksid ladudes olema kohustuslikud?
- Kas põhjusekoodid peaksid mõningate kaupade jaoks olema kohustuslikud või valikulised?
- Mitu põhjusekoodi te vajate?
- Kas peate korrigeerimiseks valima eelvalimiseks piiratud põhjusekoodide loendi?
- Kuidas peaksid vöötkoodilugejate kasutajad põhjusekoode kasutama? Kas põhjusekoodid peaksid olema eelvalitud, kohustuslikud või mitteredigeeritavad?
- Kas laotöötajad vajavad mobiilse seadme skannerites erinevat põhjusekoodi käitumist? Kui vastus on jah, saate luua rohkem menüükäske ja määrata need erinevatele inimestele.
- Kas põhjusekoodid peaksid juhtima finantsilist vastaskonto sisestamist?

## <a name="turn-on-reason-code-features-in-your-system"></a>Lülitage põhjusekoodi funktsioonid oma süsteemis sisse

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Kui te ei näe kõiki selles teemas kirjeldatud funktsioone süsteemis, peate tõenäoliselt lülitama sisse *vaba kaubavaru sisestamise, kasutades vastaskontode funktsiooniga ühendatud konfigureeritavaid põhjusekoode*. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *sisestage vaba kaubavaru korrigeerimised, kasutades vastaskontodega ühendatud konfigureeritavaid põhjusekoode*

## <a name="set-up-reason-codes"></a>Põhjusekoodide häälestamine

### <a name="set-up-reason-code-policies"></a>Põhjusekoodi poliitikate seadistamine

Saate luua mitu põhjuse koodi poliitikat, et kontrollida, millal ja kuidas inventuuri põhjusekoode rakendatakse. Igal põhjuse koodi poliitikal võib olla üks kahest inventuuri põhjuse koodi tüübist (*Valikuline* või *Kohustuslik*). Inventuuri põhjusekoodi poliitikaid saab kasutada lao või kauba tasemel.

Põhjusekoodi poliitika loomiseks järgige neid samme.

1. Minge **Varude haldus** \> **Seadistus** \> **Varud** \> **Põhjusekoodi poliitikate loendamine**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku poliitika.
1. Seadke uuele poliitikale väli **Nimi**.
1. Väljal **Inventuuri põhjusekoodi tüüp** valige kas *Kohustuslik* või *Valikuline*, et määrata, kas põhjuskoodi valimine peaks olema vabatahtlik või kohustuslik ühes järgmistest varude korrigeerimisprotsessidest.

    - Tsükliline inventuur (mobiilne seade)
    - Punktinventuur (mobiilne seade)
    - Läveinventuur (mobiilne seade)
    - Saabumise korrigeerimine (mobiilne seade)
    - Väljastuse korrigeerimine (mobiilne seade)
    - Inventuuritööleht (rikas klient)
    - Koguse korrigeerimine/võrgupõhine inventuur (rikas klient)

Põhjusepoliitika saate seadistada nii üksikute ladude kui ka toodete jaoks. Toote põhjusekoodi häälestus võib toote lao häälestuse alistada.

> [!NOTE]
> Ladude ja kaupade puhul, mille väli **Loenduspõhjuse koodi poliitika** on seatud väärtusele *Kohustuslik*, ei saa loenduspäevikut täita ja sulgeda enne põhjusekoodi esitamist. Lisateabe jaoks vt järgmist jaotist.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Määrake laodele loendamise põhjuse koodipoliitika

Inventuuri põhjusekoodi poliitika määramiseks laole järgige neid samme.

1. Avage **Varude haldus** \> **Seadistus** \> **Laovarude jaotamine** \> **Laod**.
1. Valige loendipaanil ladu.
1. Valige toimingupaani vahekaardi **Ladu** grupis **Seadistamine** suvand **Põhjusekoodi poliitika loendamine**. Seejärel läbige dialoogiboksis **Määrake inventuuri põhjusekoodi poliitika** üks järgmistest sammudest.

    - Poliitika seadistuse kasutamiseks iga kauba puhul määratlemaks, kas inventuuritöölehed on selle jaoks kohustuslikud, sisestage väärtus puudub (või kustutage olemasolev väärtus).
    - Lao inventuuritöölehtede põhjusekoodide nõudmiseks valige põhjusepoliitika, kus **inventuuri põhjuse koodi tüübi** väli on seatud väärtusele *Kohustuslik*.
    - Kui põhjuse kood on lao töölehtede loendamisel valikuline, valige põhjuspoliitika, kus väli **Loendamise põhjuse koodi tüüp** on seatud *Valikuline*.

### <a name="assign-counting-reason-code-policies-to-products"></a>Määrake toodetele loendamise põhjuse koodipoliitika

Inventuuri põhjusekoodi poliitika määramiseks tootele järgige neid samme.

1. Avage **Tooteteabe haldus** \> **Tooted** \> **Väljastatud tooted**.
1. Valige ruudustikus toode.
1. Valige toimingupaani vahekaardi **Toode** grupis **Seadistamine** suvand **Põhjusekoodi poliitika loendamine**. Seejärel läbige dialoogiboksis **Määrake inventuuri põhjusekoodi poliitika** üks järgmistest sammudest.

    - Poliitika seadistuse kasutamiseks lao puhul määratlemaks, kas inventuuritöölehed on toote jaoks kohustuslikud, sisestage väärtus puudub (või kustutage olemasolev väärtus).
    - Toote inventuuritöölehtede põhjusekoodide nõudmiseks valige põhjusepoliitika, kus **inventuuri põhjuse koodi tüübi** väli on seatud väärtusele *Kohustuslik*. See säte alistab laotaseme põhjusekoodi sätted.
    - Kui põhjuse kood on toote töölehtede loendamisel valikuline, valige põhjuspoliitika, kus väli **Loendamise põhjuse koodi tüüp** on seatud *Valikuline*. See säte alistab laotaseme põhjusekoodi sätted.

### <a name="set-up-counting-reason-codes"></a>Seadistage loendamise põhjuste koodid

Loendamise põhjuste koodide seadistamiseks toimige järgmiselt.

1. Minge **Varude haldus** \> **Seadistus** \> **Varud** \> **Põhjusekoodide loendamine**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.
1. Seadistage uuele reale **inventuuri põhjuse kood** ja **kirjeldus** väljad.
1. Vastaskonto määramiseks sisestage või valige väärtus väljal **Vastaskonto**.

    > [!NOTE]
    > Kui inventuuri põhjuse koodile on määratud vastaskonto, on inventuuritöölehe sisestamisel see inventuuri põhjusekood, sisestatakse väärtus määratud vastaskontole, mitte lao sisestusreeglite vaikekontole.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Seadistage loenduse põhjusekoodi grupid

*Inventuuri põhjusekoodi gruppe* saab kasutada Warehouse Management mobiilirakenduse menüü-üksuste *Korrigeerimine* ja *Reguleerimine välja* välja korrigeerimise osana inventuuri põhjusekoodide loendi piiramiseks. (Lisateavet inventuuri põhjusekoodigruppide kohta vt teemast [Seadistage mobiilse seadme menüü-üksused korrigeerimiseks ja välja reguleerimiseks](#setup-adjustment-in-out) selle teema jaotises hiljem.)

1. Minge **Varude haldus** \> **Seadistus** \> **Varud** \> **Põhjusekoodi gruppide loendamine**.
1. Grupi lisamiseks valige toimingupaanilt suvand **Uus**.
1. Seadistage uuele grupile **inventuuri põhjuse grupp** ja **Grupi kirjeldus** väljad.
1. Valige toimingupaanil nupp **Salvesta**.
1. Jaotises **Üksikasjad** valige tööriistaribal **Uus**, et lisada rida ruudustikule. Seadistage siis uuele reale väli **Inventuuri põhjusekood**. 
1. Korrake eelmist sammu, et määrata vajadusel veel koode. Kui peate grupist koodi eemaldama, valige see ja valige tööriistaribal käsk **Kustuta**.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Põhjusekoodide seadistamine mobiilse seadme menüükäskude jaoks

Põhjusekoode saate konfigureerida järgmiste vaba kaubavaru korrigeerimistüüpide jaoks:

- Tsükliline inventuur
- Punktinventuur
- Läveinventuur
- Saabumise korrigeerimine
- Väljastuse korrigeerimine

Enamasti saate igale asjassepuutuvale mobiilseadme menüü-üksusele määrata järgmise teabe.

- Kas põhjusekood kuvatakse inventuuri ajal mobiilse seadme töötajale.
- Vaikepõhjusekood, mis kuvatakse mobiilse seadme menüükäsus
- Kas kasutaja saab põhjusekoodi redigeerida.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Seadistage inventuurisprotsessi jaoks mobiilseadme menüüelemendid

Mobiilseadme menüüelemendi seadistamiseks inventuuriprotsessiks toimige järgmiselt.

1. Avage **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüükäsud**.
1. Valige loendipaanil vastav menüükäsk või looge uus menüükäsk.
1. Valige toimingupaanil **Tsükliline inventuur**.
1. Väljal **Inventuuri vaikepõhjusekood** määrake vaikimisi põhjusekood, mis tuleks salvestada, kui loendamiseks kasutatakse mobiilseadme menüüelementi.
1. Valige väljal **Kuva inventuuri põhjusekood** üks järgmistest väärtustest.

    - *Rida* – kuvatakse põhjuse kood pärast iga hälbe kirjendamist.
    - *Peida* – põhjusekoodi ei näidata.

1. Määrake **Muuda inventuuri põhjuse koodi** väärtuseks *Jah*, et töötaja saaks põhjuse koodi muuta, kui see loendamise ajal mobiilseadmes kuvatakse. Selleks et vältida töötaja koodi redigeerimist, määrake selle väärtuseks *Ei*.

> [!NOTE]
> Nupu **Tsükliline inventuur** saab lubada igas mobiilse seadme menüükäsus, kus saab teha inventuuri. Näidete hulka kuuluvad menüükäsud punktinventuuride jaoks, kasutaja suunatud töö ja süsteemi suunatud töö.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Seadistage mobiiliseadme menüü-üksused saabumise ja väljastuse korrigeerimiseks

Mobiilseadme menüüelemendi seadistamiseks sisse- või väljareguleerimiseks toimige järgmiselt.

1. Avage **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüükäsud**.
1. Menüü-üksuse loomiseks valige toimingupaanilt suvand **Uus**.
1. Seadistage uuele menüükäsule **mobiilikauba nimi** ja **pealkirja** väljad.
1. Seadke **Režiim** välja väärtuseks *Töö*.
1. Valige suvandi **Kasuta olemasolevat tööd** sätteks *Ei*.
1. Väljal **Töö loomise protsess** valige *Saabumise korrigeerimine* või *Väljastuse korrigeerimine*.
1. Määrake kiirkaardil **Üldine** järgmised väljad. (Kõik need väljad lisatakse, kui valite **Töö loomise protsessi** väljal *Saabumise korrigeermine* või *Väljastuse korrigeerimine*.)

    - **Kasutage protsessi juhendit** – kui loote *Väljastuse korrigeerimine* protsessi, seadke selle valiku väärtuseks *Jah*. Kui loote *väljaste korrigeerimise* protsessi, on selle valiku väärtuseks alati määratud *Jah*.
    - **Inventuuri vaikepõhjusekood** - määrake vaikimisi põhjusekood, mis tuleks salvestada, kui loendamiseks kasutatakse mobiilseadme menüüelementi.
    - **Kuva inventuuri põhjusekood** - valige üks järgmistest väärtustest.

        - *Rida* – kuvatakse põhjuse kood pärast iga hälbe kirjendamist.
        - *Peida* – põhjusekoodi ei näidata.

    - **Muuda inventuuri põhjuse koodi** - määrake väärtuseks *Jah*, et töötaja saaks põhjuse koodi muuta, kui see loendamise ajal mobiilseadmes kuvatakse. Selleks et vältida töötaja koodi redigeerimist, määrake selle väärtuseks *Ei*.
    - **Inventuuri põhjusekoodi grupp** – valige põhjuse koodigrupp, kui soovite piirata töötajatele esitatud valikute loendit. Põhjusekoodigruppide seadistamisteabe saamiseks vt käesoleva teema varasemat jaotist [Inventuuri põhjusekoodide gruppide seadistamine](#reason-groups). 

> [!NOTE]
> Kui määrate inventuuri põhjusekoodi grupi menüü-üksustesse *Saadetise korrigeerimine* ja *Väljastuse korrigeerimine*, kus suvandi **Kasuta protsessijuhendit** väärtuseks on määratud *Jah*, saate Warehouse Management mobiilirakenduses töötlemise osana saada inventuuri põhjusekoodide piiratud loendi.
>
> **Kasuta protsessi juhendit** suvand võib aidata ka vältida suurte korrigeerimiskoguste toimumist ekslikult. (Näiteks võib töötaja kogemata skannida kaubakoodi vöötkoodi koguse väärtuse asemel.) Selle funktsiooni häälestamiseks seadistage **Kasuta protsessi juhendit** valiku väärtuseks *Jah* iga asjakohase menüükäsu puhul. Seejärel minge **Laohalduse \> Seadistamine \>Töötaja** juurde ja seadistage igale asjassepuutuvale laotöötajale **korrigeerimise koguse piirangu** väli, et määrata maksimaalne korrigeerimiskogus, mille töötaja saab registreerida.

## <a name="processing-that-uses-counting-reason-codes"></a>Töötlemine, mis kasutab inventuuri põhjusekoode

Kui töötajad kasutavad Warehouse Management mobiilirakendust, salvestatakse põhjusekoodid. Kui inventuuri kinnitusprotsessi ei ole määratletud, kasutatakse salvestatud põhjusekoode kohe pärast seda inventuuritöölehe sisestuse osana.

### <a name="cycle-count-approvals"></a>Tsüklilise inventuuri kinnitused

Enne inventuuri kinnitamist saab töötaja muuta selle inventuuriga seotud põhjusekoodi. Inventuuri kinnitamisel sisestatakse põhjusekood inventuuritöölehe ridadele.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Tsüklilise inventuuri kinnituste põhjusekoodide muutmine

Tsüklite arvu kinnitamise muutmiseks toimige järgmiselt.

1. Minge **Laohaldus** \> **Tsükliline inventuur** \> **Ülevaatuse ootel tsüklilise inventuuri töö**.
1. Valige ruudustikus tsüklite loendus.
1. Toiminguriba vahekaardil **Töö** valige suvand **Tsükliline inventuur**. Siis valige väljal **Põhjuse kood** uus põhjuse kood.

Põhjusekoodid lisatakse töölehe ridadele inventuuritöölehtedel tüübiga *Inventuuritööleht*.

1. Avage **Laohaldus** \> **Töölehe sisestused** \> **Kauba inventuur** \> **Inventuur**.
2. Valige inventuuritöölehe rea üksikasjade väljal **Inventuuri põhjuse kood** praegusele olukorrale sobiv põhjusekood.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Vaadake inventuuri ajalukku salvestatud põhjusekoode

Inventuuri ajaloos salvestatud põhjusekoodide vaatamiseks järgige neid samme.

1. Avage **Laohaldus** \> **Päringud ja aruanded** \> **Inventuuri ajalugu**.
1. Valige loendipaanil kaubaloenduse kirje.
1. Väljal **Inventuuri põhjuse kood** vaadake inventuuriajalugu, mis on kirjendatud põhjuse koodi kaudu.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Kasuta koguse korrigeerimiseks või võrgus inventuuriks põhjusekoode

Koguse korrigeerimiseks või veebipõhiseks inventuuriks põhjuse koodi kasutamiseks järgige neid samme.

1. Avage **Laohaldus \> Päringud ja aruanded \> Vabade kaubavarude loend**.
1. Valige toimingupaanilt **Koguse korrigeerimine**.
1. Valige **Koguse korrigeerimine** ja seejärel väljal **Inventuuri põhjusekood** valige põhjusekood.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
