---
title: Maksuarvutusega alustamine
description: Selles teemas selgitatakse, kuidas seadistada maksuarvestusi.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ae2c20fe79c2f8fd8d102740441230ae443f16a3
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952517"
---
# <a name="get-started-with-tax-calculation"></a>Maksuarvutusega alustamine

[!include [banner](../includes/banner.md)]

See teema annab teavet selle kohta, kuidas alustada maksuarvestusega. Selle teema jaotised juhendavad teid läbi kõrgema taseme kujunduse ja konfigureerimisetappide elutsükli Microsoft Dynamics teenustes (LCS), Regulatory Configuration Service (RCS) Dynamics 365 Finance ja Dynamics 365 Supply Chain Management. 

Seadistus koosneb kolmest põhi astmest.

1. LCS-s installi maksuarvestuse lisandmoodul.
2. RCS-is seadistage maksuarvestuse funktsioon. Need häälestusandmed pole spetsiifilised iga juriidilise üksuse jaoks. Seda saab jagada finants- ja Supply Chain Management -i kõigi juriidiliste üksuste vahel.
3. Finantside ja Supply Chain Management -is seadistage juriidilise üksuse maksuarvestuse parameetrid.

## <a name="high-level-design"></a>Kõrgtaseme kujundus

### <a name="runtime-design"></a>Käitusaja kujundus

Järgmine näide näitab maksuarvestuse kõrgema taseme käitusaja kujundust. Kuna maksuarvutust saab integreerida mitme Dynamics 365 rakendusega, kasutab näide integratsiooni finantsiga.

1. Finantsis luuakse kanne, nt müügitellimus või ostutellimus.
2. Finantsid kasutavad automaatselt käibemaksugrupi ja kauba käibemaksugrupi vaikeväärtusi.
3. Kui **kandel** on valitud nupp Käibemaks, käivitatakse maksu arvutamine. Finantsid saadab siis lasti maksuarvutuse teenusesse.
4. Maksuarvestuse teenus sobitab tasu koormuse eelmääratletud reeglitega maksufunktsioonis, et leida täpsem käibemaksugrupp ja kauba käibemaksugrupp samaaegselt.

    - Kui tasukoormust saab vastendada maksugrupi kohaldatavusmaatriksiga, alistab see käibemaksugrupi väärtuse vastendatud maksugrupi **väärtusega** kohaldatavusreeglis. Muidu jätkatakse finantside käibemaksugrupi väärtuse kasutamist.
    - Kui last on vastendatud kauba maksugrupi kohaldatavusmaatriksiga, alistab see kauba käibemaksugrupi väärtuse ja kohaldatavusreeglis vastendatud kauba **maksugrupi** väärtuse. Muidu jätkatakse finantside kauba käibemaksugrupi väärtuse kasutamist.

5. Maksuarvestuse teenus määrab lõplikud maksukoodid, kasutades käibemaksugrupi ja kauba käibemaksugrupi ristvalikut.
6. Maksuarvestuse teenus arvutab maksu lõplike maksukoodide alusel, mille ta määratles.
7. Maksu arvutamise teenus tagastab maksuarvutuse tulemuse finantsid.

