---
title: Allhange
description: See artikkel aitab teil koostada allhanke lühiülevaadet tootmises Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: ef8f30e934ece4a148c6f5259d74f8f67799999d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854173"
---
# <a name="subcontracting"></a>Allhange

[!include [banner](../includes/banner.md)]

See artikkel aitab teil koostada Microsofti allhankelepingu lühiülevaadet Dynamics 365 Supply Chain Management. Selle artikli esimeses osas kirjeldatakse andmete seadistamist. Teises osas läbite juhise etapid.

## <a name="target-audience"></a>Sihtpublik

Selles artiklis kirjeldatakse allhanke seadistamist tootmises. Allhanke tegevusvoo põhiseadistamiseks kasutate olemasolevaid andmeid juriidilises isikus HQUS. Demoandmed juriidilises isikus HQUS sisaldavad eelmääratud seadistusparameetreid, mis toetavad juhendi etappides. Kuigi juhend käsitleb peamisi valupunkte ja väljakutseid erinevate rollide puhul, saab selle lõpule viia süsteemiadministraator.

## <a name="demo-scenario"></a>Demostsenaarium

Juriidilises isikus HQUS toodetakse kvaliteetkõlareid. Tootmisprotsessi käigus läbivad kõlarid kolme järgmist toimingut.

- **Eelkooste** – kõlarikorpuse kokkupanek. Korpuse materjal komplekteeritakse materjalilaost enne toimingu käivitamist.
- **Katmine** – pärast kõlarikorpuse kokkupanekut tuleb see katta. Selle toimingu viib lõpule hankija (alltöövõtja). Eelnevalt kokkupandud kõlarikorpus tarnitakse katmise alltöövõtjale koos kahe materjaliga.
- **Lõpetamine** – pärast seda, kui alltöövõtja on eelnevalt kokkupandud kõlarikorpuse katnud, tagastatakse see juriidilisele isikule HQUS, et kõlar lõplikulkt kokku panna.

Järgmisel joonisel on kujutatud kolm toimingut ja materjalid, mida neis tarbitakse.

