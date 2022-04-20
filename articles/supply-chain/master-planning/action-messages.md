---
title: Tegevussoovitused
description: Tegevussoovitus on süsteemi loodud soovitus olemasoleva plaanitud või kinnitatud tellimuse muutmiseks.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570250"
---
# <a name="action-messages"></a>Tegevussoovitused

[!include [banner](../includes/banner.md)]

Tegevussoovitus on süsteemi loodud teade olemasoleva plaanitud, kinnitatud või kinnitatud tellimuse muutmiseks.

Koondplaneerimise arvutus loob tegevusteated muutunud vajadustele reageerimiseks. Näiteks lähetuskuupäeva või kogust muudetakse müügitellimusel pärast seda, kui olete juba loonud ostutellimuse selle müügitellimuse nõudluse täitmiseks. Sel juhul loob koondplaneerimise kalkulatsioon ühe või mitu tegevusteadet, mis soovitavad ostutellimust uuendada. Saate otsustada, kas teha soovitatud muudatused.

Saate seadistada, kuidas kaubale lisatavad laovarugrupi tegevusteated arvutatakse.

## <a name="select-action-messages"></a>Tegevusteadete valimine

Lehel **Laovarude grupid** saate valida tegevusteated, mida süsteem peaks koostama, ja laovarude grupid või kaubad, millele teated kehtivad. Järgmises tabelis loetletakse tegevusteade, mille saate valida.

| Sõnum | Kirjeldus |
|---|---|
| Varasem | Süsteem loob vajaduse järgi tegevusteated, et teisaldada tellimused varasemale kuupäevale. Väljal Ettemakse **marginaal** saate määrata maksimaalse päevade arvu, mis võib sissetuleku ja väljamineku vahel ilma eelneva tegevuseta edasi minna. |
| Lükka edasi | Süsteem loob vajaduse järgi tegevusteated, et teisaldada tellimused hilisemale kuupäevale. Väljal Edasilükatud **marginaal** saate määrata maksimaalse päevade arvu, mis võib sissetuleku ja väljamineku vahel edasi lükata. |
| Vähenda | Süsteem loob tegevusteated, kui tootmistellimusi, ostutellimusi ja muid sissetulekukandeid tuleb vähendada, et vältida laotasemete ülejääki. |
| Kasv | Süsteem loob tegevusteated, kui tootmistellimusi, ostutellimusi ja muid sissetulekukandeid tuleb suurendada, et vältida laovarude puudujääke. |
| Tuletatud tegevused | Sissetulekukannete jaoks loodud tegevusteateid levitatakse mis tahes tuletatud nõuetele ning nendele nõuetele vastava sissetulekukannete jaoks luuakse vajalikud tegevussõnumid. |

Järgmistes jaotistes antakse mõned üksikasjalikud stsenaariumid.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Tegevuste suurendamine ja vähendamine toote vaiketellimuse kogustega

Kauba vaike-tellimissätete **lehel** saate seadistada minimaalse tellimuse koguse, maksimaalse tellimuse koguse ja mitu väärtust. Sel juhul võtab süsteem neid sätteid tegevuste soovitamisel arvesse, kindlustamaks, et soovitused ei põhjustaks alapakkumist.

Näiteks on teil üksus, mis sisaldab selle vaiketellimuse sätete lehel järgmiseid **sätteid**:

- **Minimaalne tellimusekogus:** *0*
- **Tellimuse maksimaalne kogus:** *90*
- **Mitu:** *20*

Kui selle kauba koguseks on 60 nõudlust, luuakse koondplaneerimisel plaanitud ostutellimus kogusele 60. Kui nõudlus suureneb 30 korda, soovitab koondplaneerimine kasvu 40, sest see võtab arvesse 20kordseid ja ei põhjusta mitte kunagi alapakkumist.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Tegevus sõnumid ohutusvaruga seotud tellimuste kohta

Tegevus sõnumid tellimustele, mis tarnivad ohutusvaru, ei soovita kunagi vähendada kogust allapoole ohutusvaru jaoks vajalikku kogust. See tähendab, et kui on olemas tellimus, mis varustab ohutusvaru ja kliendi nõudlust ning nõudlust väheneb või tühistatakse, soovitab koondplaneerimine plaanitud tellimust vähendada nõudluse vähendamisega. Siiski ei soovita see kunagi väärtust, mis on väiksem kui vajalik ohutusvaru.

Süsteem ei soovita tegevusse edasi anda ohutusvaru tarnimist, kuna eeldatakse, et ohutusvaru tuleb tarnida vajalikul ajal ja nõutud kuupäeval.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Kooslustega seotud ettemaksed ja edasilükkamised

Koosluse komponentidega seotud tegevused tuleb rakendada enne nende emaüksuste tegevust, kuna see võib mõjutada kõrgema taseme kooslustega seotud edasisi tellimusi. Seejärel peate käivitama koondplaneerimise uuesti, et sobivaid tegevusi ümber arvutada ja soovitada.

Näiteks on teil järgmine olukord:

- Tootmise tüüpi *lõplikul heal* *FG-l* on kooslus, mis sisaldab toormaterjali *RM*.
- Tänane kuupäev on 21. jaanuar.
- Olemasolev vabastatud tootmistellimus FG *jaoks on* planeeritud 25. jaanuariks.
- Olemasoleva tootmistellimuse toetamiseks on koondplaneerimine loonud nõutava toormaterjali RM jaoks plaanitud *ostutellimuse*. Tellimuse vajaduse kuupäev on 25. jaanuar.
- Täna luuakse FG *jaoks* uus müügitellimus. Selle vajaduse kuupäev on täna (21. jaanuar).
- 21. jaanuar on rm kalendris *tarnimiseks* suletud, kuid 22. jaanuar on avatud.

Kui koondplaneerimine on käitatud, loob see edasisi tegevussõnumeid, mis soovitavad varem planeeritud tootmise teisaldamist nii, et saate täita tänast tellimust.

- Uue nõudluse saavutamiseks soovitab see FG tootmistellimuse teisaldamist *kuni* 21. jaanuarini. (See teeb selle soovituse ilma suletud kuupäeva arvessemata *Rm*.)
- *Kuna* tootmistellimuse jaoks on rm veel vajalik, soovitab see ka plaanitud ostutellimuse teisaldamist. Sel korral kontrollib see siiski RM-i *kalendrit*. Seetõttu soovitab see plaanitud ostutellimuse teisaldamist RM-ilt *22*. jaanuari (kuna 21. jaanuar on suletud).

Nagu näete, saab nõutud toormaterjali *RM* plaanitud FG tootmise jaoks liiga *hilja*. Seega peate kõigepealt rakendama edasist tegevust RM-i plaanitud ostutellimusele *ja* siis käivitama koondplaneerimise uuesti. Sel hetkel loob koondplaneerimine uue tegevussõnumi, mis *soovitab tootmistellimuse teisaldamist FG-sse* 22. jaanuari.
