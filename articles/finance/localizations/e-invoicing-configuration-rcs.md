---
title: Konfigurace Elektronické fakturace v Regulatory Configuration Services (RCS)
description: Toto téma vysvětluje, jak konfigurovat Elektronickou fakturaci v Dynamics 365 Regulatory Configuration Services (RCS).
author: gionoder
ms.date: 11/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 640244612a2a553ec09661635787cb7f8694283b
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779663"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>Konfigurace Elektronické fakturace v Regulatory Configuration Services (RCS)

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace o možnostech konfigurace Elektronické fakturace ve službě Dynamics 365 Regulatory Configuration Services (RCS).

Prostřednictvím funkcí konfigurace vám Elektronická fakturace pomůže splnit obchodní a regulační požadavky na elektronické faktury, aniž byste museli provádět jakékoli kódování. A ve scénářích, kdy elektronické faktury musí být elektronicky schváleny webovou službou, vám možnosti konfigurace také pomohou splnit požadavky na výměnu zpráv s webovou službou, aniž byste museli dělat jakýkoli kód.

## <a name="electronic-reporting"></a>Elektronická sestava

Elektronické výkaznictví (ER) podporuje Elektronickou fakturaci.

Mapování a formáty datového modelu jsou konfigurovatelné komponenty, které se vytvářejí a udržují prostřednictvím ER a používají se v Elektronické fakturaci. Návrhář formátů ER je nástroj pro vytváření a údržbu formátů souborů. Používá se ke konfiguraci funkcí elektronické fakturace.

