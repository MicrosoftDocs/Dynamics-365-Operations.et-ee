---
title: Ostutellimuste loomine
description: Selles artiklis kirjeldatakse protsessi ja valikuid ostutellimuse käsitsi koostamisel.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16e6170bdc8f0adcefbe310fcbf61c06aa68f02d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207967"
---
# <a name="create-purchase-orders"></a>Ostutellimuste loomine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse protsessi ja valikuid ostutellimuse käsitsi koostamisel.

Kui ostutellimuse loote, määratakse ostutellimuse päises kogu tellimuse üldine teave ja seejärel saate ostutellimuse ridu lisada. Selles artiklis kirjeldatakse mõningaid kõige sagedamini kasutatavaid valikuid.  

Saate koostada ostutellimusi ka teiselt ostutellimuse dokumendilt või müügitellimuselt ridu kopeerides. Sel juhul võite muuta varude märgi vastupidiseks, nagu muudaksite vastupidiseks arvel oleva märgi kreediti näitamiseks.  

Kuigi ostutellimusi saab käsitsi luua, luuakse need tavaliselt teistest protsessidest. Tellimusi saab automaatselt luua muude dokumentide (nt taotluste) põhjal. Teine võimalus on luua need koondplaneerimise protsessi käigus plaanitud ostutellimuste kaudu. Kui kasutate ostulepinguid, saab ostutellimused luua toiminguga **Väljalaskeorder**. Ostutellimuse automaatseks loomiseks on ka paremaid meetodeid. Näiteks saab tellimusi koostada, kui kasutate otsetarnet või kontsernisiseseid tellimusahelaid.

## <a name="creating-a-purchase-order-header"></a>Ostutellimuse päise loomine
Kui loote uue ostutellimuse, kuvatakse dialoogiboks, kuhu saate sisestada ostutellimuse päise jaoks kõige üldisemat teavet. Kui klõpsate dialoogiboksi sulgemiseks valikut **OK**, luuakse tellimus ja saate siis päises lisateavet täpsustada.  

Esimene asi, mida ostutellimuse loomisel peab arvestama, on tellimuse tüüp. Kõige sagedamini kasutatakse tüüpi **Ostutellimus**. Kuid kui on vajalik kreeditarve, võite kasutada tüüpi **Tagastatud tellimus**.  

Peate määrama hankija väljal **Hankija konto**. Selle välja puhul võite otsida kontot või hankija nime. Kui hankija tarnib mitmest kohast, kuid kasutab ühte arve kontot, võite valida selle arvekonto väljalt **Arve konto** ja kasutada seda siis erinevate hankija kontodega. Kui peate looma ostutellimuse toodetele, mida korduvalt ei tellita, võite kasutada valikut **Ühekordne hankija**. Selle valikuga luuakse automaatselt uus hankija konto, mis märgitakse ühekordseks kontoks, et toetada hilisemat ühekordsete kontode eemaldamise protsessi moodulis **Ostureskontro**. Kui valite hankija konto, pärivad paljud ostutellimuse päise väljad vaikeväärtused hankija kontoga seotud teabest. Näiteks kopeeritakse vaiketarnekoht ja ladu hankija andmetest. Kuid need vaikeväärtused saab alistada, kui ost on mõeldud teise koha jaoks.  

Kui hankija on andnud tellimusele viitenumbri, saate salvestada selle teabe väljale **Hankija viide**. Tagastatud tellimuste puhul tuleb määrata väärtus väljal **RMA** tagastamise töötlemiseks hankija volitusele viitamiseks.  

Kui tellimusega on seotud ostuleping, tuleb määrata see teave väljal **Ostuleping**.  

Ostutellimuse päises on ka teave tasude kohta, mis kehtivad eraldi ridade asemel tervele tellimusele. Tellimusele saab automaatselt tasusid lisada, kui hankijale või hankija tasugrupile on seadistatud automaatsed tasud. Tellimuse päisesse saab ka käsitsi tasusid lisada, klõpsates tegumiribal valikut **Tasude haldamine**.

