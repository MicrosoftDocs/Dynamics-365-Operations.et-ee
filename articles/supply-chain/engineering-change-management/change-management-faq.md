---
title: Tehnilise muudatuse haldamise KKK-d
description: Selles jaotises antakse vastuseid korduma kippuvatele küsimustele tehniliste muudatushalduste funktsiooni kohta.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba489358ef2d74e816186f29956aea5538a2432825c7d949e7c9cc23d947b997
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714374"
---
# <a name="engineering-change-management-faq"></a>Tehnilise muudatuse haldamise KKK-d

[!include [banner](../includes/banner.md)]

Selles jaotises antakse vastuseid korduma kippuvatele küsimustele tehniliste muudatushalduste funktsiooni kohta.

## <a name="should-i-track-the-version-in-transactions"></a>Kas jälgida versiooni kannetes?

Kui loote tehnika muutmise kategooria, on **tehnika muutmise kategooria üksikasjade lehel** valik, mille nimi on **kannetes versiooni jälitamine**. Mis säte see on ja mida see teeb?

- Kui seadistate kannetes valiku Jälgi versiooni valikule Jah, siis filtreeritakse välja Dimensioonigrupp nii, et kuvatakse ainult need dimensioonigrupid, kus **versioon** on *aktiivne* **dimensioon**.
- Kui seadistate kannetes valiku **Jälgi versiooni valikule** *Ei*, siis filtreeritakse välja **Dimensioonigrupp** nii, et **kuvatakse ainult need dimensioonigrupid**, kus versiooni dimensioon ei ole aktiivne dimensioon.

### <a name="if-you-track-the-version-in-transactions"></a>Kui versiooni kannetes jälgitakse

Tehnika kategooriate puhul, kus valisite dimensioonigrupi, kus versioon on aktiivne dimensioon, jälgite selle kategooria toodete kandeversioone. Sellisel juhul on tehniline toode tooteetalon ja toote iga versioon on tootevariant, mis kasutab versiooni tootedimensiooni. Muid dimensioone saab kasutada koos versioonidimensiooniga.

Sellisel juhul koheldakse kõiki tehnika versioone kõigis protsessides variandina. Seepärast, kui teil on kandes kindel variant (nii, et saate määrata, milline variant müüti või osteti), peate haldama iga versiooni laovaru, koondplaneerimine plaanib tarneid iga versiooni jaoks jne. Kui kustutate versiooni turult, peate muudatuse kajastamiseks kohandama käsitsi selle algus- ja lõppkuupäevi. Samuti tuleb teil varusid hallata veendumaks, et teil ei ole teie ladudes kasutamata kaupade versioone.

Kuigi see valik nõuab rohkem halduskoormust, soovitame seda, kui vajate iga kande puhul kasutatavate versioonide kõrget jälgitavust.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Kui versiooni kannetes ei jälgita

Tehnika kategooriate puhul, kus valisite dimensioonigrupi, kus versioon **ei ole** aktiivne dimensioon, **ei** jälgi te selle kategooria toodete kandeversioone. Sellisel juhul, kui te ei kasuta ühtegi teist dimensiooni, on tehnika toode eristatav toode. Toodet saab endiselt versioonida ja hallata kindlate versioonide (nt nende koosluse \[ BOM] ja protsessi) teavet, kuid te ei saa jälgida, millist konkreetset versiooni igas kandes kasutati. Kehtivuse algus- ja lõppkuupäev näitavad iga versiooni kehtivust.

Seda valikut on palju lihtsam hallata, sest kui soovite muuta versiooni ühest versioonist teise, peate tegema vajalikud muudatused muudatuse järjestuses ning seejärel uuendama tehnikaversioonis kehtivad algus- ja lõppkuupäevad. Tootmisprotsessid komplekteerivad seejärel toote (ja selle konkreetse versiooni) nõutava koosluse ja protsessi.

Enamik organisatsioone valivad selle suvandi, kuna see pakub versiooni- ja muudatusehaldust, kuid ei lisa versiooni jälgimise lisakulu igale kandele, varude puhul ja koondplaneerimise ajal.

## <a name="which-fields-are-copied-from-the-released-item-template"></a>Millised väljad kopeeritakse väljastatud kauba malli poolt?

