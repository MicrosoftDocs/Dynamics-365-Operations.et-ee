---
title: Soodustuse plaani loomine
description: Soodustuse plaanide seadistamine rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bcbf4c1a7f136e5563bf1210b6c09228dad95dea
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429241"
---
# <a name="create-a-benefits-plan"></a>Soodustuse plaani loomine

Selles artiklis kirjeldatakse, kuidas seadistada soodustuse plaani rakenduses Dynamics 365 Human Resources.

1. Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Soodustuse plaanid**.

2. Valige suvand **Uus**.

3. Määrake vahekaardil **Üldine** järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Plaan** | Plaani kordumatu identifikaator. |
   | **Kirjeldus** | Plaani kirjeldus. |
   | **Plaani tüüp** | Uue plaani loomisel peate määrama plaani tüübi. Plaani tüüp on kindlate soodustuste tüüpide kõrgetasemeline rühmitamine. Iga plaani tüüp määrab, kas töövõtja saab registreeruda mitmes seda tüübi plaanis, täpsustab, kas kontaktid on kasusaajad või sõltuvad, ja määratleb katvuse valikud. Saate luua uusi kohandatud plaanide tüüpe, et need vastaksid teie soodustuste pakkumustele. Peamised soodustusplaanide tüübid on järgmised. <ul><li>401K</li><li>ADD</li><li>Hambaravi</li><li>Vormisolek</li><li>FSA</li><li>Elu</li><li>LTD</li><li>Meditsiin</li><li>PTO</li><li>STD</li><li>Nägemine</li></ul> |
   | **Plaani tüübi kood** | Plaani tüübi kood. |
   | **Programm** | Määratleb plaani valikuliselt määramise programmi. |
   | **Kogum** | Määratleb plaani valikuliselt määramise kogumi. |
   | **Põhiveokiri** | Määratleb, kas plaan on antud kogumi koondplaan. |
   | **Olek** | Näitab soodustuse plaani praegust olekut. Vaikeväärtus on Aktiivne. Kui muudate olekuks Passiivne, ei ole plaan registreerimise ajal valimiseks saadaval. |
   | **Kehtivuse alguskuupäev ja -aeg** | Plaani alguskuupäev ja -kellaaeg. Vaikeväärtus on praegune süsteemikuupäev. |
   | **Kehtivuse lõppkuupäev ja -aeg** | Plaani lõppemise kuupäev ja kellaaeg (olekuks seatakse Passiivne). Vaikeväärtus on 12/31/2154, mis tähendab, et mitte kunagi. |