## <a name="adding-purchase-order-lines"></a>Ostutellimuse ridade lisamine
Ostutellimused võivad olla füüsiliste toodete või teenuste kohta. Laomudeligrupi seadistus määrab, kas konkreetne kaubakood kehtib tootele või teenusele. Tavaliselt määratletakse ostetav kaup kaubakoodiga. Kuid kui tellimus on toodete või teenuste kohta, mida otseselt tarbitakse, võite määratleda kauba ka hankekategooria abil.  

Ostutellimuse ridadel on palju välju, kuid paljudel neist väljadest on vaikeväärtus või väärtus, mis pärineb tellimuse päisest. Toote või teenuse valimisel määratakse lisaväljad. Need väljad, mis määratakse kõige sagedamini käsitsi, hõlmavad kaubakoodi, koguse ja soovitud tarnekuupäeva välju. Teave ühiku hinna ja allahindluste kohta on samuti väga tähtis, kuid nende väljade väärtused määratakse sageli kaubanduslepete või ostulepingutega.  

Toote valimisel saab otsida kaubakoodi asemel toote nime või selle osa. Kui tootel on mitu varianti (nt erinevaid suurusi), näete saadaolevate variantide ülevaadet, kasutades funktsiooni **Lisa ridu** või kasutades otsingut, mis on saadaval väljal **Variandi number**.  

Sageli tuleb määrata igal ostutellimuse real valitud kaubale mitu dimensiooni. Määratavad dimensioonid sõltuvad tooteetaloni definitsioonile määratud dimensioonigruppidest. Näiteks tuleb sageli määrata laoala ja ladu, et näidata asukohta, kuhu toode tuleks tarnida. Tootevariandid saab tähistada variandi numbriga või sisestades vähemalt ühe tootedimensiooni väärtuse (nt värv, suurus, konfiguratsioon või stiil). Jälgimisdimensioonid (nt partii ja seerianumber) võimaldavad iga varude partiid kordumatult tuvastada. Kui olete tellimuse koostanud, saate jäädvustada tellimusele dimensiooniväärtused, kasutades toimingut **Registreerimine**. Näiteks olete tellinud kaupa koguses viis ühikut. Hiljem registreerite, et kolm nendest ühikutest on mustad ja kaks sinised. Selline lähenemine on alternatiiv dimensiooniteabe salvestamisele saabumise registreerimise ajal.  

Saate kontrollida ladustatud toodete laokannete oleku üksikasju. Näiteks võib olla vaja kontrollida vaba kaubavaru selleks, et aidata teil otsustada, kui palju tellida. Teise võimalusena võite vaadata tellitud koguse varude olekut, et näha, kas sissetuleva kauba saabumine on registreeritud.  

Ostutellimuse real, mida kasutatakse toote tagastamiseks hankijale, on negatiivne kogus. Konkreetse partii saab valida toiminguga **Reserveerimine**.  

Mõnikord võib olla vaja tellitud kogust jagada, et selle erinevaid osi saaks tarnida erinevatel kuupäevadel. Need tarned saab seadistada toiminguga **Tarnegraafik**, mis on saadaval menüüs **Ostutellimuse rida** vaates **Read**.  

Tasusid saab ostutellimuse ridadele automaatselt lisada, kui hankijale või hankija tasugrupile ja kaubale või kauba tasugrupile on seadistatud automaatsed tasud. Kuid tavaliselt lisatakse tasud käsitsi tellimuse rea tasandil. Tasu lisamiseks avage leht **Tasude haldamine**, kasutades toimingut **Tasude haldamine** menüüs **Finantsid** vaates **Read**. Otse tellimuse rea tasandil tasu lisamise eelis on see, et tasu saab eraldada laokuluna. Tasukoodide seadistamiseks toote hinna arvestamiseks kasutage debiteerimisvalikut **Kaup**. Seda tüüpi tasud tuleb enne tellimuse kinnitamist ostutellimuse päisest ridadele eraldada. Näiteks võib olla vaja eraldada tasud igal real oleva koguse põhjal. Tasukategooria mõjutab ka seda, kuidas tasusid arvestatakse. Näiteks fikseeritud tasud näitavad fikseeritud summat ja tasuprotsent arvutatakse tellimuse rea netosumma protsendina. Ostutellimused saab määrata koormale ja koorma hulka võib kuuluda eeldatavate transpordikulude prognoos. Selle kulu saab eraldada koormalt tagasi ostutellimuse ridadele.

