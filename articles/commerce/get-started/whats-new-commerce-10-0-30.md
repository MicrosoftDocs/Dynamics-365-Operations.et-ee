---
title: Dynamics 365 Commerce eelvaade 10.0.30 (november 2022)
description: See artikkel kirjeldab funktsioone, mis on uued või muutunud Microsoft Dynamics 365 Commerce 10.0.30-
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405517"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Dynamics 365 Commerce eelvaade 10.0.30 (november 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles artiklis loetletakse funktsioonid, mis on eelvaate versiooni Microsoft Dynamics 365 Commerce 10.0.30 uued või muutunud. Sellel versioonil on järgu number 10.0.1362 see on saadaval järgmises graafikus.

- **Avaldamise eelvaade:** september 2022
- **Väljalaske üldine kättesaadavus (ise värskendamine):** oktoober 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendus):** november 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda artiklit värskendada, et kaasata funktsioonid, mis lisati koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---------|------------------|----------------|--------------| 
| Klienditugi   | e-kaubanduse saidi vestlus, kasutades portaale Power Virtual Agents. | See funktsioon annab e-ärisaidi kasutajatele valiku kasutada tugitaotluste Power Virtual Agents jaoks vestlusaknaid. | Administraatorite/tegijate poolt lõppkasutajatele lubatud |
| Ülevaated  |  Müügikoha (POS) tegevusülevaate sündmuste voogesitus teie kontole Application Insights. | [Juurdepääsulogide sisse Application Insights](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  IT-toote/arendaja liitumine   |
|  Maksed  | PayPali tellimuse tugi peale 29-päevase autoriseerimisperioodi. | PayPali maksimaalne autoriseerimisperiood on 29-päevane, pärast mida tuleb luua uus autoriseerimise ja tellimuse ID. Teise võimalusena pakub PayPal võimalust viidata PayPal-tellimusele üldtellimusena, lubades mitmeid autoriseerimist ja fikseerib sama tellimuse ID suhtes, selle asemel et luua uus autoriseerimine ja tellimuse ID 29-ks päevaks). | PayPal makseühenduse konfigureerimisel Commerce Headquartersis on lisatud väli **OrderIntent** ja sellel võib olla kaks väärtust:<p><p>- **Autoriseerimine** : see konfiguratsioon on vaikekonfiguratsioon (kui väli on jäetud tühjaks, **tegutseb** Autoriseerimine vaikimisi). OrderIntenti konfigureerimine autoriseerimise **korrespondeeruks** PayPaliga **processing_instruction** ja **NO_INSTRUCTION**.**·** Tellimus autoriseeritakse PayPaliga ja autoriseerimist ei saa selle väärtuse kasutamisel muuta.<p>- **Salvesta** : kui **OrderIntent väärtus** on seatud väärtusele **Salvesta**, seostub see korreleerumine PayPali **processing_instruction** väärtusega **ORDER_SAVED_EXPLICITLY**. Tellimuseviited salvestatakse PayPal Service’is selle väärtuse kasutamisel.  |
| Müügikoha sisselogimine  | [Luba iseteeninduse diagnoosivõimalused kassasse sisselogimiseks](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  See funktsioon pakub iseteenindusdiagnoosfunktsioone müügikohas (POS) ja Commerce headquartersis, et aidata töötajatel ja juhtidel kiiresti kassasse sisselogimise probleemide juurpõhjusi tuvastada ja parandada.<p><p>- – kassa sisselogimiskuval kuvatud nurjumisteated parandati, et anda konkreetset juurpõhjuse teavet, mis aitab kassat kasutavad töötajad mõista, mis läks valesti, et probleemi lahendamiseks vajalikke tegevusi teha.<p>: testlogimise **funktsioon** on **saadaval** Rakenduse Commerce headquarters lehel Töötajad, et kassaseadmete seadistanud kaupluse juhatajad saaksid kassa sisselogimine simuleerida. Sisselogimistõrke korral pakub see funktsioon toimingutavaid tõrkeotsingu juhendeid, et juhatajad saaksid kontrollida asjakohaseid konfiguratsioone, lahendada probleeme ja kinnitada parandused.  | Vaikimisi sees |


## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste platvormi värskendused

Dynamics 365 Finance 10.0.30 sisaldab platvormi uuendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.30 finantside ja toimingute rakendustest](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Veaparandused

Teavet versiooni 10.0.30 igas värskenduses kaasatud vigaparanduste kohta logige sisse elutsükli teenustesse (LCS) [ja vaadake KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) artiklit. 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 2 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 2 plaan](/dynamics365-release-plan/2022wave2/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-features"></a>Eemaldatud ja taunitud funktsioonid

Artikli [eemaldatud või taunitud funktsioonid Dynamics 365 Commerce](removed-deprecated-features-commerce.md) kirjeldavad funktsioone, mis on Commerce’i eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Commerce](removed-deprecated-features-commerce.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
