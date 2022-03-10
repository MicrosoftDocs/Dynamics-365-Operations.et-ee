---
title: Commerce’i kanalite fiskaalüksuse integreerimise seadistamine
description: Sellest teemast leiate juhised kaubanduse kanalite fiskaalüksuse integratsiooni funktsiooni seadistamise kohta.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c15104e0f34c1f6cb6a599d506dad741be3e5e9e
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388386"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Commerce’i kanalite fiskaalüksuse integreerimise seadistamine

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Sellest teemast leiate juhised kaubanduse kanalite fiskaalüksuse integratsiooni funktsiooni seadistamise kohta. Lisateavet fiskaalüksuse integratsiooni kohta vt teemast [Kaubanduse kanalite fiskaalüksuse integratsiooni ülevaade](fiscal-integration-for-retail-channel.md).

## <a name="set-up-commerce-parameters"></a>Äriparameetrite seadistamine

1. Valige lehel **Kaubanduse ühisparameetrid** vahekaardil **Üldine** suvandi **Luba fiskaalüksuse integratsioon** sätteks **Jah**.
1. Määratlege vahekaardil **Numbriseeriad** järgmiste viidete jaoks numbriseeriad.

    - Fiskaalüksuse tehnilise profiili number
    - Fiskaalkonnektori grupi number
    - Registreerimisprotsessi number

1. Määratlege lehel **Kaubanduse parameetrid** fiskaalüksuse funktsiooniprofiili numbri jaoks numbriseeria.

    > [!NOTE]
    > Numbriseeriad on valikulised. Kõigi fiskaalüksuse integratsiooniüksuste puhul saab numbrid luua kas numbriseeriate põhjal või käsitsi.

## <a name="set-up-a-fiscal-registration-process"></a>Fiskaalüksuse registreerimisprotsessi seadistamine

Fiskaalüksuse integratsiooni seadistamise protsess hõlmab järgmisi ülesandeid.

- Fiskaalüksuse registreerimiseks kasutatavaid fiskaalseadmeid või -teenuseid tähistavate fiskaalkonnektorite, nt fiskaalprinterid, konfigureerimine.
- Fiskaalseadmetes või -teenustes fiskaalkonnektorite abil registreeritavaid fiskaaldokumente loovate dokumendipakkujate konfigureerimine.
- Fiskaalüksuse registreerimise registreerimisetappide jada ning iga etapi puhul kasutatavate fiskaalkonnektoreid ja fiskaaldokumendi pakkujaid määratleva fiskaalüksuse registreerimisprotsessi konfigureerimine.
- Fiskaalüksuse registreerimisprotsessi määramine kassa funktsiooniprofiilidele.
- Konnektori tehniliste profiilide määramine riistvaraprofiilidele.
- Määrake konnektori tehnilised profiilid müügikoha riistvarale või funktsiooniprofiilidele.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Fiskaaldokumendi pakkujate konfiguratsioonide üleslaadimine

Fiskaaldokumendi pakkuja vastutab fiskaaldokumentide loomise eest, mis tähistavad kandeid ja sündmusi, mis on kassas registreeritud vormingus, mida kasutatakse ka fiskaalseadme või -teenusega suhtlemiseks. Näiteks võib fiskaaldokumendi pakkuja luua fiskaalsissetuleku esituse XML-vormingus.

Fiskaaldokumendi pakkujate konfiguratsioonide üleslaadimiseks järgige neid samme.

1. Minge Commerce headquartersi finantsdokumendi pakkujate lehele **(jaemüügi** ja ärikanali häälestus **\> Fiskaaldokumendi \> pakkujad \>).**
1. Laadige üles XML-konfiguratsioon iga seadme või teenuse jaoks, mida plaanite kasutada.

> [!TIP]
> Valides käsu **Kuva**, saate vaadata kõiki funktsiooniprofiile, mis on seotud praeguse fiskaaldokumendi pakkujaga.

> [!NOTE]
> Andmetüüpide vastendamist käsitletakse fiskaaldokumendi pakkuja osana. Samale konnektorile erinevate vastenduste loomiseks (nt riigipõhised määrused), tuleb luua erinevad fiskaaldokumendi pakkujad.

### <a name="upload-configurations-of-fiscal-connectors"></a>Laadi üles fiskaalkonnektorite konfiguratsioonid

