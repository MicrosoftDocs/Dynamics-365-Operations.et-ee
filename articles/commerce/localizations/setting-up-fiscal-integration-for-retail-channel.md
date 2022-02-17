---
title: Commerce’i kanalite fiskaalüksuse integreerimise seadistamine
description: Sellest teemast leiate juhised kaubanduse kanalite fiskaalüksuse integratsiooni funktsiooni seadistamise kohta.
author: EvgenyPopovMBS
ms.date: 01/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fd37934e1ebd103d66c5181e0bfb75047f4cb6a3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076959"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Commerce’i kanalite fiskaalüksuse integreerimise seadistamine

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Sellest teemast leiate juhised kaubanduse kanalite fiskaalüksuse integratsiooni funktsiooni seadistamise kohta. Lisateavet fiskaalüksuse integratsiooni kohta vt teemast [Kaubanduse kanalite fiskaalüksuse integratsiooni ülevaade](fiscal-integration-for-retail-channel.md).

## <a name="set-up-commerce-parameters"></a>Saate häälestada Commerce'i parameetreid.

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

### <a name="upload-configurations-of-fiscal-document-providers"></a>Rahandusdokumendi pakkujate konfiguratsioonide üleslaadimine

Fiskaaldokumendi pakkuja vastutab fiskaaldokumentide loomise eest, mis tähistavad kandeid ja sündmusi, mis on kassas registreeritud vormingus, mida kasutatakse ka fiskaalseadme või -teenusega suhtlemiseks. Näiteks võib fiskaaldokumendi pakkuja luua fiskaalsissetuleku esituse XML-vormingus.

Rahandusdokumentide pakkujate konfiguratsioonide üleslaadimiseks tehke järgmist.

1. Avage Commerce'i peakontoris **leht Fiskaaldokumendi pakkujad** (**jae- ja kaubanduskanali \> häälestus \> Fiskaalintegratsiooni \> fiskaaldokumendi pakkujad**).
1. Laadige üles XML-konfiguratsioon iga seadme või teenuse jaoks, mida kavatsete kasutada.

> [!TIP]
> Valides käsu **Kuva**, saate vaadata kõiki funktsiooniprofiile, mis on seotud praeguse fiskaaldokumendi pakkujaga.

> [!NOTE]
> Andmetüüpide vastendamist käsitletakse fiskaaldokumendi pakkuja osana. Samale konnektorile erinevate vastenduste loomiseks (nt riigipõhised määrused), tuleb luua erinevad fiskaaldokumendi pakkujad.

### <a name="upload-configurations-of-fiscal-connectors"></a>Fiskaalkonnektorite konfiguratsioonide üleslaadimine

