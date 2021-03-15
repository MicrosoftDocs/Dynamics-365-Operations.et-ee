---
title: Kuluarvutustabelid
description: Kuluarvutustabeli seadistus täidab kahte eesmärki. Esimese sihina määrate müüdud kaupade maksumuse teabe kuvamise vormingu toodetud kauba või tootmistellimuse kohta. Vormindatud kuva nimetatakse kuluarvutustabeliks. Teise sihina määrate kaudse kulu arvutamise alused. Kuluarvutustabeli seadistus põhineb kulugrupi teabekuvamise funktsioonil ja kaudse kulu arvutamise valemitel. Selles artiklis on kirjeldatud kuluarvutustabeli seadistuse kahte eesmärki.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df761015ed9382f59fa8ba7df9e5856db06287c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987650"
---
# <a name="costing-sheets"></a>Kuluarvutustabelid

[!include [banner](../includes/banner.md)]

Kuluarvutustabeli seadistus täidab kahte eesmärki. Esimese sihina määrate müüdud kaupade maksumuse teabe kuvamise vormingu toodetud kauba või tootmistellimuse kohta. Vormindatud kuva nimetatakse kuluarvutustabeliks. Teise sihina määrate kaudse kulu arvutamise alused. Kuluarvutustabeli seadistus põhineb kulugrupi teabekuvamise funktsioonil ja kaudse kulu arvutamise valemitel. Selles artiklis on kirjeldatud kuluarvutustabeli seadistuse kahte eesmärki. 

Kuluarvutustabel on vormindatud kuva teabest toodetud kaupade või tootmistellimuse jaoks müüdud kaupade kulu kohta. Kuluarvutustabeli seadistamisel saate määratleda teabe vormingu ja ka kaudsete kulude arvutamise aluse. Kuluarvutustabeli seadistus põhineb kulugrupi teabe kuvamise funktsioonil ja kaudse kulu arvutamiseks kasutatavatel valemitel. Siin leiate kuluarvutustabeli seadistamise kahe eesmärgi kohta lisateavet.
-   **Määrata kuluarvutustabeli vorming.** Kasutajamääranguga kuluarvutustabeli vorming määrab hinnasegmentatsiooni, mis hõlmab toodetud kauba tuletusreeglit. Näiteks saab kauba tuletusreegli teabe kulugruppide järgi segmentida näiteks materjali-, tööjõu- ja üldkuludeks. Need kulugrupid määratakse kaupadele, kulukategooriate protsessitoimingutele ja kaudsete kulukalkulatsioonide valemitele. Kuluarvutustabeli vorming nõuab harilikult vahepealsete kogusummade arvutamist, kui määratletud on mitu kulugruppi. Näiteks saab liita mitu materjaliga seotud kulugruppi. Kuluarvutustabeli vormingu määrang on valikuline, kuid kuluarvutustabeli vorming tuleb määrata, kui hakatakse kaudset kulu arvutama.
-   **Määrata kaudsete kulude arvutamise alus.** Kaudsed kulud kajastavad tootmise üldkulu, mis seostub toodetava kauba tootmisega. Kaudse kulu arvutamise valemit võib väljendada lisatasu või tariifina. Lisatasu esindab väärtuse protsenti, kuna aga tariif esindab protsessioperatsiooni suurust tunni kohta. Kulugrupp määratleb arvutamisvalemi aluse, näiteks 100-protsendise lisatasuna tööjõu kulugrupi eest või 50,00 USA dollari suuruse tunnitasuna masina kulugrupi eest. Kui soovite määratleda arvutamisvalemi ja selle kulugrupi aluse, peate kuluarvutustabeli seadistamiseks määrama kulugrupi, mis esindab üldkulu, ja valima kas lisatasu või tariifse lähenemise.

Iga arvutusvalem tuleb sisestada kulukirjena. Kulukirje koosneb määratud kuluversioonist, lisatasu protsendist või tariifi suurusest, kulugrupi alusest, olekust ja jõustumiskuupäevast. Kulugrupi algsel sisestamisel on selle olek **Ootel** ja sel on jõustumiskuupäev. Kulukirje aktiveerimisel värskendatakse olekut, nii et kirje on praegune aktiivne kirje, ja jõustumiskuupäev värskendatakse aktiveerimiskuupäevale. Kulukirje võib määrata ka tegevuskohapõhise arvutusvalemi jaoks tegevuskoha. Samuti on teil võimalik jätta väli **Tegevuskoht** tühjaks näitamaks, et arvutusvalem on ettevõtteülene valem. Kulukirje võib vajadusel koosneda määratud kaubast või kaubagrupist, kui arvutusvalem on märgitud kui kauba kohta. 

Praeguseid aktiivseid kaudse kulu arvutamise valemite kulukirjeid kasutatakse tootmistellimuse kulude hindamiseks. Neid kasutatakse ka tegeliku aja- ja materjalikuluga seotud tegelike kulude arvutamiseks. Ootel kulukirjeid kasutatakse koosluse arvutustes tulevaseks kuupäevaks. 

Kaks blokeerivat kuluversiooni poliitikat määravad, kas ootel kulusid saab säilitada ja käivitada. Kasutage blokeerivat poliitikat andmete säilitamise lubamiseks ning siis kuluandmete säilitamise ennetamiseks kuluversiooni piires. 

Kui olete määratlenud kuluarvutustabeli vormingu ja kaudsete kulude arvutuse, peate läbima eraldi etapi teabe valideerimiseks ja salvestamiseks. Kuluarvutustabel tähistab ettevõtteülest vormingut tuletusreegli teabe kooskõlastatud kuvamiseks. 

Kuluarvutustabel kuvatakse lehe **Kauba kulu arvutamine** osana. Kuluarvutustabeli saab kuvada toodetud kauba arvutatud kulukirje kohta lehel **Kauba hind** või tellimusekohase arvutamise kirje kohta lehel **Koosluse arvutuse tulemused**. Samuti saab selle kuvada tootmistellimuse puhul lehe **Hinnakalkulatsioon** osana.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]