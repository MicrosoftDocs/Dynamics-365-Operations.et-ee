---
title: Eraldustingimused
description: See artikkel annab teavet põhikonto eraldamistingimuste kasutamise kohta.
author: rachel-profitt
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: twheeloc
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d62c0cc79c9d61e0ebb1c2c62a345ad47412d0d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859823"
---
# <a name="allocation-terms"></a>Eraldustingimused

[!include [banner](../includes/banner.md)]

See artikkel annab teavet põhikonto eraldamistingimuste kasutamise kohta. Eraldustingimusi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni vahel. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.

Iga põhikontol loodav eraldustingimus määratleb ühe allikaga põhikontolt või finantsdimensioonide kombinatsioonist eraldatava kande protsendi. Lisaks määratlete sihtpõhikonto ja finantsdimensioonid, kust summa eraldatakse. 

Eraldamise jaoks lähtefinantsdimensiooni määratledes saate valida, kas iga dimensioon on spetsiifiline või mittespetsiifiline. Spetsiifiline tähendab, et lähtekande finantsdimensioon peab ühtima valitud dimensiooniga. Kui valite mittespetsiifilise, tähendab see, et ühtimisel võidakse arvesse võtta finantsdimensiooni ükskõik millist väärtust.

Eraldustingimuse jaoks sihtpearaamatukontot määratledes peate määrama põhikonto, millele summa eraldate. Saate kasutada sama põhikontot, kuhu on sisestatud lähtekanne, või mõnda muud põhikontot. Kui kasutatakse sama põhikontot, kuvatakse kirje salvestamisel hoiatus. Lisaks põhikonto määramisele peate määrama ka sihtdimensioonid. Iga dimensiooni puhul saate määrata, kas soovite sihtfinantsdimensiooni väärtust säilitada või muuta. Kui valite ei, peate finantsdimensiooni jaoks valima uue väärtuse. Kui valite jah, ei täpsustata täiendavat teavet ja süsteem säilitab sisestamisel algsed finantsdimensioonid.

Põhikontole lisatavate eraldustingimuste arv ei ole piiratud. Siiski ei või eraldustingimuses eraldamisprotsentide summa ületada 100. Saate luua eraldusi, mis on alla 100 protsendi, kui osa algse kande summast peaks jääma lähtefinantsdimensioonidesse. Eraldustingimusi saab põhikontole lisada juriidilise isiku alistusena. Kui kasutate jagatud kontoplaani, tuleb eraldustingimused määratleda iga juriidilise isiku jaoks. Nupule **Eraldustingimused** juurdepääsu saamiseks peate esmalt valima juriidilise isiku alistuses märkeruudu **Eraldamine**.

## <a name="allocation-term-example"></a>Eraldustingimuse näide
Olete määratlenud oma organisatsiooni CORPORATE jaoks kulukeskuse, mille number on 000. Kommunaalkulude arvete sisestamisel kodeeritakse need CORPORATE'I kulukeskusesse. Teie ettevõte on määratlenud reegli, et kõik kommunaalkulud tuleb eraldada protsendi alusel igale kulukeskusele. Teised osakonna ja äriüksuse finantsdimensioonid jäävad samaks.

Selle näite puhul luuakse kommunaalkulude põhikonto jaoks uus eraldustingimus. Iga kulukeskuse jaoks luuakse üks rida eraldatava protsendiga. Iga rea lähtefinantsdimensioonide **Valikukriteeriumid** oleksid **Kulukeskuse** jaoks **Spetsiifiline** ja väärtuseks seataks 000: CORPORATE. Osakonna ja äriüksuse puhul oleks suvandi **Valikukriteeriumid** väärtus **Mittespetsiifiline**.

Kiirkaardil **Sihtpearaamatukohto** on põhikontoks sama kommunaalkulude konto ning suvandi **Säilita lähtefinantsdimensioonid** väärtuseks seatakse **Jah** üksuste **Äriüksus** ja **Osakond** puhul. Suvandi **Säilita lähtefinantsdimensioonid** väärtuseks seatakse **Ei** üksuse **Kulukeskus** puhul ning valitud väärtuseks on asjakohane kulukeskus, millele te eraldate. Kui eraldada tuleb kolmele kulukeskusele, siis luuakse kolm eraldustingimuste kirjet. Iga eraldustingimus erineb teistest vaid kulukeskuse poolest, mis on määratud sihtpearaamatukontol.

## <a name="create-an-allocation-term-on-a-main-account"></a>Põhikontol eraldustingimuse loomine

1. Avage **navigeerimispaanil** **Moodulid > Pearaamat > Kontoplaan > Kontod > Põhikontod**.
2. Otsige loendist ja valige soovitud kirje.
3. Valige kiirkaardil **Juriidilise isiku alistamised** suvand **Lisa**.
4. Valige **Ettevõte** ja seejärel **Lisa**.
5. Valige märkeruut **Eraldus**.
6. Valige **Eraldustingimused**.
7. Valige vaikekirje muutmiseks **Redigeeri** või kirje lisamiseks **Uus**.
8. Sisestage väljale **Protsent** kannete protsent, mida soovite eraldada.
9. Valige kiirkaardil **Lähtefinantsdimensioon** jaotises **Valikukriteeriumid** iga finantsdimensiooni jaoks suvand.
    - Kui valite väärtuse **Spetsiifiline**, siis valige parempoolsest ripploendist finantsdimensiooni väärtus.
    - Kui valite väärtuse **Mittespetsiifiline**, ei nõuta finantsdimensiooni kohta täiendavat teavet.
10. Valige kiirkaardil **Sihtpearaamatukonto** väljal **Kontole** põhikonto, kuhu soovite eraldada kande protsendi.
11. Valige jaotises **Säilita lähtefinantsdimensioonid** iga finantsdimensiooni jaoks suvand.
    - Kui valite väärtuse **Ei**, siis valige seejärel parempoolsest rippkastist finantsdimensiooni väärtus, kuhu soovite kande eraldada.
    - Kui valite **Jah**, siis pole täiendavat teavet vaja. Süsteem säilitab eraldamise sisestamisel algse kande väärtuse.
12. Korrake juhiseid 7–11 iga järgmise eralduse puhul. Kõigi eralduste summa on näidatud väljal **Koguprotsent**. See summa ei tohi ületada 100.
13. Sulgege kõik lehed.

>[!NOTE] 
> Te võite kasutada nuppu **Kopeeri**, et valitud eraldus dubleerida.

Kui põhikonto jaoks luuakse eraldustingimus, sisestab süsteem automaatselt uue kande, kui sisestatakse kanne, mis ühtib eraldustingimuste lähtefinantsdimensioonidega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
