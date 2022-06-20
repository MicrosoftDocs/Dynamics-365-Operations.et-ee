---
title: Lao sisestusreeglid
description: See artikkel annab ülevaate lao sisestusprofiilidest.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cae5b39ef8e6e153fe522dee1874deae2a2cb86e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901338"
---
# <a name="inventory-posting-profiles"></a>Lao sisestusreeglid

[!include [banner](../includes/banner.md)]

Lao sisestusreeglid kontrollivad varude alammooduli kannete sisestamist pearaamatusse. Lao alammooduli kandeid saab luua paljudest **moodulitest, sh Müük ja turundus**, **Hange** ja hanked, **Tootmise** juhtimine jne. Lao alam pearaamatukanded võivad olla sisestatud mis tahes ajal, mil kaupa müügitellimuses või ostutellimuses kasutatakse. 

Võidakse sisestada täiendavaid varude alamvõtme kandeid:
- Dokumendi iga uuendamine.
- Kui sisestatakse müügitellimuse saateleht või arve.
- Ostutellimuse toote sissetuleku või arve loomisel

Lisateabe saamiseks minge varude alamvõtme kannetele.

## <a name="inventory-transaction-overview"></a>Laokannete ülevaade

Iga varude alamtüübi kanne sisaldab:
 - Kogus 
 - Hind 
 - Sait 
 - Ladu 
 - Asukoht 

Varude alammooduli kannetes luuakse pearaamatus füüsilise sisestamise ja finantsilise sisestamise kaudu kaks kirjet. Lisateavet vt füüsilistest ja finantsilisi [uuendustest](/supply-chain/cost-management/physical-financial-updates.md).
Järgmine näide on kolme reaga ostutellimus. Oletame näiteks, et kogu tellimus on ühele laokohale ja laole. Igal ostutellimuse real on üks seotud InventTrans kirje — tuntud ka kui laokanne — ja igal real on kogus 10. Järgmine diagramm näitab ühe ostutellimuse päise seost kolme ostutellimuse reaga, igaüks ühe InventTransi kirjega.

![Seose diagramm ostutellimuse jaoks, kus kolm rida on igaüks ühe InventTrans kirjega.](./media/InventTransRelationship.PNG)

Esimesel ostutellimuse real on saadud kogus 5. Teise rea täielik kogus ja ostutellimuse kolmandalt realt saadud kogus puudub. Nüüd on esimese ostutellimuse reaga seotud teine laokanne. Teise ostutellimuse rea kanne uuendatakse kandeks Vastu **võetud** ja kolmas kanne jääb samaks. Järgmine diagramm näitab suhet ostutellimuse rea 1 täiendava InventTrans-kirjega.

![Kolme reaga ostutellimuse suhtediagramm Üks rida on osaliselt vastuvõetud ja kuvab kaks InventTransi kirjet.](./media/InventTransRelationshipPartialReceipt.PNG)

Selles näites sisestatakse kanne pearaamatusse; See on füüsiline kanne. Kauba mudeligrupp on konfigureeritud füüsiliste varude sisestamiseks ja kõik kaubad kasutavad sama kauba mudeligruppi. Lao sisestusprofiil kasutab ühte põhikontode komplekti. Luuakse üks kanne ja Kirje InventTrans lingib nii InventTrans 1 kui ka InventTrans 2 samale kandele.

Seejärel saadud arve koguse kohta, mis on saadud ridadel 1 ja 2. Pearaamatus luuakse teine kanne; See on finantskanne. Kauba mudeligrupp on konfigureeritud finantsiline laovaru sisestamiseks. Teine kanne on seotud inventTrans 1 ja InventTrans 2-ga.

Sõltuvalt kuluarvestuse mudelist võib teie lao alammooduli kannete jaoks olla olemas kolmas pearaamatu sisestus, mis on seotud lao sulgemise ja tasakaalustamisega. Lisateabe saamiseks minge lao [sulgemisele](/supply-chain/cost-management/inventory-close.md). Kõikide laokannete üksikasjade vaatamiseks valige laohalduse **päringud** > **ja aruannete** > **kanded**.

>[!Important]
> Varude kanded tükeldatakse iga varude dimensioonide kordumatu kombinatsiooni ja iga osalise värskenduse jaoks. Seda kuvati eelnevas näites osaliste uuenduste kohta.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Tükelda varud varude dimensiooni näite alusel

Näites on ostutellimuse rida 3 seeriakaup. Vastuvõtuprotsessi käigus registreeritakse ostutellimusele kümme seerianumbrit. Laokanne tükeldatakse 10 laokandeks. Järgmine diagramm näitab suhteid ja täiendavaid laokandeid, igaüks oma seerianumbriga, mis on seotud ostutellimuse reaga 3.

![Kolme reaga ostutellimuse suhtediagramm Üks rida on seeriaks jaotatud ja näitab täiendavaid InventTransi kirjeid.](./media/InventTransRelationshipSerialNumber.PNG)