4. Vahekaardil **Konfigureerimine** määrake olenevalt loodava plaani tüübist järgmiste väljade väärtused.

   | Plaani tüüp | Väli | Kirjeldus |
   | --- | --- | --- |
   | Meditsiiniline (meditsiiniline, hambaravi, nägemine, HMO) | COBRA | Määrab, kas plaanile rakendub eelarve vastavusseviimise konsolideeritud koondõigusakt (COBRA, Consolidated Omnibus Budget Reconciliation Act). |
   | Meditsiiniline (meditsiiniline, hambaravi, nägemine, HMO) | HIPAA | Määrab, kas plaanile rakendub tervisekindlustuse teisaldatavuse ja vastavuse seadus (HIPAA, Health Insurance Portability and Accountability Act). |
   | <ul><li>Meditsiiniline (meditsiiniline, hambaravi, nägemine, HMO)</li><li>Muu (PTO, vormisolek)</li><li>Muud</li><li>Pikaajaline invaliidsus</li><li>ADD (Tavaline elu, Vabatahtlik elu)</li><li>Säästmine (näiteks 401(k))</li><li>FSA</li></ul> | Maksueelselt kõlblik | Määrab, kas plaanile saab teha osamakseid enne maksude arvestamist. |
   | <ul><li>Meditsiiniline (meditsiiniline, hambaravi, nägemine, HMO)</li><li>Muu (PTO, vormisolek)</li><li>Pikaajaline invaliidsus</li><li>ADD (Tavaline elu, Vabatahtlik elu)</li><li>Säästmine (näiteks 401(k))</li><li>FSA</li></ul> | Maksujärgselt kõlblik | Määrab, kas plaanile saab teha osamakseid pärast maksude arvestamist. |
   | <ul><li>Meditsiiniline (meditsiiniline, hambaravi, nägemine, HMO)</li><li>Muu (PTO, vormisolek)</li><li>Pikaajaline invaliidsus</li><li>ADD (Tavaline elu, Vabatahtlik elu)</li><li>Säästmine (näiteks 401(k))</li><li>FSA</li></ul> | Kaasautor | Määrab, kes teeb plaanile osamakseid – töövõtja, tööandjale või mõlemad. |
   | <ul><li>Pikaajaline invaliidsus</li><li>ADD (Tavaline elu, Vabatahtlik elu)</li></ul> | Minimaalne kindlustus | Plaani jaoks nõutav minimaalne kindlustuskaitse summa. |
   | <ul><li>Pikaajaline invaliidsus</li><li>ADD (Tavaline elu, Vabatahtlik elu)</li></ul> | Maksimaalne kindlustus | Plaani jaoks nõutav maksimaalne kindlustuskaitse summa. |
   | <ul><li>Pikaajaline invaliidsus</li><li>ADD (Tavaline elu, Vabatahtlik elu)</li></ul> | Kindlustuse astmelise muutuse kasutamine | Määrab, kas kontrollida, kas katvussumma vastab kehtivale astmelisele summale. |
   | <ul><li>Pikaajaline invaliidsus</li><li>ADD (Tavaline elu, Vabatahtlik elu)</li></ul> | Summa muutuse samm | Plaani kindlustuskaitse sammu summa. Näiteks kui sammu summa on 1000, ei saa töötaja kindlustus olla 200 500 dollarit, see peab olema ümardatud üles 201 000 dollarini või alla 200 000 dollarini. |
   | <ul><li>Pikaajaline invaliidsus</li><li>ADD (Tavaline elu, Vabatahtlik elu)</li></ul> | Astmeline suund | Määrab ümardamise suuna – ülespoole või allapoole –, kui kindlustussumma ei vasta summa sammu väärtusele. |
   | ADD (Tavaline elu, Vabatahtlik elu) | Kindlustatavustõend | Määrab, kas töövõtja peab esitama kindlustatuse kohta tõendi. |
   | ADD (Tavaline elu, Vabatahtlik elu) | Summa | Summa arvestusvaluutas. See väli on aktiivne ainult siis, kui valitakse märkeruut Kindlustatavustõend on valitud. |
   | <ul><li>Säästmine (näiteks 401(k))</li><li>FSA</li></ul> | Minimaalne aastane panus | Plaani jaoks nõutav minimaalne lisatav summa. |
   | <ul><li>Säästmine (näiteks 401(k))</li><li>FSA</li></ul> | Maksimaalne aastane panus | Plaani jaoks nõutav maksimaalne lisatav summa. |
   | Säästmine (näiteks 401(k)) | Tööandja maksimaalne aastane summa | Maksimaalne summa, mille tööandja saab soodustuse perioodi jooksul töötaja säästuplaani lisada. Selle välja kasutamiseks peate märkima ruudu Tööandja vaste. |
   | Säästmine (näiteks 401(k)) | Tööandja sobivus | Määrab, kas tööandja teeb töövõtja säästuplaani osamakseid. |
   | Säästmine (näiteks 401(k)) | Tööandja vastendatud protsent | Töövõtja panuse protsent, mille tööandja ühitab. |
   | Säästmine (näiteks 401(k)) | Tööandja vaste ülemmäär | Maksimaalne protsent, millele tööandja ühitab. Näiteks kui tööandja ühitab 100% töövõtja osamaksetest kuni 6% töövõtja palgast, on tööandja ühitamise ülemmäär 6%. |

5. Määrake vahekaardil **Seadistus** järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Registreeringu lubamine/jätkamine** | Määrab, kas töövõtjad saavad plaanis registreeruda, kui nad vastavad sobivuse nõuetele.</br></br>Kui see on seatud väärtusele Ei, ei ole plaan sobivuse töötlemisel töötajate jaoks saadaval. |
   | **Registreeri eelmise aasta alusel automaatselt** | Määrab, kas kõlbliku töövõtja plaan registreeritakse automaatselt, kui ta oli eelmisel aastal registreeritud. |
   | **Automaatne registreerimine vaikesättena** | Määrab, kas registreerimise plaanid valitakse vaikimisi. Plaan ei ole kohustuslik, seega töövõtja saab vaikevalikut muuta. |
   | **Registreerimine on suletud** | Määrab, kas piirata plaan ainult sobivatele töövõtjatele, kes olid plaani registreeritud eelmisel aastal. |
   | **Kohustuslik plaan** | Määrab, kas töövõtjaid registreeritakse plaani automaatselt. Töövõtjad ei saa registreerimise valikut muuta. |
   | **Jõustumise kuupäev** | Plaani loomise kuupäev ettevõttes. |
   | **Hankija konto** (soodustuse pakkuja) | Hankija, kellele ettevõte plaani osana preemiaid maksab. |
   | **Nimi** (soodustuse pakkuja) | Tarnija nimi. |
   | **Hankija viide** (soodustuse pakkuja) | Hankija viide plaanile. Näiteks ettevõtte rühma plaani number. |
   | **Alternatiivne viide** (soodustuse pakkuja) | Hankija alternatiivne viide plaanile. Näiteks ettevõtte kontonumber. |
   | **Valuuta** (soodustuse pakkuja) | Pakkujale preemiate maksmiseks kasutatav valuuta. |
   | **Kulukonto** (soodustuse pakkuja) | Pearaamatukonto, mida kasutatakse plaani preemiate kulukontona. |
   | **Hankija konto** (soodustuse haldaja) | Hankija, kellele ettevõte plaani haldamiseks maksab. Kui plaani hallatakse ise, jätke see väli tühjaks. |
   | **Nimi** (soodustuse haldaja) | Soodustuse haldaja hankija nimi. |
   | **Hankija viide** (soodustuse haldaja) | Haldaja hankija viide plaanile. |
   | **Alternatiivne viide** (soodustuse haldaja) | Haldaja hankija alternatiivne viide plaanile. |
   | **Valuuta** (soodustuse haldaja) | Soodustuse haldajale maksmiseks kasutatav valuuta. |
   | **Kulukonto** (soodustuse haldaja) | Pearaamatukonto, mida kasutatakse plaani haldamisega seotud kulude kulukontona. |