## <a name="purchase-order-actions"></a>Ostutellimuse tegevused
Kui olete lisanud ostutellimusele päise ja read, peate sageli tegema lisatoiminguid enne, kui tellimus on kinnitamiseks valmis. Kuna saadaval on nii palju võimalusi, võib olla abiks funktsiooni [Tegevuse otsing](../../fin-and-ops/get-started/action-search.md) kasutamine vastava menüü-üksuse otsimiseks.  

Tellimusel saab tooteid konfigureerida nii, et neil on lisakaubad. Lisakaubad on tooted, mida tuleb või saab osta koos teiste toodetega. Lisatooted võib lisada tasuta kaasnevate toodetena või otsustada, kas lisada need tellimusele või mitte. Lisakaupu saab pärast iga lisatavat tellimuse rida üle vaadata. Kuid ilmselt on mugavam vaadata üle ja lisada vastavad lisakaubad kõigile tellimuse ridadele, kasutades lehte **Lisakaubad**, mille saate avada tegumiribalt.  

Allahindlused lisatakse ridadele tavaliselt nende loomise ajal. Kuid mõningad allahindlused kehtivad tervele tellimusele.

-   Toiming **Lõppallahindlus** arvutab allahindluse protsendi, mis rakendatakse tervele tellimusele. Ärge ajage seda segamini sularahaallahindluse protsendiga. Sularahaallahindlusi rakendatakse arve tasumisel ja need sõltuvad makse tasakaalustamisest konkreetseks kuupäevaks.
-   Kui rakendub multiallahindlus, tuleb kasutada toimingut **Multiallahindlus** selle arvutamiseks ja tellimusele määramiseks. Multiallahindlused on allahindlused, mida saab pakkuda, kui tellimusel olevate toodete kombinatsioon ületab ühise läve. Seda liiki allahindlusi kasutab ainult mõni ettevõte.

Tasud, mille kood kasutab deebeti tüüpi **Kaup**, tuleb määrata rea tasandile enne, kui tellimuse saab kinnitada. Neid tasusid võib olla mugav määrata tellimuse päise tasandil, et saaksite määrata tasu kogusumma. Kuid sellisel juhul tuleb tasu eraldada siis igale reale, enne kui tellimuse saab kinnitada. Saate kasutada toimingut **Tasude eraldamine** summade jagamiseks tasudest, mis määratakse päise tasandil tellimuse ridadele. Tasud saab jagada iga rea netosumma järgi, vastavalt tellitud kogusele, või ühtlaselt tellimuse ridadele. Kui olete tasud ridadele eraldanud, eemaldatakse tasu tellimuse päisest.  

Ostutellimused saab konfigureerida nõudma, et eelarvevahendid eraldataks tellimusele enne selle töötlemist. Sel juhul võite kasutada eelarve eraldamiseks toimingut **Eelarve kontrollimine**.  

Ostutellimuse täitmist võib olla vaja edasi lükata. Näiteks võib olla toodete või teenuste kohta vaja lisateavet või peate kulutuse tegemiseks loa saama. Tellimusega viivitamiseks on mitu võimalust. Näiteks võite oodata tellimuse kinnitamisega. Teine võimalus (kui kasutatakse muudatuse haldamise töövoogu) on tellimuse kinnitamiseks esitamata jätmine. Kui peate blokeerima kõik konkreetse hankija tellimused, võite hankija koondandmete töötlemiseks märkida hankija olekuks **Ootel**. On ka olukordi, mis võivad tellimuse töötlemist takistada. Näiteks võib töötlemine olla takistatud, kui krediidilimiite on ületatud või vajalikud eelarvevahendid pole saadaval.

<a name="additional-resources"></a>Lisaressursid
--------

[Ostutellimuse ülevaade](purchase-order-overview.md)

[Ostutellimuste kinnitamine](purchase-order-approval-confirmation.md)

[Toote sissetulek ostutellimuste suhtes](product-receipt-against-purchase-orders.md)

[Hankija arvete ülevaade](../../finance/accounts-payable/vendor-invoices-overview.md)