Kui iga seerianumber on saadud ühe toote sissetulekuga, luuakse üks lisakanne ülaltoodud näites. Füüsilise kande väli seostatakse iga seerianumbriga. Sama kehtib finantsvärskenduse kohta ostutellimuse arveldamisel.

## <a name="inventory-transactions"></a>Laokanded

Laokandeid saate vaadata varude kannete **lehe jaotises** Varud ja **laohaldus või** Kuluhaldus **·**. Valides lao ja valides seejärel Kanded, saate vaadata konkreetse lähtedokumendi reaga (nt ostutellimuse reaga või müügitellimuse reaga) **seotud laokandeid** **.** 

Laokannete **lehel** on järgmised väljad.

| Väli            | Kirjeldus                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Kaubakood      | Kandega seotud kaubakood.                                                                  |
| Füüsiline kuupäev    | Kuupäev, mil varud lattu saabuvad, laost lahkuvad, tootmises tarbitakse või toodetakse. Näiteks sisestuskuupäev kuupäeval
Müügitellimuse saatelehe sisestamine või ostutellimuse toote sissetuleku sisestamine.                             |
| Finantskuupäev   | Kuupäev, mil laokanne suleti ja kulu pearaamatus kirjendatakse. Näiteks arve sisestuskuupäev 
müügi- või ostutellimuse loomiseks. Viitedokumendi uuendused ei ole lubatud pärast finantskuupäeva asustatud. |
| Viide        | Näitab kande allikat ja dokumenditüüpi, mis kuvatakse väljal **Number**. Näiteks müügitellimus, ostutellimus või üleviimistellimuse sissetulek.                                                 |
| Number           | Näitab kande viite ID-d. Näiteks kui viiteväli **näitab** müügitellimust, näitab **numbriväli** müügitellimuse numbrit.                                                       |
| Sissetulek (olek) | Sissetulekutest laokannete puhul näitab see väli sissetuleku olekut. Näiteks ostutellimus on sissetulek ja selle olekuks võib olla Tellitud **või** Ostetud **·**.                                                            |
| Väljaminev (olek)   | Väljaminek laokannete puhul näitab see väli väljaminek olekut. Näiteks müügitellimus on väljaminek ja selle olekuks võib olla Tellimusel **või** **Müüdud**.                         |
| Kogus         | Laokande kogus. Positiivseid numbreid kasutatakse lao sissetulekute puhul, samas kui negatiivseid numbreid kasutatakse lao väljaminek.                                                                                                                          |
| Ühik             | Koguse mõõtühik.                                                                                   |
| Tegeliku kaalu kogus      | Kande tegeliku kaalu kogus Lisateabe saamiseks minge jaotisesse Tegeliku [kaaluga kaupade teave](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Tegeliku kaalu ühik          | Tegeliku kaalu mõõtühik, millega tegeliku kaalu kogust väljendatakse                                                         |
| Omahind      | Laokande lõppkulu. See väli täidetakse kande finantsiliselt uuendamisel. Sõltuvalt kuluarvestuse metodoloogiast võib lao sulgemise ja korrigeerimise protsess seda välja uuendada.                            |

## <a name="inventory-status"></a>Lao olek

Igal laokandel on olek, mis kuvatakse kas väljal Sissetulek **või** **Väljaminek**. Kasutatav väli sõltub laokannete tüübist. Sissetulekud on kanded, mis tõstvad varusid. Näiteks positiivse kogusega ostutellimus või müügitellimuse tagastus negatiivse kogusega. Väljaminek on laokanded, mis vähendasid ladu. Näiteks positiivse kogusega müügitellimus või ostutellimuse tagastus negatiivse kogusega.

### <a name="receipt-status"></a>Sissetuleku olek

Järgmises tabelis kirjeldatakse sissetuleku **olekut**.

| **Sissetuleku olek** | **Kirjeldus**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Tellitud            | Sissetulekut tähistav mis tahes laokande algolek. See hõlmab positiivse koguse, tootmistellimuste või müügitellimuse tagastustega ostutellimusi negatiivse kogusega.                                                   |
| Registreeritud         | Seda olekut kasutatakse siis, kui kaheastmeline vastuvõtuprotsess on olemas või kui kauba saabumis kasutatakse näitamaks, et toode on saabunud. Kasutatakse siis, kui partii- või seerianumbrid on "eraldatud" või tellimusele registreeritud. Kauba saabumise kohta lisateabe saamiseks minge saabumise [ülevaatesse](/supply-chain/inventory/arrival-overview.md). |
| Vastuvõetud           | Seda olekut kasutatakse kande füüsilisel uuendamisel. Ostutellimuse puhul on selleks toote sissetuleku sisestamisel. Müügitellimuse tagastuse puhul on see siis, kui saateleht sisestatakse.                                                                            |
| Ostetud          | Seda olekut kasutatakse kande finantsiliselt uuendamisel. Ostutellimuse või müügitellimuse tagastuse puhul on see siis, kui luuakse arve.                                                                                             |

### <a name="issue-status"></a>Väljamineku olek

Järgmine tabel kirjeldab väljaminek **olekut**.

| **Väljamineku olek**  | **Kirjeldus**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Tellimusel          | Väljaminek tähistav laokande algolek. See hõlmab positiivse koguse, tootmistellimuste koosluse või valemiridadega müügitellimusi või negatiivse kogusega ostutellimuste tagastusi.                                             |
| Reserveeritud tellitud  | Varude olek näitab, et varud reserveeritakse tellimuse suhtes, mis on loodud, kuid pole veel füüsiliselt laos vastu võetud. Varude sissetulekul uuendatakse olekuks automaatselt Füüsiliselt **reserveeritud**. Reserveeringute kohta lisateabe saamiseks minge varude [koguste reserveerimiseks](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Füüsiliselt reserveeritud | See olek näitab, et varud on konkreetse tellimuse jaoks eraldatud või reserveeritud. Kui varud on reserveeritud, ei ole see füüsiliselt saadaval muude tellimuste jaoks.                                 |
| Komplekteeritud         | See näitab, et varud on laost komplekteeritud. Ladu on veel laos füüsiliselt eemaldatud, seda ei eemaldata, kuid pole muude tellimuste jaoks saadaval.  |
| Maha arvatud          | Seda olekut kasutatakse kande füüsilisel uuendamisel. Müügitellimuse puhul on see siis, kui saateleht sisestatakse; ostutellimuse tagastuse jaoks, see siis, kui toote sissetulek on sisestatud.                                                                      |
| Müüdud              | Seda olekut kasutatakse kande finantsiliselt uuendamisel. Ostutellimuse või müügitellimuse puhul on see arve loomisel.|

Laokannete kohta lisateabe saamiseks minge varude kannete [üksikasjadesse](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Varude sisestusprofiili konfigureerimine

Lao sisestusprofiili konfigureerimiseks järgige neid samme.

1.  Saate avada **laohalduse seadistuse** > **·** > **sisestamise** > **·**.
2.  Valige kande tüübi vahekaart. Näiteks valige **ostutellimus**.
3.  Valige sisestamistüübile raadionupp. Näiteks valige kuludele **ostu kulu**.
4.  Valige suvand **Uus**.
5.  **Väljal Kaubakood** valige suvand Tabel **, Grupp**,**Kõik** **või** **Kategooria**. Näiteks kindla kaubagrupi sisestusreeglite konfigureerimiseks valige **Grupp**.
     - Kui valisite **sammus** 5 valiku Tabel, valige sisestusreeglile konkreetne kaubakood väljal **Kauba** seos.
     - Kui valisite **5**. sammus grupi, **valige sisestusreegli** **jaoks kaubagrupp väljal Kauba** seos.
     - Kui valisite **sammus** 5 väärtuse Kõik, **on kauba** seose väli tühi.
     - Kui valisite **sammus** 5 valiku Kategooria, **on kauba** seose väli tühi. Kasutage välja **Kategooriaseost**, et valida kategooria, mille osas sisestusreeglit rakendatakse.

6.  **Valige väljal Konto** kood suvand Tabel **, Grupp** **või** **Kõik**. Näiteks sisestusreeglite rakendamiseks kõigi hankijate puhul valige suvand **Kõik**.
     - Kui valisite **sammus** 5 valiku Tabel, valige sisestusreeglile konkreetne hankijakood väljal **Konto** seos.
     - Kui valisite **sammus** 5 valiku Grupp, valige sisestusreegli jaoks hankijagrupp väljal **Konto** seos.
     - Kui valisite **sammus** 5 väärtuse Kõik, **on konto** seose väli tühi.

7.  Valitud sisestustüübiga konkreetse maksugrupi seostamiseks valige **käibemaksugrupp**. Kui see väli on tühi, rakendub sisestamistüüp kõigile olemasolevatele maksugruppidele. Maksugruppidele määratud sisestamine kehtib ainult müügi- ja ostukannetele.
8.  Määrake kontonumber, et sisestada kontotüüp põhikonto **väljale**. Kui konto numbrit pole raamatupidamistüübina kasutamiseks loodud, saate luua uue konto. Uue konto saate luua pearaamatu **põhikonto** üksikasjade lehel.

## <a name="additional-resources"></a>Lisaressursid

Iga lao sisestusreeglite **lehe vahekaart** on seotud jaotise <a0/& alam alamvõtmega Dynamics 365 Supply Chain Management. Lisateabe saamiseks minge:
-   [Müügitellimuse sisestamine](sales-order-posting.md)
-   [Ostutellimuse sisestamine](purchase-order-posting.md)
-   [Varude sisestamine](inventory-posting.md)
-   [Tootmise juhtimise sisestamine](production-posting.md)
-   [Standardkulu hälbe sisestamine](standard-cost-variance-posting.md)
