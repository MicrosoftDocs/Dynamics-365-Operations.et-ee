---
title: Hüljatud ostukorvide tuvastamine ja teatiste saatmine klientidele
description: See teema kirjeldab, kuidas kohandada hülgatud Microsoft Dynamics 365 Commerce ostukorvi konnektori näidisrakendust, et tuvastada mahajäetud ostukorvid ja saata klientidele meeldetuletuse meiliteatis.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1db4e988653aa55db2b18fb201edeafc4d16a1bc
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489026"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Hüljatud ostukorvide tuvastamine ja teatiste saatmine klientidele

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas kohandada hülgatud Microsoft Dynamics 365 Commerce ostukorvi konnektori näidisrakendust, et tuvastada mahajäetud ostukorvid ja saata klientidele meeldetuletuse meiliteatis.

Tulu taastamine ja klientide kinnipidamine ostukorvist loobutud teatiste kaudu on oluline Dynamics 365 Commerce tugifunktsioon. Rakenduse Commerce abandoned cart connector näidisrakenduse kohandamisel pääsevad jaemüüjad juurde jaemüügiserveris asuvattele ostukorvidele, mida ei ole ajaakna ajal muudetud, mille jaemüüjad määratlevad. Seejärel saab neid ostukorvisid tuua, toote- ja kliendiandmetega laiendada ning saata edasi kolmanda osapoole meili turunduspakkujale, kes saab luua meiliteatisi ja saata neile kliente.

Loobutud ostukorvi meiliteatis, mille kliendid saavad, võib sisaldada järgmist teavet:

- Kliendi eesnimi.
- Kliendi perekonnanimi.
- Kliendi meiliaadress.
- URL, mis tagastab kliendi ostukorvi.
- Kande valuuta.
- Loend toodetest kliendi ostukorvis. Iga toote kohta lisatakse järgmine teave:

    - Toote kuvatav nimi
    - Toote ID (kasutatakse URL-i panekuks tootekirjelduse lehele)
    - Toote pilt, mille suurust saab automaatselt muuta, et mahutada erinevad vaate suurused
    - Tootepildi asetekst
    - Toote ühikuhind

## <a name="abandoned-cart-connector-sample"></a>Mahajäetud ostukorvi konnektori näidis

Konnektori mudel, mille Microsoft pakub jaemüügi tarkvara arenduskomplekti (SDK) kaudu, võimaldab loobutud ostukorvi teabe toomist ja saatmist kolmanda osapoole meili turunduspakkujale. See konnektor tegeleb sidega jaemüügiserveriga, kasutab turbeks Azure'i võtme hoidlat, tegeleb määratud ajaakna ostukorvi toomise planeerimisega ning toob tellimuse- ja tooteandmed. Samuti pakub see näidis rakendamise integratsiooniks kolmanda osapoole meili turunduse pakkujaga. Ühendus on loodud suhtlema [boksist väljas emarsy-dega](https://emarsys.com). Kuid seda on lihtne kohandada integreerimaks muude lahendustega, nagu konstantne kontakt, Mailchimp ja SendGrid.

Järgmine näide näitab ostukorvi konnektori näidisrakenduse komponente.