Kui tehnikaettevõte loob tehnika toote, luuakse see toode tehnikaettevõttes väljastatud tootena. Loodud väljastatud toode põhineb valitud *väljastatud kauba* mallil. (Väljastatud kauba mall on ise olemasolev väljastatud toode.) Väljastatud kaubamalli kasutatakse ka siis, kui toode vabastatakse tegevusettevõttesse. Igal juhul määratleb väljastatud kauba mall enamiku väljastatud toote väljaväärtustest ja need väärtused tulevad seostatud **Väljastatud toote üksikasjade** lehelt.

Järgmistes tabelites kuvatakse väljad, mis kopeeritakse nende protsesside käigus.

| Kiirkaart | Väljad, mis kopeeritakse toote loomisel tehnikaettevõttes | Väljad, mis kopeeritakse vabastamisel tegevusettevõttesse |
|---|---|---|
| **Üldine** | Kõik jaotise **Administreerimine** väljad | Samad väljad, mis kopeeritakse tehnikaettevõttele |
| **Ost** | Kõik väljad | Kõik väljad, v.a **Ühik** |
| **Müük** | Kõik järgmiste jaotiste väljad: **Müügitellimus**, **Haldus**, **Maksustamine**, **Hinna uuendamine**, **Baasmüügihind**, **Tasud**, **Allahindlused** ja **Alternatiivtoode** | Kõik samad väljad, mis kopeeritakse tehnikaettevõttele, v.a **Ühik** |
| **Väliskaubandus** | Kõik väljad | Kõik väljad |
| **Halda varusid** | Kõik väljad ja jaotised, *v.a* **füüsilised dimensioonid** ja **tegelik kaal** | Kõik samad väljad, mis kopeeritakse tehnikaettevõttele, v.a **Ühik** |
| **Insener**, **Plaan**, **Kulude haldamine**, **Projektide haldamine**, **Finantsdimensioonid** ja **Ladu** | Kõik väljad | Kõik väljad, v.a **BOM-i ühik** |
| **Tootevariandid** | Kõik väljad jaotises **Vaikimisi tootevariant** | Samad väljad, mis kopeeritakse tehnikaettevõttele |

Lisaks eelmises tabelis kuvatud väljadele kopeeritakse kõik tellimuse vaikesätted väljastatud kaubamallist, nii toote loomisel tehnikaettevõttes kui ka siis, kui see vabastatakse tööettevõttesse. (Väljastatud kaubamalli tellimuse vaikesätete vaatamiseks avage vastav **Väljastatud toote üksikasjade** leht ja seejärel valige tegevuspaani vahekaardil **Varude haldamine** suvand **Tellimuse vaikesätted**.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Kas luua tehnika toodete jaoks eraldi juriidiline isik või kasutada olemasolevat juriidilist isikut?

Teie äritegevuse nõuded määravad, kas peaksite looma tehnikatoodete jaoks uue juriidilise isiku.

Luues eraldi tehnikaettevõtte, saate hoida tehnikaandmed eraldi ja lisada seejärel muudatusi vastavalt neile, mida need on vajalikud teie kohalike tegevusettevõtete jaoks. Nii saate saavutada järgmiseid eesmärke.

- Säilita eraldi üksus, kus luuakse ja hallatakse tehnika tooteid.
- Ennetada tehnika toodete kuvamist koos ülejäänud väljastatud toodetega, kuni need on valmis ja väljastatud.
- Eristada selgelt andmeid, mida dikteeritakse tehnika ja kohalike andmete järgi.

Aga te peaksite tõenäoliselt kasutama olemasolevat juriidilist isikut tehnikaettevõttena, kui teie puhul kehtivad järgmised tingimused.

- Süsteemis on ainult üks juriidiline isik ja/või te ei nõua selget eraldust inseneritavate toodete vahel.
- Te ei soovi palju andmeid dubleerida, nt ressursigruppe, ressursse, operatsioone ja (võib-olla) saite.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Mis on tehnikaversioonide ja variantide nomenklatuur?

Tehnikatoodete ja tootevariantide nomenklatuur töötab järgmiselt.

- Tehnikatoote puhul (st eristatav toode, kui dimensioone ei kasutata, või tooteesimene, kui kasutatakse mis tahes dimensioone), määratletakse numbrireegli nomenklatuur tehnika tootekategoorias. Seal saate kasutada numbriseeriat, tekstikonstante ja atribuudinimesid ja -väärtusi.
- Igale tehnika toote variandile (kui teie tehnika toode on tooteetelm, on variandid seadistatud tehnika tootekategoorias, kus saate määrata dimensioonigrupi), määratletakse iga variandi numbrireegli klassifikatsioon dimensioonigrupis. Sel juhul saate kasutada koondi toote ID-d ning dimensiooniväärtusi ja -nimesid.