6. Vajadusel filtreerige vahekaardil **Filtrid**. Saate filtreerida järgmiste väljade põhjal.

   - **Äriüksus**
   - **Osakond**
   - **Juriidiline isik**
   - **Koht**
   - **Ametikoht**

7. Määrake vahekaardil **Sobivusreeglid** järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Rea number** | Sobivusreegli reanumber. |
   | **Sobivusreegel** | Soodustuse plaanile rakendatav sobivusreegel. See sobivus reegel rakendatakse vastavale tegevuse tüübile ja seostatakse määratud katvuse ooteaja ja mahaarvamistega. |
   | **Tegevuse tüüp** | Sobivusreegli rakendamise tegevus: soodustuste registreerimine või soodustuste aegumine. |
   | **Kehtivusperioodi ooteaeg** | Väärtus vormilt Ooteajad. Katvuse ooteaeg juhib päevade või kuude arvu, kaua töövõtja ootab soodustuse katvust või soodustuse aegumist, mis põhineb sobivusreegli ja tegevuse tüübi kriteeriumitel. |
   | **Mahaarvamise ooteaeg** | Väärtus vormilt Ooteajad. Mahaarvamise ooteaeg juhib päevade või kuude arvu, kaua töövõtja ootab soodustuse palgast mahaarvamist, mis põhineb sobivusreegli ja tegevuse tüübi kriteeriumitel. |

8. Valige käsk **Salvesta**.

## <a name="view-enrolled-workers"></a>Registreeritud töötajate vaatamine

Saate kuvada töötajad, kes on valitud soodustuse plaani registreeritud.

1. Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Soodustuse plaanid**.

2. Valige suvand **Registreeritud töötajad**.

## <a name="attach-coverage-options"></a>Lisa kindlustussuvandid

Saate lisada valitud soodustuse plaanile katvuse valikuid. Katvuse valikute lisamine toob katvuse valiku jaoks määra ja mahaarvamise seadistuse kokku.  Näide. Meditsiiniplaani puhul valiks kasutaja pere katvuse valiku.  Seejärel valiksid nad seotud plaani jaoks pere määra (määratud seadistuses Määr) ja seotud plaani mahaarvamise (määratud määra seadistuses). See annab tööandja ja töövõtj valitud katvuse kulu. Seejärel kordaksite protsessi Töötaja+1 katvuse või Töötaja katvuse jaoks.

1. Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Soodustuse plaanid**.

2. Valige suvand **Lisa katvuse valikud**.

## <a name="override-eligibility-rules"></a>Sobivusreeglite tühistamine

Saate lisada töötajaid plaani sobivusreeglite eranditena. Iga lisatav töötaja on soodustuse plaani jaoks sobiv.

1. Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Soodustuse plaanid**.

2. Valige suvand **Sobivusreegli tühistamine**.

## <a name="view-attached-periods"></a>Lisatud perioodide kuvamine

Saate vaadata saadaolevate soodustuste perioodide loendit.

1. Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Soodustuse plaanid**.

2. Valige suvand **Perioodid**.

## <a name="view-plan-information"></a>Plaani teabe kuvamine

Saate sisestada plaani kirjelduse, et aidata töövõtjaid soodustuste valimisel. Siia sisestatav plaani teave kuvatakse töövõtja iseteeninduses, kui liikuda üle katvuse valikute loendis üle plaani.

1. Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Soodustuse plaanid**.

2. Valige suvand **Plaani teave**.

## <a name="view-flex-credit-programs"></a>Paindliku krediidiga programmide kuvamine

1. Tööruumis **Soodustuste haldus** jaotises **Plaanid** valige suvand **Soodustuse plaanid**.

2. Valige suvand **Paindliku krediidiga programmid**.