![Ostukorvi konnektori näidisrakenduse komponendid](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> Mõned regioonid nõuavad, et kliendid ei saaks keelduda ostukorvi andmete saatmisest meili turunduspakkujale või taotleda oma andmete eemaldamist. Microsoft ei paku klientidele siiski neid valikuid. Seega, kui plaanite teha äri neid volitavates regioonides, peate klientide eelistuste jälgimiseks esitama nõutava infrastruktuuri ja kohandused ning nende alusel tõkestama kliendiandmete saatmist meiliplatvormile. Peate kliendi taotluse korral määratlema ka kliendi andmete puhastamise protsessi oma meili turunduse pakkujalt.

## <a name="obtain-the-code-sample"></a>Hangi koodi näidis

Mahajäetud ostukorvi konnektori näidisrakendus sisaldub Retail SDK versioonis 10.0.16. Koodi leiate jaotisest **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample**. Lisateavet Retail SDK kohta ja selle hankimise [kohta vt jaemüügi tarkvara arenduskomplektist (SDK).](retail-sdk/retail-sdk-overview.md)

> [!NOTE]
> Kuigi näidiskood tehti esimest korda kättesaadavaks versioonis 10.0.16, ühildub see jaemüügiserveri versiooniga 10.0.13 ja hilisema versiooniga.

## <a name="prerequisites-and-dependencies"></a>Eeltingimused ja sõltuvused

Enne kui saate korvi mahajäetud konnektori näidiskoodi juurutada ja konfigureerida, peavad olema täidetud järgmised eeltingimused.

### <a name="access-to-commerce-resources"></a>Juurdepääs Äriressurssidele

Ostukorvi konnektori rakenduse konfigureerimiseks ja juurutamiseks peab teil olema juurdepääs järgmistele Commerce'i ressurssidele:

- Administraatori juurdepääs Commerce headquartersile teie keskkonnas
- Juurdepääs elutsükli Microsoft Dynamics teenuste (LCS) projektile teie keskkonnas

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Allajäetud ostukorvi konnektori rakendus kasutab Azure'i Cosmos DB eelnevalt toodud ostukorvide ID-de ja ajatemplite jälgimiseks. Võite kasutada Azure'i Cosmos DB nende andmete säilitamiseks või kohandada koodi näidist, et integreerida teise andmete talletussuvandiga. Lisateavet Azure'i kohta Cosmos DB vt "Tere tulemast [Azure'i"Cosmos DB](/azure/cosmos-db/introduction).

Kui kasutate Azure'i Cosmos DB, peavad enne näidiste käivitamist olema täidetud järgmised eeltingimused:

- Teil peab olema aktiivne Azure'i Cosmos DB konto. Kui teil kontot pole, vaadake teemat [Andmebaasikonto loomine](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- URI **ja** **PRIMARY KEY** (või **SECONDARy KEY**) **väärtused** peate azure'i konto võtmetest azure'i Cosmos DB portaalis tooma. Lisateavet lõpp-punkti ja võtmeteabe toomise kohta Azure'i Cosmos DB [konto puhul vt vaadake, kopeerige ja looge uuesti pääsuvõtmeid ja paroole](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure'i võtmehoidla

Korvi allutatud korvi konnektori rakendus kasutab võtme vault turvatud juurdepääsu nõudvad eri komponentide nimede ja saladuste salvestamiseks.

Võtme hoidla häälestamiseks järgige neid samme.

1. Portaali abil järgige Azure'i [pinu keskuse võtme vaulti haldamise juhiseid](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. Looge saladusi järgmise teabe jaoks:

    - Emarsys-rakenduse programmeerimisliidese (API) kasutajanimi ja API saladus
    - Korvi hülgamise rakenduse ID ja saladus

Mahajäetud ostukorvi konnektori näidiskood kasutab võtme vault pääsuks Azure'i vaikemandame. Peate sisestama **loendi** ja **lugemise** õigused identiteedile, mida plaanite kasutada võtme hoidlale juurdepääsemiseks.

Lisateavet Azure'i vaikemandaatide kohta vt teemast [DefaultAzureCredential Class](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Mahajäetud ostukorvi konnektori näidisrakenduse rakenduse ID loomine rentnikule Azure AD

Peate (AD) rentnikule looma korviühenduse näidisrakenduse Azure Active Directory ID. Lisateavet rakenduse ID loomise kohta vt portaali kaudu rakenduse [ja teenuse subjekti Azure AD loomiseks, mis pääseb juurde ressurssidele](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Lisage mahajäetud ostukorvi konnektori näidisrakenduse rakenduse ID jaemüügiserveri API lubatud loendisse

Seejärel peate jaemüügiserveri API lubatud loendile lisama korviühenduse näidisrakenduse ID. Lisateavet selle kohta, kuidas lisada rakenduse ID Azure'i loendisse Lubatud, [vt jaemüügiserveris teenuse tugiteenuste autentimist](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Konfigureerige mahajäetud ostukorvi konnektori näidisrakendus

Ostukorvi konnektori näidisrakenduse **konfigureerimiseks muutke kausta AbandonedCartDetectionSample** juurkaustas asuvat konfiguratsioonifaili appSettings.json **·**. Järgmised tabelid kirjeldavad konfiguratsioonifaili atribuute.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Atribuut    | Kirjeldus |
| ----------- | ----------- |
| KeyVaultURI | Domeeninime süsteemi (DNS) nimi võtme hoidlale, mida kasutate Azure'i portaalis. |

### <a name="retailserverclientoptions"></a>Välja RetailServerClientOptions atribuut

| Atribuut                                      | Kirjeldus |
| --------------------------------------------- | ----------- |
| Rentniku ID                                      | Teie Azure AD Azure'i rentniku rentniku ID. |
| RetailServerAudienceId                        | Jaemüügiserveri sihtgrupi ID. Vaikeväärtuse võite jätta. |
| Atribuut AppIdKeyVaultSecretName                       | Allajäetud ostukorvi konnektori näidisrakenduse rakenduse ID jaoks loodud saladuse nimi. |
| Atribuut AppSecretKeyVaultSecretName                   | Selle saladuse nimi, mis talletab rakenduse saladust ostukorvi konnektori näidisrakenduse ID jaoks. |
| Atribuut RetailServerUrl                               | Teie jaemüügiserveri eksemplari URL. Selle väärtuse leiate LCS-st. |
| OperatingUnitNumber                           | Tootmisüksuse number (OUN). Selle väärtuse leiate Commerce Headquartersist. |
| Kaasa eiramineCartsModifiedSinceLastMinutes | Allajäetud ostukorvide ajaakna algus, mille soovite tuua. Väärtust väljendatakse minutite arvuna enne praegust kellaaega. Näiteks seadke selle atribuudi väärtuseks 120 **, et tuua kõik ostukorvid, mida viimati muudeti 120** minutit tagasi ja ajaakna lõpu vahel, **mille määratleb atribuut ExcludeAkenCartsModifiedSinceLastMinutes**. |
| Välja jättaAbandonedCartsModifiedSinceLastMinutes | Allajäetud ostukorvide ajaakna lõpp, mille soovite tuua. Väärtust väljendatakse minutite arvuna enne praegust kellaaega. Näiteks kui **atribuudi IncludeEiraCartsModifiedSinceLastMinutes** **väärtuseks on seatud 120, seadke selle atribuudi väärtuseks 30** **,** et tuua kõik ostukorvid, mis muudeti 120 minutit tagasi kuni 30 minutit tagasi. Tegelikult määrab see atribuut aja hulga, mille võrra soovite oodata, enne kui korvi deklareeritakse. |
| ReturnToCartUrl                               | Ostukorvi URL teie e-äri saidil failis app.config kasutatavas **vormingus**. |

### <a name="azurecosmosoptions"></a>AzureCosónOptions

Korvi allajäetud toomise töö olek, ostukorvi ID-d ja muudetud ajatemplid talletatakse Azure'is Cosmos DB. Vaikimisi konfiguratsioonifaili sätted giidvad Azure'i kohaliku emulaatori eksemplarile Cosmos DB. Kui juurutate konnektori tootmisele, peate need sätted värskendama nii, et need vadaavad Azure'i Cosmos DB eksemplarile teie Azure'i kordustellimuses. Kohaliku või kasti testimiseks saate kasutada Azure'i [Cosmos DB emulaatorit](/azure/cosmos-db/local-emulator).

| Atribuut    | Kirjeldus |
| ----------- | ----------- |
| EndPointUri | Lõpp-punkti URI, mida pakub Azure või emulaator. |
| PrimaryKey  | Primaarvõti, mida pakub Azure või emulaator. |
| DatabaseId  | Andmebaasi ID. Võite jätta vaikeväärtuse või pakkuda oma väärtust. |
| ContainerId | Konteineri id. Võite jätta vaikeväärtuse või pakkuda oma väärtust. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Kui integreerite muu meili turunduse pakkujaga kui Emarsys, **peate laiendama IEmailProvider** liidest nii, et see oleks sobiv, et suhelda selle pakkujaga.

| Atribuut                      | Kirjeldus |
| ----------------------------- | ----------- |
| APIUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId (välise id)               | Emarsys-is loodud välise sündmuse kirje ID. Allajäetud ostukorvi meiliteatiste **saatmiseks** loodud kampaania käivitussätetest leiate väärtuse. |
| ApiUserNameKeyVaultSecretName | Võtme nimi, kuhu emarsys API kasutajanimi salvestatakse. |
| ApiSecretKeyVaultSecretName   | Võtme nimi, kuhu Emarsys API saladus salvestatakse. |
| EmarsysContactKeyId           | E-kirja veeru ID Emarsysi kontaktiandmebaasis. Vaikeväärtus on **3** ja seda ei tohiks muuta. |

### <a name="mediaoptions"></a>MediaOptions

Kui kasutate rakenduse Commerce e-commerce võimalusi, saate tootepiltide toomiseks kasutada Commerce'i digitaalse vara haldust. Lisateavet pildi suuruse muutja võimaluste kohta digitaalvarahalduses vt [konfiguratsioonist ImageSettings viewport](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Atribuut                             | Kirjeldus |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Teie saidi digitaalse varahalduri juur-URL. Väärtuse leiate Media Serveri baas-URL-i **atribuudivõtmest** **Rakenduse Retail ja Commerce \> Channel häälestuse \> kanali profiilides** Commerce Headquartersis. |
| ImageViewPorts                       | Konteineri sõlm üksikute vaateporti konfiguratsioonide jaoks. |
| ImageViewPorts/viewport              | Vaatepordi definitsioon. Selle atribuudi abil saate määrata vaatepordi laiusevahemikud pikslites. Näiteid, mis näitavad, kuidas seda atribuuti kasutatakse, vaadake konfiguratsioonifaili **appSettings.json**. |
| ImageViewPorts/imageWidth            | Vaatepordi pildilaius pikslites. |
| imageViewPorts/imageHehti           | Vaatepordi pildikõrgus pikslites. |
| imageViewPorts/useForDefaultImageTag | Tõene **·**/**väärtus,** mis näitab, kas vaatepordiga `<picture>` määratletud pildidimensioone tuleb kasutada juhul, kui HTML-silt ei ole veebibrauseri või meilikliendi puhul toetatud. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
