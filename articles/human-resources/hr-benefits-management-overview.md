---
title: Soodustuste halduse ülevaade
description: Selles teemas antakse ülevaade rakenduse Dynamics 365 Human Resources soodustuste halduse funktsioonist.
author: twheeloc
ms.date: 12/06/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e53a68aed2e4b1e0b0d7797e7326e223c47443f4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687187"
---
# <a name="benefits-management-overview"></a>Soodustuste halduse ülevaade


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Konkurentsivõime säilitamiseks peate pakkuma parimate töövõtjate meelitamiseks ja säilitamiseks rikkalikku soodustuste komplekti. Lisaks tavapärastele soodustustele, nagu ravi- ja hambaravikindlustus, võite tahta pakkuda ka laiendatud teenuseid, nagu abi adopteerimisel, vabaajaprogrammid ja toetus töörõivaste jaoks. Rakenduse Microsoft Dynamics 365 Human Resources soodustuste haldus pakub paindlikku lahendust, mis toetab mitmesuguseid soodustuste võimalusi. Human Resources sisaldab ka hõlpsasti kasutatavat töövõtja kogemust, mis teie pakutavat tutvustab.

- Täiustatud soodustuse plaanid võimaldavad teil luua ja hallata ainulaadseid soodustuse plaane ning toetada keerukaid soodustuse tabeleid ja pesastatud tasemeid. Saate lihtsama töövõtja kogemuse jaoks hõlpsalt luua soodustusprogramme, kogumeid ja automaatse registreerimise reegleid.
- Paindliku krediidiga programmid võimaldavad proportsionaalselt jaotada pensioni- ja teiste elusündmuste toetusi.
- Ulatuslikud sobivusreeglid tagavad, et muudate õigeid soodustused kättesaadavaks õigetele töötajatele.
- Veebipõhine soodustuste registreerimine tagab teie töövõtjatele lihtsa kogemuse.
- Kvalifitseeritud elusündmuse töötlemine toetab tulevasi elusündmusi.

Kui soovite ligipääsu demoandmetelel, peate oma liivakastikeskkonna uuesti juurutama.