Fiskaalkonnektor vastutab fiskaalseadme või -teenusega suhtlemise eest. Näiteks võib fiskaalkonnektor saata fiskaalprinterile fiskaalsissetuleku, mille fiskaaldokumendi pakkuja lõi XML-vormingus. Lisateavet fiskaalintegratsiooni komponentide kohta leiate teemast [Fiskaalregistreerimise protsess ja fiskaalseintegratsiooni näidised fiskaalseadmete ja -teenuste jaoks](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Fiskaalkonnektorite konfiguratsioonide üleslaadimiseks tehke järgmist.

1. Avage Commerce'i peakontoris **leht Fiskaalkonnektorid** (**jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalkonnektorid**).
1. Laadige üles XML-konfiguratsioon iga seadme või teenuse jaoks, mida kavatsete kasutada fiskaalse integratsiooni eesmärgil.

> [!TIP]
> Valides käsu **Kuva**, saate vaadata kõiki funktsiooni- ja tehnilisi profiile, mis on seotud praeguse fiskaalkonnektoriga.

Fiskaalkonnektorite ja fiskaaldokumendi pakkujate konfiguratsiooni näidised leiate teemast [Fiskaalüksuse integratsiooni näidised Commerce SDK-s](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Konnektori funktsionaalsete profiilide loomine

Konnektori funktsionaalsete profiilide loomiseks toimige järgmiselt.

1. Avage Commerce'i peakontoris **leht Konnektori funktsionaalsed profiilid** (**jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsiooni konksuktor \> funktsionaalsed profiilid**).
1. Selle fiskaalse konnektoriga seotud fiskaalse konnektori ja fiskaaldokumendi pakkuja iga kombinatsiooni puhul looge konnektori funktsionaalne profiil, järgides järgmisi juhiseid.

    1. Valige konnektori nimi.
    1. Valige dokumendipakkuja.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Andmete vastendamise parameetrite muutmine konnektori funktsionaalses profiilis

Saate muuta andmetüüpide vastendamise parameetreid konnektori funktsiooniprofiilis. Järgmises tabelis on toodud mõned näited andmete kaardistamise parameetritest konnektori funktsionaalses profiilis.

| Parameeter | Vorming | Näide |
|-----------|--------|---------|
| KM-määrade seadistamine | väärtus: KM-määr | 1 : 2000, 2 : 1800 |
| KM-koodide vastendamine | KM-kood: väärtus | KM20 : 1, KM18 : 2 |
| Maksevahendi tüüpide vastendamine | TenderType: väärtus | Sularaha: 1 kaart: 2 |

Finantsdokumendi pakkuja konfiguratsioonis määratletud vaikeparameetrite taastamiseks valige lehel Konnektori funktsionaalsete profiilide **värskendus** **·**.

> [!NOTE]
> Konnektori funktsiooniprofiilid on ettevõttekohased. Kui kavatsete kasutada sama fiskaalse konnektori ja fiskaaldokumendi pakkuja kombinatsiooni erinevate ettevõtete jaoks, peaksite looma iga ettevõtte jaoks konnektori funktsionaalse profiili.

### <a name="create-connector-technical-profiles"></a>Konnektori tehniliste profiilide loomine

Konnektori tehniliste profiilide loomiseks tehke järgmist.

1. Avage Commerce'i peakontoris **leht Connector tehnilised profiilid** (**jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsiooni \> konnektor tehnilised profiilid**).
1. Looge iga fiskaalse konnektori jaoks konnektori tehniline profiil, järgides järgmisi juhiseid.

    1. Valige konnektori nimi.
    1. Valige konnektori tüüp.

        - Seadmete või teenuste puhul, mis on ühendatud riistvarajaamaga või esinevad kohalikus võrgus, valige **Kohalik**.
        - Välisteenuste puhul valige **Väline**.
        - Commerce'i käitusaja (Commerce'i käitusaja)CRT sisemiste konnektorite puhul valige **Sisemine**. 

    1. Valige konnektori asukoht.

        - Kui konnektor asub riistvarajaamas, valige **Riistvarajaam**.
        - Kui konnektor asub kassaregistris, valige **Registreeri**.

Parameetreid konnektori tehnilise profiili vahekaartidel **Seade** ja **Sätted** saab muuta. Vaikeparameetrite taastamiseks, mis on määratletud fiskaalkonnektori konfiguratsioonis, valige käsk **Värskenda**. Kui laaditakse XML-konfiguratsiooni uut versiooni, saate teate, milles öeldakse, et praegust fiskaalse konnektorit või fiskaaldokumendi pakkujat juba kasutatakse. See protseduur ei kirjuta üle konnektori funktsiooni- ja tehnilistele profiilidele varem käsitsi tehtud muudatusi. Uue konfiguratsiooni parameetrite vaikekomplekti rakendamiseks valige Värskenda lehel Konnektori funktsionaalsed profiilid **või** lehel Konnektori tehnilised profiilid **.** **·**

Kui peate seadistama konkreetse kassaaparaadi või -poe jaoks kindlad parameetrid, järgige neid juhiseid.

1. Valige **menüükäsk Alistamine**.
1. **Looge lehel Alistamine** uus kirje.
1. Valige kauplus või kassaaparaat. Valitud tehnilise profiili parameetreid saate alistada üksiku kassaregistri või kõigi kassaregistrite jaoks üksikus kaupluses.
1. Sisestage vahekaardile **Seade** valitud kassaaparaadi või -poe parameetrid.

### <a name="create-fiscal-connector-groups"></a>Fiskaalse konnektorigruppide loomine

Fiskaalkonnektori grupp ühendab fiskaalkonnektorite, mis teostvad samu funktsioone ja mida kasutatakse fiskaalüksuse registreerimise protsessi samas etapis, funktsiooniprofiile. Näiteks kui kaupluses saab kasutada mitut fiskaalprinteri mudelit, saab nende fiskaalprinterite fiskaalkonnektorid koondada fiskaalkonnektorite gruppi.

Fiskaalse konnektorigrupi loomiseks tehke järgmist.

1. Avage **leht Fiskaalkonnektori rühm** (**jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalse konnektorigrupid**).
1. Looge uus fiskaalse konnektori grupp.
1. Konnektori grupile funktsiooniprofiilide lisamine. Valige vahekaardil **Funktsiooniprofiilid** suvand **Lisa** ja valige profiili number. Konnektorite grupis saab igal fiskaalkonnektoril olla ainult üks funktsiooniprofiil.
1. Funktsiooniprofiili kasutamise peatamiseks valige suvandi **Keela** sätteks **Jah**. See muudatus mõjutab ainult praegust konnektorigruppi. Saate jätkata sama funktsiooniprofiili kasutamist teistes konnektorigruppides.

### <a name="create-a-fiscal-registration-process"></a>Finantsregistreerimise protsessi loomine

Fiskaalüksuse registreerimisprotsess määratletakse registreerimisetappide jada ja igas etapis kasutatava konnektorigrupi järgi.

Finantsregistreerimise protsessi loomiseks tehke järgmist.

1. Avage Commerce'i peakontoris **eelarve registreerimise protsessi** leht (**jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalne registreerimisprotsessid**).
1. Looge iga kordumatu finantsregistreerimisprotsessi jaoks uus kirje.
1. Lisage protsessi registreerimise juhised, järgides järgmisi juhiseid.

    1. Valige **Lisa**.
    1. Valige fiskaalkonnektori tüüp.
    1. Valige väljal **Grupi number** sobiv fiskaalkonnektorite grupp.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Finantsregistreerimise protsessi olemite määramine müügikoha profiilidele

Finantsregistreerimise protsessi olemite määramiseks müügikoha profiilidele tehke järgmist.

1. Avage Commerce'i peakontoris **kassafunktsioonide profiilide** leht (**Retail and Commerce \> Channeli häälestus \> kassas häälestus \> kassaprofiilid \> funktsionaalsuse profiilid**). 
1. Määrake finantsregistreerimise protsess kassa funktsiooniprofiilile.
1. Valige käsk **Redigeeri** ja seejärel valige vahekaardil **Fiskaalüksuse registreerimisprotsess** väljalt **Protsessi number** soovitud protsess.
1. Minge kassa **riistvaraprofiili** lehele (**Jaemüügi- ja kaubanduskanali \> häälestus \> kassa häälestus \> müügikoha profiilid \> Riistvaraprofiilid**).
1. Määrake riistvaraprofiilile konnektori tehnilised profiilid. 
1. Valige **Redigeeri** ja seejärel lisage vahekaardile **Välis välisseadmed** rida. 
1. Valige väljal **Profiili number** konnektori tehniline profiil.

> [!NOTE]
> Samale riistvaraprofiilile saab lisada mitu tehnilist profiili. Siiski peab riistvaraprofiilil või kassa funktsiooniprofiilil olema mis tahes fiskaalkonnektorite grupiga ainult üks ühisosa.

Finantsregistreerimisvoo määratleb finantsregistreerimise protsess ja ka mõned fiskaalintegratsiooni komponentide parameetrid: CRT rahandusdokumendi pakkuja laiendus ja fiskaalse konnektori riistvarajaama laiendus.

- Sündmuste ja kannete tellimus fiskaalüksuse registreerimisele on eelmääratletud fiskaaldokumendi pakkujas.
- Fiskaaldokumendi pakkuja vastutab ka fiskaalüksuse registreerimiseks kasutatava fiskaalkonnektori tuvastamise eest. See vastab konnektori funktsiooniprofiilidele, mis on kaasatud fiskaalüksuse registreerimise protsessi praeguse etapi jaoks määratud fiskaalkonnektorite gruppi koos konnektori tehnilise profiiliga, mis on määratud kassaga seotud riistvarajaama riistvaraprofiilile.
- Fiskaaldokumendi pakkuja kasutab fiskaaldokumendi pakkuja konfiguratsiooni andmetüüpide vastenduse sätteid kannete/sündmuste andmete, nagu maksud ja maksed, teisendamiseks fiskaaldokumendi loomise ajal.
- Kui fiskaaldokumendi pakkuja loob fiskaaldokumendi, võib fiskaalkonnektor saata selle samal kujul fiskaalseadmele või selle sõeluda ja teisendada seadme rakendusliidese (API) käskude jadaks olenevalt sellest, kuidas kommunikatsiooni käsitletakse.

### <a name="validate-the-fiscal-registration-process"></a>Finantsregistreerimise protsessi kinnitamine

Soovitatav on kinnitada finantsregistreerimise protsess järgmistel juhtudel.

- Olete lõpetanud kõik uue registreerimisprotsessi sätted. Need sätted hõlmavad registreerimisprotsesside määramist kassa funktsioonide profiilidele ja riistvaraprofiilidele.
- Olete muutnud olemasolevat finantsregistreerimise protsessi ja need muudatused võivad põhjustada käitusajal mõne muu fiskaalse konnektori valimise. (Näiteks olete muutnud konnektorirühma fiskaalse registreerimise protsessietapi jaoks, lubanud konnektori funktsionaalse profiili konnektorirühmas või lisanud konnektorirühmale uue konnektori funktsionaalse profiili.)
- Olete muutnud konnektoritehniliste profiilide määramist riistvaraprofiilidele.

Finantsregistreerimise protsessi kinnitamiseks tehke järgmist.

1. Avage Commerce'i peakontoris **eelarve registreerimise protsessi** leht (**jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalne registreerimisprotsessid**).
1. Rahandusregistreerimise protsessi kinnitamiseks valige **Kinnita**.
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

Tõrkekäsitluse sätete seadistamiseks tehke järgmist.

1. Lehel **Fiskaalüksuse registreerimisprotsess** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalüksuse registreerimisprotsessid**) saate määrata fiskaalüksuse registreerimisprotsessi iga etapi kohta järgmised parameetrid.

    - **Luba vahelejätmine** – see parameeter lubab tõrketöötluse dialoogiboksis suvand **Jäta vahele**.
    - **Luba registreerituks märkimine** – see parameeter lubab tõrketöötluse dialoogiboksis suvandi **Märgi registreerituks**.
    - **Luba edasilükkamine** – see parameeter lubab dialoogiboksis **Veakäsitlus suvandi Edasilükkamine**.
    - **Jätka tõrke korral** – kui see parameeter on lubatud, saab fiskaalüksuse registreerimise protsess kande või sündmuse fiskaalüksuse registreerimise nurjumise korral kassaregistris tegevust jätkata. Muidu peaks operaator järgmisel kandel või sündmusel fiskaalüksuse registreerimise käitamise jaoks nurjunud fiskaalüksuse registreerimist uuesti proovima, selle vahele jätma või märkima kande või sündmuse registreerituks. Lisateavet vaadake teemast [Valikuline fiskaalüksuse registreerimine](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Kui lubatud on parameeter **Jätka tõrke korral**, siis on parameetrid **Luba vahelejätmine** ja **Luba registreerituks märkimine** automaatselt keelatud.

1. Dialoogiboksis Vahelejätmine **ja** registreeritud **suvanditeks märkimine nõuavad, et** luba registreerimine vahele jätta või registreerida registreeritud **õigusena** märkimine. Selle õiguse lubamiseks avage **leht Õigusegrupid** (**jaemüügi- ja kaubandustöötajate \>\> õiguste rühmad**) ja seadke **suvand Luba vahele registreerimine või märgi registreeritud** suvandiks **Jah**.
1. **Dialoogiboksi Veakäsitlemine suvand Lükka edasi** nõuab, et **luba lubamine lubataks**. Õiguse lubamiseks avage **leht Õigusegrupid** (**jaemüügi- ja kaubandustöötajate \>\> õiguste rühmad**) ja seadke **suvand Luba edasilükkamine** valikuks **Jah**.
1. Suvandid **Jäta vahele**, **Märgi registreeritud** ja **Edasilükkamine** võimaldavad operaatoritel sisestada lisateavet, kui finantsregistreerimine nurjub. Selle funktsiooni kättesaadavaks tegemiseks peaksite määrama **eelarvekonnektori rühmas jäta vahele**, **Märgi registreeritud** ja **Lükka infokoodid edasi**. Seejärel salvestatakse operaatorite sisestatav teave teabekoodi kandena, mis on lingitud fiskaalkandega. Lisateavet teabekoodide kohta vt teemast [Teabekoodid ja teabekoodigrupid](../info-codes-retail.md).

    > [!NOTE]
    > Käivitusfunktsiooni **Toode** ei toetata teabekoodide puhul, mida kasutatakse fiskaalkonnektorite gruppides suvandite **Jäta vahele** ja **Märgi registreerituks** puhul.

    - **Valige lehe Fiskaalse konnektori rühma** vahekaardil **Infokoodid** väljadel **Vahele,** **Märgi registreeritud** ja **Edasi.**

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