![Eelkooste, katmine ja lõpetamine ning materjalid, mida need sisaldavad.](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Seadistus

Enne selle juhendiga alustamist peate seadistama andmed.

### <a name="set-up-the-finished-product"></a>Valmistoote seadistamine

See protseduur aitab teil seadistada väljastatud toote D8100 – kaetud korpus.

1. Valige **Tooteteabe haldus \> Tooted \> Väljastatud tooted**, et avada leht **Väljastatud toote üksikasjad**.
2. Sisestage kiirfiltri väljale **D8100** olemasoleva väljastatud toote leidmiseks.

    ![Väljastatud toote D8100 filtreerimine väljastatud toote üksikasjade lehel.](./media/subcontract02_filtering-released-products.png)

3. Valige toimingupaani vahekaardil **Insener** suvand **Protsess**, et avada leht **Protsess**.

    Lehel **Protsess** kuvatakse väljastatud toote D8100 kaheksa protsessiversiooni. Kaheksa protsessiversiooni on jaotatud nelja protsessi vahel saidil 1 ja saidil 5. Protsessi 000400 kasutatakse kuluarvutuseks, protsessi 00041 kasutatakse siis, kui katmistoiming on sisemine, ja protsessi 00042 kasutatakse siis, kui katmistoiming on väline.

    ![Kaheksa protsessiversiooni protsessi lehel.](./media/subcontract03_route-page.png)

4. Valige ülemisel paanil ruudustikus **Versioonid** protsessiversioon **00042** saidile **5**.
5. Valige alumisel paanil vahekaardil **Ülevaade** ruudustikust toiming **20** (**Cbnt CtSc**).

    ![Valitud on toiming 20 protsessiversiooni 00042 puhul saidile 5.](./media/subcontract04_route-version-operation.png)

6. Valige vahekaart **Üldine**.

    Pange tähele, et välja **Protsessi tüüp** väärtus on **Hankija**. See väärtus näitab, et toiming 20 (Cbnt CtSc) on alltöövõtu toiming.

    ![Marsruudi tüübi väljal on vahekaardil Üldine määratud väärtus Pakkuja.](./media/subcontract05_general-tab.png)

7. Valige vahekaart **Ressursinõuded**.

    Võimalusi kasutatakse tootmise plaanimisel rakendatava ressursi leidmiseks. Toimingu 20 (Cbnt CtSc) puhul pange tähele, et nõutav on ressurss, millel on kaks võimalust: **Katmine** ja **Kaetud korpused**.

    ![Katmine ja kaetud korpused vahekaardil Ressursinõuded.](./media/subcontract06_resource-requirements-tab.png)

8. Valige suvand **Rakendatavad ressursid**, et avada dialoogiboks **Rakendatavad ressurssid**.

    Leiti kolm ressurssi, mis vastavad toimingu ressursinõuetele. Pange tähele, et ressursside 8851 ja 8852 tüüp on **Hankija**.

    ![Kolm sobivat ressurssi dialoogiboksis Rakendatavad ressurssid.](./media/subcontract07_applicable-resources-dialog.png)

9. Valige **OK**, et sulgeda dialoogiboks **Rakendatavad ressurssid** ja naasta lehele **Protsess**.
10. Sulgege leht **Protsess**, et naasta lehele **Väljastatud toote üksikasjad**.

    ![Väljastatud toodete üksikasjade leht.](./media/subcontract08_released-product-details-page.png)

11. Valige toimingupaani vahekaardil **Insener** suvand **Koosluse versioonid**, et avada leht **Koosluse versioonid**.

    Lehel **Koosluse versioonid** kuvatakse väljastatud toote D8100 neli koosluse (BOM) versiooni. Kooslust 000040 kasutatakse kuluarvutuseks ja plaanimiseks, kooslust 000041 kasutatakse siis, kui katmistoiming tehakse ettevõttesiseselt ning kooslusi 000042 ja 000043 kasutatakse siis, kui katmistoiming hangitakse.

    Pange tähele, et kaup S8050 on toode kaubatüübiga **Teenus**. See kaup kujutab alltöövõtulepinguga tööd.

    ![Neli koosluseversiooni koosluse versioonide lehel.](./media/subcontract09_bom-versions-page.png)

12. Valige kiirkaardil **Koosluse read** suvand **Redigeeri**, et avada dialoogiboks **Koosluserea redigeerimine**.

    Kui tootmistellimus on loodud ja väljastatud toote D8100 puhul hinnatud, luuakse kaubale S8050 automaatselt ostutellimus. See ostutellimus seotakse tootmistellimusega. Ostutellimuste automaatseks loomiseks tuleb välja **Rea tüüp** väärtuseks seada **Hankija** ja valida tuleb alltöövõtja hankija konto. Selles näites on hankija konto US-801.

    Pange tähele, et koosluse rida on ühendatud katmistoiminguga toimingu numbri (antud juhul 20) kaudu.

    ![Koosluserea redigeerimise dialoogiboks.](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Laotöölistele parooli loomine

Peate määratlema pihuseadet kasutavatele laotöötajatele parooli.

1. Valige **Laohaldus \> Seadistus \> Töötaja**, et avada leht **Töö kasutajad**.
2. Valige kiirkaardil **Kasutajad** rida kasutajale **51**.

    ![Töö kasutajate leht.](./media/subcontract11_work-users-page.png)

3. Valige suvand **Parooli lähtestamine**.
4. Sisestage väljadele **Parool** ja **Parooli kinnitus** väärtus **1**.
5. Valige suvand **Sea parool**.

## <a name="step-by-step-walkthrough"></a>Üksikasjalik juhend

**Stsenaarium ja taust**

Tootele D8100, kaetud korpus, luuakse tootmistellimus 10 ühikuga. Korpuste katmine on alltöövõtulepinguga toiming, mille teeb hankija US-801, Perfect Coating Solutions. Tootmistellimuse hõlmab kolme toimingut. Esimeses toimingus pannakse korpus ettevõttesisese toiminguna eelnevalt kokku. Eelkooste jaoks vajalik materjal väljastatakse toormaterjali laost komplekteerimiseks. Kui eelkooste on lõpule viidud, saadetakse eelnevalt kokkupandud korpus Perfect Coating Solutionsile koos kahe katmistoimingu jaoks vajaliku materjaliga. Kui kaetud korpus saadetakse hankijalt tagasi, läbib see lõpliku ettevõttesisese koostetoimingu, enne kui see lõpetatuna kinnitatakse.

1. Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.
2. Valige toimingupaanil suvand **Uus tootmistellimus**, et avada dialoogiboks **Tootmistellimuse loomine**.

    ![Tootmistellimuse loomise dialoogiboks.](./media/subcontract12_create-production-order-dialog.png)

3. Valige väljal **Kaubakood** väärtus **D8100**.
4. Kaubakoodi valimisel kuvatakse varude dimensioonide väljad. Valige väljal **Värv** väärtus **Kroom**.

    Ilmub teateaken küsimusega, kas sisestada tuleks koosluse ja protsessi aktiivsed versioonid.

    ![Teateaken.](./media/subcontract13_message-box.png)

5. Valige **Jah**. 

    Dialoogiboksis **Tootmistellimuse loomine** on väljadel **Koosluse number** ja **Protsessi kood** automaatselt valitud vastavalt toote D8100 koosluse ja protsessi aktiivsed versioonid. Praegusel juhul on valitud kooslus **000040** ja protsess **000040**.
    
    > [!NOTE]
    > Nii koosluse kui ka protsessi puhul kasutatakse kuluarvutuseks ja plaanimiseks versiooni 000040.

6. Valige väljal **Tegevuskoht** väärtus **5**.
7. Valige väljal **Ladu** väärtus **51**.
8. Muutke väljadel **Koosluse number** ja **Protsessi kood** väärtust, milleks on automaatselt valitud **000042**.

    > [!NOTE]
    > Nii koosluse kui ka protsessi puhul kasutatakse versiooni 000042 korpuse katmiseks alltöövõtulepinguga hankijaga US-801.

    ![Tootmistellimuse loomise määratud väärtuste seadistamine dialoogiboksis.](./media/subcontract14_create-production-order-dialog-set.png)

9. Valige käsk **Loo**, et luua tootmistellimus ja naasta lehele **Kõik tootmistellimused**.

    ![Uus tootmistellimus kõikide tootmistellimuste lehel.](./media/subcontract15_new-production-order.png)

10. Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Hinnang**, et avada dialoogiboks **Hinnang**.

    ![Hinnangu dialoogiboks.](./media/subcontract16_estimate-dialog.png)

11. Valige **OK**, et kinnitada hinnang ja naasta lehele **Kõik tootmistellimused**.

    > [!NOTE]
    > Kui tootmistellimus on hinnatud, luuakse teenusüksuse S8050 jaoks hankijale US-801 tootmistellimus.

12. Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Kooslus**, et avada leht **Kooslus**, kus saate vaadata tootmistellimuse koosluseridu.

    Teenuseüksuse S8050 puhul pange tähele, et seal on viide ostutellimusele, mis loodi tootmistellimuse hindamisel.

    ![Tootmistellimuse koosluse read koosluse lehel.](./media/subcontract17_production-order-bom-lines.png)

13. Sulgege leht **Kooslus**, et naasta lehele **Kõik tootmistellimused**.
14. Valige toimingupaani vahekaardil **Ajakava** suvand **Tööde planeerimine**, et avada dialoogiboks **Töö planeerimine**.
15. Määrake järgmised väärtused.

    - Valige väljal **Plaanimissuund** suvand **Edasi homsest**.
    - Valige suvandi **Piiratud võimsus** sätteks **Jah**.

    ![Tööde planeerimise dialoogiboks.](./media/subcontract18_job-scheduling-dialog.png)

16. Valige **OK**, et sulgeda dialoogiboks **Tööde planeerimine** ja naasta lehele **Kõik tootmistellimused**.
17. Valige toimingupaani vahekaardil **Ajakava** suvand **Gantt**, et avada leht **Gantti diagramm – ressursivaade**.

    Gantti diagramm annab visuaalse ülevaate tootmistööde ajakavast ressurssidel. Pange tähele, et väline katmistöö koosneb kolmest tööst: protsessitöö, transporditöö ja ooteajatöö.

    ![Gantt diagramm Gantt`i diagrammil – ressursivaate leht.](./media/subcontract19_gantt-chart.png)

18. Sulgege leht **Gantti diagramm – ressursivaade**, et naasta lehele **Kõik tootmistellimused**.
19. Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Väljastamine**, et avada dialoogiboks **Väljastamine**.

    ![Väljastamise dialoogiboks.](./media/subcontract20_release-dialog.png)

20. Valige dialoogiboksi **Väljastamine** sulgemiseks **OK**.
21. Valige suvandid **Tootmise juhtimine \> Perioodilised ülesanded \> Väljasta lattu \> Koosluse- ja valemiridade automaatne väljastamine**, et avada dialoogiboks **Koosluse- ja valemiridade automaatne väljastamine**.

    ![Koosluse- ja valemiridade automaatse väljastamise dialoogiboks.](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Valige koosluse- ja valemiridade töö automaatse väljastamise töö käitamiseks **OK**.

    See töö väljastab lattu toormaterjalide komplekteerimistöö.

23. Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.
24. Valige kiirfiltri abil tootmistellimus, millega olete töötanud.
25. Valige toimingupaani vahekaardil **Ladu** suvand **Töö üksikasjad**, et avada leht **Töö**.

    Pange tähele, et lehel kuvatakse toormaterjali komplekteerimise kohta kaks töökomplekti. Esimene töö on materjalide M8100 ja M8101 kohta. Neid materjale tarbib toiming 10. Teine töö on materjalide M8202 ja M8250 kohta. Neid materjale tarbib toiming 20, mis tehakse alltöövõtulepinguga.

    ![Kaks toormaterjali komplekteerimise töökomplekti lehel Töö.](./media/subcontract22_work-page.png)

26. Käivitage mobiilirakendus Warehouse Management laotöö töötlemiseks toimingu 10 puhul.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.
28. Valige kiirfiltri abil tootmistellimus, millega olete töötanud.
29. Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Alusta**, et avada dialoogiboks **Alustamine**.
30. Määrake vahekaardil **Üldine** järgmised väärtused.

    - Valige väljal **Toimingust nr** väärtus **10**.
    - Valige väljal **Toiminguni nr** väärtus **10**.

    ![Määratud väärtused üldise vahekaardil 1.](./media/subcontract23_start-dialog.png)

31. Valige **OK**, et sulgeda dialoogiboks **Alustamine** ja naasta lehele **Kõik tootmistellimused**.

    Pange tähele, et tootmistellimuse olek on nüüd **Alustatud**. Toimingu 10 materjale tarbib komplekteerimislehe töölehe automaatne sisestamine. Aja tarbimist toimingu 10 puhul võtab arvesse protsessikaardi töölehe automaatne sisestamine.

32. Käivitage mobiilirakendus Warehouse Management laotöö töötlemiseks toimingu 20 puhul.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Alusta**, et avada dialoogiboks **Alustamine**.
34. Määrake vahekaardil **Üldine** järgmised väärtused.

    - Valige väljal **Toimingust nr** väärtus **20**.
    - Valige väljal **Toiminguni nr** väärtus **20**.
    - Sisestage väljale **Kogus** väärtus **10**.
    - Valige väljal **Sisesta komplekteerimisleht kohe** suvand **Ei**.

    ![Määratud väärtused üldise vahekaardil 2.](./media/subcontract24_general-tab.png)

35. Valige **OK**, et sulgeda dialoogiboks **Alustamine** ja naasta lehele **Kõik tootmistellimused**.

    Komplekteerimisleht luuakse materjalide jaoks, mida kasutatakse katmistoimingu puhul, ja teenusüksuse jaoks. Teenusüksus kujutab alltöövõtulepinguga toimingut.

36. Valige toimingupaani vahekaardil **Vaade** suvand **Komplekteerimisleht**, et avada leht **Komplekteerimisleht**.
37. Valige komplekteerimisleht, mis pole sisestatud, ja seejärel valige töölehe number töölehe ridade kuvamiseks.

    ![Komplekteerimislehe lehe töölehe read.](./media/subcontract25_picking-list.png)

38. Valige toimingupaanil suvandid **Printimine** \> **Komplekteerimislehe aruanne**, et avada dialoogiboks **Komplekteerimislehe aruanne**.
39. Seadke suvandi **Kasuta tarneteate paigutust** sätteks **Jah**.

    ![Komplekteerimislehe aruande dialoogiboks.](./media/subcontract26_picking-list-report-dialog.png)

40. Valige aruande **Komplekteerimisleht** loomiseks **OK**.

    Selles näites prinditakse hankija tarneteade tootmise komplekteerimislehe töölehelt. Tarneteade määrab katmistoimingut tegevale hankijale tarnitavad materjalid.

    ![Komplekteerimislehe aruanne.](./media/subcontract27_picking-list-report.png)

41. Sulgege aruanne **Komplekteerimisleht**, et naasta lehele **Komplekteerimisleht**.
42. Valige toiminguribal suvand **Sisestamine**, et avada dialoogiboks **Töölehe sisestamine**.

    ![Töölehe sisestamise dialoogiboks.](./media/subcontract28_post-journal-dialog.png)

43. Valige dialoogiboksi **Töölehe sisestamine** sulgemiseks **OK**.
44. Avage ostutellimus.

    ![Ostutellimuse leht.](./media/subcontract29_purchase-order-page.png)

45. Valige toimingupaani vahekaardil **Ostmine** suvand **Kinnita**.
46. Valige dialoogiboksi **Töölehe sisestamine** avamiseks käsk **Sisesta**.
47. Valige **OK**, et sulgeda dialoogiboks **Töölehe sisestamine** ja naasta lehele **Ostutellimus**.
48. Muutke ühiku hinnaks **33** asemel **40**.

    ![Ostutellimuse lehel muudetud ühiku hind.](./media/subcontract30_unit-price.png)

49. Kinnitage ostutellimus uuesti.
50. Toote sissetulek.

    ![Toote sissetuleku sisestamise dialoogiboks.](./media/subcontract31_posting-product-receipt-dialog.png)

51. Ostuarve.
52. Värskendage vastendamise olekut.

    ![Hankija arve leht.](./media/subcontract32_vendor-invoice-page.png)

53. Kinnita lõpetamine.

    ![Lõpetatuna kinnitamise dialoogiboks.](./media/subcontract33_report-as-finished-dialog.png)

54. Lõpeta.

    ![Lõpetamise dialoogiboks.](./media/subcontract34_end-dialog.png)

55. Kuluvõrdlus.

    ![Kuluvõrdluse diagrammid.](./media/subcontract35_cost-comparison-charts.png)

Puuduv seadistus andmetes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]