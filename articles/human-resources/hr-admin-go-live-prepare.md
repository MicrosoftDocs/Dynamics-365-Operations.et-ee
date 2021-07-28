---
title: Ettevalmistamine Human Resourcesi kasutuselevõtmiseks
description: Sellel lehel antakse juhiseid, kuidas valmistuda Dynamics 365 Human Resourcesi kasutuselevõtmiseks.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ece4875b69d3cf797ab90e54f0cc0fda317cc931
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359649"
---
# <a name="prepare-for-human-resources-go-live"></a>Ettevalmistamine Human Resourcesi kasutuselevõtmiseks

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas valmistuda Dynamics 365 Human Resourcesi projekti avaldamiseks Microsoft Dynamics Lifecycle Servicesi (LCS) abil. 

Selles graafikus esitatakse kasutuselevõtmise protsessi etappe. 

![Kasutuselevõtmise protsess.](./media/hr-admin-go-live-prepare-process.png)

Järgmises tabelis loetletakse kõik protsessi etapid, eeldatav kestus ja tegevuse eest vastutav isik.

| Faas | Tegevus | Kestus/millal | Kes | Märkmed |
| --- | --- | --- | --- |--- |
| 1 | Kasutuselevõtmise kuupäeva värskendamine LCS-is | Hiljemalt 2–3 kuud enne | Partner/klient | Vahe-eesmärkide kuupäevi tuleks pidevalt ajakohastada. |
| 2 | Kontroll-loendi lõpule viimine ja saatmine | Pärast kasutaja nõusoleku testimise (UAT) lõpule viimist | Partner/klient | Järgige juhiseid jaotises [FastTracki kasutuselevõtmise hindamine](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projekti hindamine (FastTrack) | FastTracki arhitekt* | Arhitekt annab hinnangu pärast kontroll-loendi saamist ja jätkab läbivaatamist, kuni küsimused on selgitatud ja vajadusel lahendus on leitud. |
| 4 | Projekti töötuba (FastTrack) | FastTracki arhitekt* | |
| 5 | Andmepaketi importimised | Sõltub projektist | Partner/klient | Järgige juhiseid jaotises [Andmehalduse ülevaade](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).|
| 6 | Tootmiseks valmis | Kui kõik eelmised etapid on lõpule viidud | Partner/klient | Partner/klient saab juhtida töökeskkonda.|
| 7 | Üleminekutegevused | Sõltub projektist | Partner/klient | |
| 8 | Kasutuselevõtt | Sõltub projektist | Klient | |

> [!IMPORTANT]
> *3. ja 4. etapp viiakse lõpule ainult klientide puhul, kes kvalifitseeruvad FastTrackile.

## <a name="completing-the-lcs-methodology"></a>LCS-i metoodika lõpule viimine

Iga juurutusprojekti oluline vahe-eesmärk on üleminek töökeskkonda. Etapi lõpule viimise protsess koosneb kahest osast. 

- Tegelik töö, nt sobivuse-erinevuse analüüs või kasutaja nõusoleku testimine (UAT). 
- Vastava etapi lõpetatuks märkimine LCS-i metoodikas. 

Metodoloogia etappide lõpule viimine on hea tava, kuna edenete rakendamisel. Ärge oodake viimase minutini. Töökindla juurutuse saamine on kliendi huvides. 

## <a name="uat-for-your-solution"></a>UAT teie lahenduse jaoks

UAT faasis peate katsetama kõiki juurutatud äriprotsesse ja tehtud kohandusi juurutusprojekti liivakastikeskkonnas. Edukaks kasutuselevõtuks peaksite UAT faasi lõpule viimisel võtma arvesse järgmist. 

- Soovitame teil UAT-protsess alustada puhtast ja värskest keskkonnast, milles GOLD-konfiguratsiooni andmed kopeeritakse keskkonda enne UAT-protsessi alustamist. Soovitame teil kasutada tootmiskeskkonda GOLD-keskkonnana seni, kuni hakkate tööle, mis hetkel saab keskkonnaks tootmine.
- Testjuhtumid hõlmavad kogu nõuete ulatust. 
- Testige migreeritud andmete abil. See peaks sisaldama andmeid, nagu töötajad, töökohad ja ametikohad. Lisage ka algsaldo, nt puhkuste ja puudumiste viitvõlad. Viimaks lisage ka avatud kanded, nt praegused soodustuste registreerimised. Viige testimine lõpule kõigi andmetüüpidega, isegi kui andmekogum pole lõpetatud. 
- Testige kasutades õigeid turberolle (vaikerollid ja kohandatud rollid), mis on kasutajatele määratud. 
- Veenduge, et lahendus vastaks mis tahes ettevõtte- ja valdkonnapõhistele regulatiivsetele nõuetele. 
- Dokumenteerige kõik funktsioonid ja hankige kliendilt kinnitus ning nõusolek. 

## <a name="mock-go-live"></a>Go-live'i mudeldamine

Enne töösse minekut peate teostama go-live mudeldamise, et testida samme, mida on vaja pärandsüsteemilt uuele süsteemile üleminekuks. Te peaksite oma go-live mudeldamise teostama liivakastikeskkonnas ja kaasama kõik üleminekuplaani sammud.

- Soovitame teil kasutada GOLD konfiguratsioonikeskkonnana tootmiskeskkonda kuni go-live'ini.
- Tagage, et teil on kindel haldusprotsess, et kaitsta tootmiskeskkonda juhuslike kannete või uuenduste eest enne käikuvõtmist.
- Kui olete valmis teostama UAT-d või go-live mudeldamist, värskendage liivakastikeskkonda töökeskkonnast. Lisateavet leiate artiklist [Eksemplari kopeerimine](hr-admin-setup-copy-instance.md).
- Testige kõiki oma üleminekuplaani etappe liivakastikeskkonnas ja seejärel valideerige liivakasikeskkond pistekontrollide või UAT-skriptide kaudu keskkonnas testide tegemisega.
  - Katsed peaksid hõlmama kõiki kasutuselevõtu jaoks vajalike andmete migratsioone, k.a üleminekuid.
  - Protsess peaks hõlmama pärandsüsteemide äralõikamise proovi.
  - Lisage kindlasti kõik integratsiooni ülemineku etapid või välised süsteemi etapid oma ülemineku mudelisse.
- Kui ülemineku mudeldamise ajal ilmneb mis tahes probleeme, võib olla vaja ka teist ülemineku mudeldamist. Seetõttu on soovitatav planeerida oma projektiplaani kaks ülemineku mudeldamist.

## <a name="fasttrack-go-live-assessment"></a>FastTracki kasutuselevõtu hindamine

Kliendid, kes on kvalifitseeritud FastTrackile ja on seotud FastTracki lahenduse arhitektiga, saavad viia lõpule kasutuselevõtu läbivaatuse Microsoft FastTrackiga. Lisateabe saamiseks vt  [Microsoft FastTrack](/dynamics365/fasttrack/). 

Umbes kaheksa nädalat enne kasutuselevõttu palub FastTracki meeskond teil täita [kasutuselevõtu kontroll-loendi](https://go.microsoft.com/fwlink/?linkid=2146013).

Projektijuht või peamine projekti liige peab viima lõpule kasutuselevõtu kontroll-loendi projekti kasutuselevõtule eelnevas faasis. Tavaliselt viiakse kontroll-loend lõpule neli kuni kuus nädalat enne plaanitud kasutuselevõtu kuupäeva, kui UAT on lõpule viidud või peaaegu lõpule viidud. 

Kui olete kasutuselevõtu kontroll-loendi lõpule viinud, saatke see meili teel FastTracki lahenduse arhitektile. Lisage meili saajate hulka alati kliendi ja juurutuse partneri peamine aktsionär. 

Pärast kontroll-loendi esitamist vaatab teie FastTracki lahenduse arhitekt projekti läbi ja annab hinnangu, mis kirjeldab võimalikke riske, häid tavasid ja soovitusi projekti edukaks kasutuselevõtmiseks. Mõnel juhul võib lahenduse arhitekt tuua ohutegurid esile ja paluda riskivähendusplaani. 

## <a name="see-also"></a>Vt ka

[Süsteemi Go-live KKK](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