Další podrobnosti získáte v tématu [Přehled elektronického výkaznictví (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)

## <a name="electronic-invoicing-features"></a>Funkce elektronické fakturace

Funkce elektronické fakturace jsou zodpovědné za generování elektronických faktur prostřednictvím Elektronické fakturace. Zapouzdřují pravidla konfigurace a používají je ke zpracování dat, která Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management odesílá do Elektronické fakturace a do elektronických faktur.

Funkce také podporují scénáře, kde je vyžadován soulad se specifikacemi formátu souboru a výstupem je samostatný elektronický soubor. Ve většině případů zveřejňuje specifikace formátu souboru finanční úřad.

Funkce konečně podporují výměnu zpráv s externími webovými službami, které jsou hostovány buď daňovým úřadem, nebo nějakou akreditovanou stranou, a žádosti o povolení nebo razítko schválení v elektronické faktuře.

## <a name="availability-of-electronic-invoicing-features"></a>Dostupnost funkcí elektronické fakturace

Dostupnost funkcí elektronické fakturace závisí na zemi nebo regionu. Ačkoli jsou některé funkce obecně dostupné, jiné jsou v preview.

### <a name="generally-available-features"></a>Obecně dostupné funkce

V následující tabulce jsou uvedeny funkce elektronické fakturace, které jsou obecně dostupné.

| Země nebo oblast | Název funkce                         | Obchodní dokument |
|----------------|--------------------------------------|-------------------|
| Rakousko        | Rakouské elektronické faktury (AT)    | Prodejní a projektové faktury |
| Belgie        | Belgická elektronická faktura (BE)      | Prodejní a projektové faktury |
| Brazílie         | Brazilský NF-e (BR)                  | Fiskální dokument model 55, opravné dopisy, zrušení a vyřazení |
| Brazílie         | Brazilian NFS-e ABRASF Curitiba (BR) | Fiskální dokumenty služby |
| Brazílie         | Brazilský import NF-e z e-mailu (BR) | Model 55 fiskálního dokumentu |
| Dánsko        | Dánská elektronická faktura (DK)       | Prodejní a projektové faktury |
| Egypt          | Egyptská elektronická faktura (EG)     | Prodejní a projektové faktury |
| Estonsko        | Estonská elektronická faktura (EE)     | Prodejní a projektové faktury |
| Finsko        | Finská elektronická faktura (FI)      | Prodejní a projektové faktury |
| Francie         | Francouzská elektronická faktura (FR)       | Prodejní a projektové faktury |
| Německo        | Německá elektronická faktura (DE)       | Prodejní a projektové faktury |
| Itálie          | FatturaPA (IT)                       | Prodejní a projektové faktury |
| Nizozemsko    | Nizozemská elektronická faktura (NL)        | Prodejní a projektové faktury |
| Norsko         | Norská elektronická faktura (NO)    | Prodejní a projektové faktury |
| Španělsko          | Španělská elektronická faktura (ES)      | Prodejní a projektové faktury |
| Evropa         | Elektronická faktura PEPPOL            | Prodejní a projektové faktury PEPPOL |
| Evropa         | Faktura dodavatele PEPPOL                | Import faktur dodavatele PEPPOL |
| Saúdskoarabské království   | Saúdskoarabská elektronická faktura (SA)| Prodejní a projektové faktury |

### <a name="preview-features"></a>Funkce náhledu

V následující tabulce jsou uvedeny funkce elektronické fakturace, které jsou aktuálně v preview.

| Země nebo oblast | Název funkce                         | Obchodní dokument |
|----------------|--------------------------------------|-------------------|
| Mexiko         | Mexické CFDI (MX)                    | Prodejní faktury, dodací listy, převody zásob, doplňky plateb a zrušení |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Konfigurovatelné komponenty funkcí elektronické fakturace

Funkce elektronické fakturace se skládají z následujících skupin konfigurovatelných komponent:

- **Formáty**: Formáty umožňují konfigurovat, co musí Elektronická fakturace generovat, když se z elektronického dokumentu stane elektronická faktura. Formáty zahrnují konfiguraci formátu pro elektronickou fakturu a pro soubory a zprávy, které se používají k odesílání požadavků a přijímání odpovědí, když je vyžadována komunikace s externí webovou službou.
- **Akce**: Akce vám umožní nakonfigurovat, jak Elektronická fakturace generuje transformaci elektronického dokumentu, který aplikace Finance a Supply Chain Management odeslaly do elektronické faktury.
- **Pravidla použitelnosti**: Pravidla použitelnosti vám umožňují konfigurovat kontext, který Elektronická fakturace musí vzít v úvahu při zpracování funkce elektronické fakturace.
- **Proměnné**: Proměnné umožňují konfigurovat podporu pro konstrukci logiky konfigurace. Proměnné mohou fungovat jako vstup hodnot k provedení konkrétní akce. Alternativně mohou fungovat jako výměna hodnot mezi Finance a Supply Chain Management a Elektronickou fakturací.
- **Mapování modelu elektronického dokumentu**: Mapování modelu elektronického dokumentu umožňuje konfigurovat mapování modelu ER. Mapování modelu definuje mapování dat abstraktní faktury, která je integrována do Elektronické fakturace při odesílání elektronických dokumentů.
- **Kontextový model faktury**: Kontextový model faktury umožňuje konfigurovat kontextový model faktury ER a definovat kontext funkce elektronické fakturace.
- **Typy odpovědí**: Typy odpovědí vám umožňují konfigurovat, co musí Elektronická fakturace aktualizovat ve Finance Supply Chain Management v důsledku zpracování elektronické faktury.

### <a name="formats"></a>Formáty

Následující seznamy ukazují konfigurace formátu ER, které jsou k dispozici pro funkce elektronické fakturace.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Rakouské (AT) elektronické faktury: Prodejní a projektové faktury pro Rakousko

- Prodejní faktura OIOUBL
- Faktura k projektu OIOUBL
- Prodejní dobropis OIOUBL
- Dobropis k projektu OIOUBL

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgická (AT) elektronická faktura: Prodejní a projektové faktury pro Belgii

- Prodejní faktura UBL BE
- Projektová faktura UBL BE
- Dobropis k projektu UBL BE
- Prodejní dobropis UBL BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brazilské (BR) NF-e: NF-e Federal (Brazílie)

- Formát exportu odeslání NF-e (BR)
- Formát opravného dopisu NF-e (BR)
- Formát exportu zrušení NF-e (BR)
- Formát exportu zahození NF-e (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brazilian NFS-e (BR): NFS-e ABRASF město Curitiba

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF dotaz Curitiba (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Dánská (AT) elektronická faktura: Prodejní a projektové faktury pro Dánsko

- Prodejní faktura OIOUBL
- Faktura k projektu OIOUBL
- Prodejní dobropis OIOUBL
- Dobropis k projektu OIOUBL

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Nizozemská (AT) elektronická faktura: Prodejní a projektové faktury pro Nizozemsko

- Prodejní faktura UBL NL
- Projektová faktura UBL NL
- Dobropis k projektu UBL NL
- Prodejní dobropis UBL NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Egyptská (AT) elektronická faktura: Prodejní a projektové faktury pro Egypt

- Prodejní faktura (EG) (fakturace)
- Projektová faktura (EG) (fakturace)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Estonská (AT) elektronická faktura: Prodejní a projektové faktury pro Estonsko

- Prodejní faktura (EE)
- Projektová faktura (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Finská (AT) elektronická faktura: Prodejní a projektové faktury pro Finsko

- Prodejní faktura (FI)
- Projektová faktura (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Francouzská (AT) elektronická faktura: Prodejní a projektové faktury pro Francii

- Prodejní faktura UBL FR
- Projektová faktura UBL FR
- Dobropis k projektu UBL FR
- Prodejní dobropis UBL FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Německá (AT) elektronická faktura: Prodejní a projektové faktury pro Německo

- Prodejní faktura (DE)
- Projektová faktura (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Italská (AT) elektronická faktura: Prodejní a projektové faktury pro Itálii

- Prodejní faktura (IT)
- Projektová faktura (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Mexické (MX) CFDI: CFDI pro Mexiko

- Formát faktury CFDI (MX)
- Dodací list CFDI (MX)
- Převod zásob CFDI (MX)
- Formát platby CFDI (MX)
- Formát zrušení faktury CFDI (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norská (AT) elektronická faktura: Prodejní a projektové faktury pro Norsko

- Prodejní faktura OIOUBL
- Faktura k projektu OIOUBL
- Prodejní dobropis OIOUBL
- Dobropis k projektu OIOUBL

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>Elektronická faktura PEPPOL: prodejní a projektové faktury PEPPOL

- Prodejní faktura PEPPOL
- Projektová faktura PEPPOL
- Prodejní dobropis PEPPOL
- Projektový dobropis PEPPOL

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Španělská (AT) elektronická faktura: Prodejní a projektové faktury pro Španělsko

- Prodejní faktura (ES)
- Projektová faktura (ES)

#### <a name="saudi-arabian-sa-electronic-invoice-sales-and-project-invoices-for-saudi-arabia"></a>Saudskoarabská (AT) elektronická faktura: Prodejní a projektové faktury pro Saudskou Arábii

- Prodejní e-faktura (SA)
- Projektová e-faktura (SA)

Kromě konfigurací formátu ER, které jsou k dispozici ihned pro použití ve službě elektronické fakturace, můžete také vytvořit své vlastní konfigurace formátu ER. Konfigurace formátu, které jsou vytvořeny pro použití s funkcemi elektronické fakturace, však nepodporují přímý odkaz na tabulky Finance nebo Supply Chain Management nebo žádným z odpovídajících metadat. Podporovány jsou pouze odkazy na mapování modelu ER.

### <a name="actions"></a>Akce

V následující tabulce jsou uvedeny dostupné akce a to, zda jsou aktuálně obecně dostupné nebo stále v preview.

| Akce                                        | popis                                                                  | Dostupnost         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Převod dokumentu                            | Spusťte formát elektronického výkaznictví a transformujte dokument.                   | Obecně dostupné  |
| Podepsat dokument xml                             | Podepisujte dokumenty XML digitálním podpisem.                                   | Obecně dostupné  |
| Podepsat dokument JSON pro egyptský daňový úřad | Podepisujte dokumenty JSON digitálním podpisem pro egyptský daňový úřad.       | Obecně dostupné  |
| Integrace s egyptskou službou ETA           | Komunikujte s egyptským daňovým úřadem.                                     | Obecně dostupné  |
| Volejte brazilskou službu SEFAZ                  | Integrace s brazilskou službou SEFAZ pro odesílání fiskálních dokumentů.       | Obecně dostupné  |
| Volání mexické služby PAC                      | Integrace s mexickou službou PAC pro odesílání CFDI.                      | Náhled           |
| Odezva procesu                              | Analýza odpovědi přijatou z volání webové služby.                     | Obecně dostupné  |
| Použití MS Power Automate                         | Integrace s tokem vytvořeným v Microsoft Power Automate.                       | Náhled           |

### <a name="applicability-rules"></a>Pravidla použitelnosti

Pravidla použitelnosti jsou konfigurovatelné klauzule, které jsou definovány na úrovni funkcí elektronické fakturace. Pravidla jsou nakonfigurována tak, aby poskytovala kontext pro provádění funkcí elektronické fakturace prostřednictvím sady funkcí elektronické fakturace.

Když je obchodní dokument z Finance nebo Supply Chain Management odeslán do elektronické fakturace, obchodní dokument nenese výslovný odkaz, který umožňuje sadě funkcí elektronické fakturace volat konkrétní funkci elektronické fakturace ke zpracování odeslání.

Pokud je však správně nakonfigurován, obchodní dokument obsahuje nezbytné prvky, které umožňují elektronické fakturaci vyřešit, která funkce elektronické fakturace musí být vybrána, a poté vygenerovat elektronickou fakturu.

Pravidla použitelnosti umožňují sadě funkcí elektronické fakturace najít přesné funkce elektronické fakturace, které je nutné použít ke zpracování podání. To se provádí porovnáním obsahu odeslaného obchodního dokumentu s klauzulemi z pravidel použitelnosti.

Například dvě funkce elektronické fakturace se souvisejícími pravidly použitelnosti jsou nasazeny do sady funkcí elektronické fakturace.

| Funkce elektronické fakturace | Pravidla použitelnosti        |
|------------------------------|--------------------------- |
| A                            | <p>Země = BR</p><p>a</p><p>Právnická osoba = BRMF</p>  |
| mld.                            | <p>Země = MX</p><p>a</p><p>Právnická osoba = MXMF</p>  |

Pokud je obchodní dokument z Finance nebo Supply Chain Management odeslán do sady funkcí elektronické fakturace, obchodní dokument obsahuje následující atributy vyplněné jako:

- Země = BR
- Právnická osoba = BRMF

Sada funkcí elektronické fakturace vybere funkci elektronické fakturace **A** ke zpracování podání a vygenerování elektronické faktury.

Stejným způsobem, pokud obchodní dokument obsahuje:

- Země = MX
- Právnická osoba = MXMF

Funkce elektronické fakturace **B** je vybrána ke generování elektronické faktury.

Konfigurace pravidel použitelnosti nemůže být nejednoznačná. To znamená, že dvě nebo více funkcí elektronické fakturace nemůže mít stejné klauzule, jinak to povede k žádnému výběru. Pokud dojde k duplikaci funkcí elektronické fakturace, použijte další klauzule, abyste umožnili rozlišit mezi dvěma funkcemi elektronické fakturace, aby se předešlo nejednoznačnosti.

Zvažte například funkci elektronické fakturace **C** . Tato funkce je kopií funkce elektronické fakturace **A**.

| Funkce elektronické fakturace | Pravidla použitelnosti        |
|------------------------------|--------------------------- |
| A                            | <p>Země = BR</p><p>a</p><p>Právnická osoba = BRMF</p>  |
| K                            | <p>Země = BR</p><p>a</p><p>Právnická osoba = BRMF</p>  |

V tomto příkladu funkce **C** je před odesláním obchodního dokumentu, který obsahuje následující:

- Země = BR
- Právnická osoba = BRMF

Funkce elektronické fakturace nedokáže rozlišit, která funkce elektronické fakturace musí být použita ke zpracování podání, protože podání obsahuje přesně stejná ustanovení.

Chcete-li vytvořit rozdíl mezi těmito dvěma funkcemi prostřednictvím pravidel použitelnosti, je třeba k jedné z funkcí přidat novou klauzuli, která umožní nastavení možnosti elektronické fakturace vybrat správnou funkci elektronické fakturace.

| Funkce elektronické fakturace | Pravidla použitelnosti        |
|------------------------------|--------------------------- |
| A                            | <p>Země = BR</p><p>a</p><p>Právnická osoba = BRMF</p>  |
| K                            | <p>Země = BR</p><p>a</p><p>Právnická osoba = BRMF</p><p>a</p><p>Model=55</p>  |

K podpoře vytváření složitějších klauzulí jsou k dispozici následující zdroje:

Logické operátory:
- A
- nebo

Typy operátoru:
- Equal
- Not equal
- Greater than
- Less than
- Větší než nebo rovno
- Menší než nebo rovno
- Contains
- Začíná na

Datové typy:
- Řetězec
- Počet
- Logická
- Datum
- UUID

Schopnost seskupovat a oddělovat klauzule.
Příklad vypadá takto.

| Funkce elektronické fakturace | Pravidla použitelnosti        |
|------------------------------|--------------------------- |
| K                            | <p>Země = BR</p><p>a</p><p>(Právnická osoba = BRMF</p><p>nebo</p><p>Model=55)</p>  |


## <a name="configuration-providers"></a>Poskytovatelé konfigurace

Poskytovatelé konfigurace poskytují funkce elektronické fakturace a jejich komponenty ER, jako je mapování modelu, konfigurace formátu a kontextový model. Publikují funkce elektronické fakturace a komponenty ER v přidruženém globálním úložišti. Odtud je mohou stáhnout další organizace.

Než nakonfigurujete funkce elektronické fakturace prostřednictvím RCS, musíte nakonfigurovat svou vlastní organizaci jako poskytovatele konfigurace v modulu **Elektronické výkaznictví**. Další informace o tom, jak nastavit poskytovatele konfigurace jako **Aktivní** naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Prohlížení funkcí elektronické fakturace v globálním úložišti

Chcete-li procházet funkce elektronické fakturace, které jsou k dispozici v globálním úložišti pro konkrétního poskytovatele konfigurace, synchronizujte instanci RCS vaší organizace. Po dokončení synchronizace se aktualizuje seznam dostupných funkcí elektronické fakturace.

## <a name="importing-electronic-invoicing-features"></a>Importování funkcí elektronické faktury

Než použijete nebo nakonfigurujete funkce elektronické fakturace, musíte je importovat do instance RCS vaší organizace. Operace importu vytvoří místní kopii funkcí a zkopíruje všechny artefakty ER, které funkce používají (například konfigurace formátu a konfigurace modelu) do instance RCS vaší organizace.

Můžete importovat funkci elektronické fakturace od libovolného poskytovatele konfigurace.

## <a name="creating-electronic-invoicing-features"></a>Vytváření funkcí elektronické faktury

Funkci elektronické fakturace můžete vytvořit buď úplně od začátku, nebo ji odvodit z jiné funkce doplňku elektronické fakturace.

Když vytvoříte funkci elektronické fakturace od nuly, musíte ručně přidat komponenty ER (například konfigurace verzí funkcí a další konfigurace, například nastavení verze funkce a nastavení aplikace). Když vytvoříte prvek odvozením z jiného prvku, zdědí nový prvek všechny konfigurace od originálu. 

## <a name="electronic-invoicing-feature-version"></a>Verze funkce elektronické fakturace

Funkce elektronické fakturace mají verze. Když je vytvořena nová verze, číslo verze se automaticky zvýší. Pro novou verzi lze definovat datum „platnost od“.

Verze funkcí elektronické fakturace dodržují životní cyklus, který má až tři stavy:

- **Návrh** – Pokud je verze prvku v tomto stavu, můžete upravit jeho konfigurační atributy a jakékoli jeho artefakty (například konfigurace formátu souboru).
- **Kompletní** – Pokud je verze funkce v tomto stavu, byla publikována do globálního úložiště, které je přidruženo k vaší organizaci. Už nemůžete upravovat verzi prvku ani žádnou z komponent ER.
- **Publikováno** – Pokud je verze funkce v tomto stavu, byla publikována v Elektronické fakturaci. Už nemůžete upravovat verzi prvku ani žádnou z komponent ER.

### <a name="feature-configurations"></a>Konfigurace funkce

Konfigurace funkcí obsahují všechny konfigurace formátu ER, které funkce elektronické fakturace používají. Všechny elektronické soubory, které funkce elektronické fakturace používá během zpracování, pocházejí z konfigurací formátu, které byly přidány do konfigurací funkcí této funkce.

Z konfigurací funkcí můžete přistupovat k návrháři formátu ER, což je nástroj ER, který se používá k vytváření konfigurací formátu.

### <a name="feature-setup"></a>Nastavení funkce

Nastavení funkcí se používá v kombinaci s konfiguracemi funkcí. Každé nastavení funkce zapouzdřuje sadu akcí, pravidla použitelnosti a proměnné, které poskytují očekávané chování, aby funkce elektronické fakturace mohla splnit konkrétní požadavek na elektronickou fakturu.

### <a name="application-setup"></a>Nastavení aplikace

Nastavení aplikace musí být spojeno s dříve vytvořenou připojenou aplikací.

Prostřednictvím nastavení aplikace můžete nakonfigurovat část funkce elektronické fakturace, kterou je třeba provést ve Finance a Supply Chain Management. Alespoň tři konfigurovatelné komponenty jsou povinné bez ohledu na funkci elektronické fakturace:

- **Název tabulky** – Entita v Finance a Supply Chain Management, která uchovává zaúčtované faktury a na které je založena funkce elektronické fakturace.
- **Kontext** – Název modelu kontextu faktury, který byl nakonfigurován prostřednictvím ER.
- **Mapování obchodního dokumentu** – Název modelu mapování faktury, který byl nakonfigurován prostřednictvím ER.

> [!IMPORTANT]
> Konfiguraci zadanou v nastavení aplikace lze zobrazit v sekci Finance a Supply Chain Management. Přejděte na **Správa organizace \> Nastavení \> Parametr elektronického dokumentu**. Na kartě **Elektronický dokument** vyberte **Nasadit** a potom vyberte možnost **Připojená aplikace**.

### <a name="deploying-feature-versions"></a>Nasazení verzí funkcí

V RCS používáte příkaz **Nasadit** k cílovému publikování verze funkce elektronické fakturace. Vyberte **Nasadit** a poté vyberte jednu z následujících možností k definování cíle nasazení: 

- **Prostředí služby** – Když je cílem nasazení prostředí služby, verze funkce elektronické fakturace se publikuje do prostředí služby. Elektronická fakturace je poté připravena přijímat a zpracovávat elektronické dokumenty, které odesílají Finance a Supply Chain Management.
- **Připojená aplikace** – Když je cílem nasazení připojená aplikace, konfigurace poskytovaná nastavením aplikace se zapíše do instance Finance a Supply Chain Management, která k ní byla dříve přidružena.

Pouze verze s elektronickou fakturací, které mají stav **Dokončeno** lze nasadit do prostředí služby nebo do připojené aplikace.

### <a name="removing-feature-versions"></a>Odstranění budoucích verzí

V RCS používáte příkaz **Zrušit nasazení** k odebrání konkrétní verze funkce elektronické fakturace z prostředí služby v Elektronické fakturaci.

> [!IMPORTANT]
> Příkaz **Zrušit nasazení** funguje pouze v prostředí služby. Neodstraňuje verze funkcí elektronické fakturace z připojených aplikací.

### <a name="rebasing-electronic-invoicing-features"></a>Změna základu funkcí elektronické faktury

Když je jedna funkce elektronické fakturace odvozena od jiné, příkaz **Změna základu** aktualizuje odvozený prvek o změny, které byly zavedeny v původním prvku.

## <a name="additional-resources"></a>Další prostředky

- [Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