Fiskaalkonnektor vastutab fiskaalseadme või -teenusega suhtlemise eest. Näiteks võib fiskaalkonnektor saata fiskaalprinterile fiskaalsissetuleku, mille fiskaaldokumendi pakkuja lõi XML-vormingus. Lisateavet fiskaalintegratsiooni komponentide kohta vt fiskaalregistreerimisprotsessist [ja fiskaalintegratsiooni näidised fiskaalseadmetest ja teenustest](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Fiskaalkonnektorite konfiguratsioonide üleslaadimiseks järgige neid samme.

1. Minge Commerce Headquartersi lehele Fiskaalühendused (jaemüügi **ja ärikanali** häälestus **Fiskaalintegratsiooni \>\> fiskaalühendused \>).**
1. Laadige üles XML-konfiguratsioon iga seadme või teenuse jaoks, mida plaanite kasutada fiskaalintegratsiooni eesmärkidel.

> [!TIP]
> Valides käsu **Kuva**, saate vaadata kõiki funktsiooni- ja tehnilisi profiile, mis on seotud praeguse fiskaalkonnektoriga.

Fiskaalkonnektorite ja fiskaaldokumendi pakkujate konfiguratsiooni näidised leiate teemast [Fiskaalüksuse integratsiooni näidised Commerce SDK-s](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Loo konnektori funktsiooniprofiilid

Konnektori funktsiooniprofiilide loomiseks järgige neid samme.

1. Minge Commerce headquartersi konnektori funktsiooniprofiilide **lehele** (Jaemüügi **ja ärikanali \> häälestuse \> Fiskaalintegratsiooni konnektori \> funktsiooniprofiilid**).
1. Looge fiskaalühenduse ja fiskaaldokumendi pakkuja iga selle fiskaalühendusega seotud kombinatsiooni jaoks konnektori funktsiooniprofiil järgmiste sammude abil:

    1. Valige konnektori nimi.
    1. Valige dokumendipakkuja.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Muuda andmevastenduse parameetreid konnektori funktsiooniprofiilis

Saate muuta andmetüüpide vastendamise parameetreid konnektori funktsiooniprofiilis. Järgmises tabelis on toodud mõned näited andmevastendusparameetritest konnektori funktsiooniprofiilis.

| Parameeter | Vorming | Näide |
|-----------|--------|---------|
| KM-määrade seadistamine | väärtus: KM-määr | 1 : 2000, 2 : 1800 |
| KM-koodide vastendamine | KM-kood: väärtus | KM20 : 1, KM18 : 2 |
| Maksevahendi tüüpide vastendamine | TenderType: väärtus | Sularaha: 1 kaart: 2 |

Fiskaaldokumendi pakkuja konfiguratsioonis määratletud vaikeparameetrite taastamiseks valige **suvand Uuenda konnektori** funktsiooniprofiilide **lehel**.

> [!NOTE]
> Konnektori funktsiooniprofiilid on ettevõttekohased. Kui plaanite kasutada fiskaalühenduse ja finantsdokumendi pakkuja sama kombinatsiooni erinevate ettevõtete jaoks, peate looma igale ettevõttele konnektori funktsiooniprofiili.

### <a name="create-connector-technical-profiles"></a>Loo konnektori tehnilised profiilid

Konnektori tehniliste profiilide loomiseks järgige neid samme.

1. Minge Commerce headquartersi konnektori tehniliste profiilide **lehele** (Jaemüügi **ja ärikanali \> häälestus \> Finantsintegratsiooni konnektori \> tehnilised profiilid**).
1. Looge konnektori tehniline profiil igale fiskaalühendusele järgmiste sammude abil:

    1. Valige konnektori nimi.
    1. Valige ühenduse tüüp:

        - Riistvarajaamaga ühendatud või kohalikus võrgus pakutavate seadmete ja teenuste jaoks valige **Kohalik**.
        - Valige väliste teenuste jaoks **väline**.
        - Sisemiste ühenduste jaoks commerce runtime's (CRT) valige **Sisemine**. 

    1. Valige konnektori asukoht:

        - Kui ühendus asub riistvarajaamas, valige **riistvarajaam**.
        - Kui konnektor asub kassaregistris, valige **register**.

Parameetreid konnektori tehnilise profiili vahekaartidel **Seade** ja **Sätted** saab muuta. Vaikeparameetrite taastamiseks, mis on määratletud fiskaalkonnektori konfiguratsioonis, valige käsk **Värskenda**. XML-i konfiguratsiooni uue versiooni laadimise ajal saate te sõnumi, mis näitab, et praegune fiskaalkonnektor või finantsdokumendi pakkuja on juba kasutusel. See protseduur ei kirjuta üle konnektori funktsiooni- ja tehnilistele profiilidele varem käsitsi tehtud muudatusi. Vaikeparameetrite komplekti rakendamiseks uues konfiguratsioonis valige suvand Uuenda kas **lehel Konnektori** **funktsiooniprofiilid või Konnektori** tehnilised profiilid **.**

Kui peate üksiku kassaregistri või kaupluse jaoks seadistama kindlad parameetrid, järgige neid samme.

1. **Valige alistamise** menüükäsk.
1. **Looge alistamise** lehel uus kirje.
1. Valige kauplus või kassaregister. Valitud tehnilised profiili parameetrid saate alistada üksiku kassaregistri või kõigi kassaregistrite jaoks üksikus kaupluses.
1. Sisestage **vahekaardil** Seade parameetrid valitud kassaregistri või kaupluse jaoks.

### <a name="create-fiscal-connector-groups"></a>Fiskaalühenduse gruppide loomine

Fiskaalkonnektori grupp ühendab fiskaalkonnektorite, mis teostvad samu funktsioone ja mida kasutatakse fiskaalüksuse registreerimise protsessi samas etapis, funktsiooniprofiile. Näiteks kui kaupluses saab kasutada mitut fiskaalprinteri mudelit, saab nende fiskaalprinterite fiskaalkonnektorid koondada fiskaalkonnektorite gruppi.

Fiskaalühenduse grupi loomiseks järgige neid samme.

1. Minge lehele Fiscal **Connectori grupp** (**Jaemüügi- ja ärikanali häälestus \>\> Fiskaalintegratsiooni fiskaalühenduse \> grupid**).
1. Looge uus fiskaalühenduse grupp.
1. Konnektori grupile funktsiooniprofiilide lisamine. Valige vahekaardil **Funktsiooniprofiilid** suvand **Lisa** ja valige profiili number. Konnektorite grupis saab igal fiskaalkonnektoril olla ainult üks funktsiooniprofiil.
1. Funktsiooniprofiili kasutamise peatamiseks valige suvandi **Keela** sätteks **Jah**. See muudatus mõjutab ainult praegust konnektorigruppi. Saate jätkata sama funktsiooniprofiili kasutamist teistes konnektorigruppides.

### <a name="create-a-fiscal-registration-process"></a>Fiskaalregistreerimisprotsessi loomine

Fiskaalüksuse registreerimisprotsess määratletakse registreerimisetappide jada ja igas etapis kasutatava konnektorigrupi järgi.

Fiskaalregistreerimisprotsessi loomiseks järgige neid samme.

1. Minge Commerce Headquartersi fiskaalregistreerimise protsessi lehele (jaemüügi **ja ärikanali häälestus** **Fiskaalintegratsiooni fiskaalregistreerimise \> protsessid \>).\>**
1. Looge iga kordumatu finantsregistreerimisprotsessi jaoks uus kirje.
1. Lisage protsessile registreerimistoiminguid järgmiste sammude abil:

    1. Valige **Lisa**.
    1. Valige fiskaalkonnektori tüüp.
    1. Valige väljal **Grupi number** sobiv fiskaalkonnektorite grupp.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Määrake fiskaalregistreerimisprotsessi üksused kassaprofiilidele

Fiskaalregistreerimise protsessi üksuste määramiseks kassa profiilidele järgige neid samme.

1. Minge commerce headquartersi kassa funktsiooniprofiilide **lehele** (**Rakenduse Retail ja Commerce \> Channel häälestus kassa \> häälestuse \> kassaprofiilid \> Funktsiooniprofiilid**). 
1. Määrake fiskaalregistreerimise protsess kassa funktsiooniprofiilile.
1. Valige käsk **Redigeeri** ja seejärel valige vahekaardil **Fiskaalüksuse registreerimisprotsess** väljalt **Protsessi number** soovitud protsess.
1. Valige vahekaardil **Finantsteenused** konnektori tehnilised profiilid konnektori asukoha **registriga**.
1. Minge kassa riistvaraprofiili **lehele** (**jaemüügi ja ärikanali \> häälestuse \> kassa \> häälestuse kassaprofiilid \> Riistvaraprofiilid**).
1. Määrake konnektori tehnilised profiilid riistvaraprofiilile. 
1. Valige **käsk** Redigeeri ja seejärel lisage **rida vahekaardilE** Finantsvaluutad. 
1. Valige profiili **numbri väljal** konnektori tehniline profiil.
1. Valige vahekaardil **Rahandusseadmete ühendus** tehnilised profiilid konnektori asukoha **riistvarajaamaga**.

> [!NOTE]
> Samale riistvaraprofiilile saab lisada mitu tehnilist profiili. Siiski peab riistvaraprofiilil või kassa funktsiooniprofiilil olema mis tahes fiskaalkonnektorite grupiga ainult üks ühisosa.

Fiskaalregistreerimise voo määrab fiskaalregistreerimise protsess ja ka mõned fiskaalintegratsiooni komponentide parameetrid: CRT fiskaaldokumendi pakkuja laiend ja fiskaalühenduse riistvarajaama laiend.

- Sündmuste ja kannete tellimus fiskaalüksuse registreerimisele on eelmääratletud fiskaaldokumendi pakkujas.
- Fiskaaldokumendi pakkuja vastutab ka fiskaalüksuse registreerimiseks kasutatava fiskaalkonnektori tuvastamise eest. See vastab konnektori funktsiooniprofiilidele, mis on kaasatud fiskaalüksuse registreerimise protsessi praeguse etapi jaoks määratud fiskaalkonnektorite gruppi koos konnektori tehnilise profiiliga, mis on määratud kassaga seotud riistvarajaama riistvaraprofiilile.
- Fiskaaldokumendi pakkuja kasutab fiskaaldokumendi pakkuja konfiguratsiooni andmetüüpide vastenduse sätteid kannete/sündmuste andmete, nagu maksud ja maksed, teisendamiseks fiskaaldokumendi loomise ajal.
- Kui fiskaaldokumendi pakkuja loob fiskaaldokumendi, võib fiskaalkonnektor saata selle samal kujul fiskaalseadmele või selle sõeluda ja teisendada seadme rakendusliidese (API) käskude jadaks olenevalt sellest, kuidas kommunikatsiooni käsitletakse.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Saate häälestada fiskaalregistreerimise piirangutega kassaaparaate.

Saate valida registrid, kus fiskaalregistreerimine on keelatud, näiteks juhul, kui peate nendele seadmetele tagama ainult mitterahaliste toimingute (nt tootekataloogi otsing, kliendi otsing või kande mustandi loomine).

Finantsregistreerimispiirangutega registrite häälestamiseks järgige neid samme.

1. Minge Commerce Headquartersi jaemüügi ja ärikanali häälestuse **\> fiskaalintegratsiooni \> finants registreerimisprotsessidesse \>**.
1. Valige nõutav protsess.
1. Valige kassaregistrid **, mille kohta on fiskaalprotsessi piirangud** vahekaart.
1. Lisage kassaaparaate vastavalt vajadusele rahandusprotsessi piirangutega.

### <a name="validate-the-fiscal-registration-process"></a>Kinnitage fiskaalregistreerimise protsess.

Finantsregistreerimise protsessi on soovitatav kontrollida järgmistel juhtudel:

- Olete kõik uue registreerimisprotsessi sätted lõpule viinud. Need sätted hõlmavad registreerimisprotsesside määramist kassa funktsiooniprofiilidele ja riistvaraprofiilidele.
- Olete olemasolevat fiskaalregistreerimise protsessi teinud muudatusi ja need muudatused võivad põhjustada erineva fiskaalühenduse valiku käitusajal. (Näiteks olete muutnud fiskaalregistreerimisprotsessi etapi konnektorigruppi, aktiveerinud konnektori funktsionaalse profiili konnektorigrupis või lisanud konnektori gruppi uue konnektori funktsiooniprofiili.)
- Olete teinud muudatusi konnektori tehniliste profiilide määramisel riistvaraprofiilidele.

Fiskaalregistreerimisprotsessi kinnitamiseks järgige neid samme.

1. Minge Commerce Headquartersi fiskaalregistreerimise protsessi lehele (jaemüügi **ja ärikanali häälestus** **Fiskaalintegratsiooni fiskaalregistreerimise \> protsessid \>).\>**
1. Valige **suvand Kinnita** fiskaalregistreerimise protsessi kinnitamiseks.
1. Käivitage lehel **Jaotusgraafik** tööd **1070** ja **1090**, et edastada andmed kanali andmebaasile.

## <a name="set-up-fiscal-texts-for-discounts"></a>Fiskaaltekstide seadistamine allahindluste jaoks

Mõnel juhul tuleb allahindluse kohaldamisel printida fiskaalsissetulekule spetsiaalne tekst. Saate allahindluste fiskaaltekstid seadistada lehel **Fiskaalkonnektorite grupp** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalkonnektorite grupid**).

- Kassas kohaldatavate käsitsi allahindluste puhul tuleb määrata fiskaaltekst teabekoodile või teabekoodigrupile, mis on määratud kassa funktsiooniprofiilis teabekoodina **Toote allahindlus**.

    1. Valige lehel **Fiskaalkonnektorite grupp** suvand **Fiskaalsissetuleku tekst**.
    1. Valige vahekaardil **Teabekoodid** käsk **Lisa** ja valige teabekood või teabekoodigrupp.
    1. Valige väljal **Teabekoodi number** soovitud väärtus.
    1. Väljal **Alamkoodi number** valige väärtus, kui valitud teabekoodi puhul on vajalik alamkood.
    1. Väljal **Fiskaalsissetuleku tekst** määrake fiskaaltekst, mis tuleb fiskaalsissetulekule printida.
    1. Valige suvandi **Prindi kasutaja sisend fiskaalsissetulekule** sätteks **Jah**, et asendada fiskaalsissetulekul olev tekst teabega, mille kasutaja kassas käsitsi sisestab. See suvand kehtib ainult teabekoodide puhul, mille sisendtüüp on **Tekst**.

    > [!NOTE]
    > Saate määrata fiskaalteksti mitmele teabekoodile, et toetada stsenaariume, milles kasutatakse teabekoodigruppe, lingitud teabekoode ja käivitatud teabekoode. Nende stsenaariumide puhul sisaldab fiskaalsissetulek fiskaaltekste kõigist teabekoodidest, mis on lingitud kandereaga, millele kohaldub allahindlus.

- Kanalipõhiste allahindluste puhul peate määratlema fiskaalteksti allahindluse ID-le.

    1. Valige lehel **Fiskaalkonnektorite grupp** suvand **Fiskaalsissetuleku tekst**.
    1. Valige lehel **Allahindluse** käsk **Lisa** ja valige allahindluse ID.
    1. Väljal **Fiskaalsissetuleku tekst** määrake fiskaaltekst, mis tuleb fiskaalsissetulekule printida.

    > [!NOTE]
    > Kui samale kandereale kohaldub mitu allahindlust, sisaldab fiskaalsissetulek fiskaaltekste kõigist selle kandereaga lingitud allahindlustest.

## <a name="set-error-handling-settings"></a>Tõrketöötluse sätete määramine

Fiskaalüksuse integratsioonis saadaolevad tõrketöötluse sätted määratakse fiskaalüksuse registreerimisprotsessis. Lisateavet tõrketöötluse kohta fiskaalüksuse integratsioonis vt teemast [Tõrketöötlus](fiscal-integration-for-retail-channel.md#error-handling).

Tõrke käsitlemise sätete häälestamiseks järgige neid samme.

1. Lehel **Fiskaalüksuse registreerimisprotsess** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalüksuse registreerimisprotsessid**) saate määrata fiskaalüksuse registreerimisprotsessi iga etapi kohta järgmised parameetrid.

    - **Luba vahelejätmine** – see parameeter lubab tõrketöötluse dialoogiboksis suvand **Jäta vahele**.
    - **Luba registreerituks märkimine** – see parameeter lubab tõrketöötluse dialoogiboksis suvandi **Märgi registreerituks**.
    - **Luba edasi** lükkamine – see parameeter lubab **tõrgete** käsitlemise dialoogiboksis valikut Lükka edasi.
    - **Jätka tõrke korral** – kui see parameeter on lubatud, saab fiskaalüksuse registreerimise protsess kande või sündmuse fiskaalüksuse registreerimise nurjumise korral kassaregistris tegevust jätkata. Muidu peaks operaator järgmisel kandel või sündmusel fiskaalüksuse registreerimise käitamise jaoks nurjunud fiskaalüksuse registreerimist uuesti proovima, selle vahele jätma või märkima kande või sündmuse registreerituks. Lisateavet vaadake teemast [Valikuline fiskaalüksuse registreerimine](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Kui lubatud on parameeter **Jätka tõrke korral**, siis on parameetrid **Luba vahelejätmine** ja **Luba registreerituks märkimine** automaatselt keelatud.

1. Tõrgete **käsitlemise** dialoogiboksis **registreeritud valikute** Vahelejätmine ja Märkimine jaoks **nõuab, et suvand Luba registreerimine vahele jätta või registreeritud** õigusena märkimine oleks lubatud. Õiguse lubamiseks minge **õiguste** gruppide lehele (**Jaemüügi \>\>** ja äri töötajate õiguste grupid) **ja seadke suvandi Luba registreerimine vahelejätmine või märgi** registreeritud suvandiks **Jah**.
1. Tõrgete **käsitlemise** dialoogiakna suvand Lükka edasi nõuab, et luba edasi **lükkamine** oleks lubatud. Loa lubamiseks minge õiguste gruppide **lehele** (**Jaemüügi \>\>** ja äri töötajate õiguste grupid) ja **seadke suvandi Luba edasilükkumine väärtuseks** **Jah.**
1. **Suvandite Jäta** vahele, Märgi kui registreeritud **ja Lükka edasi** **valikud lubavad operaatoritel sisestada täiendavat teavet,** kui fiskaalregistreerimine nurjub. Funktsiooni kättesaadavaks määramiseks peate määrama **fiskaalühenduse** **grupis** jätte, **märgi** kui registreeritud ja lükkama teabekoodid edasi. Seejärel salvestatakse operaatorite sisestatav teave teabekoodi kandena, mis on lingitud fiskaalkandega. Lisateavet teabekoodide kohta vt teemast [Teabekoodid ja teabekoodigrupid](../info-codes-retail.md).

    > [!NOTE]
    > Käivitusfunktsiooni **Toode** ei toetata teabekoodide puhul, mida kasutatakse fiskaalkonnektorite gruppides suvandite **Jäta vahele** ja **Märgi registreerituks** puhul.

    - Valige Fiskaalühenduse **grupi** **·** **lehe** teabekoodide vahekaardil teabekoodid või teabekoodigrupid väljadel Jäetud, Märgi **kui registreeritud** ja Edasi **lükatud**.

    > [!NOTE]
    > Fiskaalüksuse registreerimisprotsessi mis tahes etapis saab luua ühe fiskaaldokumendi ja ühe mittefiskaaldokumendi. Fiskaaldokumendi pakkuja laiendus tuvastab iga kande või sündmuse tüübi seose fiskaal- või mittefiskaaldokumentidega. Tõrketöötluse funktsioon kohaldub ainult fiskaaldokumentidele.
    >
    > - **Fiskaaldokument** – kohustuslik dokument, mis tuleb edukalt registreerida (nt fiskaalsissetulek).
    > - **Mittefiskaaldokument** – kande või sündmuse lisadokument (nt kinkekaardi sedel).

1. Kui operaator peab pärast seisundikontrolli tõrke esinemist olema võimeline jätkama praeguse operatsiooni (näiteks kande loomine või lõpetamine) protsessi, siis peaksite lubama loa **Luba seisundikontrolli tõrge vahele jätta**, mille leiate lehelt **Lubade grupid** (**Jaemüük ja kaubandus \> Töövõtjad \> Lubade grupid**). Lisateavet seisundikontrolli protseduuri kohta leiate teemast [Fiskaalüksuse registreerimise seisundikontroll](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Fiskaalüksuse x-/z-aruannete seadistamine kassast

Fiskaalüksuse x-/z-aruannete käitamise lubamiseks kassast peate lisama kassa ekraanipaigutusse uued nupud.

- Järgige lehel **Nupupaneelid** teemas [Kassatoimingute lisamine kassa paigutustele nupupaneeli koostaja abil](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) toodud juhiseid kujundaja installimiseks ja kassa ekraanipaigutuse värskendamiseks.

    1. Valige värskendatav paigutus. 
    1. Lisage uus nupp ja määrake nupu **Prindi fiskaalüksuse x** atribuut.
    1. Lisage uus nupp ja määrake nupu **Prindi fiskaalüksuse z** atribuut.
    1. Käivitage lehel **Jaotusgraafik** töö **1090**, et edastada muudatused kanali andmebaasile.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Edasi lükatud fiskaalüksuse registreerimise käsitsi käivitamise lubamine

Edasi lükatud fiskaalüksuse registreerimise käsitsi käivitamise lubamiseks peaksite kassa paigutusse lisama uue nupu.

- Järgige lehel **Nupupaneelid** teemas [Kassatoimingute lisamine kassa paigutustele nupupaneeli koostaja abil](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) toodud juhiseid kujundaja installimiseks ja kassa ekraanipaigutuse värskendamiseks.

    1. Valige värskendatav paigutus.
    1. Lisage uus nupp ja määrake nupu atribuut **Lõpeta fiskaalüksuse registreerimise protsess**.
    1. Käivitage lehel **Jaotusgraafik** töö **1090**, et edastada teie muudatused kanali andmebaasile.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