![Maksuarvutuse käitusaja kujundus.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Kõrgtaseme konfiguratsioon

Järgmised sammud annavad kõrgel tasemel ülevaate maksuarvestuse teenuse konfiguratsiooniprotsessist.

1. Installige LCS-i **oma** LCS-projekti maksuarvutuse lisandmoodul.
2. RCS-s looge **käibemaksu arvutamise** funktsioon.
3. RCS-s seadistage **maksuarvestuse** funktsioon:

    1. Valige maksu konfiguratsiooni versioon.
    2. Loo maksukoodid.
    3. Looge maksugrupp.
    4. Looge kauba käibemaksugrupp.
    5. Valikuline: looge maksugrupi kohaldatavus, kui soovite alistada kliendi või hankija koondandmetest sisestatud vaikimisi käibemaksugrupi.
    6. Valikuline: looge kaubagrupi kohaldatavus, kui soovite kauba koondandmetest sisestatud kauba käibemaksu vaikegrupi alistada.

4. RCS-s täitke ja avaldage **maksuarvestuse** funktsioon.
5. Valige finantsides avaldatud **maksuarvutuse** funktsioon.

Pärast nende sammude sooritamist sünkroonitakse järgmised seadistused automaatselt RCS-st finantsidesse.

- Käibemaksukoodid
- Käibemaksugrupid
- Kauba käibemaksugrupid

Selle teema ülejäänud jaotised pakuvad üksikasjalikumaid konfigureerimistoiminguid.

## <a name="prerequisites"></a>Eeltingimused

Enne kui saate selles teemas järelejäänud protseduurid lõpule viia, peavad olema täidetud järgmised eeltingimused:<!--TO HERE-->

- Teil peab olema juurdepääs oma LCS-i kontole ja peate olema juurutanud LCS-projekti, millel on 2 või kõrgema taseme keskkond, mis käitab Dynamics 365 versiooni 10.0.21 või uuemat versiooni.
- Peate looma oma organisatsioonile RCS-keskkonna ja teil peab olema juurdepääs oma kontole. Lisateavet RCS-keskkonna loomise kohta vt [Regulatory Configuration Service ülevaadet](rcs-overview.md).
- Järgmised funktsioonid peavad teie **Funktsioonihalduse** Finance ja Supply Chain Management keskkonna tööruumis olema vastavalt ärihuvile sisse lülitatud:

    - Maksuarvutusteenus
    - Toeta mitut käibemaksu registreerimisnumbrit
    - Maks üleviimistellimuses

- Järgmised funktsioonid peavad olema sisse lülitatud teie **Funktsioonihalduse** tööruumis juurutatud RCS-i keskkonnas.

    - Globaliseerimisfunktsioonid

## <a name="set-up-tax-calculation-in-lcs"></a>LCS-is maksuarvestuse seadistamine

1. Logige sisse [LCS](https://lcs.dynamics.com)
2. Viige integratsiooni seadistus Microsoft Power Platform -i jaoks lõpule. Lisateavet vt teemast [Lisandmooduli ülevaade](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Valige üks teie juurutatud mittetootmiskeskkonnast ja seejärel valige **Installi uus lisandmoodul**.
4. Valige **Maksuarvestus**.
5. Lugege tingimusi ja nõustuge nendega ning valige seejärel **Installi**.

## <a name="set-up-tax-calculation-in-rcs"></a>RCS-is maksuarvestuse seadistamine

Selle jaotise sammud ei ole seotud kindla juriidilise üksusega. Seda protseduuri tuleb teha ainult üks kord ning seda saab täita mis tahes RCS-i juriidilises üksuses.

1. Logige teenusesse [RCS](https://marketing.configure.global.dynamics.com/) sisse.
2. **Elektroonilise atuandluse** tööruumis, lisage uus konfiguratsiooni pakkuja. Kasutage oma ettevõtte nime pakkuja nimena. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Valige äsja loodud konfiguratsioonipakkuja ja valige **Määra aktiivseks**.
4. Valige **Microsoft** konfiguratsiooni pakkuja ja seejärel valige **Hoidlad**.
5. Väljalt **Tüüp** valige **Globaalne**.
6. Valige **Avamine**.
7. Minge **Maksu andmemudelisse**, laiendage failipuud ja valige seejärel **Maksukonfiguratsioon**.
8. Valige õige [maksukonfiguratsiooni](global-tax-calcuation-service-overview.md#versions) versioon, mis põhineb teie finantsversioonil, ja seejärel valige **käsk** Impordi.
9. Minge tagasi **Globaliseerimisfunktsioonide** tööruumi, valige **Funktsioonid**, valige **maksuarvutuse** paan ja seejärel valige **Lisa**.
10. Saate valida ühe järgmistest funktsioonitüüpidest:

    - **Uus funktsioon** – Looge funktsiooniseadistuse, kus sisu on tühi.
    - **Põhineb olemasoleval funktsioonil** – Looge funktsioon olemasolevast funktsioonist ja kopeerige sisu olemasolevast funktsiooni seadistusest.

11. Sisestage funktsiooni nimi ja kirjeldus ja seejärel valige **Loo funktsioon**.

    Pärast funktsiooni loomist luuakse automaatselt selle mustandversioon. Saate valida **Too see versioon** et lähtestada mustandiversioon mis tahes lõpetatud versioonile.

12. Valige funktsiooni mustandversioon ja seejärel käsk **Redigeeri**. **Maksuarvestuse seadistuse** leht on täidetud.
13. Valige **Konfiguratsiooniversioon**. Peaksite nägema konfiguratsiooni versiooni, mille importisid sammus 8.

    Microsoft pakub vaikemaksukonfiguratsiooni maksu arvutamise lisandmooduli jaoks. See konfiguratsioon katab enamiku maksuarvutuse käitumiste nõuded. Seda uuendatakse turu tagasiside põhjal. Kui peate konfiguratsiooni konkreetsetele nõuetele vastamiseks laiendama, vaadake [Kuidas ehitada maksuteenuse laiendust](./tax-service-add-data-fields-tax-integration-by-extension.md) saamaks lisateavet selle kohta, kuidas luua ja valida omamaksukonfiguratsiooni.

14. Pärast **Konfiguratsiooniversiooni** valimist kuvatakse veel mitu vahekaarti. Kohustusliku vahekaardi seadistamiseks järgige siin kuvatud tellimust.

    **Kohustuslik seadistus**

    - **Maksukoodid** - kasutatakse koondandmete säilitamiseks. Kõik sellel vahekaardil loodud maksukoodid sünkroonitakse lahendusega Finance automaatselt, kui lubate praeguse versiooni.
    - **Maksugrupp** – määratlege grupi maksugrupi koondandmed ja maksukoodid.
    - **Maksugrupp** – määratlege grupi maksugrupi koondandmed ja maksukoodid.

    **Valikuline häälestus**

    - **Maksugrupi kohaldatavus** – määratlege maatriks, mis määrab maksugrupi. Kui selle maatriksi kohaldatavusreeglid ei ühti Dynamics 365 maksustatava dokumendiga, maksuarvutus kasutab maksustatava dokumendi real vaikeväärtust.
    - **Maksugrupi kohaldatavus** – määratlege maatriks, mis määrab maksugrupi üksuse. Kui selle maatriksi kohaldatavusreeglid ei ühti Dynamics 365 maksustatava dokumendiga, maksuarvutus kasutab maksustatava dokumendi real vaikeväärtust.
    - **Kliendi maksukohustuslase registreerimisnumbri rakendatavus** - Kui teil on mitu maksuregistreerimise numbrit ühe kliendi kohta, saab maksuarvestuse lisandmoodul õige maksuregistreerimise numbri määrata automaatselt. Määrake selle vahekaardi maatriksis reeglid, mida tuleks määramiseks kasutada. Vastasel juhul jätkavad finants- ja Supply Chain Management käibemaksu registreerimisnumbri vaikenumbri kasutamist müügikannete maksustatavate dokumentide puhul.
    - **Hankija maksukohustuslase registreerimisnumbri rakendatavus** - Kui teil on mitu maksuregistreerimise numbrit ühe hankija kohta, saab maksuarvestuse lisandmoodul õige maksuregistreerimise numbri määrata automaatselt. Määrake selle vahekaardi maatriksis reeglid, mida tuleks määramiseks kasutada. Vastasel juhul jätkavad finants ja Supply Chain Management maksu registreerimisnumbri vaikenumbri kasutamist müügikannete maksustatavate dokumentide puhul.
    - **Loendikoodi rakendatavus** - Määrab automaatselt välja **Loendi kood** väärtuse paindlikumate ja konfigureeritavate reeglite abil. Määrake selle vahekaardi maatriksis reeglid, mida tuleks määramiseks kasutada. Vastasel juhul jätkavad finants- ja Supply Chain Management maksu vaikekoodi kasutamist maksustatavate dokumentide puhul.

14. Vahekaardil **Maksukoodid** valige **Lisa** ning sisestage maksukood ja kirjeldus.
15. Valige **maksukomponent**. Maksukomponent on meetodite grupp, mis määratleti valitud maksukonfiguratsiooni eelmises versioonis. Saadaval on järgmised maksu komponendid:

    - netosumma järgi
    - brutosumma järgi
    - Koguse järgi
    - Marginaali järgi
    - Maks maksult

16. Valige käsk **Salvesta**. Valitud maksukomponendi põhjal on saadaval veel välju.
17. Kasutage järgmisi valikuid maksukoodi olemuse tuvastamiseks:

    - On vabastatud
    - On kasutusmaks
    - On pöördtasu
    - Välista baassumma arvutamisel

    Kasutusmaksu stsenaariumi korral seadistage positiivne maksumäär ja märkige see kui **Kasutusmaks**.

    Pöördtasu stsenaariumi korral seadistage kaks maksukoodi, millest ühel on positiivne maksumäär ja teine, millel on negatiivne maksumäär, kuid sama määra väärtus. Märkige negatiivne maksukood kui **Pöördtasu**. Lisateavet finantsis pöördtasu lahenduse kohta vt [Pöördtasu mehhanism VAT/GST skeem](emea-reverse-charge.md).

    Mõne maksutüübi puhul, mis tuleks hinna maksu baassumma arvutusest inklusiivsete kannete korral välistada (näiteks mõne riigi tollimaksud) valige märkeruut **Välista baasmaksusumma arvutus** . Selle parameetri kohta lisateabe saamiseks vt teemat [Hinnale maksu arvutamine, kui hinnad sisaldavad makse on lubatud](global-exclude-from-tax-base-amount-calculation.md).

    Halda maksumäärasid ja maksusumma limiite selle maksukoodi jaoks.

18. Korrake samme 14–17 kõigi vajalike maksukoodide lisamiseks.
19. Vahekaardil **Maksugrupp** valige veerg **Maksugrupp**, lisage see maatriksisse sisestustingimusena ja seejärel lisage read maksugrupi koondandmete säilitamiseks.

    Siin on näide.

    | Maksugrupp    | Maksukoodid           |
    | ------------ | ------------------- |
    | DEU_Domestic | DEU_VAT19; DEU_VAT7 |
    | DEU_EL       | DEU_Vabastus          |
    | BEL_Domestic | BEL_VAT21; BEL_VAT6 |
    | BEL_EL       | BEL_Vabastus          |

20. Vahekaardil **Maksugrupp** valige veerg **Üksuse maksugrupp**, lisage see maatriksisse sisestustingimusena ja seejärel lisage read maksugrupi koondandmete säilitamiseks.

    Siin on näide.

    | Kauba käibemaksugrupp | Maksukoodid                                    |
    | -------------- | -------------------------------------------- |
    | Täis           | DEU_VAT19; BEL_VAT21; DEU_Vabastus; BEL_Vabastus |
    | Alandatud        | DEU_VAT7; BEL_VAT6; DEU_Vabastus; BEL_Vabastus   |

21. Vahekaardil **Maksukoodide kohaldatavus** valige veerud, mis on nõutavad õige maksugrupi määramiseks, ja seejärel valige **Lisa**. Sisestage või valige väärtused iga veeru jaoks. **Maksugrupi** väli on selle maatriksi väljund. Kui see vahekaart ei ole konfigureeritud, kasutatakse kandereal käibemaksugruppi.

    Siin on näide.

    | Äriprotsess | Kust lähetatud | Saaja | Maksugrupp    |
    | ---------------- | --------- | ------- | ------------ |
    | Müük            | DEU       | DEU     | DEU_Domestic |
    | Müük            | DEU       | FRA     | DEU_EL       |
    | Müük            | BEL       | BEL     | BEL_Domestic |
    | Müük            | BEL       | FRA     | BEL_EL       |

22. Vahekaardil **Maksukoodide kohaldatavus** valige veerud, mis on nõutavad õige maksugrupi määramiseks, ja seejärel valige **Lisa**. Sisestage või valige väärtused iga veeru jaoks. **Maksugrupi üksus** väli on selle maatriksi väljund. Kui see vahekaart ei ole konfigureeritud, kasutatakse kandereal käibemaksugruppi.

    Siin on näide.

    | Kauba kood | Kauba käibemaksugrupp |
    | --------- | -------------- |
    | D0001     | Täis           |
    | D0003     | Alandatud        |

    Lisateavet maksukoodide määramise kohta maksu arvutuses vt [käibemaksugrupi ja kauba käibemaksugrupi määramise loogika](global-sales-tax-group-determination.md).

23. Seadistage ettevõtte vajadustest lähtuvalt kliendimaksude registreerimisnumbrite, müüja maksukohustuslaste registreerimisnumbrite ja loendikoodide rakendatavus.
24. Valige **Salvesta** ja sulgege seejärel leht.
25. Valige **Muuda olekut** \> **Lõpule viidud**. Pärast oleku muutmist olekuks **Lõpetatud** ei saa seda versiooni enam redigeerida.
26. Valige **Muuda olekut** \> **Avalda**. See maksufunktsiooni häälestuse versioon tõugatakse globaalsesse hoidlasse ja on nähtav igale finantsi juriidilisele üksusele.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Maksuarvestuse seadistamine rakenduses Dynamics 365

Pärast seadistuse lõpule viimist RCS-s on teil maksufunktsiooni avaldatud versioon. Järgige neid samme finantside maksuarvestuse häälestamiseks.

Selle jaotise seadistas juriidiline üksus. Peate selle konfigureerima iga juriidilise üksuse jaoks, kelle jaoks soovite finantsis maksuarvestuse lubada.

1. Rakenduses Finance minge **Maks** \> **Seadistamine** \> **Maksukonfiguratsioon** \> **Maksuarvutuse parameetrid**.
2. Vahekaardil **Üldine** määrake järgmised väljad.

    - **Luba maksuarvutuse teenus** – Märkige see ruut, et lubada juriidilisele üksusele maksuarvutus. Kui see ei ole praegusele juriidilisele üksusele lubatud, kasutab juriidiline isik maksu määramiseks ja arvutamiseks olemasolevat maksumootorit.
    - **Funktsiooni häälestus** – Valige juriidiliseüksuse avaldatud maksu funktsiooni häälestus ja versioon. Lisateavet avaldatud maksufunktsiooni seadistamis- ja lõpuleviimise kohta vt selle teema eelmisest jaotisest.
    - **Äriprotsess** – valige lubatud äriprotsessid.

3. Määratlege vahekaardil **Arvutus** juriidilise isiku eeldatav ümardamisreegel. Lisateavet ümardamisloogika kohta vt [maksu arvutamise ümardamisreeglid](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Määratlege vahekaardil **Tõrkekäsitlus** juriidilise isiku eeldatav tõrke käsitlemise meetod. Saadaval on järgmised kolm valikut:

    - Ei
    - Hoiatus
    - Viga

    Iga tulemusekoodi jaoks saate jaotises **Üksikasjad** seadistada tõrke käsitlemise meetodi. Kui mõnda tulemusekoodi ei ole maksuarvestuse teenusest sünkroonitud, saate seadistada vaikemeetodi ka jaotises **Üldine**.

5. Vahekaardil **Mitme KM-i registreerimine** saate lülitada KM-i deklaratsioone, EL-i käibenimekirja ja Intrastati eraldi, et töötada mitme KM-i registreerimisstsenaariumiga. Lisateavet mitme käibemaksuregistreerimise maksuaruandluse kohta vt [mitme KM-i registreerimise aruandlus](emea-reporting-for-multiple-vat-registrations.md).
6. Salvestage seadistus ja korrake eelmiseid samme iga täiendava juriidilise isiku puhul. Kui uus versioon avaldatakse ja soovite seda rakendada, seadistage **Funktsiooni häälestus** väljal **Üldine** vahekaardil **Maksu arvutamise parameetrite** lehel (vt 2. juhist).