> [!NOTE]
> Nüüd saate soodustuste halduslehti kohandada. Lehele **Katvuse valik** saab soodustuste plaanide kohta lisada katvuse määradega seotud kohandatud välju. Lisateavet kohandatud väljadega töötamise kohta leiate teemast [Kohandatud väljad](hr-developer-custom-fields.md).
>
> ![Soodustuste halduse kohandatud väljad](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Soodustuste halduse lubamine

Selles teemas kirjeldatakse, kuidas funktsioone rakenduses Human Resources sisse lülitada. Lisaks selgitab see, millised rakenduse Human Resources olemasolevad funktsioonid soodustuste haldamine pärast soodustuste haldamise sisselülitamist asendab ja keelab.

> [!IMPORTANT]
> Keskkonnas **Tootmine** ei saa soodustuste haldust keelata, kui olete selle lubanud. Enne soodustuste halduse keskkonnas **Tootmine** lubamist soovitame lubada ja testida soodustuste haldust keskkonnas **Liivakast**. Olemasolevate pärandsoodustuse funktsioonide ja uute pärandsoodustuse funktsioonide vahel on olulisi erinevusi, mis vajavad täiendavat seadistamist ja mida tuleks enne tootmise alustamist testida.

Lisateabe saamiseks vaadake jaotist [Funktsioonide haldamine](hr-admin-manage-features.md).

## <a name="process-overview"></a>Protsessi ülevaade

Soodustuste konfigureerimise protsess hõlmab järgmisi ülesandeid.

1.  Seadistage nõutav soodustusteave.
2.  Seadistage valikuline soodustusteave.
3.  Soodustusplaanide häälestus.
4.  Paindkrediidi programmide häälestus (valikuline).
5.  Vajaliku töötaja teabe konfigureerimine.
6.  Valikulise töötaja teabe konfigureerimine.
7.  Töödelge töötajaid abikõlblikkuse kindlakstegemiseks.
8.  Töötajad valivad plaanid töötajate iseteeninduse kaudu (valikuline).
9.  Kinnitage töötaja plaani valikud.
10. Elusündmuse töötlemine (valikuline).
11. Hinnauuendused (valikuline).

## <a name="set-up-required-benefit-information"></a>Seadistage nõutav soodustusteave

Enne, kui töötajaid saab plaanidesse registreerida, tuleb seadistada mitu komponenti:

- **Soodustushalduse parameetrid** – need sätted on ettevõtete vahel ühiskasutuses. Saate seadistada vaikimisi põhjusekoodid, lubada **Soodustuste iga-aastase palga** suvandi, seadistada vaikemaksesageduse uute palkade jaoks ja lubada eluea sündmused. Lisateavet vt teemast [Soodustuste haldamise parameetrite määramine](hr-benefits-setup-parameters.md).
- **Isikliku kontakti sobivuse suvandid** – isiklikud kontaktid on isikud, kes on seadistatud plaanidest kas sõltuvad või kasusaajad. Tavaliselt on need lapsed, abikaasad või usaldusorganisatsioonid. Lisateavet leiate teemast [Isiklike kontaktide sobivuse suvandite konfigureerimine](hr-benefits-setup-contact-eligibility-options.md).
- **Laovarude valikud** - seadistage laovarude tüübid, mis on plaani jaoks saadaval. Määratlege täpsemalt, kes peaks olema kaetud või kui palju laovarusid on saadaval. Lisateabe saamiseks vt jaotist [Laovarude loomine](hr-benefits-setup-coverage-options.md).
- **Plaanitüübid** – seadistage plaanitüübid, mis on soodustusplaani loomisel saadaval. Plaanide tüüpide näidete hulgas on näiteks **Hambaravi**, **Visioon** ja **Hoiukontod**. Mõned olulised sätted plaani tüübil määravad soodustusplaanis saadaolevad sätted. Lisateabe saamiseks vt [Plaani tüüpide loomine](hr-benefits-setup-plan-types.md).
- **Sobivuse reegleid** - kasutatakse selleks, et määrata, kas töötaja on plaani jaoks sobilikud. Iga hüvitisplaaniga peab olema seotud vähemalt üks sobivuse reegel. Lisateavet leiate teemast [Sobivuse reeglite ja suvandite konfigureerimine](hr-benefits-setup-eligibility-rules.md).
- **Maksesagedused** – maksesagedused on nõutavad määrade konfigureerimisel. Intressimääraga kasutatav maksesagedus aitab kindlaks teha summa, mille töötaja ja/või tööandja võlgneb nädalas, kuus või aastas. Lisateavet vt teemast [Maksesageduste seadistamine](hr-benefits-setup-payment-frequencies.md).
- **Määrad** – hinnad määravad, kui palju hüvitis maksab töötajale või tööandjale. Kui töötajale tuleks raha tagasi eraldada (näiteks jõusaali liikmeks krediit), sisestatakse negatiivne määr. Lisateavet vt teemast [Määrade konfigureerimine](hr-benefits-setup-rates.md).
- **Järgu määrad** – järgumäärasid kasutatakse juhul, kui intressimäär peab mõne kriteeriumi alusel muutuma. Kõige tavalisem järgumäär on üks vanusel põhinev kiht. Siiski võib kehtestada ka kaheastmelisi intressimäärasid, kus määr võib muutuda sõltuvalt soost, vanusest või muudest kriteeriumidest.
- **Mahaarvamised** – mahaarvamised on põhiliselt päiseteave/-koodid, mis edastatakse palgasüsteemi kasuks mahaarvamiste tuvastamiseks. Peate need mahaarvamised seadistama, kuna need on soodustusplaanis nõutavad. Lisateavet vt teemast [Mahaarvamiste konfigureerimine](hr-benefits-setup-deductions.md).
- **Soodusperioodid** – soodustusperiood on periood, mil töötajatel on soodustuskatvus. Seda nimetatakse ka plaaniaastaks. Siin seadistatakse ka avatud registreerimisperioodid.

## <a name="set-up-optional-benefit-information"></a>Seadistage valikuline soodustusteave

Soodustusplaani loomiseks ei pea järgmisi komponente seadistama.

- **Programmid** – programm on soodustuste kogum, mida juhivad samad sobivuse reeglid. Näiteks võivad kõik müügiosakonnad mobiiltelefoni saada.
- **Kogumid** – kogum on soodustuste grupp, kus enne lisaplaanide valikut tuleb valida üks plaan. Näiteks võib suure mahaarvatava meditsiiniplaani komplekteerida tervishoiukonto (HSA) plaaniga.
- **Elusündmuse tüübid** – elusündmused on sündmused, mis võimaldavad muuta töötaja katvust. Elusündmuse tüübid on seotud plaanitüübiga. Näiteks võib meditsiiniplaani tüüp lubada plaane muuta sünnituse või lapsendamise või perekonnaseisu muutumise tõttu. Kindlustusplaani tüüp ei pruugi aga elusündmuste tõttu mingeid muudatusi lubada. Lisateavet vt jaotisest [Elusündmuse tüüpide konfigureerimine](hr-benefits-setup-life-event-types.md).
- **Ootepäevad ja -perioodid** – soodustuse ooteperioodi saab seadistada soodustusplaanis. Näiteks võib äsja palgatud töötaja 401(k) registreeruda alles pärast kolme kuud töötamist. Sellisel juhul on ooteaeg kolm kuud. Ootepäevi kasutatakse ooteperioodil, kui uusi registreerimisi saab töödelda ja teenusepakkujale esitada ainult kindlal kuu päeval. Näiteks kui 401(k) registreerimisi saab töödelda alles kuu viieteistkümnendal päeval, pärast kolme kuud töötamist, on seatud ooteaeg kolm kuud ja ootepäev viieteistkümnes. Lisateavet vt jaotisest [Ootepäevade konfigureerimine](hr-benefits-setup-waiting-days.md) ja [Ooteperioodide konfigureerimine](hr-benefits-setup-waiting-periods.md).
- **Põhjuse koodid** – põhjusekoode kasutatakse selgitamiseks, miks soodustus töötaja jaoks võib olla muutunud. Lisateavet põhjusekoodide kohta vt teemast [Põhjusekoodide seadistamine](hr-benefits-setup-reason-codes.md).

## <a name="set-up-benefit-plans"></a>Soodustusplaanide häälestus

Soodustusplaani koostamisel peate enne töötajate registreerimist täitma järgmised sammud.

- Soodustusperioodi määramine.
- Lisa kindlustussuvandid.
- Saate vahekaardil **Üldine** seada kehtivuse algus- ja lõppkuupäeva.
- Määrake vähemalt üks sobivuse reegel.
- Seadistage vahekaardil **Seadistamine** väli **Luba/jätka registreerimist**.

Lisateavet soodustusplaanide seadistamise kohta vt teemast [Soodustusplaanide seadistamine](hr-benefits-plans-setup.md).

## <a name="set-up-flex-credit-programs-optional"></a>Paindkrediidi programmide häälestus (valikuline)

Saate kasutada paindliku krediidiga programme, et registreerida töötajad eelmääratud hulgale paindlikule krediidile. Töötajad saavad valida, kuidas oma paindlikku krediiti jaotada. Näiteks kui töötaja on juba kaetud oma abikaasa tervisekindlustuse plaaniga, ei pea nad tervisekindlustuse jaoks oma krediiti kasutama. Seetõttu võivad nad soovida kasutada neid muude soodustuste jaoks. Lisateavet paindkrediidiprogrammi kohta vt [Paindkrediidiprogrammide seadistamine](hr-benefits-plans-flex-credit-programs.md).

## <a name="configure-required-employee-information"></a>Vajaliku töötaja teabe konfigureerimine

Enne eeliste andmist töötajatele peate sisestama nõutava nendega seotud teabe. 

Töötajale peab olema **määratud** positsioon. Positsiooni **saab** määrata töötajale lehekülgedel Töötaja **või** Positsioon **·**, värskendades **töötajamäärangut**. 

Järgmisena peavad töötajad olema registreerunud põhipalga plaani alguskuupäeval või **neil peab olema iga-aastase hüvitise palgasumma**. Enne fikseeritud tasu **töötajale** määramiseks peab **positsioon** olema määratud. 

> [!NOTE] 
> Põhitasu **alguskuupäev ei saa** olla positsiooni määramise **kuupäevast varem.**

Teise võimalusena, kui teil on töötaja, kes saab täiendavat kompensatsiooni, nagu komisjonitasu, **saate** lisada töötajakirjele soodustused iga-aastase palga summa. Inimressursid kasutavad põhipalga **iga-aastase** summa määratlemisel põhipalga **aastasumma asemel**. **Soodustuste aastane palgasumma** peab kehtima alates töövõtja alustamise kuupäevast või soodustuse perioodi algusest, olenevalt sellest, kumb on hilisem. Siiski ei ole ametikohal vaja määrata soodustuste aastase palga **määramist**. Soodustuste aastapalga funktsiooni lubamiseks minge inimressursside jagatud **parameetrite** lehele soodustuste **halduse vahekaardil**.**See** funktsioon on vaikimisi välja lülitatud.

> [!IMPORTANT]
> Kui töötajale on **sisestatud** nii põhipalk **kui** ka soodustused iga-aastase palga summa, **kasutatakse** kattesummade määramiseks soodustuste aastapalka. **Lehekülje Töötaja jaotises** Tööhõive üksikasjad **peate** valima väärtuse väljal **Soodustuse tasusagedus**.

## <a name="configure-optional-employee-information"></a>Valikulise töötaja teabe konfigureerimine
Kui loote soodustusplaani, mis kasutab sool või vanusel põhinevaid määrasid, peate soodustuse maksumuse arvutamiseks sisestama töötaja sünnikuupäeva ja soo.

## <a name="process-employees-to-determine-eligibility"></a>Töödelge töötajaid abikõlblikkuse kindlakstegemiseks
Enne, kui töötajaid saab plaanidele registreerida, käitatakse sobivuse töötlemine, et määrata, milliste plaanide jaoks nad sobilikud on. Sobivuse protsessi tulemusi saate vaadata protsessi tulemuste **vaaturis**. Lisateavet vt teemast [Protsessi registreerimise sobivus](hr-benefits-process-enrollment-eligibility.md).

## <a name="employees-select-plans-using-employee-self-service-optional"></a>Töötajad valivad plaanid töötaja **iseteeninduse abil** (valikuline)

Avatud registreerimise toimumisel, kui töötajad palgatakse uuesti või toimub elusündmus, saavad töötajad valida või uuendada oma soodustusi **Töötajate iseteeninduse abil**. Lisateavet vt teemast [Töötaja iseteeninduse konfigureerimine](hr-benefits-setup-employee-self-service.md).

## <a name="confirm-employee-plan-selections"></a>Kinnitage töötaja plaani valikud

Soodustused, mille töötajad valivad, tuleb kinnitada enne, kui töötajad loetakse neisse registreerituks. Soodustusi saab valida ka töötaja nimel. Soodustuste valimiseks või kinnitamiseks valige lehel **Töötaja** vahekaardil **Soodustused** valik **Töötaja soodustusplaanid**. Mitme töötaja soodustuste valimiseks või kinnitamiseks kasutage **Töötaja soodustusplaanide hulgivärskenduse** lehte.

## <a name="life-event-processing-optional"></a>Elusündmuse töötlemine (valikuline)

Töötaja töötsükli jooksul võib igal töötajal olla erinevaid elusündmusi, nagu näiteks tööhõive muutused või ülalpeetavate või kasusaajate muutused. Elusündmuste kasutamiseks peate need lubama lehel **Human Resources jagatud parameetrid**. Seadistage plaanitüüpidele elusündmuse tüübid ja elusündmuse valikud.

Enne kui saate elusündmusi töödelda, peate olema käitanud avatud registreerimist vähemalt üks kord värbamise ajavahemikus. Ameerika Ühendriikides on avatud registreerimine tavaliselt üks kord aastas. Väljaspool Ameerika Ühendriike võib avatud registreerimine toimuda värbamise ajal. Elusündmuse töötlemine ei nõua töötajatelt soodustusplaani valimist. Töötajad peavad siiski olema kaasatud avatud registreerimiste töötlemisse. Lisateavet vt järgmistest teemadest:

- [Elusündmuste töötlemine](hr-benefits-process-life-events.md)
- [Elusündmuste muudatuste töötlemine](hr-benefits-process-life-event-changes.md)
- [Elusündmuste sobivuse töötlemine](hr-benefits-process-life-event-eligibility.md)

## <a name="rate-updates-optional"></a>Hinnauuendused (valikuline)

Mõnikord muutub hüvitiste määr plaaniperioodi jooksul. Määrade värskendamiseks töötajate puhul, kes on plaani juba registreeritud, peate need muudatused töötlema. Lisateavet vt teemast [Määramuudatuste töötlemine](hr-benefits-process-rate-changes.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
